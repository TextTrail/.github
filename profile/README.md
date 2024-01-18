# Introduction 
# Versions 📰
## Frontend :computer:
| Software | Recommended version | Getting Started Guide |
| ------------|:-----------: | ---------------------- |
| node | 16.16.0      | https://nodejs.org/en/learn/getting-started/how-to-install-nodejs |
| npm | 8.15.1       | https://docs.npmjs.com/downloading-and-installing-node-js-and-npm/ |
| angular | 15.2.10       | https://angular.io/quick-start |
## Backend :satellite:

| Software | Recommended version | Getting Started Guide |
| ------------|:-----------: | ---------------------- |
| Python| 3.11.5      | https://www.python.org/about/gettingstarted/ |
| PyPDF2| 3.0.1       | https://pypi.org/project/PyPDF2/ |


# Usage :thought_balloon:

## Backend :satellite:

To use the Backend/API, clone the "Pre_process" repository and run the Python app continuously.

Copy code

`python Pre_processing.py` 

## Frontend :computer:

To connect the Frontend with the API on your server, locate the `config.json` file. Specify your publicly available API to communicate with the backend.

### Development

To set up a development environment, clone the repository.

Run `npm install` to install required dependencies; then run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any source files.

### Production

To build the application, run `ng build`. The built project will be stored in the `dist/` directory.
