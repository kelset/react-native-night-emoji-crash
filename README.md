# react-native-night-emoji-crash
Sample repo to repro the crash that we detected on Android 7 and 8 (haven't tested on other versions of Android):

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

This only happens on Android: I tested the steps on iOS (yes, there is a GBoard for iOS) and it doesn't happen there - btw there the words that 'trigger' emoji suggestions are different, the only one that triggers the same emoji on both platforms is "piano" 🎹 (and on iOS it doesn't crash, on Android yes) (ok maybe not the only one, but the only one I found quickly).
