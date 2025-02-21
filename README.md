# Expo Camera: Inconsistent onCameraReady Triggering

This repository demonstrates an uncommon bug related to the Expo Camera API's `onCameraReady` prop.  The issue lies in the inconsistent and unreliable triggering of `onCameraReady` across different devices and Expo SDK versions.  Attempting to access camera functionalities before the camera is fully ready can lead to crashes or unpredictable behavior.

## Bug Description

The `onCameraReady` callback, intended to signal camera readiness, is not always fired reliably. This makes it challenging to ensure that code interacting with the camera doesn't execute before the camera is properly initialized.

## How to Reproduce

1. Clone this repository.
2. Install dependencies: `npm install` or `yarn install`.
3. Run the app using Expo Go or a similar Expo client.
4. Observe that camera functions might fail or behave erratically, especially on certain devices or Expo SDK versions.

## Solution

The provided solution implements a loading state and a timeout mechanism to handle situations where `onCameraReady` might not fire promptly. This ensures smoother functionality and prevents unexpected errors.