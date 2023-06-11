# Mood Tracker

Mood Tracker is a web application that allows users to track their daily moods over a period of days. Users can select their current mood from a list of options and submit it. The application keeps a record of the mood entries in a history log, allowing users to view their mood history.

## Features

- Select and submit moods
- View your mood history log
- Responsive design for different screen sizes

## Technologies Used

- Vue.js: JavaScript framework for building user interfaces
- SCSS: CSS extension language
- HTML: Markup language for creating web pages

## Getting Started

To get a local copy of the project up and running, follow these steps:

1. Clone the repository: ` git clone <repository url> `

2. Install the dependencies: `npm install `

3. Run the development environment: `npm run serve `

4. Access the application at `http://localhost:8080`.

## Project Structure

The project includes the following components:

- `src`: Contains the source code of the Vue application
  - `components`: Contains Vue components used in the application
    - `MoodEntryForm.vue`: Component responsible for capturing and submitting mood entries
    - `MoodHistory.vue`: Component displaying the history log of mood entries
    - `MoodTracker.vue`: Main component that integrates other components and manages the overall application state
  - `scss`: Contains SCSS stylesheet for styling the components
  - `App.vue`: The root component of the application, renders the main layout
  - `main.js`: The entry point of the application, where Vue is initialized and the root component is mounted


## License

This project is licensed under the MIT License.


