# Flutter Meal App

This Flutter-based Meal App allows users to explore a variety of meals categorized by cuisine type. Users can view detailed meal information, apply dietary filters such as gluten-free or vegan, and manage a list of their favorite meals. The app is designed with clean architecture and state management using the Provider package.

## Overview

The Meal App serves as a recipe exploration tool that helps users:
- Browse meals by different food categories
- Filter meals based on dietary preferences
- View detailed instructions and ingredients for each meal
- Mark and unmark favorite meals
- Navigate easily using a bottom tab layout

## Main Features

- Category-wise meal listing
- Detailed meal view with ingredients and cooking steps
- Favorite meals management
- Dietary filters: gluten-free, lactose-free, vegan, and vegetarian
- Tab-based navigation between categories and favorites
- Drawer-based navigation to filter screen
- State management using Provider

## Project Structure
lib/
├── screens/                # All major UI screens
│   ├── home_screen.dart    # Main dashboard (Tabs: Categories/Favorites)
│   ├── category_screen.dart# GridView of meals by category
│   ├── meal_detail_screen.dart # Ingredients/steps + favorite toggle
│   └── filters_screen.dart # Dietary preference settings
├── widgets/                # Reusable components
│   ├── meal_card.dart      # Compact meal preview card
│   └── section_header.dart # Styled section titles
├── providers/              # State management
│   └── meals_provider.dart # Handles favorites/filters
├── models/                 # Data structures
│   ├── meal.dart           # Meal model (id, title, ingredients...)
│   └── category.dart       # Category model (id, title, color)
└── data/                   # Mock data
    └── dummy_data.dart     # Hardcoded meal database


## How It Works

1. The app starts in `main.dart` where all the providers are initialized and routes are set.
2. The home screen (`tabs.dart`) presents two main tabs: Categories and Favorites.
3. Selecting a category leads to the meals screen where meals for that category are listed.
4. Selecting a meal shows a detailed page with ingredients and steps.
5. Users can apply dietary filters from the filter provider, and those are used by `meals_provider.dart` to dynamically update meal lists.
6. Users can favorite or unfavorite meals, which is managed by `favorites_provider.dart`.

## Demo Video

To view a working demo of this application:  
[ Watch Demo Video ](https://drive.google.com/file/d/17tJrGAuJ9_cvD_gHnAKwMu9jR17vbzQD/view?usp=drive_link)  


## Future Scope

- Integration with a backend service or database for real-time meal data
- User authentication and personalized meal lists
- Search functionality for quicker meal lookup
- Integration of animations and transitions for enhanced UI experience
- Option to add new custom meals by the user


    
