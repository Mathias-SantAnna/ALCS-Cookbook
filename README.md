Welcome all,

This is the Code Institute student template.

<!--![image](https://github.com/Mathias-SantAnna/alcs-cookbook/blob/main/readme/alcs-cookbook-readme-logo.png)-->

# ALCS Cookbook <a name="top"></a>

This is a dynamic recipe website that I created as a project to learn and sharpen my skills, after a break in coding. I have the idea from home where we couldn't decide which dish to make at dinner.

So this website is designed to help users to manage (create, read, update and delete), to share their favorite recipes and discover new ones from the community.

The website is fully responsive and offers various features for both general users and administrators. The link to the live website is available [HERE](https://alcs-cookbook.herokuapp.com/).

## USER EXPERIENCE DESIGN

The website caters to two main types of users: those who are looking to discover and save recipes, and administrators who manage the content. As a web development student, I built this website to provide users with an intuitive platform for cooking inspiration and to hone my skills in full-stack development.

**<ins>New User</ins>**

> *"As a logged in user I can manage my recipes as in create, read, update and delete."*
> *"As a logged in user I can search, view and share the community recipes and my own as well."*
> *"As a new user I can register so that I can access registered user functions."*

> **Note:**<br>
> **ID9**: The search function is designed to allow users to find recipes based on keywords, ingredients, or categories.

**<ins>Admin's Story</ins>**
<!-- 
 
 I WILL WORK FROM HERE ON...

> **Note:**<br>
> **ID5**: Recipes can be edited or removed by the admin, ensuring the content stays relevant and up-to-date. This is important for managing a large database of recipes.

<div align="right"><a href="#top">🔝</a></div>

## UX 5 PLANES

### Strategy Plane

The following features were identified as essential to meet the needs of the users as defined in the user stories:

| Opportunity                               | Importance | Viability / Feasibility |
| :---------------------------------------- | :--------: | :---------------------: |
| Browsing recipes by categories            |     5      |            5            |
| Viewing detailed recipe information       |     5      |            5            |
| Search function                           |     5      |            5            |
| User accounts                             |     4      |            5            |
| Saving favorite recipes                   |     5      |            4            |
| Submitting new recipes                    |     4      |            5            |
| Editing and removing recipes (Admin)      |     5      |            5            |
| Rating and commenting on recipes          |     4      |            4            |
| User-friendly navigation                  |     5      |            5            |
| Mobile responsiveness                     |     5      |            5            |

The following additional features could enhance the user experience but were considered optional due to time constraints or complexity:

| Opportunity                                    | Importance | Viability / Feasibility |
| :--------------------------------------------- | :--------: | :---------------------: |
| Nutritional information per recipe             |     4      |            3            |
| Social media integration                       |     3      |            2            |
| Advanced filtering options                     |     3      |            2            |
| Meal planning tools                            |     3      |            2            |
| Shopping list generation based on recipes      |     2      |            2            |

### Scope Plane

The website includes the following essential pages and features to fulfill the user and admin objectives:

- A clear and accessible **Home Page** displaying popular recipes and navigation links.
- **Recipe Browsing Pages** organized by categories (e.g., Appetizers, Main Courses, Desserts).
- **Recipe Details Page** where users can view ingredients, instructions, and user comments.
- A **Search Page** to find recipes by keywords or ingredients.
- **User Account Pages** where users can sign up, log in, and manage their saved recipes.
- **Recipe Submission Page** allowing users to submit new recipes for review.
- **Admin Pages** for managing recipes, including adding, editing, and deleting content.
- Error handling with **404 and 500 Pages** to guide users when encountering invalid pages.

### Structure Plane

— **Front-end** —

The front end is built with HTML, CSS, and JavaScript, providing the following core pages:

- **Home** (`index.html`):<br>
  This page serves as the main entry point, featuring a search bar, category navigation, and highlights of popular or new recipes.

- **Browse Recipes** (`recipes.html`, `recipes/<category>.html`):<br>
  Allows users to explore recipes by category or view all available recipes.

- **Recipe Details** (`recipe/<recipe_id>.html`):<br>
  Provides detailed information about a selected recipe, including ingredients, preparation steps, and user reviews.

- **User Profile** (`profile.html`):<br>
  Enables users to view and manage their saved recipes and personal details.

- **Recipe Submission** (`submit_recipe.html`):<br>
  A form where users can submit new recipes for inclusion on the website.

- **Admin Dashboard** (`admin_dashboard.html`):<br>
  Available only to admins, this page allows management of the site's content, including recipes and user accounts.

- **Error Pages** (`404.html`, `500.html`):<br>
  Custom error pages that enhance the user experience when something goes wrong.

— **Back-end** —

The back-end infrastructure is developed using Django, with PostgreSQL as the database for production and SQLite for development.

### Skeleton Plane

The website is designed to be fully responsive, providing a seamless experience across devices. Wireframes for the key pages are outlined below:

<details>
<summary>Home (index.html)</summary><br>
![Wireframe: Home](https://github.com/Mathias-SantAnna/alcs-cookbook/blob/main/readme/ux/home.png)
</details>

<details>
<summary>Browse Recipes (recipes.html)</summary><br>
![Wireframe: Browse Recipes](https://github.com/Mathias-SantAnna/alcs-cookbook/blob/main/readme/ux/browse-recipes.png)
</details>

<details>
<summary>Recipe Details (recipe/<recipe_id>.html)</summary><br>
![Wireframe: Recipe Details](https://github.com/Mathias-SantAnna/alcs-cookbook/blob/main/readme/ux/recipe-details.png)
</details>

<details>
<summary>User Profile (profile.html)</summary><br>
![Wireframe: User Profile](https://github.com/Mathias-SantAnna/alcs-cookbook/blob/main/readme/ux/profile.png)
</details>

<details>
<summary>Recipe Submission (submit_recipe.html)</summary><br>
![Wireframe: Recipe Submission](https://github.com/Mathias-SantAnna/alcs-cookbook/blob/main/readme/ux/submit-recipe.png)
</details>

<details>
<summary>Admin Dashboard (admin_dashboard.html)</summary><br>
![Wireframe: Admin Dashboard](https://github.com/Mathias-SantAnna/alcs-cookbook/blob/main/readme/ux/admin-dashboard.png)
</details>

### Surface Plane

— **Colors** —

The website uses a clean and neutral color palette to ensure readability and focus on the recipe content. The primary colors include:

- **White** (#FFFFFF) for backgrounds.
- **Burnt Orange** (#D95D39) for navigation and headers.
- **Olive Green** (#3A5A40) for buttons and accents.
- **Dark Gray** (#333333) for text.

— **Typography** —

The site employs the **Merriweather** font for headings, providing a classic and readable style, and **Roboto** for body text to maintain clarity and simplicity.

<div align="right"><a href="#top">🔝</a></div>

## WEBSITE DEVELOPMENT PLAN

The development process follows a structured plan to ensure all features are implemented efficiently:

1. **Planning**: Define user stories, scope, and features.
2. **Project Setup**: Initialize the Django project, set up GitHub repository, and create a basic app structure.
3. **Authentication**: Implement user authentication with Django Allauth.
4. **Base Template**: Create a reusable base template for consistent layout across pages.
5. **Recipe Features**: Develop recipe browsing, searching, and detailed views.
6. **User Profiles**: Implement user registration, login, and profile management.
7. **Admin Features**: Develop CRUD functionality for admins to manage recipes.
8. **Styling and Responsiveness**: Apply CSS for mobile responsiveness and improve user interface design.
9. **Deployment**: Set up Heroku for production, configure AWS for static files.
10. **Testing and Debugging**: Perform thorough testing across devices and browsers.
11. **Final Review**: Polish the site, check for errors, and finalize documentation.

<div align="right"><a href="#top">🔝</a></div>

## FEATURES

### Existing Features

- **Dynamic Recipe Browsing**: Users can browse and search for recipes, view detailed information, and save favorites.
- **User Authentication**: Secure user accounts with options to save favorite recipes and submit new ones.
- **Admin Management**: Full CRUD functionality for recipes, ensuring the content is up-to-date.
- **Responsive Design**: The site is fully responsive, providing a seamless experience on all devices.

### Features Left to Implement

- **Nutritional Information**: Displaying nutritional data for each recipe.
- **Advanced Filtering**: Allow users to filter recipes by dietary preferences or cooking time.
- **Shopping List Generation**: Enable users to generate shopping lists based on selected recipes.
- **Social Media Integration**: Allow users to share recipes on social platforms.

<div align="right"><a href="#top">🔝</a></div>

## TECHNOLOGIES USED

- **HTML5**: For structuring content.
- **CSS3**: For styling the website.
- **JavaScript**: For interactive elements.
- **Python**: For back-end development.
- **Django**: As the primary web framework.
- **SQLite**: For local development database.
- **PostgreSQL**: For production database on Heroku.
- **Bootstrap**: For responsive layout and components.
- **AWS S3**: For hosting static files and images.
- **Git**: For version control.
- **Heroku**: For deploying the website.

## RESOURCES

### General Resources

- **Django Documentation**
- **Stack Overflow**
- **W3Schools**
- **Code Institute Course Materials**

### Tools

- **Balsamiq**: For wireframing.
- **Canva**: For creating logos and images.
- **PEP8 Online**: For checking Python code compliance.
- **Autoprefixer**: For ensuring cross-browser compatibility in CSS.

<div align="right"><a href="#top">🔝</a></div>

## TESTING

A detailed testing report is available in the **[TESTING.md](https://github.com/Mathias-SantAnna/alcs-cookbook/blob/main/TESTING.md)** file.

<div align="right"><a href="#top">🔝</a></div>

## PROJECT BARRIERS & SOLUTIONS



<div align="right"><a href="#top">🔝</a></div>

## VERSION CONTROL

Version control for the project is managed using Git and GitHub.

— **Setting Up** —

1. Create a remote repository on GitHub and initialize Git in the project directory.
2. Set up the `.gitignore` file to exclude unnecessary files.

— **Commitments** —

Regular commits are made to ensure that the progress is well-documented and can be rolled back if necessary.

— **Branches** —

Feature branches are used for developing new features and are merged into the main branch upon successful testing.

<div align="right"><a href="#top">🔝</a></div>

## DEPLOYMENT

The website is deployed on Heroku with PostgreSQL as the production database and AWS S3 for static files.

### Heroku Deployment

1. **Create a Heroku App**: Set up a new app in Heroku.
2. **Add PostgreSQL**: Provision a PostgreSQL database for the app.
3. **Configure Django Settings**: Adjust settings for production, including the database, static files, and allowed hosts.
4. **Deploy the App**: Push the code to Heroku, where it is automatically built and deployed.

### AWS S3 Setup

1. **Create an S3 Bucket**: Set up a new bucket in AWS for static file storage.
2. **Configure Bucket Policies**: Ensure the bucket has the correct policies to allow public access to static files.
3. **Connect to Django**: Update the Django settings to use the S3 bucket for static and media files.

<div align="right"><a href="#top">🔝</a></div>

## CREDITS

### Code

- **Bootstrap**: For responsive grid layout and components.
- **Django Documentation**: For reference on implementing features.

### Media

- **Logo and Favicon**: Created using **Canva**.
- **Recipe Images**: Sourced from **Unsplash** and **Pexels**.

<div align="right"><a href="#top">🔝</a></div>

## ACKNOWLEDGEMENTS

I would like to thank:

- **Wife & Family** for their motivation and support and love.
- **Friends & Mentor** for their encouragement, guidance, advise and help with building and testing the website.


<div align="right"><a href="#top">🔝</a></div>
is file was: **June 18, 2024**

## Gitpod Reminders

To run a frontend (HTML, CSS, Javascript only) application in Gitpod, in the terminal, type:

`python3 -m http.server`

A blue button should appear to click: _Make Public_,

Another blue button should appear to click: _Open Browser_.

To run a backend Python file, type `python3 app.py` if your Python file is named `app.py`, of course.

A blue button should appear to click: _Make Public_,

Another blue button should appear to click: _Open Browser_.

By Default, Gitpod gives you superuser security privileges. Therefore, you do not need to use the `sudo` (superuser do) command in the bash terminal in any of the lessons.

To log into the Heroku toolbelt CLI:

1. Log in to your Heroku account and go to *Account Settings* in the menu under your avatar.
2. Scroll down to the *API Key* and click *Reveal*
3. Copy the key
4. In Gitpod, from the terminal, run `heroku_config`
5. Paste in your API key when asked

You can now use the `heroku` CLI program - try running `heroku apps` to confirm it works. This API key is unique and private to you, so do not share it. If you accidentally make it public, you can create a new one with _Regenerate API Key_.

### Connecting your Mongo database

- **Connect to Mongo CLI on a IDE**
- navigate to your MongoDB Clusters Sandbox
- click **"Connect"** button
- select **"Connect with the MongoDB shell"**
- select **"I have the mongo shell installed"**
- choose **mongosh (2.0 or later)** for : **"Select your mongo shell version"**
- choose option: **"Run your connection string in your command line"**
- in the terminal, paste the copied code `mongo "mongodb+srv://<CLUSTER-NAME>.mongodb.net/<DBname>" --apiVersion 1 --username <USERNAME>`
  - replace all `<angle-bracket>` keys with your own data
- enter password _(will not echo **\*\*\*\*** on screen)_

------

## Release History

We continually tweak and adjust this template to help give you the best experience. Here is the version history:

**June 18, 2024,** Add Mongo back into template

**June 14, 2024,** Temporarily remove Mongo until the key issue is resolved

**May 28 2024:** Fix Mongo and Links installs

**April 26 2024:** Update node version to 16

**September 20 2023:** Update Python version to 3.9.17.

**September 1 2021:** Remove `PGHOSTADDR` environment variable.

**July 19 2021:** Remove `font_fix` script now that the terminal font issue is fixed.

**July 2 2021:** Remove extensions that are not available in Open VSX.

**June 30 2021:** Combined the P4 and P5 templates into one file, added the uptime script. See the FAQ at the end of this file.

**June 10 2021:** Added: `font_fix` script and alias to fix the Terminal font issue

**May 10 2021:** Added `heroku_config` script to allow Heroku API key to be stored as an environment variable.

**April 7 2021:** Upgraded the template for VS Code instead of Theia.

**October 21 2020:** Versions of the HTMLHint, Prettier, Bootstrap4 CDN and Auto Close extensions updated. The Python extension needs to stay the same version for now.

**October 08 2020:** Additional large Gitpod files (`core.mongo*` and `core.python*`) are now hidden in the Explorer, and have been added to the `.gitignore` by default.

**September 22 2020:** Gitpod occasionally creates large `core.Microsoft` files. These are now hidden in the Explorer. A `.gitignore` file has been created to make sure these files will not be committed, along with other common files.

**April 16 2020:** The template now automatically installs MySQL instead of relying on the Gitpod MySQL image. The message about a Python linter not being installed has been dealt with, and the set-up files are now hidden in the Gitpod file explorer.

**April 13 2020:** Added the _Prettier_ code beautifier extension instead of the code formatter built-in to Gitpod.

**February 2020:** The initialisation files now _do not_ auto-delete. They will remain in your project. You can safely ignore them. They just make sure that your workspace is configured correctly each time you open it. It will also prevent the Gitpod configuration popup from appearing.

**December 2019:** Added Eventyret's Bootstrap 4 extension. Type `!bscdn` in a HTML file to add the Bootstrap boilerplate. Check out the <a href="https://github.com/Eventyret/vscode-bcdn" target="_blank">README.md file at the official repo</a> for more options.

------

## FAQ about the uptime script

**Why have you added this script?**

It will help us to calculate how many running workspaces there are at any one time, which greatly helps us with cost and capacity planning. It will help us decide on the future direction of our cloud-based IDE strategy.

**How will this affect me?**

For everyday usage of Gitpod, it doesn’t have any effect at all. The script only captures the following data:

- An ID that is randomly generated each time the workspace is started.
- The current date and time
- The workspace status of “started” or “running”, which is sent every 5 minutes.

It is not possible for us or anyone else to trace the random ID back to an individual, and no personal data is being captured. It will not slow down the workspace or affect your work.

**So….?**

We want to tell you this so that we are being completely transparent about the data we collect and what we do with it.

**Can I opt out?**

Yes, you can. Since no personally identifiable information is being captured, we'd appreciate it if you let the script run; however if you are unhappy with the idea, simply run the following commands from the terminal window after creating the workspace, and this will remove the uptime script:

```
pkill uptime.sh
rm .vscode/uptime.sh
```

**Anything more?**

Yes! We'd strongly encourage you to look at the source code of the `uptime.sh` file so that you know what it's doing. As future software developers, it will be great practice to see how these shell scripts work.

---

Happy coding!
-->