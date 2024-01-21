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

# Flow of Information
For the flow of information, we decided to split the process of PDF upload and actual text retrieval into two separate steps to ensure a more responsive application. In [Figure](https://github.com/TextTrail/.github/blob/main/profile/img/api-schematic_towards.png), you can see how our uploading procedure works.

![How our uploading procedure works](https://github.com/TextTrail/.github/blob/main/profile/img/api-schematic_towards.png)

At this point, users can upload one PDF file at a time, sending the raw byte stream and the filename to the backend. The backend generates a response containing a unique identifier to identify the PDF for later use. The frontend receives this data quickly, as the reception of the PDF file and the generation of a unique identifier takes less time than the extraction of the file contents from the PDF. While this speed increase may be insignificant for smaller PDF files, it becomes more important as the PDF file size increases.

Users can repeat the uploading of different files as often as they wish. Every response is saved for the current browser session and can be accessed later on. If the user has finished uploading PDF files, they can access the uploaded files via an API call with the unique identifier attached. The backend then searches for the file in the operating system file system and responds with the corresponding processed plain text, which is sent to the frontend. If the processing step has not finished yet, the frontend user is informed to try requesting the data later, as it is not available at that moment.

Once a request arrives with a unique identifier linked to an already finished file processing, the backend responds with plain text, which is further processed by the frontend. 

A schematic of this retrieval of plain texts by a unique identifier can be seen in [Figure](https://github.com/TextTrail/.github/blob/main/profile/img/api-schematic_from.png).

![Retrieval of plain texts by a unique identifier ](https://github.com/TextTrail/.github/blob/main/profile/img/api-schematic_towards.png)

