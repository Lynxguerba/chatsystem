# Project Guidelines: Chatly

This document provides foundational mandates for the Chatly project, ensuring consistency, security, and high engineering standards.

## 1. Architecture & File Structure
- **Frontend**: Currently a static HTML/JS application using Tailwind CSS.
- **Organization**:
  - Keep logic separate from presentation where possible.
  - Future assets (images, CSS, JS) should be moved to an `assets/` directory.
  - Components or reusable HTML snippets should be identified for future refactoring into a framework (e.g., React or Vue).
- **Navigation**: Always perform a `list_directory` at the start of a task to confirm the current file state. Use `grep_search` to find specific implementation details across files.

## 2. Clean Code Standards
- **HTML/CSS**: 
  - Use semantic HTML tags.
  - Maintain consistent Tailwind utility classes usage.
  - Keep styling consistent with the "modern, alive, and polished" aesthetic (rounded corners, shadows, gradients).
- **JavaScript**:
  - Use ES6+ features (const/let, arrow functions, destructuring).
  - Avoid global variables; encapsulate logic within modules or functions.
  - For complex state management, move logic out of inline `<script>` tags into dedicated `.js` files.
- **Documentation**: Comment complex logic and maintain clear naming conventions for variables and functions.

## 3. Backend Development (Future)
- **Framework**: Prefer Node.js (Express) or Python (FastAPI) as per system defaults.
- **API Design**:
  - Follow RESTful principles.
  - Use JSON for data exchange.
  - Implement robust error handling with appropriate HTTP status codes.
- **Persistence**: Transition from in-memory arrays/JSON downloads to a real database (e.g., PostgreSQL or MongoDB) when scale requires.

## 4. Security Mandates
- **Authentication**:
  - Never store passwords in plain text. Use strong hashing (e.g., bcrypt).
  - Use JWT or secure sessions for maintaining state.
- **Data Protection**:
  - Sanitize all user inputs to prevent XSS and Injection attacks.
  - Use HTTPS for all communications (in production).
- **Secrets Management**:
  - **CRITICAL**: Never hardcode API keys, secrets, or credentials. Use `.env` files and ensure they are listed in `.gitignore`.
- **Validation**: Implement both client-side and server-side validation for all forms.

## 5. Interaction Guidelines
- **Research First**: Always analyze existing code before proposing changes.
- **Incremental Updates**: Make surgical changes to existing files using the `replace` tool.
- **Testing**: After any change, verify the functionality (e.g., check for linting errors, test form submissions).
