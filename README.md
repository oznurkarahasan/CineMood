CineMood Project Report
1. Project Overview
  CineMood is a web application where users can receive movie and TV series recommendations, track their viewing habits, and access personalized content suggestions. The platform is integrated with The Movie Database (TMDB) API to enrich the cinema experience by providing detailed information, ratings, and recommendations. CineMood caters to movie enthusiasts with features such as watchlists, favorites, and a test mode to determine user preferences.
The application emphasizes user interaction through a responsive and visually appealing design. Interactive features like animated transitions and a modular interface enhance the user experience. Additionally, CineMood prioritizes security and offers a safe, enjoyable experience with secure authentication mechanisms and data protection practices.
2. Technology Stack
CineMood is developed using modern and reliable technologies, including:
Frontend:
•	HTML: Structures the foundation of web pages.
•	CSS: Handles visual design and responsive interfaces.
•	JavaScript: Powers dynamic content and user interactions.
•	Ajax: Enables asynchronous data exchange.
Backend:
•	PHP: Manages server-side operations and API integrations.
Database:
•	PostgreSQL: Stores user data, watchlists, and favorites. Database connections and configurations are managed via db_connection.php and db.php files.
External API:
•	TMDB API: Provides movie and TV series data (details, recommendations, ratings).
Dependency Management:
•	Composer: Manages PHP dependencies.
3. Project Structure
CineMood’s file and folder structure is modular and organized. Below are the key components:
3.1 Main Directory
The main directory contains HTML pages focused on the user interface and core functionalities:
•	HTML Pages:
o	login.html: User login screen.
o	register.html: New user registration screen.
o	myAccount.html: Displays and manages user profile information.
o	moviedetails.html: Shows details of selected movies or TV shows (cast, director, synopsis, rating, etc.).
o	recommendations.html: Provides personalized movie and TV recommendations.
o	ChooseMode.html: Allows users to select different recommendation modes.
o	Animation Pages (animate.html, animate2.html, startWebsite.html): Visual transitions and animations for the interface.
3.2 PHP Folder
This folder contains server-side logic and database operations, categorized as follows:
3.2.1 Authentication
•	login.php: Manages user login.
•	register.php: Handles new user registration.
•	auth.php: Conducts session management and authentication checks.
•	forgot-password.php: Enables users to request a password reset link.
•	reset-password.php: Performs password reset operations.
•	verify-code.php: Verifies codes sent for password reset or registration.
3.2.2 User Operations
•	myaccount.php: Allows users to manage their account information (name, email, profile picture).
•	update_name.php: Updates the user’s name.
•	update_avatar.php: Updates the profile picture.
•	delete_account.php: Permanently deletes a user account.
•	get_user_info.php: Fetches user information to display in the interface.
3.2.3 Movie Operations
•	get_movies.php: Retrieves movie lists from the TMDB API.
•	get_media_details.php: Fetches details of selected movies or TV shows (director, cast, synopsis, genre, etc.).
•	get_recommendations.php: Provides movie and TV recommendations based on user habits.
•	watched.php: Tracks and lists movies the user has watched.
•	watch: Adds and lists movies the user intends to watch.
•	favorites.php: Tracks and lists the user’s favorite movies.
•	TMDB.php: Manages interaction and data exchange with the TMDB API.
3.2.4 Database and Configuration
•	db_connection.php: Establishes and manages PostgreSQL database connections.
•	db.php: Contains database configurations (table definitions, schemas, etc.).
•	config.php: Stores general project settings (API keys, database credentials, session settings).
4. Key Features
CineMood includes various features to provide a user-focused experience, enhancing functionality and user satisfaction:
4.1 User Management
•	Registration and Login System: Users can easily register or log in with email and password.
•	Password Reset: Secure password reset processes supported by verification codes.
•	Profile Management: Users can update personal information like name and profile picture.
•	Account Deletion: Users can permanently delete their accounts anytime.
4.2 Movie Management
•	Movie Search and Details: Users can search for movies and TV shows and access detailed information (cast, director, genre, synopsis).
•	Watched Movies: Users can save and view a history of watched movies.
•	Watchlist: Allows users to save movies to watch later.
•	Favorite Movies: Enables users to add favorite movies for quick access.
4.3 Recommendation System
•	Personalized Recommendations: Suggests movies and TV shows based on user habits and preferences.
•	Mode Options: Users can customize the recommendation algorithm with different modes (e.g., popular, genre-based).
•	Test Mode: Provides an interactive test to determine user tastes and tailor recommendations accordingly.
4.4 User Experience
•	Animated Transitions: Smooth and visually appealing transitions.
•	Responsive Design: Works seamlessly across mobile, tablet, and desktop devices.
•	User-Friendly Interface: Intuitive navigation ensures easy use.
5. CRUD Operations
CineMood implements basic CRUD (Create, Read, Update, Delete) operations for user and movie management. These operations are handled using PostgreSQL, PHP, and AJAX:
•	Create:
o	User registration (register.php): Adds new users to the database.
o	Movie lists (watched.php, watch_later.php, favorites.php): Saves watched, watchlist, or favorite movies.
•	Read:
o	User information (get_user_info.php): Fetches profile details.
o	Movie data (get_movies.php, get_media_details.php): Retrieves movie details from TMDB API and database.
•	Update:
o	Profile updates (update_name.php, update_avatar.php): Modifies user details.
o	Movie lists: Allows users to edit watchlist or favorite lists.
•	Delete:
o	Account deletion (delete_account.php): Removes user accounts from the database.
o	Movie removal: Lets users remove movies from watched or favorite lists.
AJAX ensures these operations are performed asynchronously (e.g., profile updates in myAccount.html or movie details in moviedetails.html).
6. Security Features
CineMood incorporates several measures to ensure the security of user data:
•	Password Reset System: Secure reset process supported by verification codes.
•	Verification Code Checks: Confirms codes sent for registration or password reset.
•	Secure Session Management: Prevents unauthorized access through secure session handling.
•	Database Connection Security: Protects against SQL injection and stores credentials encrypted.
7. Development and Maintenance
CineMood adopts a sustainable and error-focused approach during development and maintenance:
•	Dependency Management: Composer organizes and updates PHP dependencies.
•	Error Logging: Application errors are logged in error.log and reviewed regularly by developers.
•	API Test Files: Files like test_api.php verify proper TMDB API integration.
•	Modular Code Structure: Code is structured for reusability and ease of maintenance.
•	Updates and Support: The application is regularly updated with new features and user feedback.
8. Team and Task Distribution
CineMood was developed by the PresenTech team. Team members and their responsibilities are as follows:
Name	Program	Student No.	Responsibilities
Öznur Karahasan	1st Program	231106109001	Team Leader, Database Management, Frontend
Hanin Hamza	1st Program	237106109031	API Integration, Backend
Zeynep Özdemir	1st Program	210106109038	Frontend, Testing and Maintenance
Furkan Uslu	2nd Program	211106206009	Backend, Testing and Maintenance
Task Descriptions
•	Öznur Karahasan (Team Leader): Managed project coordination, designed and managed PostgreSQL database, contributed to frontend development, created animations, and performed CRUD operations (update, delete).
•	Hanin Hamza: Integrated TMDB API, developed backend logic with PHP, managed API data flow, performed CRUD operations (update, delete), and handled PHP error reporting.
•	Zeynep Özdemir: Designed user-friendly interfaces using HTML, CSS, and JavaScript, performed CRUD operations (create, read), conducted application testing, and supported maintenance.
•	Furkan Uslu: Developed backend with PHP, performed asynchronous operations with AJAX, executed CRUD operations (update, delete), participated in testing and debugging, and supported system maintenance and optimization.
9. Conclusion and Future Plans
CineMood combines modern technologies and user-friendly design to offer a user-focused movie and TV platform. TMDB API integration provides rich media content, while features like personalized recommendations and test mode enhance user experience. The security and performance-oriented approach boost the platform’s reliability.
Future Plans:
•	AI-Powered Recommendations: Enhance the recommendation system by integrating machine learning algorithms.
•	Social Features: Introduce social functionalities where users can share movie lists or create shared viewing groups.
•	Offline Mode: Enable access to watchlists and favorites without an internet connection.
•	Multi-Language Support: Expand the user base by offering interfaces and content suggestions in multiple languages.
CineMood aims to remain an innovative, user-focused platform for movie enthusiasts, constantly evolving to meet user expectations.

