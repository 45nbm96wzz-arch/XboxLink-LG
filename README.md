# XboxLink-LG

Experimental LG webOS TV launcher for Xbox Remote Play.

## What this build does

This first test build is a small TV-friendly launcher. Its button opens Microsoft's Xbox Remote Play website in the TV browser. It does **not** implement the Xbox streaming protocol itself, and successful playback on older LG webOS firmware is not guaranteed. The TV browser may reject the site or lack required WebRTC, codec, or DRM support.

The app does not collect or store Microsoft credentials. Sign in only on Microsoft's own website.

## Build an installable package

1. Open the **Actions** tab in this repository.
2. Select **Build XboxLink webOS app**.
3. Select **Run workflow** on the main branch.
4. Wait for the workflow to finish successfully.
5. Open the completed run and download the **XboxLink-LG-IPK** artifact.
6. Unzip the downloaded artifact to obtain the `.ipk` file.

The workflow uses LG's official webOS CLI packaging command to create the IPK.

## Install on an LG TV

Use the TV's Developer Mode app and its Device Portal / installation page to install the IPK, as you did with other homebrew apps. Keep Developer Mode enabled.

## Test

Launch **XboxLink** from the TV's apps list and select **OPEN XBOX REMOTE PLAY**. If Microsoft reports an unsupported browser, or the stream fails to start, that indicates a TV browser/platform compatibility limitation rather than a problem with your Xbox account.

## Current limitations

- This is a launcher/proof-of-concept, not a native Xbox Remote Play client.
- It has not yet been tested on the target TV.
- Xbox Remote Play requires browser capabilities and media support that may not be available on older webOS releases.
- No guarantee of controller input through the TV browser.
