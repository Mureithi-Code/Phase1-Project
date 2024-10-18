# Knights Gallery

## Basic Story of the Application

The Knights Gallery is a web application designed to showcase a diverse collection of knights from different genres—Historical, Legendary, and Fictional. Users can explore knights, filter them by genre, view detailed information retrieved from Wikipedia, and engage with the community by leaving comments. The application aims to provide an interactive and educational experience centered around the legendary figures of knighthood.

## Core Features of the MVP

- **Genre Filtering**: Users can select from various genres to display knights relevant to their interests.
- **Knight Details**: Clicking on a knight displays more information sourced from Wikipedia, providing users with context and history.
- **Commenting System**: Users can submit comments about knights, edit existing comments, and delete them if needed, fostering community engagement.
- **Responsive Design**: The layout adjusts to different screen sizes, ensuring usability across devices.

## API Data Used and How They Have Been Used

The application relies on two main data sources:

1. **Local JSON Server**:
   - **Knights Data**: 
     - The `GET http://localhost:3000/knights` endpoint provides knight data categorized into Historical, Legendary, and Fictional. This data is fetched to populate the gallery and filter results based on user selection.
   - **Comments**:
     - The `GET http://localhost:3000/comments` endpoint retrieves comments associated with each knight genre. Users can add new comments via the `POST` method, edit existing comments using the `PUT` method, and delete comments using the `DELETE` method.

2. **Wikipedia API**:
   - The application uses the Wikipedia API to fetch detailed information about knights. 
   - The search API (`WIKI_SEARCH_URL`) is called to find relevant pages based on the knight's name, and the detail API (`WIKI_DETAIL_URL`) retrieves extracts to display in the knight details section.

## Challenges Expected to Be Faced

- **Asynchronous Data Handling**: Managing asynchronous calls and ensuring that the UI updates correctly based on the fetched data posed initial challenges, particularly with ensuring data consistency and proper error handling.
- **API Rate Limits**: Fetching data from the Wikipedia API required careful consideration of rate limits, particularly when displaying details for multiple knights.
- **UI Responsiveness**: Creating a responsive design that adapts seamlessly to various screen sizes and devices was a significant focus to ensure a user-friendly experience.

## How the Requirements of the Project Are Met

The project meets its requirements through the following implementations:

- **Functional UI**: The application provides a clean and intuitive user interface, allowing users to filter knights and view details effortlessly.
- **Engagement Features**: The commenting system encourages user interaction by allowing users to submit, edit, and delete comments, enhancing the overall experience.
- **Dynamic Content**: By integrating the Wikipedia API, the application enriches user experience with real-time information about knights, making it both informative and engaging.
- **Performance**: The use of asynchronous JavaScript ensures smooth performance while fetching and displaying data without freezing the UI.

Overall, the Knights Gallery successfully combines interactive elements and informative content to create a comprehensive platform for exploring the world of knights.