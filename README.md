# CodepathProject 
A group repository for Android Codepath 2022 Course.
===

# TickStock

## Table of Contents
1. [Overview](#Overview)
1. [Product Spec](#Product-Spec)
1. [Wireframes](#Wireframes)
2. [Schema](#Schema)

## Overview
### Description
An app that allows the user to view stock information, favorite stocks and add them to a watchlist, view trending stocks, view top movers, and view crypto.

### App Evaluation
[Evaluation of your app across the following attributes]
- **Category:** Finance
- **Mobile:** This app would be developed for mobile but should also be available on a computer.
- **Story:** Pulls stock data from YH Finance API and allows users to view them.
- **Market:** Anyone with an interest in stocks or crypto.
- **Habit:** This app would be used when the user wants to search up stock information.
- **Scope:** We start with showing stocks and maybe include crypto, we could, in the future, allow the user to connect their financial accounts to the app and view their information in one place.

## Product Spec

### 1. User Stories (Required and Optional)

**Required Must-have Stories**

* [] Page that shows favorited stocks information
* [] Page with stocks
* [] Trending stocks
* [] Profile page
* [] Being able to log in and log out of account.

**Optional Nice-to-have Stories**

* Sort-by option for the users


### 2. Screen Archetypes

* Favorited stocks page
   * Show list of stocks favorited by the user
* Top Movers
   * List of stocks with the biggest move
* Login Screen
  * Username and password input
* Trending stocks
  * Show trending stocks
* Settings/Profile
  * Lets user log out
  * Shows username
  * Change password

### 3. Navigation

**Tab Navigation** (Tab to Screen)

* Favorited stocks
* Top Movers
* Trending stocks

**Flow Navigation** (Screen to Screen)

* Log in
   * Sign up if no log in
   * Profile page
* All screens with stock list
   * Stock details


## Wireframes
[Add picture of your hand sketched wireframes in this section]
<img src="https://i.imgur.com/PRPx0s6.jpg" width=600>

## Schema
### Models
| Property      | Type        | Description  |
| ------------- |:-------------:| ------------:|
| symbol        | string | Stock symbol seperated by comm. Max 10|
| interval      | string | price interval|
| range | string |date range |
| price | number  |Current stock price |
| User |
| favorites | Arrays|Array to hold favorited stocks/crypto|
### Networking
- Base URL - https://yfapi.net
#### List of network requests by screen
    - Home Feed
       -(Read/GET) Get the favorite stocks/crypto from the favorites array
    - Top Stocks
       -(Update/PUT) Refreshes the screen when pulling down
    - Top Crypto
       -(Update/PUT) Refreshes the screen when pulling down
    - Favorite List
       -(Read/GET) Get the favorite stocks/crypto from the favorites array
       -(Delete/DELETE) On long hold, remove specific stock/crypto from favorites list
       -(Update/PUT) Refreshes the screen when pulling down
    -News
       -(Update/PUT) Refreshes the screen when pulling down
    -Account Overview
       -(Delete/DELETE) Clear stocks -> Deletes all favorited stocks
       -(Delete/DELETE) Clear crypto -> Deletes all favorited stocks
       -(Delete/DELETE) Clear news -> Deletes all favorited news
### User Progress Report GIF
![Login and SignUp](https://github.com/SimpleCodepathProject/CodepathProject/blob/main/codepathProject.gif)
![data](https://user-images.githubusercontent.com/73362290/162507276-375e4f04-e9d9-47f0-8382-a3dea34ae242.gif)

[x] Setting Up a Log in and Sign page user Parse
[x] Setting up fragments for the top stocks feed, profile, and favorited.
[x] Successfully managed to get information from api and goes on infininetly 
