# Ishmael - BTCmobick Watch-Only Wallet

[![GitHub tag](https://img.shields.io/badge/dynamic/json.svg?url=https://raw.githubusercontent.com/hogusea/Ishmael/master/package.json&query=$.version&label=Version)](https://github.com/hogusea/Ishmael)
[![code style: prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg?style=flat-square)](https://github.com/prettier/prettier)
![](https://img.shields.io/github/license/hogusea/Ishmael.svg)

Ishmael is a BTCmobick-focused watch-only wallet fork.
It is optimized for PSBT signing flow and external signer workflows.

[![Repository](https://img.shields.io/badge/GitHub-hogusea%2FIshmael-181717?logo=github)](https://github.com/hogusea/Ishmael)

Website: [github.com/hogusea](https://github.com/hogusea)

## Recommended Companion

Use Ishmael together with **Mobick Logbook** for the intended offline signing flow.

Mobick Logbook is a SeedSigner fork:
https://github.com/hogusea/seedsigner

## BTCmobick Defaults

* Electrum: `wallet.mobick.info:40009`
* Explorer: `https://blockchain.mobick.info/`
* Watch-only import and PSBT broadcast flow enabled by default

## Android Screenshots

<p align="center">
  <img src="assets/readme/screen-wallets.png" width="24%" alt="Wallets screen">
  <img src="assets/readme/screen-settings.png" width="24%" alt="Settings screen">
  <img src="assets/readme/screen-about.png" width="24%" alt="About screen">
  <img src="assets/readme/screen-donate.png" width="24%" alt="Developer donation screen">
</p>


## BUILD & RUN IT

Please refer to the engines field in package.json file for the minimum required versions of Node and npm. It is preferred that you use an even-numbered version of Node as these are LTS versions.

To view the version of Node and npm in your environment, run the following in your console:

```
node --version && npm --version
```

* In your console:

```
git clone https://github.com/hogusea/Ishmael.git
cd Ishmael
npm install
```

Please make sure that your console is running the most stable versions of npm and node (even-numbered versions).

* To run on Android:

You will now need to either connect an Android device to your computer or run an emulated Android device using AVD Manager which comes shipped with Android Studio. To run an emulator using AVD Manager:

1. Download and run Android Studio
2. Click on "Open an existing Android Studio Project"
3. Open `build.gradle` file under `Ishmael/android/` folder
4. Android Studio will take some time to set things up. Once everything is set up, go to `Tools` -> `AVD Manager`.
    * 📝 This option [may take some time to appear in the menu](https://stackoverflow.com/questions/47173708/why-avd-manager-options-are-not-showing-in-android-studio) if you're opening the project in a freshly-installed version of Android Studio.
5. Click on "Create Virtual Device..." and go through the steps to create a virtual device
6. Launch your newly created virtual device by clicking the `Play` button under `Actions` column

Once you connected an Android device or launched an emulator, run this:

```
npx react-native run-android
```

The above command will build the app and install it. Once you launch the app it will take some time for all of the dependencies to load. Once everything loads up, you should have the built app running.

* To run on iOS:

```
npx pod-install
npm start
```

In another terminal window within the `Ishmael` folder:
```
npx react-native run-ios
```
**To debug Ishmael on the iOS Simulator, you must choose a Rosetta-compatible iOS Simulator. This can be done by navigating to the Product menu in Xcode, selecting Destination Architectures, and then opting for "Show Both." This action will reveal the simulators that support Rosetta.
**

* To run on macOS using Mac Catalyst:

```
npx pod-install
npm start
```

Open the iOS workspace under `ios/`. Once the project loads, select the main app scheme (display name `ISHMAEL`) and click Run.

## TESTS

```bash
npm run test
```


## LICENSE

MIT

## WANT TO CONTRIBUTE?

Grab an issue from [the backlog](https://github.com/hogusea/Ishmael/issues), try to start or submit a PR.

## Translations

We accept translations via pull requests in this repository.

To participate you need to:
1. Sign up to Transifex
2. Find Ishmael project
3. Send join request
4. After we accept your request you will be able to start translating! That's it!

Please note the values in curly braces should not be translated. These are the names of the variables that will be inserted into the translated string. For example, the original string `"{number} of {total}"` in Russian will be `"{number} из {total}"`.

Transifex automatically creates Pull Request when language reaches 100% translation. We also trigger this by hand before each release, so don't worry if you can't translate everything, every word counts.

## Q&A

Builds automated and tested with BrowserStack

<a href="https://www.browserstack.com/"><img src="https://i.imgur.com/syscHCN.png" width="160px"></a>

Bugs reported via BugSnag

<a href="https://www.bugsnag.com"><img src="https://images.typeform.com/images/QKuaAssrFCq7/image/default" width="160px"></a>


## RESPONSIBLE DISCLOSURE

Found critical bugs/vulnerabilities? Please open a private report with the maintainer: https://github.com/hogusea
Thanks!
