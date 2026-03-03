# React Native Test Project 🚀

A comprehensive, high-performance React Native 0.84+ boilerplate. This guide provides exhaustive instructions for setting up your environment and running the application on any platform or device.

---

## 🛠 1. Environment Configuration

### macOS Prerequisites
Run these commands to install the core toolchain:
```bash
# Core dependencies
brew install node watchman
sudo gem install cocoapods

# Android specific (JDK 17)
brew install openjdk@17
```

### Path Configuration
Add the following to your `~/.zshrc` (or `~/.bash_profile`) to ensure the build tools are discoverable:
```bash
export JAVA_HOME="/opt/homebrew/opt/openjdk@17"
export ANDROID_HOME=$HOME/Library/Android/sdk
export PATH=$PATH:$ANDROID_HOME/emulator:$ANDROID_HOME/tools:$ANDROID_HOME/tools/bin:$ANDROID_HOME/platform-tools
```
*Note: Run `source ~/.zshrc` after saving.*

### Project Initialization
```bash
npm install
cd ios && bundle install && bundle exec pod install && cd ..
```

---

## � 2. Running on iOS

### iOS Simulator
Start the app on a specific virtual device:
```bash
# List available simulators
xcrun simctl list devices

# Run on a specific one
npx react-native run-ios --simulator "iPhone 16 Pro"
```

### iOS Real Device
1.  **Connect your iPhone** via USB or same Wi-Fi.
2.  **Open Xcode**: `open ios/ReactNativeTest.xcworkspace`.
3.  **Configure Signing**:
    - Select the project in the left sidebar.
    - Go to **Signing & Capabilities**.
    - Select your **Team** (Personal Team is fine).
    - Ensure the Bundle Identifier is unique.
4.  **Run**: Select your physical device from the target selector and hit **Play**, or run:
    ```bash
    npx react-native run-ios --device "Your Device Name"
    ```

---

## 🤖 3. Running on Android

### Android Emulator
1.  **Open Android Studio** → Virtual Device Manager.
2.  **Start an AVD** (Android Virtual Device).
3.  **Launch App**:
    ```bash
    npx react-native run-android
    ```

### Android Real Device
1.  **Enable Developer Options**: Go to Settings → About Phone → Tap *Build Number* 7 times.
2.  **Enable USB Debugging**: Settings → Developer Options → USB Debugging.
3.  **Connect Device**: Plug in via USB.
4.  **Verify Connection**:
    ```bash
    adb devices
    ```
5.  **Run**:
    ```bash
    npx react-native run-android
    ```

---

## ⚡ 4. Development Workflow

### Starting Metro
The JavaScript bundler must be running for development:
```bash
npm start
```

### Dev Menu
Use these shortcuts to access the developer menu (Reload, Debug, etc.):
- **iOS Simulator**: `Cmd ⌘ + D`
- **Android Emulator**: `Cmd ⌘ + M` (macOS) or `Ctrl + M` (Windows)
- **Real Devices**: Shake the device.

---

## 🏗 Project Structure

```text
├── android/          # Native Android source
├── ios/              # Native iOS source (Swift/Objective-C)
├── __tests__/        # Jest test suites
├── App.tsx           # Main application entry component
├── index.js          # Entry point for Metro
└── package.json      # Dependencies and scripts
```

---

## � Troubleshooting

- **Pod Issues**: `cd ios && pod install --repo-update`
- **Build Fails**: `npm run clean` (if configured) or manually delete `ios/build` and `android/app/build`.
- **Metro Cache**: `npm start -- --reset-cache`
- **Missing Java**: Ensure `java -version` returns version 17.

---
*Maintained by RahulBhalley | Built with ❤️ by Antigravity*
