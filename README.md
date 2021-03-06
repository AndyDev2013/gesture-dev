# googlecardboardblackjack

**Badjack was an experimental project to try develop with hardware I've never used before and using gestures outside of what's normally used. Therefore I developed a simplified version of BlackJack where you play against the dealer.**

## Contents

* Project
* Requirements
* Installation
* How to play
* Challenges
* Technologies used

## Project

**Purpose of the application**

Building this application was a completely experimental process for me. I had never used motion gestures before in any of the previous projects worked on. The goal was to create a game that would take advantage of motion gestures and having recently acquired a Google Cardboard I wanted to work with this new hardware. Knowing the target device would be an android mobile phone there was a bunch of features that could be used for gesture detection
* Camera
* Gps
* Accelerometer
* Microphone

In the end because the primary input for the Google Cardboard being the motion of the users head to view the current scene, It was decided to use the Acceleromter are the primary method to detect head nodding and shaking.

**Gestures identified as appropriate for this application**

Due to using a mobile device and the Google Cardboard SDK I decided the best way to interact with the device would be through using the users head movements. Particularly head nodding and head shaking, for these reasons.

* You are already using your head motion as an input
* Adding extra avenues of input would lead to confusion or a learning curve e.g using your head to steer, shouting commands, and moving your body completely around around at the same time. It's too much. I wanted the learning curve to be small and the experience to be easy to get into.

## Requirements

The game was developed using the Google Cardboard SDK and meant to be played on an Android device with high pixel density and on a newish phone. The phone I tested this project on was a Sony Xperia Z3 with a screen size of 5.2inches and a resolution of 1080 x 1920 pixels.

* Android Device with Lollipop preferabley
* Google Cardboard Headset I used was similar to these [Link](http://www.amazon.com/s/ref=nb_sb_noss?url=search-alias%3Dmobile&field-keywords=google+cardboard)

## Installation

Move the apk file named "Blackjack.apk" from the root directory to your android device through USB. Make sure your android device is set up to allow development apks. Navigate to the folder where you stored the apk and run it.

## How to Play

This game works off **two** head gestures

* Nodding in agreement (Moving head up and down)
* Shaking head in disagreement (Movind head from side to side)

The game is driven by asking you a series of yes and no questions

The game greets you with a welcome message and asks you to nod your head in agreement and shake your head in disagreement. This is just to test that the device is picking up on the head movements. The screen when then freeze briefly while the level is being loaded.

The game loop is as follows

**Loop**
* Do you wish to bet
* Do you wish to take a card

To leave this loop you choose the option **to stick** and this ends the current hand. 

Once the player runs out of money or the computer. You are placed in a room just to signify the game is over with either You Win or You Lose printed on the walls.

## Challenges

The cardboard SDK was very bare bones and had no handles on how to track the movements so I had to source a script that would do it. From there I was able to recognize head movements.
Tracking head movements even with the api was hard because of the constant headmovements to user makes while wearing the device.

The head nodding and shaking puts a bit of strain on the user because of the weight of the phone and casing for the google cardboard and over time this could get annoying.

Although I didn't think of it at the time the constant head movements might effect people who experience motion sickness because of the slight delay from moving your head to when the phone moves the cameras in the scene. I personally don't experience this but it could prove an issue for other people.

## Technologies and assets used

The model for the AI was developed by an acquaintance and the blackjack table and the room itself was put together by myself from existing assets and textures I sourced.

* [Unity3D 5.2](https://unity3d.com/)
* [Google Cardboard SDK for Unity](https://developers.google.com/cardboard/unity/)
* [Head Gesture Recognizer](https://www.assetstore.unity3d.com/en/#!/content/23585)
* [Casino Assets](https://www.assetstore.unity3d.com/en/#!/content/26557)
