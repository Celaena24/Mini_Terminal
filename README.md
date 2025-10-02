# Mini Terminal

A web-based terminal emulator with an integrated file system, built using xterm.js and Node.js. This project provides a fully functional terminal experience in the browser with persistent file storage and multiple tab support.

**[Try it live!](https://326-mini-terminal.vercel.app/)**

## Features

### Terminal Emulation
- **xterm.js Integration**: Full-featured terminal emulator with cursor support and theming
- **Multiple Tabs**: Support for up to 8 concurrent terminal sessions
- **Dark/Light Theme**: Toggle between light and dark modes

### File System Operations
- **Complete Unix-like Commands**: Support for essential file operations
  - `ls` - List directory contents
  - `mkdir` - Create directories
  - `touch` - Create files
  - `cd` - Change directory
  - `pwd` - Print working directory
  - `mv` - Move/rename files and directories
  - `cp` - Copy files and directories
  - `rm` - Remove files and directories
  - `echo` - Display text
  - `cat` - Display file contents

### Built-in Text Editor
- **Ace Editor Integration**: Full-featured code editor with syntax highlighting
- **File Editing**: Create and edit files directly in the terminal interface
- **Multiple File Support**: Edit various file types with appropriate syntax highlighting

### Persistence & Data Management
- **SQLite Database**: Persistent file system storage using Sequelize ORM
- **Save/Load State**: Preserve your file system between sessions
- **Local File Upload**: Add files from your local machine to the terminal file system
- **Download Terminal Logs**: Export your terminal session history
- **File System Export**: Save your entire virtual file system as a downloadable archive

### Web Server
- **Express.js Backend**: RESTful API for file system operations
- **CORS Support**: Cross-origin resource sharing enabled
- **SQLite Integration**: Lightweight database for data persistence

## Tech Stack

- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **Terminal**: [xterm.js](https://xtermjs.org/) - Terminal emulator for the web
- **Editor**: [Ace Editor](https://ace.c9.io/) - Code editor
- **Backend**: Node.js with Express.js
- **Database**: SQLite with Sequelize ORM
- **File Handling**: JSZip for archive operations

## Installation

1. **Clone the repository**:
   ```bash
   git clone [repository-url]
   cd Mini_Terminal
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Start the server**:
   ```bash
   npm start
   ```

4. **Open your browser** and navigate to:
   ```
   http://localhost:3000
   ```

## Usage

### Basic Terminal Operations
- Type commands in the terminal just like a regular Unix terminal
- Use `help` to see available commands
- Use `man <command>` for detailed command documentation

### Managing Multiple Tabs
- Click "Open New Terminal Tab" to create additional terminal sessions
- Click "Close Current Terminal Tab" to close the active tab
- Switch between tabs using the navigation buttons

### File System Persistence
- Click "Save Terminal File System" to persist your current state
- Your file system will automatically load when you restart the application
- Use "Add Local File" to upload files from your computer

### Theme Switching
- Click the - Click the moon (🌙) icon to switch to dark mode
- Click the sun (☀️) icon to switch back to light mode 

## Project Structure

```
Mini_Terminal/
├── src/                              # Core terminal functionality
│   ├── terminal_core_generator.js    # Terminal initialization and setup
│   ├── terminal_setup_core_and_commands.js  # Command implementations
│   ├── editor_utils.js               # Text editor integration
│   └── editor_utils.css              # Editor styling
├── lib/                              # External libraries
├── routes/                           # Express.js API routes
├── server.js                         # Main server file
├── index.html                        # Main application interface
├── index.css                         # Application styling
├── package.json                      # Node.js dependencies
└── README.md                         # This file
```

## API Endpoints

- `POST /api/fs/save` - Save the current file system state
- `GET /api/fs/load` - Load the saved file system state


## Authors

- **Vicayo Zhang**
- **Aryan Ghosh**
- **Stella Dey**

---

*Built for CS 326 - A collaborative project demonstrating web-based terminal emulation and file system management.*