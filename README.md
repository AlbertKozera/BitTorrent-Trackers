# BitTorrent: Trackers

## Project Description

The goal of this project was to create three trackers for a theoretical BitTorrent network and add 11 participants. Trackers are responsible for providing information about available files and other participants. To simulate their functionality as accurately as possible, we divided the project into several smaller parts. It consists of a back-end section with two applications: one simulates theoretical tracker users, while the other acts as a server and handles trackers. The front-end section is also divided into two applications: one is a theoretical admin panel, while the other facilitates the simulation of clients.

## Technologies

The project uses the following technologies:
- **Development Environment**: IntelliJ IDEA
- **Programming Language**: Java 11
- **Web Framework**: Spring
- **Containerization**: Docker
- **Database Engine**: PostgreSQL
- **Graphic User Interface Framework**: React

## Application Structure

### Back-End

The back-end application is responsible for simulating theoretical tracker users and handling the server. Both back-end applications (server and client) have a similar project structure.

### Front-End

The front-end application is divided into two parts:
1. **Admin Panel**: Manages trackers and users, allows blocking users, and disabling trackers.
2. **Client Application**: Allows users to register, assign themselves to trackers, and download files.

#### Front-End Folder Structure:

- `api`: Contains configuration files for communication with external APIs.
- `components`: Contains independent components that can be shared between views.
- `pages`: Stores complete views made up of smaller components. The folder structure is similar to the components folder.
- `redux`: Contains files with modules responsible for managing and updating the application's state.
- `routes`: Contains files defining paths to specific pages.
- `templates`: Stores files responsible for page templates. Templates are objects on the page that arrange components and present the structure of the page.
- `index.css`: External CSS stylesheet containing global styles for the application.
- `index.tsx`: Main file of the application, where execution starts.

Communication with the back-end on the front-end side is done using Axios and Redux. Axios handles asynchronous HTTP requests to the server, while Redux updates the application state based on the server response.

### Database Schema

The database schema is presented in the project documentation.

![image](https://github.com/user-attachments/assets/d6c91501-5ab8-4b4b-85b0-28db7abe2e23)

## Fault Tolerance

The application implements fault tolerance mechanisms in various scenarios:
1. **User goes offline while downloading a file** - the download is interrupted.
2. **Tracker being used by the user is turned off during the download** - the download is interrupted.
3. **Tracker the user wants to use for downloading is turned off** - the download does not start.
4. **User is banned from the tracker** - the download does not start.

## Summary

The project met the objectives and requirements related to how trackers work in torrent networks. It effectively introduced fault tolerance mechanisms. Potential future developments could include additional functionalities, such as support for multimedia files.

## Running Instructions

1. **Running the Back-End**:
   - Configure and start the Spring Boot server.
   - Run the application simulating theoretical users.
2. **Running the Front-End**:
   - Install dependencies: `npm install`
   - Start the application: `npm start`
3. **Running the Database**: Configure and start PostgreSQL using Docker.
