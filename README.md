# Expo Linking.getInitialURL() Inconsistently Returns Null

This repository demonstrates a bug in Expo's `Linking.getInitialURL()` API where it inconsistently returns `null` when the app is launched with a deep link.  This makes it unreliable to handle initial app launch with deep links.

## Bug Description

The `Linking.getInitialURL()` method is supposed to return the initial URL used to launch the app. However, in certain situations, it returns `null` even when a deep link was used to open the app. This behavior is inconsistent and makes it difficult to build robust deep link handling logic.

## Reproduction

The `bug.js` file contains the minimal code to reproduce the issue.  You'll need to set up an Expo project and configure a deep link scheme for your app.

## Solution

The `bugSolution.js` demonstrates a possible workaround involving multiple attempts to retrieve the URL using a timeout.  However, this is not an ideal solution and highlights the need for a more reliable API behavior.