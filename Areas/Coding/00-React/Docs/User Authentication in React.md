1. **Install the necessary dependencies:**

```npm
install passport passport-github express-session
```

2. **Create an OAuth app on GitHub:**
    
    - Go to [GitHub Developer Settings](https://github.com/settings/developers).
    - Click on "New OAuth App" and fill in the details.
    - For the callback URL, use something like `http://localhost:3000/auth/github/callback` (adjust according to your setup).
3. **Configure `passport.js` in your application:**
```js
const express = require('express');
const passport = require('passport');
const GitHubStrategy = require('passport-github').Strategy;
const session = require('express-session');

const app = express();

// Session configuration
app.use(session({ secret: 'your_secret_key', resave: false, saveUninitialized: false }));
	
// Initialize passport
app.use(passport.initialize());
app.use(passport.session());
	
// GitHub strategy configuration
passport.use(new GitHubStrategy({
    clientID: 'YOUR_GITHUB_CLIENT_ID',
    clientSecret: 'YOUR_GITHUB_CLIENT_SECRET',
    callbackURL: 'http://localhost:3000/auth/github/callback'
},
function(accessToken, refreshToken, profile, done) {
    // Handle the user's profile
    // For simplicity, we'll use it as it is
    return done(null, profile);
}));

// Serialize and deserialize user
passport.serializeUser(function(user, done) {
	done(null, user);
});
	
passport.deserializeUser(function(obj, done) {
	done(null, obj);
});
	
// Authentication routes
app.get('/auth/github',
	passport.authenticate('github'));
	
app.get('/auth/github/callback',
	passport.authenticate('github', { failureRedirect: '/' }),
function(req, res) {
    // Successful authentication, redirect to home.
    res.redirect('/');
});

app.get('/', (req, res) => {
	res.send(req.isAuthenticated() ? `Hello, ${req.user.username}` : 'Hello, Guest');
});
	
app.listen(3000, () => {
	console.log('App is running on http://localhost:3000');
});

```
    
4. **Run the application:**
```npm
node app.js
```

Now, when you visit `http://localhost:3000` and click on the authentication link, you will be redirected to GitHub to log in. After logging in, you will be redirected back to your application with the authenticated session.