# ReactWpfWeb

This project was bootstrapped with [Create React Native App](https://github.com/react-community/create-react-native-app).

Below you'll find information about performing common tasks. The most recent version of this guide is available [here](https://github.com/react-community/create-react-native-app/blob/master/react-native-scripts/template/README.md).

However, I have ejected the bootstraper to support wpf. Above is to keep as reference


### How to recreate this project
``
create-react-native-app ReactWpfWeb --with-web-support
cd ReactWpfWeb
yarn run eject
yarn add rnpm-plugin-windows --dev
yarn add rnpm-plugin-wpf --dev
react-native wpf
``

### Start web
``
yarn web
``

### Start wpf
- Open the solution file in the application folder in Visual Studio (e.g., `AwesomeProject/windows/AwesomeProject.sln`)
	- *Note*: If this is your first time doing UWP development on the computer you're using, you may be asked to install additional UWP tooling. After opening the solution, right click the Solution in the `Solution Explorer` and select the option labeled `Install Missing Components`. You may have to shutdown Visual Studio to continue the installation.
- *Note*: If you are using Visual Studio 2017, you will need to retarget the ChakraBridge project. Right click the ChakraBridge project:
    - If there is not a retarget option:
        - Select "Reload", and the Visual Studio installer will open.
        - Make sure to close Visual Studio before installing
        - Make sure the 10.0.14393.0 Windows 10 SDK is selected along with any other preselected components, and click `Modify` in the installer to install the components
        - Retargeting the ChakraBridge project should be possible, so proceed to the next instructions regarding if there is a retarget option
    - If there is a retarget option:
        - Retarget by right clicking on the ChakraBridge project in the Solution Explorer and selecting `Retarget Projects` and pressing `OK` on the popup dialog (Platform Toolset should say `Upgrade to v141` in the dialog).
- Select the `Debug` configuration and the `x64` platform from the combo box controls to the left of the `Run` button and underneath the `Team` and `Tools` menu item.
	- *Note:* If you are running on, or targeting, an x86 platform select `x86` instead. If you are deploying to Windows 10 Phone, select `ARM`.
- Click the `Run` button to the right of the platform combo box control, or select the `Debug`->`Start without Debugging` menu item.
- You should now see a typical React Native app running on Windows that is showing an error saying it needs to contact the dev server. Almost there!
- Run `yarn start` from your project directory, and wait for the React Native packager to report success. Then, press control+R (or click `Reload` button) in your running app. You now see your new app! :tada:

*Note:* You should **only** modify the project and source files for your app (e.g. `AwesomeProject`). The files for the "ReactNative" and other projects shown in the Visual Studio solution are in the `node_modules` directory (which will not be committed to your source repository since it is ignored in `.gitignore`). Any changes to files in `node_modules` will be overwritten when doing an `npm install` or `npm update`. If you need to add a new native module or override some React Native behavior, see [Extending React Native](http://github.com/Microsoft/react-native-windows#extending-react-native)

### Start IOS
``
yarn ios
``

### Start Android
``
yarn android
``

### Special Thanks
Thanks to 
[Microsoft/react-native-windows](https://github.com/Microsoft/react-native-windows)
[react-community/create-react-native-app](https://github.com/react-community/create-react-native-app)