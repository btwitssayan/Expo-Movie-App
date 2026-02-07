# 🎬 Expo TMDB Movie App

Welcome to your **Expo-powered Movie Application** 👋
This project is built using **Expo** and **React Native**, leveraging the **TMDB API** to deliver a modern, fast, and visually engaging movie browsing experience.

---

## 🚀 Overview

This app allows users to:

* Browse trending and popular movies
* Search movies in real time using TMDB
* Store **search queries and interactions** in Appwrite
* Generate **Trending Movies based on real user search counts**
* View detailed movie information (ratings, overview, posters)
* Save movies for later viewing (favorites/watchlist)
* Experience smooth navigation using file-based routing

Search analytics are persisted in **Appwrite**, enabling data-driven trending sections instead of static TMDB lists.

---

## 🛠️ Tech Stack

* **Expo** – Cross-platform development
* **React Native** – Mobile UI framework
* **Expo Router** – File-based navigation
* **TMDB API** – Movie data source
* **Appwrite** – Backend-as-a-Service (search analytics & trending logic)
* **TypeScript** – Type safety and maintainability

---

## 📦 Getting Started

### 1️⃣ Install Dependencies

```bash
npm install
```

### 2️⃣ Start the Development Server

```bash
npx expo start
```

Once started, you can run the app using:

* 📱 **Expo Go** (quick testing)
* 🤖 **Android Emulator**
* 🍎 **iOS Simulator**
* 🧪 **Development Build**

---

## 🗂️ Project Structure

```bash
app/
 ├── (tabs)/              # Tab-based navigation
 ├── movie/               # Movie detail screens
 ├── search/              # Search & results
 ├── trending/            # Trending based on Appwrite analytics
 ├── index.tsx            # Home screen
 └── _layout.tsx          # App layout
```

services/

```bash
 ├── tmdb.ts              # TMDB API handlers
 ├── appwrite.ts          # Appwrite client & DB helpers
```

This project uses **file-based routing**, meaning routes are automatically generated from the `app/` directory.

📖 Learn more: [https://docs.expo.dev/router/introduction](https://docs.expo.dev/router/introduction)

---

## 🔑 Environment Variables

Create a `.env` file in the root directory and add:

````env
EXPO_PUBLIC_TMDB_API_KEY=your_tmdb_api_key
EXPO_PUBLIC_APPWRITE_ENDPOINT=https://cloud.appwrite.io/v1
EXPO_PUBLIC_APPWRITE_PROJECT_ID=your_project_id
EXPO_PUBLIC_APPWRITE_DATABASE_ID=your_database_id
EXPO_PUBLIC_APPWRITE_SEARCH_COLLECTION_ID=your_search_collection_id
```env
EXPO_PUBLIC_TMDB_API_KEY=your_tmdb_api_key
````

> ⚠️ Never commit your API keys to version control.

---

## 📊 Trending Logic (Appwrite)

Trending movies are calculated dynamically using **Appwrite search analytics**:

* Each search query is stored in Appwrite
* Movie IDs increment a `searchCount`
* Top searched movies are fetched, sorted, and displayed as **Trending**

This ensures trending results reflect **real user behavior**, not static popularity lists.

---

## ♻️ Reset the Project

If you want a clean slate:

```bash
npm run reset-project
```

This will:

* Move existing starter code to `app-example/`
* Create a fresh `app/` directory

---

## 📚 Learn More

* 📘 [Expo Documentation](https://docs.expo.dev/)
* 🧭 [Expo Router Guide](https://docs.expo.dev/router/introduction/)
* 🎓 [Learn Expo Tutorial](https://docs.expo.dev/tutorial/introduction/)

---

## 🌍 Community & Support

* ⭐ [Expo on GitHub](https://github.com/expo/expo)
* 💬 [Expo Discord](https://chat.expo.dev)

---

## ✨ Author

Developed with ❤️ by **Sayan**
Happy coding and enjoy building with Expo!
