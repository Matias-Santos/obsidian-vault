## Introduction

This web app will have the objective of giving useful notes for the user, via the inclusion of Perplexity AI to generate the notes for us, by synchronizing our Obsidian's Vault from Github services.


## Features


## Objectives

- [ ] Develop frontend for web app, following markdown standards to ensure compatibility across multiple platforms.
- [ ] Integration with Perplexity services so that we can request data from its API in an ordered manner, producing some kind of components system configured by the developer so that we can paint the UI accordingly.
- [ ] Investigate Perplexity costs in order to make an auto sustainable platform.
- [ ] Provide graphs for the user so that he can take a look at patterns from the documents he has made, possible template ideas, and relational concepts between documents.
- [ ] Give the user the ability to select which documents does he want to be processed by AI or not, with selectors for "All/None" such as in email selection.
- [ ] Buy me a coffee.


## User Flow and Implementation Steps:

#### 1. **File Upload and Integration**

- **Description:** Allow users to upload a markdown file from their desktop or import it from GitHub.
- **Features:**
    - **File Upload:** Implement a file upload button for users to select markdown files from their local machine.
    - **GitHub Integration:** Enable GitHub OAuth login and repository selection to import markdown files.
- **Tools:**
    - For GitHub: Use GitHub API for authentication and file access.
    - For file upload: Use HTML5 file input and server-side handling.

#### 2. **Markdown Parsing**

- **Description:** Parse the uploaded markdown file to prepare it for processing.
- **Features:**
    - **Markdown Parser:** Use a library like `markdown-it` or `remark` to parse the markdown content.
- **Tools:**
    - Node.js or Python libraries for markdown parsing.

#### 3. **AI Processing with Perplexity**

- **Description:** Send the parsed markdown content to the AI service (Perplexity) for summarization.
- **Features:**
    - **API Integration:** Implement API calls to Perplexity for processing the markdown content.
    - **Error Handling:** Ensure robust error handling for API calls.
- **Tools:**
    - HTTP client libraries like `axios` (for Node.js) or `requests` (for Python).

#### 4. **Displaying Summaries**

- **Description:** Display the generated summaries to the user in a user-friendly format.
- **Features:**
    - **Summary Display:** Show the AI-generated summaries prominently on the interface.
    - **Highlighting Key Points:** Highlight important information within the summary.
- **Tools:**
    - Frontend frameworks like React for dynamic and responsive UI.

#### 5. **User Interaction and Feedback**

- **Description:** Allow users to interact with the summaries and provide feedback.
- **Features:**
    - **Feedback Mechanism:** Enable users to provide feedback on the summaries to improve future processing.
    - **Editable Notes:** Allow users to edit and save notes based on the summaries.
- **Tools:**
    - UI components for feedback and note-taking.

### Example Implementation Plan:

#### 1. **File Upload and GitHub Integration**

- **Frontend:**
    - Add buttons for "Upload from Desktop" and "Import from GitHub".
    - Use file input for desktop uploads.
    - Use GitHub OAuth for authentication and repository selection.
- **Backend:**
    - Handle file uploads and GitHub API integration.
    - Parse the uploaded markdown file.

#### 2. **Markdown Parsing**

- **Backend:**
    - Parse the markdown content using `markdown-it`.
    - Extract text content and structure for processing.

#### 3. **AI Processing with Perplexity**

- **Backend:**
    - Send the extracted markdown content to Perplexity via API.
    - Receive and handle the summarization response.
- **Example Code Snippet (Node.js):**

```javascript
const axios = require('axios');

async function getSummary(content) {
  try {
    const response = await axios.post('https://api.perplexity.ai/summarize', {
      text: content
    });
    return response.data.summary;
  } catch (error) {
    console.error('Error processing markdown with Perplexity:', error);
    throw error;
  }
}
```
#### 4. **Displaying Summaries**

- **Frontend:**
    - Display the summary returned from the AI service.
    - Highlight key points in the summary.
- **Example Code Snippet (React):**

```javascript
import React, { useState } from 'react';

function SummaryDisplay({ summary }) {
  return (
    <div>
      <h2>Summary</h2>
      <p>{summary}</p>
    </div>
  );
}

export default SummaryDisplay;
```
#### 5. **User Interaction and Feedback**

- **Frontend:**
    - Add editable fields for users to refine the summary or add notes.
    - Include feedback options for users to rate the summary quality.
- **Example Code Snippet (React):**

```javascript
import React, { useState } from 'react';

function FeedbackForm({ onSubmit }) {
  const [feedback, setFeedback] = useState('');

  const handleSubmit = (e) => {
    e.preventDefault();
    onSubmit(feedback);
  };

  return (
    <form onSubmit={handleSubmit}>
      <label>
        Feedback:
        <textarea value={feedback} onChange={(e) => setFeedback(e.target.value)} />
      </label>
      <button type="submit">Submit Feedback</button>
    </form>
  );
}

export default FeedbackForm;
```

### Enhancements:

- **Batch Processing:** Allow users to upload multiple markdown files and process them in a batch.
- **Custom Summarization Settings:** Let users customize the summarization (e.g., length, focus areas).
- **Integration with Other AI Services:** Optionally integrate with other AI services for different types of processing (e.g., translation, sentiment analysis).