# Recurrly — Subscription Tracker

A mobile app built with **React Native** and **Expo** for tracking personal subscriptions, monitoring upcoming renewals, and getting a clear view of recurring spending.

> **Built following the [JavaScript Mastery](https://www.youtube.com/@javascriptmastery) YouTube channel tutorial.**

> **This is a sample/demo project.** It is provided as-is for learning and reference purposes. The creator accepts no responsibility for any issues, data loss, or damages that may arise from using this code. Use at your own risk.

---

## Features

- **Dashboard** — See total monthly spend and a list of all active subscriptions at a glance
- **Upcoming renewals** — Subscriptions renewing within the next 7 days are surfaced automatically
- **Add & manage subscriptions** — Create subscriptions with name, amount, billing cycle, category, and renewal date
- **Insights** — Visual breakdown of spending by category
- **Authentication** — Secure sign-in and sign-up powered by [Clerk](https://clerk.com)
- **Persistent storage** — Subscription data persists across sessions using Zustand + Expo SecureStore

## Tech Stack

| Layer         | Technology                                                      |
| ------------- | --------------------------------------------------------------- |
| Framework     | [Expo](https://expo.dev) (SDK 54) with Expo Router              |
| Language      | TypeScript                                                      |
| Styling       | [NativeWind](https://www.nativewind.dev/) (Tailwind CSS for RN) |
| Auth          | [Clerk](https://clerk.com)                                      |
| State         | [Zustand](https://zustand-demo.pmnd.rs/)                        |
| Date handling | [Day.js](https://day.js.org/)                                   |

## Getting Started

### Prerequisites

- Node.js 18+
- Android Studio (for Android builds) or Xcode (for iOS builds)
- A [Clerk](https://clerk.com) account with a publishable key

### Installation

1. Clone the repository and install dependencies:

   ```bash
   git clone <repo-url>
   cd react-native-recurrly
   npm install
   ```

2. Create a `.env` file in the root with your Clerk key:

   ```env
   EXPO_PUBLIC_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
   ```

3. Start the development server:

   ```bash
   npx expo start
   ```

   Then open in a:
   - [Development build](https://docs.expo.dev/develop/development-builds/introduction/) (recommended)
   - [Android emulator](https://docs.expo.dev/workflow/android-studio-emulator/)
   - [iOS simulator](https://docs.expo.dev/workflow/ios-simulator/)

### Run on a physical device

```bash
npx expo run:android --device
npx expo run:ios --device
```

## Project Structure

```
app/                  # Expo Router screens
  (auth)/             # Sign-in / Sign-up screens
  (tabs)/             # Bottom tab screens (Home, Insights, Settings, Subscriptions)
  subscriptions/      # Subscription detail screen
components/           # Reusable UI components
constants/            # Static data, icons, images, theme
lib/                  # Utilities and Zustand store
assets/               # Fonts, icons, images
```

## Disclaimer

This project is a **sample application** intended for educational and demonstration purposes only. It is not production-ready. The creator provides no warranties of any kind and assumes no liability for any use of this code. You are solely responsible for any consequences of deploying or using this software.
