# Quickstart of Coin Quest — a geo-based AR game

This quickstart will take you through the steps to create a simple geo-based AR game powered by the Spheroid Universe Platform.

## Create an account in the Spheroid Universe Platform

Before you create your app, you need to [create an account](https://spheroiduniverse.io/marketplace/register) in the Spheroid Universe Platform.

If you already have an account in the Spheroid Universe Platform, you can skip this step.

![](../../docs/images/coin-quest/01---marketplace-register.png)

## Log in to the Spheroid Demiurge IDE

Now you have the access to all Platform services, including the Spheroid Demiurge IDE. 

Log in to the [Spheroid Demiurge IDE](https://demiurge.spheroiduniverse.io/ide), using the same email and password you used to register in the Platform.

## Create your app

Open the "Apps" tab and click the "Create" button. 

![](../../docs/images/coin-quest/02---create-app-1.png)

Enter the app name, leave the check on the "Create a layer corresponding to this app" box and click the "Create App" button. The app will be created along with the layer you will later use to publish the app into.

![](../../docs/images/coin-quest/03---create-app-2.png)

If the app doesn't get immediately created, and you get the error "Can't create an app because the app with the name 'xxx' already exists", it means the name you've chosen is already taken, so try another one.

![](../../docs/images/coin-quest/04---create-app-error.png)

## Download the source code

We have already prepared for you the source code you'll need to create a demo app. Download a zip archive from [our repo](https://github.com/SpheroidUniverse/SpheroidScript).

![](../../docs/images/coin-quest/08---github-download.png)

Then extract contents of the 'SpheroidScript-master\examples\CoinQuest\src' folder from the zip archive. You're now all set to upload the source code to your app!

## Upload the source code to Spheroid Demiurge IDE

Now, what you need to do is to upload the extracted files with source code to the IDE keeping the tree structure unchanged. So in the root of your app you need to have three folders named "assets", "client" and "server", as well as the "app.json" file.

```
(Your app name)
|--- assets
|   |--- coin_gold.glb
|   |--- coin_silver.glb
|   |--- jump.ogg
|   |--- map_icon_gold.png
|   |--- map_icon_silver.png
|   |--- notification_icon_gold.png
|   |--- notification_icon_silver.png
|--- client
|   |--- Client.spheroid
|--- server
|   |--- Bounds.spheroid
|   |--- Coin.spheroid
|   |--- CoinGenerator.spheroid
|   |--- Constants.spheroid
|   |--- GetCoinsAction.spheroid
|   |--- Ruler.spheroid
|   |--- SpatialGrid.spheroid
|   |--- StartupAction.spheroid
|   \--- TakeAction.spheroid
\--- app.json
```

Currently, you can't upload a whole zip or a folder to the IDE but you can upload multiple files at once by a single drag-n-drop.

Open the "IDE" tab and select your app in the dropdown list.

![](../../docs/images/coin-quest/05---create-app-complete.png)

![](../../docs/images/coin-quest/06---ide-select-app.png)

Create the "assets" folder: right-click the app name and select the "Create a folder" option, then, when the dialog comes up, enter "assets" and click "OK".

![](../../docs/images/coin-quest/09---ide-create-folder-1.png)

![](../../docs/images/coin-quest/10---ide-create-folder-2.png)

Repeat these steps for the "client" and "server" folders. This is what you'll see after you're done:

![](../../docs/images/coin-quest/11---ide-create-folders-complete.png)

For each folder, left-click the folder to expand it. The text "Drag-n-drop files here to upload" will appear on the right. Drag-n-drop the files with the source code from the corresponding folder on your local PC.

![](../../docs/images/coin-quest/12---ide-drag-n-drop-files.png)

Then, left-click the root folder (with the same name as your app) to expand it and drag-n-drop the "app.json" file.

You're done! Now you can proceed to publishing the app.

## Publish your app

Publish your app. Click the "Publish" button in the top menu and, when the dialog comes up, keep the default settings, and click the "Publish" button at the right bottom of the dialog.

![](../../docs/images/coin-quest/13---publish-1.png)

If the publication has been successful, you will see four info messages in the "Build" tab in the bottom pane. Congratulations, you have published your app!

![](../../docs/images/coin-quest/14---publish-2.png)

If you don't see the four info messages, or you see error messages instead, check you've followed the previous steps accurately and, if so, [write us an issue](../../docs/submit-an-issue.md), and we will help you solve the problem.

## Launch your app on your mobile phone

Now as you have your app built and published, it's time to run it on your mobile phone.

Download the XR Hub Android mobile app either by [following the Google Play link](https://play.google.com/store/apps/details?id=io.spheroid.spheroidandroid) or by scanning the QR code:

![](../../docs/images/coin-quest/15---XR-Hub-QR.png)


| ![](../../docs/images/coin-quest/16---google-search.png) | ![](../../docs/images/coin-quest/17---google-app-1.png) | ![](../../docs/images/mobile-placeholder.png) | ![](../../docs/images/mobile-placeholder.png) |
| --- | --- | --- | --- |
| ![](../../docs/images/pixel.png) | ![](../../docs/images/pixel.png) | ![](../../docs/images/pixel.png) | ![](../../docs/images/pixel.png) |

Currently, XR Hub works on the Android devices that [support ARCore](https://developers.google.com/ar/discover/supported-devices) only. iOS version of the app will be released soon.

Launch the XR Hub app on your phone.


| ![](../../docs/images/coin-quest/18---google-app-2.png) | ![](../../docs/images/coin-quest/19---xrhub-splash-1.png) | ![](../../docs/images/coin-quest/20---xrhub-splash-2.png) | ![](../../docs/images/coin-quest/21---xrhub-splash-3.png) |
| --- | --- | --- | --- |
| ![](../../docs/images/pixel.png) | ![](../../docs/images/pixel.png) | ![](../../docs/images/pixel.png) | ![](../../docs/images/pixel.png) |

Tap the menu button in the bottom center, then tap the account icon and log in to the app using the same email and password you used to register in the Platform.

| ![](../../docs/images/coin-quest/22---xrhub-metaworld.png) | ![](../../docs/images/coin-quest/23---xrhub-hub.png) | ![](../../docs/images/coin-quest/24---xrhub-login-1.png) | ![](../../docs/images/coin-quest/25---xrhub-login-2.png)
| --- | --- | --- | --- |
| ![](../../docs/images/pixel.png) | ![](../../docs/images/pixel.png) | ![](../../docs/images/pixel.png) | ![](../../docs/images/pixel.png) |

When you're authorized, swipe right through the list of worlds to find the world your app has been published into (world is called "layer" in IDE). Note that if you're not logged in, you won't see the world, because the worlds created by developers are private. In the later tutorials you will learn how to add testers to your layer aka world.

| ![](../../docs/images/coin-quest/26---xrhub-user-app.png) | ![](../../docs/images/mobile-placeholder.png) | ![](../../docs/images/mobile-placeholder.png) | ![](../../docs/images/mobile-placeholder.png) |
| --- | --- | --- | --- |
| ![](../../docs/images/pixel.png) | ![](../../docs/images/pixel.png) | ![](../../docs/images/pixel.png) | ![](../../docs/images/pixel.png) |

When you've found your world, tap the "Launch" button, and you will see the coins on the screen. Congratulations, you have successfully run your app in the XR Hub! Collect some coins and see how the value on the counter changes after you tap on each coin. See the logs from the app in real time in the IDE in the "Client" and "Server" tabs in the bottom pane.

## Troubleshooting

If you have encountered any problems, please let us know by [submitting an issue](../../docs/submit-an-issue.md), we will make sure to help you find the solution. Please don't hesitate to contact us, as your issues and our replies will help to make our platform better and will be valuable to other developers.

## What next?

This quickstart has covered the bare minimum base to start developing AR applications powered by the Spheroid Universe platform.

In the next tutorials, we will take a closer look at what we've done by exploring the source code of the app.
We'll get familiar with the Spheroid Script – the Platform language.
We'll talk about the project structure and discuss some key concepts e.g. dividing code into a client-side part, and a server-side part.
Finally, we'll learn the basics of persisting data in a cloud database using the Spheroid SQL.

## What's next?

- [More examples](..)
- [Spheroid Script Documentation](https://spheroiduniverse.github.io/SpheroidScript/)
- [Got a question? Submit an issue on GitHub](../../docs/submit-an-issue.md)