# Daug mobile app

## What's Daug?

**Daug is a social network for pets.**

- Your pets can **sign up or login** using their paws.
- They can **upload selfies** or **post their thoughts** for other pets to see.
- They can also look at **other pets posts** and either **paw** (like) or **scratch** (dislike) it.


### Demo and some screenshots
### [Demo - Try it on Expo](https://exp.host/@sukhjitsingh/daug-mobile)

<div style={{display: flex; flex-direction: row}}>
  <img src="screenshots/intro.png" width="270" />
  <img src="screenshots/signup.png" width="270" />
  <img src="screenshots/login.png" width="270" />
</div>
<div style={{display: flex; flex-direction: row}}>
  <img src="screenshots/feed.png" width="270" />
  <img src="screenshots/post.png" width="270" />
  <img src="screenshots/create.png" width="270" />
</div>
<div style={{display: flex; flex-direction: row}}>
  <img src="screenshots/like.png" width="270" />
  <img src="screenshots/profile.png" width="270" />
  <img src="screenshots/edit.png" width="270" />
</div>

## Getting started

```
git clone git@github.com:sukhjitsingh/daug-mobile.git

exp start

exp ios
````

## Designs

Intro, Login & Sign Up screens are based on **Robinhood App**.

Profile screen is based on **Instagram**.

Social Feed screen is based on **Facebook**.


## Milestone #1

### Objectives

- Learn how to build & organize screens in RN
- Learn advanced RN styling and use LinearGradient, Image, Icons & Custom Fonts
- Learn how to use mock data for prototyping UI screens
- Learn how to use NPM libaries such as React Native Elements, Expo & React Native Vector Icons

### TODO

- [x] Design & build an Intro Screen
  - [ ] :star: **Bonus:** Add [Snap Carousel](https://github.com/archriss/react-native-snap-carousel) with [Lottie animations](https://docs.expo.io/versions/latest/sdk/lottie.html) to Intro Screen
- [x] Design & build a Signup Screen
  - [ ] :star: **Bonus:** Add buttons to sign up with Facebook & Twitter
- [x] Design & build a Login Screen
  - [ ] :star: **Bonus:** Add buttons to login with Facebook & Twitter
- [x] Design & build a Profile Screen
  - [x] :star: **Bonus:** Add the Logout button
- [x] Design & build a Social Feed Screen with [Mock Data](https://raw.githubusercontent.com/mobilespace/daug-mobile/c4d4a331564ee490e1162f3733f3023afe3defc3/app/utils/constants.js)
- [ ] Attach screenshots/gif of screens to `README.MD`

<!-- ### Screenshots

<div style={{display: flex; flex-direction: row}}>
  <img src="screenshots/intro_screen.png" width="250" />
</div>
<div style={{display: flex; flex-direction: row}}>
  <img src="screenshots/login_screen_1.png" width="250" />
  <img src="screenshots/login_screen_2.png" width="250" />
  <img src="screenshots/login_screen_3.png" width="250" />
</div>
<div style={{display: flex; flex-direction: row}}>
  <img src="screenshots/signup_screen_1.png" width="250" />
  <img src="screenshots/signup_screen_2.png" width="250" />
  <img src="screenshots/signup_screen_3.png" width="250" />
</div>
<div style={{display: flex; flex-direction: row}}>
  <img src="screenshots/profile_screen.png" width="250" />
</div>
<div style={{display: flex; flex-direction: row}}>
  <img src="screenshots/social_feed_screen_1.png" width="250" />
  <img src="screenshots/social_feed_screen_2.png" width="250" />
  <img src="screenshots/social_feed_screen_3.png" width="250" />
</div> -->

## Milestone #2

### Objectives

- Learn how to build navigation for Daug app using [React Navigation](https://reactnavigation.org/)
- Learn mobile design patterns for navigation & screen layouts
- Learn how to quickly build RN screens and hook them up using navigation

### TODO

- [x] Understand the 3 main navigation patterns for mobile apps:
  - [x] [StackNavigator](https://reactnavigation.org/docs/hello-react-navigation.html#creating-a-stacknavigator)
  - [x] [TabNavigator](https://reactnavigation.org/docs/tab-based-navigation.html)
  - [x] [DrawerNavigator](https://reactnavigation.org/docs/drawer-based-navigation.html)
- [x] Setup a **IntroStack** (using StackNavigator) for the Intro Screen (root), Login Screen (push) & Sign Up Screen (push)
- [x] Setup a **HomeTabs** (using TabNavigator) for the Social Feed Screen (default) and Profile Screen
- [x] Setup a **RootNavigator** (using StackNavigator) with the **IntroStack** & **HomeTabs** with `mode: "modal"`
- [x] Design & build an Edit Profile Screen
- [x] Setup a **ProfileStack** (using StackNavigator) for the Profile Screen (root), Post Details Screen (push) & Edit Profile Screen (modal) with mode: "modal" and custom RNE header component
- [x] Design & build a Post Details Screen
- [x] Design & build a Create Post Screen
- [x] Setup a **SocialStack** (using StackNavigator) for the Social Feed Screen (root), Post Details Screen (push) & Create Post Screen (modal) with mode: "modal" and custom RNE header component
- [x] :star: **Bonus:** Display Posts on ProfileScreen
- [x] :star: **Bonus:** Setup a **HomeNavigator**(using DrawerNavigator) with the **HomeTabs** (as root) and update **RootNavigator** to use **HomeNavigator** instead of **HomeTabs**
- [ ] Add working gif of app to `README.MD`

## Milestone #3

### Objectives

- Learn how to make backend API calls and User Authentication
- Learn how to setup and use Redux and AsyncStorage
- Serve as an React Native app that you can showcase on your porfolio

#### URL: [https://daug-app.herokuapp.com](https://daug-app.herokuapp.com)

### TODO

- [x] Intro Screen - Make simple **`GET`** request to **`/api`** to check server status
- [x] Signup Screen - Make **`POST`** request to **`/auth/signup`** to create a new user
	- [ ] :star: **Bonus:** Add UI validation to Signup Screen - name (not null), email (format) & password (min. 8 characters)
- [x] Login Screen - Make **`POST`** request to **`/auth/login`** to validate and login an existing user
	- [ ] :star: **Bonus:** Add UI validation to Login Screen - email (format) & password (min. 8 characters)
- [x] Social Feed Screen - Make **`GET`** request to **`/api/feed/`** to get all posts for social feed
	- [ ] :star: **Bonus:** Use `ActivityIndicator` to show placeholder loading when fetching feed data
	- [x] :star: **Bonus:** Use `DeviceEventEmitter` to trigger fetching posts when the `new_post_created` event is emitted
	- [x] :star: **Bonus:** Use `timeSince()` utility function to show relative times for post creation
- [x] Create Post Screen - Make **`POST`** request to **`/api/users/:userId/posts`** to create a new post by the user
	- [x] :star: **Bonus:** Use `DeviceEventEmitter` to emit `new_post_created` event once post is created
- [x] Profile Screen - Make **`GET`** request to **`/api/users/:userId`** to get all the profile data
	- [ ] :star: **Bonus:** Use `ActivityIndicator` to show placeholder loading when fetching profile data
	- [x] :star: **Bonus:** Use `DeviceEventEmitter` to trigger fetching profile data when the `user_profile_updated` event is emitted
- [x] Edit Profile Screen - Make **`PUT`** request to **`/api/users/:userId`** to update a user's profile information
	- [x] :star: **Bonus:** Use `DeviceEventEmitter` to emit `user_profile_updated` event once user data is updated
- [x] Setup Authentication flow for app using `AsyncStorage`. Once the user has logged in then take them to home page each time they open the app again
- [x] Add working gif of app to `README.MD`


## Wrap up

### Objectives

- Add UI polish, tie up loose end and add remaining functionality
- Update Readme with app details and publish Expo app for demo
- Serve as an React Native app that you can showcase on your porfolio

### TODO
- [x] Dynamically load user info 
- [x] Fix photo upload and add take photo functionality
- [x] Add Like, Comment and Follow API functionality
- [x] Clean up and format `README.MD` to showcase app - [follow this template](https://github.com/mobilespace/MobileGuides/blob/master/showcase_app_readme.md#readme-template-for-showcasing-a-mobile-app)
- [ ] :star: **Bonus:** Add phone number UI to Edit Profile screen
- [x] :star: **Bonus:** Add Camera functionality to Create Post screen
- [ ] :star: **Bonus:** Use Redux to share state between tab bar & screens
- [ ] Add working gif of app to `README.MD`

## Feedback

In case you have any feedback or questions, feel free to open a new issues on this repo or reach out to me [**@sukhjitsingh**](https://github.com/sukhjitsingh) on Github.

For any other questions about MobileSpace in general please reach out to [**@monte9**](https://github.com/monte9) on Github.