# menu-fetcher

This project is a side project to my bachelor thesis.
This project uses the las2peer mensa service to get the menu for mensas in Germany.


## Use
This project will only work on iPhones and iPads running at least iOS 12.
You might need to install the Shortcuts App from the AppStore.

There are currently two shortcuts. The first one gets the menu for a mensa that you can select.

This repository hosts links to two Apple shortcuts and only serves as a documentation tool on how to install the 
Shortcut on your device. 

  * Shortcut with selection: https://www.icloud.com/shortcuts/fd0953e6a9fc4711b91ff2df4a4f31ec
  * Shortcut with default mensa and push notification: https://www.icloud.com/shortcuts/ded24779fbc8463283d766c446ebf6cc

Note that you need to authorize the use of untrusted shortcuts.
To do this navigate to the `Settings` app and locate the `Shortcuts` listing. Enable `Allow Untrusted Shortcuts`
Start them by tapping on the shortcut. You can add the Shortcut as a widget on the home screen to get the menu even faster

### Shortcut with selection
This shortcut asks the user for which canteen they want to get the menu. The menu is formatted. 

### Shortcut with default mensa
This shortcut allows you to set a default mensa when adding it. It will then skip the selection step and send you the menu as a notification. 
This shortcut can be configured as an Automation. This allows you to predefine when the shortcut should run (e.g: get it on all weekdays at 10a.m).

For this, you need to be running iOS 14 or later. 
1. Choose the `Automation` tab on the bottom.
2. Tap on the "plus" button in the top right corner
3. Tap on `Create Personal Automation`
4. Select an event. (For example you could define "When I leave work" in a time range from 10a.m.-2p.m. If you go to the canteen every day you could also define it to run every weekday at 10a.m.) 
5. Make sure to disable `Ask Before Running`
6. Now click on `Next` in the top right corner
7. Click on the `Add Action` button
8. Search for `Shortcuts`
9. Click on `Run Shortcut`
10. Select the `Menu For Your Mensa` shortcut
11. Click on `Next` in the top right corner
12. Click on `Done` in the top right corner

## Adding canteens

Currently only two mensas are displayed in the list. 
Basically any mensa which is supported by the OpenMensa Api can be used. If you would like to use your own mensa, you need to look up the id of the mensa assigned to it by the open mensa api. If you know the Id the mensa can be added by adding it to the dictionary and the list. 


1. First locate the list. 
2. Click on `Add new item`
3. Enter a name
4. Copy the newly added name
5. Locate the dictionary containing the mensas
6. Click on `Add new item` 
7. Select `Dictionary` 
8. Paste the name you copied in step 4. Make sure to use the same name to add it. 
9. Tap on `0 items` 
10. Tap on `Add new item`
11. Select Text
12. Type `id` into the key (left) field
13. Paste the id that you copied from the OpenMensa api into the field next to the key field (the one which you filled out in the step before)
14. Tap on `Add new item`
15. Select Text
16. Type `name` into the key (left) field
17. Type in the name for the mensa again. This is the name which will be displayed in the title of the menu
18. Click on `Done` in the upper right corner
19. Optionally you can run a test by clicking on the play-button in the bottom right corner
20. Click on `Done` again to save the changes.
