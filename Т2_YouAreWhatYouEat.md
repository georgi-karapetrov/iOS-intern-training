# Introduction

In this day and age, there's nothing people are more concerned by but their looks. And to look good, it is generally accepted that one's weight should not be more than their height in centimeters - 100. This opens a niche in the mobile applications market for the so called 'calorie trackers'.

## Requiremets
Create an iOS application which allows the user to track their daily calorie intake. The app prompts the user to enter their height in centimeters, their weight in kilograms and their [gender](https://media3.giphy.com/media/824EEmzA21JwQ/giphy.gif). Refer to [this highly credible soruce](https://www.webmd.com/diet/features/estimated-calorie-requirement) for the calorie intake table. The user then enters preexisting foods for each meal of the day. There should be at least 10 different foods to pick from. Their common nutritional value can be pulled from [here](http://www.uncledavesenterprise.com/file/health/Food%20Calories%20List.pdf).

## Before you start
Objective C provides powerful collection classes: `NSArray`, `NSDictionary` and their [mutable](https://developer.apple.com/library/archive/documentation/General/Conceptual/CocoaEncyclopedia/ObjectMutability/ObjectMutability.html) counterparts `NSMutableArray` and `NSMutableDictoinary`. [This website](https://nsscreencast.com/episodes/072-objective-c-collections) provides insight on the basic concepts.

## What to use
The main screen of the application should be provided by a [UITableViewController](https://developer.apple.com/documentation/uikit/uitableviewcontroller?changes=_6&language=objc). A very good tutorial on it can be found [here](https://www.appcoda.com/ios-programming-tutorial-create-a-simple-table-view-app/).
For the information input screens, a regular [UIViewController](https://developer.apple.com/documentation/uikit/uiviewcontroller?changes=_3&language=objc) should do the job (Xcode's interface builder can be very useful in this case). For any prompts to the user, please refer to [UIAlertController](https://developer.apple.com/documentation/uikit/uialertcontroller?changes=_4&language=objc).

## Taking baby steps

*[:(](https://i.ytimg.com/vi/76O52P_7Krw/maxresdefault.jpg)*

Your first task will be to create the 'entering foods' aspect of it. The state of entered foods **should not** persist through app launches. After the last meal of the day is entered, the app will either [fat-shame](https://img.ifcdn.com/images/3c6d7c2394454dd722a7ad68bd917c70ac5855283b813145e26e8d51990b66be_1.jpg) the user, if they exceeded the recommended daily calorie intake, or [congratulate](https://i.chzbgr.com/full/5750370048/h74351BA8/) them if they managed to fit into the diet's recommendation. People who somehow managed to get exactly what their recommended value is (please allow a margin of +/- 20 calories here) should be reminded that there is [a special place in Hell](https://en.wikipedia.org/wiki/Limbo) for them.

## Satan speeds up
The next part of the assignment is to provide an interface for the user to create their own foods (and enter their nutritional value per 100 g on their own). Of course, this would mean that the part where all the entered information is saved to the device becomes obligatory. Use of [NSUserDefaults](https://developer.apple.com/documentation/foundation/nsuserdefaults) is highly recommended for the said task. The last step is to make the app track which day was the calorie intake information added on. Knowledge on [NSDate](https://developer.apple.com/documentation/foundation/nsdate?changes=_9&language=objc) is a must.

