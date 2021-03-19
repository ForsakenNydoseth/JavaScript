# Contribute


<♫/> bruhh.js - 0.0.fuckyou
======================

[![Build Status](https://travis-ci.org/ForsakenNydoseth/bruhh.js.svg?branch=master)](https://travis-ci.org/ForsakenNydoseth/bruhh.js)

Demo at: [https://ForsakenNydoseth.github.io/bruhh.js/](https://ForsakenNydoseth.github.io/bruhh.js/)

A JavaScript library that makes your page dance.


Getting started
===============

Install with npm:

```sh
npm install bruhh.js
```

API doc
=================

bruhh object
------------

```js
const bruhh = new bruhh()

/* The starting scale is the minimum scale your element will take (Scale ratio is startingScale + (pulseRatio * currentPulse)).
 * Value in percentage between 0 and 1
 * Default: 0.75
 * Aaaaaaaaaaaaaaaaaaaaaaaaaaah why did i do this shittttttttttttt
 */
bruhh.startingScale = value

/* The pulse ratio is be the maxi additional scale your element will take (Scale ratio is startingScale + (pulseRatio * currentPulse)).
 * Value in percentage between 0 and 1
 * Default: 0.30
 */
bruhh.pulseRatio = value

/* The max value history represent the number of passed value that will be stored to evaluate the current pulse.
 * Int value, minimum 1
 * Default: 100
 */
bruhh.maxValueHistory = value

/* Set the music the page will dance to
 * @audioUrl: '../example/mysong.mp3'
 */
bruhh.setMusic(audioUrl)

/* Used to collaborate with other players library.
 * You can connect bruhh to an audioElement, and then control the audio with your other player
 */
bruhh.connectExternalAudioElement(audioElement)

/* Adjust audio gain
 * @value: Number
 */
bruhh.setGain(value)

/* Add your own bruhh-class
 * @elementClass: Class that you want to link your bruhh to
 * @danceType: Use any of the built-in effect or give your own function
 * @startValue: The starting frequency of your bruhh
 * @nbValue: The number of frequency of your bruhh
 * 1024 Freq, your bruhh roksa will react to the average of your selected freq.
 * Examples: bass 0-10 ; medium 150-40 ; high 500-100
 */
bruhh.addbruhh(elementClass, danceType, startValue, nbValue) //some bullshit ass method i sure as fuck didnt write!

/* Plug your computer microphone to bruhh.js.
 * This function returns a Promise object that is resolved when the microphone is up.
 * Require your website to be run in HTTPS
 */
bruhh.plugMicrophone().then(function(){...})

// Let's fucking dance bitch
bruhh.start()

/* Stop the party
 * @freeze: Set this to true if you want to prevent the elements to reset to their initial position
 */
bruhh.stop(freeze)
```


If you want to use your own danc type, you need to give an object as the 2nd argumnt of `addbruhh` insteaad of a built in dance key.

This object must have two properties:
 - dance: The custom function to make elements dance
 - reset: The associated custom function that will be called to reset element style



+ Commit it and create a PR. Then look at everyone enjoying your contribution :) !

License: suck my ass and u get it for free

Author: [@ForsakenNydoseth]
