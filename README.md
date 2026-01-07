# User Save Details

A simple web application for managing user information. This application allows users to submit, view, edit, and delete user details (username, email, and phone number) through a clean and intuitive interface.

## 📋 Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Setup & Installation](#setup--installation)
- [Usage](#usage)
- [API Details](#api-details)
- [File Descriptions](#file-descriptions)
- [Developer Information](#developer-information)
- [Future Improvements](#future-improvements)

## ✨ Features

- **User Registration**: Submit user details (username, email, phone number)
- **Display Users**: View all submitted users in a list format
- **Edit Users**: Edit existing user information
- **Delete Users**: Remove users from the list
- **Form Validation**: Basic HTML5 form validation
- **Error Handling**: Graceful error handling with user-friendly messages
- **Local Storage**: Integration with browser's localStorage for data persistence

## 🛠️ Technologies Used

- **HTML5**: Structure and form elements
- **JavaScript (Vanilla)**: Core functionality and DOM manipulation
- **Axios**: HTTP client for API requests (v1.5.1)
- **CRUD Crud API**: Backend API service for data persistence

## 📁 Project Structure

```
User_SaveDetails/
│
├── index.html          # Main HTML file with form structure
├── index.js            # JavaScript logic for form handling and user management
└── README.md           # Project documentation
```

## 🚀 Setup & Installation

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, Edge)
- A local web server (optional, for development)
- Internet connection (for CDN resources and API access)

### Installation Steps

1. **Clone or download the repository**
   ```bash
   git clone <repository-url>
   cd User_SaveDetails
   ```

2. **Open the project**
   - Option 1: Open `index.html` directly in your browser
   - Option 2: Use a local web server (recommended for development)
     ```bash
     # Using Python
     python -m http.server 8000
     
     # Using Node.js (http-server)
     npx http-server
     
     # Using PHP
     php -S localhost:8000
     ```

3. **Access the application**
   - If opened directly: `file:///path/to/index.html`
   - If using a server: `http://localhost:8000`

## 📖 Usage

### Adding a User

1. Fill in the form fields:
   - **Username**: Enter the user's name
   - **Email**: Enter a valid email address
   - **Phone No**: Enter the phone number
2. Click the **Submit** button
3. The user will be added to the list below the form

### Editing a User

1. Click the **Edit** button next to the user you want to edit
2. The form fields will be populated with the user's current information
3. Modify the fields as needed
4. Click **Submit** to save the changes

### Deleting a User

1. Click the **Delete** button next to the user you want to remove
2. The user will be removed from the list immediately

## 🔌 API Details

### Endpoint

```
POST https://crudcrud.com/api/dcddd008a50945a1840dfd1d0d98de5d/appointmentData
```

### Request Format

```json
{
  "username": "string",
  "email": "string",
  "phone": "string"
}
```

### Response Format

```json
{
  "_id": "unique-id",
  "username": "string",
  "email": "string",
  "phone": "string"
}
```

**Note**: The API endpoint uses a free CRUD Crud service. The endpoint ID (`dcddd008a50945a1840dfd1d0d98de5d`) may expire after 24 hours. For production use, consider using a more permanent backend solution.

## 📄 File Descriptions

### `index.html`

The main HTML file containing:
- Form structure with three input fields (username, email, phone)
- Submit button
- Empty `<ul>` element for displaying user list
- External script references (Axios CDN and local `index.js`)

**Key Elements:**
- Form with `onsubmit` event handler
- Input fields with proper types and IDs
- Minimal inline styling for layout

### `index.js`

The JavaScript file containing all application logic:

**Main Functions:**

1. **`handleFormSubmit(event)`**
   - Prevents default form submission
   - Extracts form data
   - Sends POST request to API
   - Handles success and error cases
   - Clears form fields after submission

2. **`displayUserOnScreen(userDetails)`**
   - Creates list item with user information
   - Adds Delete and Edit buttons
   - Appends to the user list
   - Sets up event listeners for delete and edit actions
   - Manages localStorage operations

**Key Features:**
- Axios for HTTP requests
- DOM manipulation for dynamic content
- Event handling for user interactions
- localStorage integration for data persistence
- Error handling with user feedback

## 👨‍💻 Developer Information

### Development Notes

- **API Endpoint**: The current API endpoint is temporary and may expire. Consider implementing a custom backend for production.
- **Error Handling**: Basic error handling is implemented. Consider adding more detailed error messages and validation.
- **Local Storage**: The application uses localStorage, but the implementation may need refinement for better data synchronization with the API.
- **Module Export**: The file includes `module.exports` which is typically used in Node.js environments. This may not be necessary for browser-only code.

### Code Structure

- **Event-Driven Architecture**: Uses event listeners for user interactions
- **Async Operations**: Uses Axios promises for API calls
- **DOM Manipulation**: Direct DOM manipulation without a framework
- **Separation of Concerns**: Logic separated from HTML structure

### Potential Improvements

1. **Data Persistence**: Implement proper GET request to load existing users on page load
2. **Form Validation**: Add client-side validation before submission
3. **Error Messages**: Improve error handling and user feedback
4. **UI/UX**: Add CSS styling for better user experience
5. **API Management**: Create a configuration file for API endpoints
6. **Code Organization**: Consider splitting functions into modules
7. **Testing**: Add unit tests for core functionality

## 🔮 Future Improvements

- [ ] Add CSS styling for a modern, responsive UI
- [ ] Implement GET request to fetch and display existing users on page load
- [ ] Add form validation (email format, phone number format, required fields)
- [ ] Implement proper error handling with user-friendly messages
- [ ] Add loading indicators during API requests
- [ ] Implement proper update (PUT) functionality for editing users
- [ ] Add confirmation dialogs for delete operations
- [ ] Create a backend API for production use
- [ ] Add user authentication and authorization
- [ ] Implement data pagination for large user lists
- [ ] Add search and filter functionality
- [ ] Implement data export functionality (CSV, JSON)
- [ ] Add unit and integration tests
- [ ] Improve accessibility (ARIA labels, keyboard navigation)

## 📝 License

This project is open source and available for educational purposes.

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the issues page or submit a pull request.

## 📧 Contact

For questions or suggestions, please open an issue in the repository.

---

**Last Updated**: 2024

