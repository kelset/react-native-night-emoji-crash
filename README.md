# react-native-night-emoji-crash
Sample repo to repro the crash:

```
Error calling RTCEventEmitter.receiveEvent

Failed to create Value from JSON:

<stacktrace>
```

Steps to reproduce:
1. clone the repo & cd into it
2. `react-native run-android`
3. make sure the device on which you run it has the Google GBoard installed
4. tap on the textinput and write "night"
5. the GBoard will suggest in the bar the night with stars emoji 🌃
6. click on the suggestion
7. crash


Other words that trigger GBoard suggestion:
* "cat" 🐈 -> crash
* "rainbow" 🌈 -> crash
* "cloud" ☁️ -> no crash
* "sun" ⛅️ -> no crash
