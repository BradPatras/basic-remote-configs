## This repo is archived, the torch has been passed to [brc-multiplatform](https://github.com/BradPatras/brc-multiplatform)

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
`ver` is an integer value representing the config file's version. It's not required, but if it's present the client libraries will use this value when deciding if their local cache needs updating.

## In practice
This repo is hosting an [example config json file](/examples/simple.json). This example config is currently being consumed by the [Android](https://github.com/BradPatras/brc-android) and [iOS](https://github.com/BradPatras/brc-ios) library's sample apps. 

🔐 &nbsp; Both libraries allow for custom request headers to facilitate auth tokens or whatever else you might need.

Check out the individual android/iOS library pages for language-specific examples of the library in action.
