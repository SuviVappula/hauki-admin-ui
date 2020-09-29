This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `yarn start`

Runs the app in the development mode.<br />
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br />
You will also see any lint errors in the console.

It is possible to configure API's URL by setting env variable API_URL, for example, `API_URL=http://localhost:9000 yarn start`. The default is http://localhost:8080

### `yarn test`

Launches the test runner in the interactive watch mode.<br />
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `yarn test-cypress`

Runs cypress (e2e) tests locally.

### `yarn build`

Builds the app for production to the `build` folder.<br />
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br />
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `yarn eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

## Docker

### How to build a docker image
```bash
docker build . -t hauki-admin-ui
```

### How to run the docker image
```bash
docker run -p 3000:8000 -e API_URL=<api-url-here> USE_AXE=<true|false> hauki-admin-ui
```

## RELEASE

### Release to Dev environment

Release to dev environment https://hauki-admin-ui.dev.hel.ninja is handled automatically from master branch. Updates to master branch triggers
azure pipeline that will run tests, build and push image to dockerhub, and finally release it to dev environment hosted by red hat openshift.
Currently azure-pipeline is configured directly from version control, but red hat openshift configuration resides in openshift cluster.
