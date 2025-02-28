# StudyNotion Edtech Project


# Step-by-Step Guide to Host StudyNotion App on GitHub Pages

## Prerequisites
- A GitHub account
- Node.js installed on your machine
- A React app ready to be deployed

## Step 1: Create a GitHub Repository
1. Go to [GitHub](https://github.com) and log in to your account.
2. Click on the `+` icon at the top right corner and select `New repository`.
3. Enter a name for your repository and click `Create repository`.

## Step 2: Install `gh-pages` Package
1. Open your terminal.
2. Navigate to the root directory of your React app.
3. Run the following command to install the `gh-pages` package:
    ```bash
    npm install gh-pages --save-dev
    ```

## Step 3: Update `package.json`
1. Open the `package.json` file in your React app's root directory.
2. Add the following properties at the top of the file:
    ```json
    "homepage": "https://your-username.github.io/your-repo-name"
    ```
3. Add the following scripts to the `scripts` section of your `package.json`:
    ```json
    "scripts": {
      "predeploy": "npm run build",
      "deploy": "gh-pages -d build"
    }
    ```

## Step 4: Build and Deploy Your App
1. In the terminal, run the following command to build and deploy your React app to GitHub Pages:
    ```bash
    npm run deploy
    ```

## Step 5: Configure GitHub Pages
1. Go to your repository on GitHub.
2. Click on the `Settings` tab.
3. Scroll down to the `GitHub Pages` section.
4. Under `Source`, select the branch `gh-pages` from the dropdown menu.
5. Click `Save`.

## Step 6: Access Your Deployed App
1. After a few minutes, your React app should be accessible at the URL you specified in the `homepage` property of your `package.json`:
    ```plaintext
    https://your-username.github.io/your-repo-name
    ```

## Example `package.json`
Below is an example of what your `package.json` might look like after making the necessary changes:
```json
{
  "name": "your-app-name",
  "version": "0.1.0",
  "private": true,
  "homepage": "https://your-username.github.io/your-repo-name",
  "dependencies": {
    "react": "^17.0.1",
    "react-dom": "^17.0.1",
    "react-scripts": "4.0.1"
  },
  "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test",
    "eject": "react-scripts eject",
    "predeploy": "npm run build",
    "deploy": "gh-pages -d build"
  },
  "devDependencies": {
    "gh-pages": "^3.1.0"
  }
}
```

Follow these steps, and your React app should be successfully hosted on GitHub Pages!