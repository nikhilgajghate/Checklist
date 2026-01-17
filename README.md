# Daily Checklist Application

A modern, user-friendly desktop application for tracking daily action items and tasks. Built with Python and CustomTkinter for a beautiful, modern UI.

## Installation

### Prerequisites
- Python 3.11 or higher
- pip (Python package installer)

### Setup

1. **Clone or download this repository**
   ```bash
   git clone <repository-url>
   cd checklist
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the application**
   ```bash
   python src/checklist_app.py
   ```

   Or simply double-click `run_checklist.bat` on Windows.

## Building the Executable

To create a standalone `.exe` file that can be run without Python installed:

1. **Install PyInstaller** (if not already installed)
   ```bash
   pip install pyinstaller
   ```

2. **Build the executable**
   ```bash
   python build_exe.py
   ```

3. **Find your executable**
   The executable will be created in the `dist/` folder as `ChecklistApp.exe`

## Usage

### Adding Tasks
1. Type your task in the input field at the top
2. Press Enter or click "Add Task"
3. Your task will appear in the list below

### Managing Tasks
- **Complete a task**: Click the checkbox next to the task
- **Edit a task**: Double-click the task text or click the ✏️ button
- **Delete a task**: Click the 🗑️ button next to the task
- **Clear completed**: Click "Clear Completed" to remove all finished tasks
- **Clear all**: Click "Clear All" to remove all tasks (with confirmation)

### Data Storage
- Tasks are automatically saved to `checklist_data.json` in the same directory
- The file is created automatically when you add your first task
- Your tasks will be restored when you restart the application

## File Structure

```
checklist/
├── src/
│   └── checklist_app.py      # Main application code
├── requirements.txt          # Python dependencies
├── build_exe.py             # Script to build executable
├── run_checklist.bat        # Windows batch file to run app
├── README.md               # This file
└── dist/                   # Generated executable (after building)
    └── ChecklistApp.exe
```

## Customization

### Changing the Theme
You can modify the appearance by editing these lines in `src/checklist_app.py`:

```python
ctk.set_appearance_mode("dark")  # Options: "dark", "light", "system"
ctk.set_default_color_theme("blue")  # Options: "blue", "green", "dark-blue"
```

### Window Size
Modify the window size by changing these lines:

```python
self.root.geometry("800x600")  # Width x Height
self.root.minsize(600, 400)    # Minimum window size
```

## Development

### Running in Development Mode
```bash
cd src
python checklist_app.py
```

### Code Structure
- `ChecklistApp` class: Main application logic
- `create_widgets()`: UI layout and widget creation
- `add_task()`, `toggle_task()`, `delete_task()`, `edit_task()`: Task management functions
- `save_data()`, `load_data()`: Data persistence functions

## License

This project is open source and available under the [LICENSE](LICENSE) file.
