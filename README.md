# Cordova text-to-speech plugin

This is a simple app which demonstrates the [Ionic Native 3 tts plugin](https://ionicframework.com/docs/native/text-to-speech/) which takes advatage of the [Cordova text-to-speech plugin](https://github.com/vilic/cordova-plugin-tts). Idea of this app is a text synthesis, which means you can type a text in the input field and the cordova plugin plays your text as audio. 

![Screenshot](https://github.com/GehirnWabbel/Cordova-Text-to-Speech-Demo/blob/master/screenshotTTS.png)

## Prerequisites
- Make sure Cordova and Ionic are installed on your machine. If this is not the case look it up [here](https://ionicframework.com/docs/v1/guide/installation.html).
- Due to the use of cordova, this app needs to run either on your mobile device or a simulator.
- Supported platforms are:
    - iOS 7+
    - Windows Phone 8
    - Android 4.0.3+ (API Level 15+)

## Installation
As a next step you need to install the cordova text-to-speech plugin and the ionic native plugin. Run the following commands in your console.

```sh
$ ionic cordova plugin add cordova-plugin-tts
$ npm install --save @ionic-native/text-to-speech
```
## Essential code

```typescript
// Use of Cordova Plugin
  async sayText():Promise<any>{
    try{
      await this.tts.speak(this.text);
      console.log("Successfully spoke " + this.text)
    }
    catch(e){
  console.log(e);
    }
  }
```
