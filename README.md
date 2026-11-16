# Motive-Fitness-App-

    Motive is a fitness and wellness app for everyday life. It helps people find workouts, explore meal ideas, plan activities, and keep track of their movement. Toffee, a friendly poodle coach, welcomes users and offers simple encouragement along the way.

**Author and Developer: Prince Ram (ramutan)**

![Toffee, the Motive poodle coach](assets/toffee-poodle.png)

##Features

- Welcome and account creation flow before the overview 
- Sign in, forgot password, show/hide passwoed controls
- Workout ideas for the gym, home, and outdoors
- Meal inspiration with sample calories and macronutrient details
- Activity calendar and progress overview
- Tofee coach chat with local, rule-based replies
- Cream-colored light theme and dark theme with an icon toggle
- Responsive browser prototype and native iOS/Android app 
- Supabase authentication and account-scoped activity and meal logging in the mobile app

## Project versions

### Browser prototype

`index.html` is a standalone browser version with the dashboard, workout and nutrition pages, calendar, progress view, coach chat, theme toggle, and local account gate. Open it in a browser or serve the `outputs` folder with a static web host.

The browser account flow is a local prototype. It stores the account name and email in that browser and does not provide secure password authentication or cloud data storage. Use the Expo app with Supabase for real accounts and saved data.

### Native mobile app

`motive-mobile` is the Expo and React Native app for iOS and Android. Account creation, sign-in, password reset, and saving activities and meals use Supabase when it is configured.

## Tech stack

- Expo SDK 56
- React Native 0.85 and React 19
- TypeScript
- Supabase Auth and Postgres
- React Native SVG
- Static HTML, CSS, and JavaScript for the browser prototype

## Project structure

```text
outputs/
|-- README.md
|-- index.html                         # Browser app
|-- assets/
|   |-- toffee-poodle.png              # Toffee image supplied by Prince Ram
|   |-- photos/                         # Color workout and food photos
|   `-- *.svg                           # Browser illustrations
`-- motive-mobile/
    |-- App.tsx                         # Welcome/auth, tabs, features, and app state
    |-- app.json                        # Expo and store identifiers
    |-- eas.json                        # EAS build profiles
    |-- package.json
    |-- .env.example                     # Supabase environment template
    |-- assets/photos/                  # Bundled mobile photo assets
    |-- src/
    |   |-- components/PoodleCoach.tsx  # Toffee coach image component
    |   |-- lib/
    |   |   |-- supabase.ts             # Supabase client and session storage
    |   |   |-- saveActivity.ts          # Activity logging
    |   |   `-- saveMeal.ts              # Meal logging
    |   `-- theme.ts                     # Cream and dark palettes
    `-- supabase/migrations/
        `-- 001_initial_schema.sql       # Profiles, activities, meals, and RLS
```

## Run the broswer prototype

Open `index.html` in a modern browser. For a local web server, run this from the `outputs` directory:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Run the mobile app

Install Node.js and npm, then run these commands from `motive-mobile`:

```bash
npm install
npm run start
```

Open the QR code with Expo Go, or start a simulator with `npm run android` or `npm run ios`. The iOS simulator requires macOS. The mobile app requires a configured Supabase project to create accounts and enter the overview.