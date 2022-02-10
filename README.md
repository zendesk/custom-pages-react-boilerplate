# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app) and modified for Zendesk Guide's [custom pages](https://support.zendesk.com/hc/en-us/articles/4409012911770-Creating-custom-pages-in-your-help-center).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](#deployment)

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Deployment

After building your application, you’re now ready to embed it into your Help Center! The first thing you need to do is navigate to the newly created ‘build’ directory. Here you’ll find a few files that will be necessary for us to create our new custom page.

1. index.html
2. static/css/bundle.min.css
3. static/bundle.min.js

The index.html file will be the code we’ll input into our actual custom page, though we’ll still need to access the javascript and css that we created for our project. To do this we’ll first upload the js and css file as assets into your help center. Once done, we’ll then copy the code from your index.html file into the custom page and adjust the file paths to the assets. It will look something like this:

```html
<!doctype html>
<html lang="en">

  <head>
    <meta charset="utf-8" />
    <link rel="icon" href="/favicon.ico" />
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:wght@100;200;300;400&family=Poppins:wght@400;600;700;800&display=swap"
      rel="stylesheet" />
    <meta name="viewport" content="width=device-width,initial-scale=1" />
    <title>Developer Support Custom Pages Example</title>
    <script defer="defer" src="{{asset 'bundle.min.js'}}"></script>
    <link href={{asset "bundle.min.css" }} rel="stylesheet">
  </head>

  <body><noscript>You need to enable JavaScript to run this app.</noscript>
    <div id="root"></div>
  </body>
</html>
```

### Once done, you’re all set to publish
