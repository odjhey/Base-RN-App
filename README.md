
1. `mkcd APP`
1. `git init`
1. `touch readme.md`
1. `y add -D react-native-cli`
1. `y react-native init APP_NAME --template typescript`
1. `mkdir server`
1. `mv APP_NAME client`
1. `git add .`
1. `git add -f client/android/gradle/wrapper/gradle-wrapper.jar`
1. update client npm scripts
    ```json
    "scripts": {
        "android": "react-native run-android",
        "ios": "react-native run-ios",
        "start": "react-native start",
        "test": "jest --verbose --coverage",
        "test:w": "jest --watch",
        "lint": "eslint .",
        "storybook": "(adb reverse tcp:7007 tcp:7007 || true) && start-storybook",
        "sb": "npm run storybook start",
        "prestorybook": "rnstl",
        "mst-gql:scaffold": "mst-gql --format ts --roots ROOTS http://localhost:4000/graphql   "
    }
    ```
1. rename package name inside client/template
1. `y android`
1. `y add -D @storybook/react-native`
1. `y add -D @storybook/react-native-server`
1. `mkdir storybook`
1. `y add -D react-native-storybook-loader`
1. update npm config (for storyloader)
    ```json
    "config": {
      "react-native-storybook-loader": {
        "searchDir": [
          "./storybook/stories"
        ],
        "pattern": "**/*.story.tsx",
        "outputFile": "./storybook/storyLoader.js"
      }
    },
    ```
1. react native elements and vector icons
1. add files
    1. /storybook/**
    1. /components
    1. /storybook/storyLoader
