
# Introduction

## Versions 📰

### Frontend :computer:
| Software | Recommended version | Getting Started Guide |
| ------------|:-----------: | ---------------------- |
| Node.js (node) | 16.16.0 | [Install Node.js](https://nodejs.org/en/learn/getting-started/how-to-install-nodejs) |
| npm | 8.15.1 | [Download and Install npm](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm/) |
| Angular | 15.2.10 | [Angular Quick Start Guide](https://angular.io/quick-start) |

### Backend :satellite:
| Software | Recommended version | Getting Started Guide |
| ------------|:-----------: | ---------------------- |
| Python | 3.11.5 | [Python Getting Started](https://www.python.org/about/gettingstarted/) |
| PyPDF2 | 3.0.1 | [PyPDF2 Documentation](https://pypi.org/project/PyPDF2/) |

# Usage :thought_balloon:

## Backend :satellite:

To use the Backend/API, follow these steps:

1. Clone the "Pre_process" repository.
2. Run the Python app continuously using the following command:
    ```
    python Pre_processing.py
    ```

## Frontend :computer:

To connect the Frontend with the API on your server, follow these steps:

1. Locate the `config.json` file.
2. Specify your publicly available API to communicate with the backend.

### Development

To set up a development environment, follow these steps:

1. Clone the repository.
2. Run the following commands in the terminal:
    ```
    npm install
    ng serve
    ```
3. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any source files.

### Production

To build the application, run the following command:
```
ng build
```
The built project will be stored in the `dist/` directory.

# Flow of Information

The process of PDF upload and text retrieval is split into two steps for a more responsive application.

1. **PDF Upload Process**:
    - Users can upload one PDF file at a time.
    - The backend generates a unique identifier for each uploaded PDF.
    - The frontend quickly receives this identifier.
    - Uploaded files are saved for the current browser session.
    
2. **Text Retrieval Process**:
    - Users can access uploaded files via an API call with the unique identifier.
    - The backend searches for the file and responds with processed plain text.
    - If processing is not finished, the user is informed to retry later.
    - Once processing is complete, the backend responds with plain text.
    
For visual representations of these processes, refer to the following figures:

- **PDF Upload Process**: [Figure](https://github.com/TextTrail/.github/blob/main/profile/img/api-schematic_towards.png)

- **Text Retrieval Process**: [Figure](https://github.com/TextTrail/.github/blob/main/profile/img/api-schematic_from.png)
