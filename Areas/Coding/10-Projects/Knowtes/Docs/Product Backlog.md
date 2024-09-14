
## [[0001 - As a user, I want to Login to Github]]

- **Subtasks:**
    - Implement GitHub OAuth authentication.
    - Create a login UI.
    - Handle access tokens securely.
- **Considerations:**
    - Ensure security best practices for OAuth.
    - Provide clear error messages for failed login attempts.

## [[0002 - As a user, I want to import my Vault from Github]]

- **Subtasks:**
    - Fetch user repositories after successful login.
    - Allow users to select a repository as their vault.
    - Clone or download the selected repository.
- **Considerations:**
    - Handle different repository structures.
    - Provide feedback during the import process.

## [[0003 - As a user, I want to select the Documents I want to get notes on]]

- **Subtasks:**
    - Display a list of documents from the imported vault.
    - Implement a selection mechanism (checkboxes, drag-and-drop, etc.).
- **Considerations:**
    - Support for different document formats.
    - Handle large numbers of documents efficiently.


## [[0004 - As a user, I want the notes to be presented on a new markdown]]

- **Subtasks:**
    - Generate notes based on selected documents.
    - Create a new markdown file with the generated notes.
    - Save the new markdown file to the vault.
- **Considerations:**
    - Ensure the notes are well-formatted.
    - Handle edge cases (e.g., empty documents).


## [[0005 - As a user, I want the notes to be presented on the same markdown]]

- **Subtasks:**
    - Append notes to the existing markdown document.
    - Save changes to the original file.
- **Considerations:**
    - Avoid overwriting existing content unintentionally.
    - Maintain clear separation between original content and new notes.


## [[0006 - As a user, I want to review all the notes made from this website whenever I login to Github]]

- **Subtasks:**
    - Store a history of notes made during previous sessions.
    - Display the history upon login.
- **Considerations:**
    - Ensure data consistency across sessions.
    - Provide an intuitive UI for reviewing notes.


## [[0007 - As a user, I want to get recommendations on my notes patterns, templates and other advices]]

- **Subtasks:**
    - Analyze user notes for patterns.
    - Provide recommendations based on analysis.
    - Implement a recommendation engine.
- **Considerations:**
    - Ensure recommendations are relevant and useful.
    - Allow users to give feedback on recommendations.


## [[0008 - As a user, I want to get graphs and scores based on how I make documentation]]

- **Subtasks:**
    - Track metrics related to note-taking and documentation.
    - Generate visualizations (graphs, charts) from these metrics.
    - Calculate scores or ratings based on the metrics.
- **Considerations:**
    - Ensure visualizations are clear and informative.
    - Provide explanations for the scores and metrics used.


## [[0009 - As a user, I want to upload a test markdown from my Desktop]]
\
- **Subtasks:**
    - Implement a file upload mechanism.
    - Parse and display the uploaded markdown.
    - Integrate the uploaded markdown into the existing system.
- **Considerations:**
    - Handle different markdown formats and content.
    - Ensure security by validating uploaded files.


## [[0010 - As a user, I want to edit existing markdown notes directly within the app]]

- **Subtasks:**
    - Implement a markdown editor.
    - Enable saving changes to the vault.
- **Considerations:**
    - Support common markdown features (e.g., headers, lists, code blocks).
    - Provide a user-friendly editing interface.


## [[0011 - As a user, I want to collaborate on notes with other GitHub users]]

- **Subtasks:**
    - Implement sharing and collaboration features.
    - Allow users to invite collaborators.
    - Handle concurrent edits and version control.
- **Considerations:**
    - Ensure real-time updates for collaborators.
    - Resolve conflicts effectively.


## [[0012 - As a user, I want to receive notifications for important updates or changes]]

- **Subtasks:**
    - Implement a notification system.
    - Allow users to customize notification preferences.
- **Considerations:**
    - Ensure notifications are timely and relevant.
    - Provide both in-app and email notifications.

## [[0013 - As a user, I want to search through my notes and documents efficiently]]

- **Subtasks:**
    - Implement a search functionality.
    - Support searching by keywords, tags, and dates.
- **Considerations:**
    - Ensure search results are accurate and relevant.
    - Optimize performance for large volumes of data.


## [[0014 - As a user, I want to tag and categorize my notes for better organization]]

- **Subtasks:**
    - Implement tagging and categorization features.
    - Allow users to create and manage custom tags.
- **Considerations:**
    - Provide an intuitive UI for managing tags.
    - Enable filtering and sorting by tags and categories.


## [[0015 - As a user, I want to export my notes and documents in different formats]]

- **Subtasks:**
    - Implement export functionality.
    - Support formats such as PDF, HTML, and plain text.
- **Considerations:**
    - Ensure exported files maintain original formatting.
    - Provide options for customizing export settings.


## [[0016 - As a user, I want to integrate with other tools and platforms (e.g., Google Drive, Dropbox)]]

- **Subtasks:**
    - Implement integration with third-party services.
    - Allow users to import/export documents from/to these services.
- **Considerations:**
    - Ensure seamless and secure data transfer.
    - Provide clear setup instructions for integrations.


## [[0017 - As a user, I want to track my progress and activity within the app]]

- **Subtasks:**
    - Implement activity tracking and logging.
    - Provide a dashboard or summary view of user activity.
- **Considerations:**
    - Ensure privacy and data security for activity logs.
    - Offer insights and analytics based on user activity.


## [[0018 - As a user, I want to customize the app’s appearance and settings]]

- **Subtasks:**
    - Implement customization options (themes, fonts, layout).
    - Allow users to save and apply their preferences.
- **Considerations:**
    - Ensure customizations are easy to manage.
    - Provide a preview before applying changes.


## [[0019 - As a user, I want to receive support and access help resources within the app]]

- **Subtasks:**
    - Implement a help and support section.
    - Provide FAQs, tutorials, and contact options.
- **Considerations:**
    - Ensure help resources are easy to find and use.
    - Offer multiple support channels (chat, email, documentation).


## [[0020 - As an admin, I want to manage users and monitor app usage]]

- **Subtasks:**
    - Implement admin dashboard and user management features.
    - Provide tools for monitoring app usage and performance.
- **Considerations:**
    - Ensure admin features are secure and robust.
    - Offer insights and reports to help with app maintenance.


## [[0021 - As a user, I want to sync my notes across multiple devices]]

- **Subtasks:**
    - Implement synchronization features.
    - Ensure data consistency across devices.
- **Considerations:**
    - Handle offline access and syncing when reconnected.
    - Optimize for performance and minimal data usage.


## [[0022 - As a user, I want to automate repetitive tasks using scripts or macros]]

- **Subtasks:**
    - Implement scripting or macro functionality.
    - Provide a way to create, edit, and execute scripts.
- **Considerations:**
    - Ensure scripts are secure and sandboxed.
    - Provide examples and templates for common tasks.


## [[0023 - As a user, I want to backup and restore my notes and settings]]

- **Subtasks:**
    - Implement backup and restore features.
    - Allow users to schedule automatic backups.
- **Considerations:**
    - Ensure backups are stored securely.
    - Provide clear instructions for restoring from a backup.


## [[0024 - As a user, I want to set reminders and deadlines for my notes]]

- **Subtasks:**
    - Implement a reminder and deadline system.
    - Allow users to set and manage reminders.
- **Considerations:**
    - Integrate with notification systems.
    - Provide options for recurring reminders.


## [[0025 - As a user, I want to integrate with calendar applications]]

- **Subtasks:**
    - Implement integration with popular calendar apps (Google Calendar, Outlook).
    - Allow users to link notes to calendar events.
- **Considerations:**
    - Ensure data synchronization is accurate and timely.
    - Provide options for one-way or two-way sync.


## [[0026 - As a user, I want to protect my notes with encryption and passwords]]

- **Subtasks:**
    - Implement encryption for notes.
    - Allow users to set passwords for sensitive documents.
- **Considerations:**
    - Ensure encryption is strong and meets industry standards.
    - Provide recovery options for forgotten passwords.


## [[0027 - As a user, I want to view my notes in different themes or layouts]]

- **Subtasks:**
    - Implement multiple themes and layout options.
    - Allow users to switch themes and layouts easily.
- **Considerations:**
    - Ensure themes are visually appealing and accessible.
    - Provide a preview before applying a theme.


## [[0028 - As a user, I want to integrate with task management tools (e.g., Trello, Asana)]]

- **Subtasks:**
    - Implement integration with task management platforms.
    - Allow users to create and manage tasks linked to notes.
- **Considerations:**
    - Ensure seamless data exchange between the app and task management tools.
    - Provide clear setup instructions and options.


## [[0029 - As a user, I want to receive insights and analytics on my note-taking habits]]

- **Subtasks:**
    - Implement an analytics dashboard.
    - Provide insights on frequency, length, and topics of notes.
- **Considerations:**
    - Ensure data privacy and anonymization of insights.
    - Offer actionable recommendations based on analytics.


## [[0030 - As a user, I want to share my notes or documents with others easily]]

- **Subtasks:**
    - Implement sharing features via email, link, or social media.
    - Allow users to set permissions for shared notes.
- **Considerations:**
    - Ensure shared content is secure and access-controlled.
    - Provide options for public or private sharing.


## [[0031 - As a user, I want to integrate voice-to-text functionality for creating notes]]

- **Subtasks:**
    - Implement voice-to-text features.
    - Allow users to dictate notes and convert them to text.
- **Considerations:**
    - Ensure high accuracy and support for multiple languages.
    - Provide editing options for dictated text.


## [[0032 - As a user, I want to use templates for creating consistent and structured notes]]

- **Subtasks:**
    - Implement a template library.
    - Allow users to create and save custom templates.
- **Considerations:**
    - Provide a variety of pre-made templates.
    - Ensure templates are easy to use and customize.


## [[0032 - As a user, I want to use templates for creating consistent and structured notes]]

- **Subtasks:**
    - Implement a template library.
    - Allow users to create and save custom templates.
- **Considerations:**
    - Provide a variety of pre-made templates.
    - Ensure templates are easy to use and customize.


## [[0033 - As a user, I want to integrate with note-taking apps like Evernote or OneNote]]

- **Subtasks:**
    - Implement integration with popular note-taking apps.
    - Allow users to import and export notes to/from these apps.
- **Considerations:**
    - Ensure data is accurately transferred and formatted.
    - Provide options for one-way or two-way sync.


## [[0034 - As a user, I want to lock specific notes to prevent accidental changes]]

- **Subtasks:**
    - Implement a locking feature for notes.
    - Allow users to lock and unlock notes easily.
- **Considerations:**
    - Provide a clear indicator for locked notes.
    - Ensure locked notes are protected from edits until unlocked.


## [[0035 - As Knowtes, I want to be able to have a conversation with Open AI]]

- Subtasks:
	- Set up Perplexity AI Integration
	- Define User Interface
	- Handle API Requests
	- Stream Responses
	- State Management
	- Error Handling
- Considerations: 
	- Provide clear business solution to consume the API without bankruptcy