# 4. Website Creation

## 4.1 Install Required Tools

1. Install [Node.js](https://nodejs.org/en) (npm is packaged with Node).
2. [Optional] Install GitHub tools:

   **You can use the terminal if you are comfortable with it.**

  - [GitHub CLI](https://cli.github.com/) (optional)
  - [GitHub Desktop](https://desktop.github.com/download/) (optional)

## 4.2 Download the Workshop Repository
1. Fork this repository.
[Funko Showcase Workshop Repository](https://github.com/do-community/funko-showcase-workshop)

  ![Fork the repo](https://doimages.nyc3.cdn.digitaloceanspaces.com/GitHub/funko-showcase-workshop/4-Website/forkrepo.png)

2. Clone your new repository to your local machine using the web URL or use GitHub Desktop.
  
  ![Clone the repo](https://doimages.nyc3.cdn.digitaloceanspaces.com/GitHub/funko-showcase-workshop/4-Website/clonerepo.png)

## 4.3 Add Your Connection String & Database Information
1. In the `/start` folder of your project, find a file named `.envsample`.
2. Rename this file to `.env`.
3. Open this file, and add your specific details.
4. MONGODB_URI should be your full connection string that we created in step 2.2, including your password. Add this after the "=".
5. DATABASE_NAME should be the name of your database.  We recommended using ```funko-database```. Add this after the "=".
6. COLLECTION_NAME should be the name of your collection. We recommended using ```funko-collection```. Add this after the "=".
7. Save your file.

## 4.3 Install Dependencies

1. In a terminal, open your new code folder.
2. Change your working directory to `/start`
    ```bash
    cd start
    ```
3. Run the following command to install project dependencies:
    ``` bash
    npm install
    ```

## 4.4 Run Your Website Locally

1. Run the application:
    ```bash
    npm run dev
    ```
3. Open your browser and navigate to `http://localhost:3000` or whatever the open port is to see what the site looks like.

    > **NOTE:** Notice that the application currently only shows the images for each item in our collection.  After we deploy our app, we will do more work on the UI of our application to show the rest of the metadata.

4. When you're done viewing the app, make sure to hit Ctrl+C in your terminal to end the process.

## 4.5 Improve the Website
> **NOTE:** We're going to make a small custom change to our app here, but we will be making future modifications after the app is successfully deployed.

1. In your `/start` directory, open the file `/components/Header/Header.tsx`.
2. You will see a code block that defines our page's header.
    ```html
    <Box sx={{ flexGrow: 1 }}>
      <BackgroundAppBar position="static" sx={{ display: 'flex', justifyContent: 'center', alignItems: 'center' }}>
        <Toolbar variant="dense">
          <Typography variant="h1" component="div" sx={{ flexGrow: 1, color: 'white', fontFamily: 'Henny Penny' }}>
            Funko Showcase
          </Typography>
        </Toolbar>
      </BackgroundAppBar>
    </Box>
    ```
3. Change the `Funko Showcase` text to something custom to you, like `Jeff's Funko Collection`.
4. Save the file.
5. By having `npm run dev` running, the browser will reload automatically with your changes.

## 4.6 Commit Changes to GitHub

1. Push your updated code up to GitHub (you can also do this in GitHub Desktop):
    ```bash
    git add .
    git commit -m "Initial commit"
    git push origin main
    ```

→ [Next Up: App Platform](APP-PLATFORM.md)
