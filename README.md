# React Native Test Project 🚀

A premium boilerplate setup for high-performance cross-platform development. Built with React Native 0.84+, TypeScript, and modern dev-tooling.

---

## 🛠 Features

- **TypeScript** - Core type-safety out of the box.
- **Modern CLI** - Using `@react-native-community/cli`.
- **Pre-configured** - Optimized for both iOS and Android.
- **Fast Refresh** - Real-time development experience.

---

## 🚀 Quick Start

### 1. Prerequisites
Ensure you have the following installed:
- [Node.js](https://nodejs.org/) (v18+)
- [Watchman](https://facebook.github.io/watchman/)
- [Ruby](https://www.ruby-lang.org/) (for CocoaPods)
- [JDK 17](https://openjdk.org/) (for Android)

### 2. Installation
Install dependencies and pods:
```bash
npm install
cd ios && bundle exec pod install && cd ..
```

### 3. Run the Application

#### **iOS**
```bash
npx react-native run-ios
```

#### **Android**
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

- **Metro Bundler**: Keep it running in the background (`npm start`).
- **Debugging**: Use `Cmd + D` (iOS) or `Cmd + M` (Android) to open the Dev Menu.
- **Type Checking**: Run `tsc` to verify TypeScript integrity.

---

## 📄 License
This project is open-source and available under the [MIT License](LICENSE).

---
*Created with ❤️ by Antigravity*

