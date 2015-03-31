Air Native Extension for Flurry Analytics (iOS + Android)
======================================

This is an [Air native extension](http://www.adobe.com/devnet/air/native-extensions-for-air.html) for [Flurry](http://flurry.com) SDK on iOS and Android. Forked from [FreshPlanet](http://freshplanet.com). Extended functionality by [A Sling and a Stone] (http://aslingandastone.com).


Flurry SDK Versions
---------

* iOS: 6.2.0
* Android: 5.3.0


Installation
---------

The ANE binary (AirFlurry.ane) is located in the *bin* folder. You should add it to your application project's Build Path and make sure to package it with your app (more information [here](http://help.adobe.com/en_US/air/build/WS597e5dadb9cc1e0253f7d2fc1311b491071-8000.html)).


##Usage

####Start a Flurry session

```actionscript
Flurry.getInstance().setIOSAPIKey(YOUR_IOS_API_KEY_HERE);
Flurry.getInstance().startSession();
```

####Stop a Flurry session

```actionscript
Flurry.getInstance().stopSession();
```

####Log an Event

```actionscript
Flurry.getInstance().logEvent("Basic Event");
```

####Log an Event with Parameters

```actionscript
Flurry.getInstance().logEvent("Basic Event", {param1:value1});
```

####Log a Timed Event

```actionscript
Flurry.getInstance().startTimedEvent("Basic Timed Event");
```

Timed events must be stopped when completed. 

```actionscript
Flurry.getInstance().stopTimedEvent("Basic Timed Event");
```


####Log a Timed Event with Parameters

```actionscript
Flurry.getInstance().startTimedEvent("Basic Timed Event", {param1:value1});
```

Authors & License
------

This ANE has been written by [Thibaut Crenn](https://github.com/titi-us) and [Alexis Taugeron](http://alexistaugeron.com). It belongs to [FreshPlanet Inc.](http://freshplanet.com) and is distributed under the [Apache License, version 2.0](http://www.apache.org/licenses/LICENSE-2.0).

Extended functionality by [Cam Heikkinen](https://twitter.com/camaech). Written for [A Sling and a Stone] (http://aslingandastone.com).