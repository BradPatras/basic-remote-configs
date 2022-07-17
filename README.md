[![Maven Central](https://maven-badges.herokuapp.com/maven-central/io.github.bradpatras/brc-android/badge.png)](https://maven-badges.herokuapp.com/maven-central/io.github.bradpatras/brc-android)
[![spm version](https://img.shields.io/badge/Swift%20Package%20Manager-0.1.0-blue)](https://github.com/BradPatras/brc-ios/releases)
# basic-remote-configs  🛰📝
Bare-bones remote config platform for android and iOS.  Motivation for this project is having simple remote configs in my app projects where pulling in Firebase would be overkill.

#### Android library repo: [brc-android](https://github.com/BradPatras/brc-android)
#### iOS library repo: [brc-ios](https://github.com/BradPatras/brc-ios)

## Config file format
Configs are in JSON format. Compatible data types include `integer`, `string`, `boolean`, `null`, and `array(integer|string|boolean)`. Nested objects are not supported.

Example of config format
```json
{
  "ver": 1,
  "someFlag": false,
  "someMessage": "Welcome to easy config!",
  "nullValue": null,
  "arrayOfWords": ["super", "duper", "simple", "configs"]
}
```
`ver` is an integer value representing the config file's version. It's not required, but the client libraries use this value to publish only updates to listeners after fetching configs.

## In practice
This repo is hosting an [example config json file](/examples/simple.json). This example config is currently being consumed by the [Android Library's](https://github.com/BradPatras/brc-android) sample app. 

⚠️ &nbsp; In the current state of the library, config files need to be publicly accessible. 🤷🏻‍♂️ 

Check out the individual android/iOS library pages for language-specific examples of the library in action.
