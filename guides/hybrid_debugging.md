# Debugging Hybrid Mobile Apps

> This guide assumes you are using [Capacitor](https://capacitorjs.com/) in your project for mobile functionality. Also, if you'd like to setup and use live reloading within your project, intructions on how to do so can be found [here](https://capacitorjs.com/docs/v3/guides/live-reload).

<br>

## iOS

1. Ensure your development environment is ready for generating iOS builds by following the instructions [here](https://capacitorjs.com/docs/v3/getting-started/environment-setup#ios-development).
2. From your Capacitor project folder, run `npx cap run ios`.
3. Select the device or emulator you'd like to deploy your build on from the terminal prompt.
4. Open Safari and from the top bar, go to **Develop >** ***your machine's name*** **>** ***device/emulator name***. This should open Safari's developer tools, targeting your deployed application and allowing you to debug as you would a normal web deployment.

<br>

## Android

1. Ensure you have [Chrome](https://www.google.com/chrome/) installed and your development environment is ready for generating Android builds by following the instructions [here](https://capacitorjs.com/docs/v3/getting-started/environment-setup#android-development).
2. From your Capacitor project folder, run `npx cap run android`.
3. Select the device or emulator you'd like to deploy your build on from the terminal prompt.
4. Open Chrome and go to `chrome://inspect/#devices`. Click on **inspect** underneath your connected device. This should open Chrome's developer tools, targeting your deployed application and allowing you to debug as you would a normal web deployment.

<br>
