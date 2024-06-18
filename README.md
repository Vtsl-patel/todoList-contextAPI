# Todo Application

This is a simple Todo application built with React and the Context API. The app allows users to add, update, delete, and toggle the completion status of todos. It also persists todos in local storage.

## Features

- Add new todos
- Edit existing todos
- Mark todos as complete/incomplete
- Delete todos
- Persist todos in local storage

## Installation

To get started with the project, clone the repository and install the dependencies:

```bash
git clone https://github.com/Vtsl-patel/todoList-contextAPI.git
cd todoList-contextAPI
npm install
```

## Running the Application

To run the application in development mode, use the following command:

```bash
npm run dev
```

## Project Structure

The project consists of the following main components and files:

- App.js: The main application component that sets up the TodoProvider and renders TodoForm and TodoItem components.
- context/TodoContext.js: Defines the context and provider for managing todos state.
- components/TodoForm.js: Component for adding new todos.
- components/TodoItem.js: Component for displaying and interacting with individual todos.

## Using Context API in the Todo Application
The Todo application utilizes React's Context API to manage state and functions related to todos throughout the application. Here's how Context API was implemented:

### 1. Context Creation:

- TodoContext: Created a context using createContext() to hold state (todos) and functions (addTodo, updateTodo, deleteTodo, toggleComplete) related to managing todos.

### 2. Provider Component:

- TodoProvider: Implemented a provider component (TodoProvider) that wraps the main application (App) and provides the todos state and functions to all components within its tree using TodoContext.Provider.

### 3. Consuming Context:

- useTodo Hook: Created a custom hook (useTodo) that utilizes useContext to access the TodoContext and its values (todos state and todo management functions) in any component where it's needed.

### 4.Integration in Components:

- TodoForm: Uses useTodo hook to access addTodo function from context to add new todos.
- TodoItem: Uses useTodo hook to access updateTodo, deleteTodo, and toggleComplete functions from context to edit, delete, and toggle completion of todos.

### 5. Persistence:

- Local Storage: Utilized localStorage to persist todos across sessions. The todos state is initialized with data retrieved from localStorage and updated on state changes.

By leveraging the Context API, the application ensures efficient state management and facilitates the seamless sharing of state and functions among different components, thereby enhancing maintainability and scalability.

## Usage

### Adding a Todo
1. Enter a todo message in the input field.
2. Click the "Add" button to add the todo to the list.

### Editing a Todo
1. Click the edit (✏️) button next to the todo you want to edit.
2. Modify the todo message in the input field.
3. Click the save (📁) button to save changes.

### Toggling Todo Completion
1. Click the checkbox next to a todo to mark it as complete or incomplete.

### Deleting a Todo
1. Click the delete (❌) button next to the todo you want to remove.

## Styling
The application uses Tailwind CSS for styling. The styles are applied directly to the elements using Tailwind's utility classes.

## Acknowledgments

This project was created as a learning exercise for React and the Context API.

Feel free to reach out with any questions or suggestions!
