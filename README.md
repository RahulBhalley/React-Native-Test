# React Native Test Project 🚀

A premium boilerplate setup for high-performance cross-platform development. Built with React Native 0.84+, TypeScript, and modern dev-tooling.

---

## 🛠 Initial Setup & Environment

This project requires a specific environment configuration to run correctly on both iOS and Android.

### 1. Install Prerequisites (macOS)
Run the following commands to install the necessary tools:
```bash
# File watcher and iOS dependency manager
brew install watchman
sudo gem install cocoapods

# Java Development Kit (Required for Android)
brew install openjdk@17
```

### 2. Configure Environment Variables
Add these to your shell profile (e.g., `~/.zshrc` or `~/.bash_profile`):
```bash
export JAVA_HOME="/opt/homebrew/opt/openjdk@17"
export ANDROID_HOME=$HOME/Library/Android/sdk
export PATH=$PATH:$ANDROID_HOME/emulator:$ANDROID_HOME/tools:$ANDROID_HOME/tools/bin:$ANDROID_HOME/platform-tools
```

### 3. Install Project Dependencies
```bash
# Install JavaScript packages
npm install

# Install iOS native dependencies
cd ios && bundle install && bundle exec pod install && cd ..
```

---

## 🚀 Running the Application

### Metro Bundler
First, start the JavaScript bundler:
```bash
npm start
```

### iOS
To launch on a specific simulator (e.g., iPhone 16 Pro):
```bash
npx react-native run-ios --simulator "iPhone 16 Pro"
```

### Android
Ensure an emulator is running (or a device is connected via ADB):
```bash
npx react-native run-android
```

---

## 🏗 Project Structure

```text
├── android/          # Native Android project
├── ios/              # Native iOS project
├── __tests__/        # Unit and Integration tests
├── App.tsx           # Application root component
├── index.js          # Entry point
└── metro.config.js   # Metro Bundler configuration
```

---

## 💎 Development Tips

- **Dev Menu**: Use `Cmd + D` (iOS) or `Cmd + M` (Android) to open the Dev Menu.
- **Fast Refresh**: UI updates automatically on save.
- **Doctor Check**: Run `npx react-native doctor` to debug environment issues.

---

## 📄 License
This project is open-source and available under the [MIT License](LICENSE).

---
*Created with ❤️ by Antigravity*


