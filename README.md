# Unistack Expo

A universal React Native application built with Expo, featuring SQLite database integration, secure storage, and modern navigation.

## Features

- **Cross-platform**: Runs on iOS, Android, and Web
- **Database**: SQLite with Drizzle ORM for type-safe database operations
- **Storage**: Secure storage with Expo Secure Store and MMKV for fast key-value storage
- **Navigation**: File-based routing with Expo Router
- **Animations**: Smooth animations with React Native Reanimated
- **Theming**: Dark and light mode support with automatic system detection
- **Notifications**: Push notification support
- **Fonts**: Custom font loading with Expo Font

## Tech Stack

- **Framework**: [Expo](https://expo.dev/) with [Expo Router](https://docs.expo.dev/router/introduction/)
- **Language**: TypeScript
- **Database**: [SQLite](https://docs.expo.dev/versions/latest/sdk/sqlite/) with [Drizzle ORM](https://orm.drizzle.team/)
- **Storage**: [Expo Secure Store](https://docs.expo.dev/versions/latest/sdk/securestore/) + [MMKV](https://github.com/mrousavy/react-native-mmkv)
- **Navigation**: [React Navigation](https://reactnavigation.org/)
- **Animations**: [React Native Reanimated](https://docs.swmansion.com/react-native-reanimated/)
- **UI**: React Native with custom themed components

## Prerequisites

- Node.js (v18 or later)
- npm or yarn
- Expo CLI: `npm install -g @expo/cli`
- For iOS: Xcode (macOS only)
- For Android: Android Studio

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/sushilburagute/unistack-expo.git
   cd unistack-expo
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm start
   ```

## Running the App

### Development

- **Start development server**: `npm start`
- **Run on iOS**: `npm run ios`
- **Run on Android**: `npm run android`
- **Run on Web**: `npm run web`

### Building

Follow the [Expo build documentation](https://docs.expo.dev/build/introduction/) for production builds.

## Project Structure

```
unistack-expo/
├── app/                    # App screens and navigation (Expo Router)
│   ├── _layout.tsx        # Root layout
│   ├── (tabs)/            # Tab-based navigation
│   │   ├── _layout.tsx    # Tab layout
│   │   ├── index.tsx      # Home tab
│   │   └── two.tsx        # Second tab
│   ├── modal.tsx          # Modal screen
│   ├── +html.tsx          # HTML fallback
│   └── +not-found.tsx     # 404 screen
├── src/
│   └── db/                # Database configuration
│       └── schema.ts      # Database schema (Drizzle)
├── components/            # Reusable components
├── constants/             # App constants (colors, etc.)
├── assets/                # Static assets (fonts, images)
├── app.json               # Expo configuration
├── package.json           # Dependencies and scripts
├── tsconfig.json          # TypeScript configuration
├── babel.config.js        # Babel configuration
├── metro.config.js        # Metro bundler config
└── drizzle.config.ts      # Drizzle configuration
```

## Database Setup

The app uses SQLite with Drizzle ORM. To set up the database:

1. Configure your database schema in `src/db/schema.ts`
2. Update `drizzle.config.ts` with your database configuration
3. Run migrations: `npx drizzle-kit generate` and `npx drizzle-kit push`

## Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin feature/your-feature`
5. Submit a pull request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
