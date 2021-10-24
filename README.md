# basic-remote-configs
Bare-bones remote config library

Example of config format
```json
{
  "ver": 1,
  "exampleFlag": true
  "exampleMessage": null
}
```
`ver` is an integer value representing the config file's version, it is the only required config key and is essential for the clients to ensure the most recent version is being used.

Compatible data types include `integer`, `string`, `boolean`, `null`, and `array(integer|string|boolean)`.
