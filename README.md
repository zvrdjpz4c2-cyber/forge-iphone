# Forge for iPhone

An iPhone app for the workout tracker at https://jacked.floot.app. Sign in using your existing tracker account. Your workout history stays in the tracker; this repository contains no account passwords or personal workout data.

## Download the iPhone app

Open **Actions → Build iPhone IPA → Run workflow**. Once the run succeeds, download **Forge-iPhone-IPA** from the run's **Artifacts** section. Extract the downloaded archive and give **Forge-unsigned.ipa** to your installer, which must sign it.

The app needs an internet connection and supports iPhone on iOS 16 or later. Its home-screen name is Forge. Wait for “All changes saved” before closing a workout.

## Source and build

`forge-ios-cloud-source.zip` contains the SwiftUI/WebKit app, Xcode project, icons and build helper. The workflow extracts the source and compiles an unsigned device build on a standard GitHub macOS runner. No Apple credentials or developer certificates are used. Builds start only when requested manually.

This app displays the published workout tracker, so exercise updates made to the website appear in the app too.
