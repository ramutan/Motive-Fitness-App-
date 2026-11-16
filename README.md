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