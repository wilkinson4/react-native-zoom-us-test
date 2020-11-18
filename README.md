# zoom-us-test

Example repository of using [react-native-zoom-us bridge](https://www.npmjs.com/package/react-native-zoom-us).

## Usage

* `yarn`
* on ios only: `cd ios/ && pod install && cd ..`
* Go to https://marketplace.zoom.us/develop/create and Create SDK App, then copy `sdkKey` and `sdkSecret`
* Open `App.tsx` and look for `TODO` - update it with your `sdkKey`, `sdkSecret`.
  * For `startMeeting` provide: `meetingNumber`, `userId`, and `zoomAccessToken`.
  * For `joinMeeting` provide: `meetingNumber` and `password`
* `yarn start`
* `yarn run android` or `yarn run ios`

## Smoke Test Procedure
The following procedure covers testing of the bridge.

### Android

#### Emulator
1. [ ] Development: `yarn run android`

#### Real Device
1. [ ] Development: `yarn run android`
2. [ ] Release: `cd android && ./gradlew assembleRelease && cd ..`, `adb install android/app/build/outputs/apk/release/app-release.apk`

### iOS

#### Emulator
1. [ ] Development: `yarn run ios`

#### Real Device
Note: You will need to allow to install app; look for: Settings -> General -> Device Management -> Apple Development

1. [ ] Development: x-code: Run
2. [ ] Release: change: `ios/ZoomUsTest.xcodeproj/xcshareddata/xcschemes/ZoomUsTest.xcscheme -> <LaunchAction> -> buildConfiguration = "Release"`, x-code: Run
