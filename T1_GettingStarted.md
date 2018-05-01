#Getting started

First: [dry](http://i0.kym-cdn.com/photos/images/newsfeed/000/880/036/864.jpg) theory. Read [this](https://developer.apple.com/library/content/documentation/iPhone/Conceptual/iPhoneOSProgrammingGuide/Introduction/Introduction.html#//apple_ref/doc/uid/TP40007072-CH1-SW1), [this](https://developer.apple.com/library/content/documentation/iPhone/Conceptual/iPhoneOSProgrammingGuide/ExpectedAppBehaviors/ExpectedAppBehaviors.html#//apple_ref/doc/uid/TP40007072-CH3-SW2) and [this](https://developer.apple.com/library/content/documentation/iPhone/Conceptual/iPhoneOSProgrammingGuide/TheAppLifeCycle/TheAppLifeCycle.html#//apple_ref/doc/uid/TP40007072-CH2-SW1) page of the programming guide.

Applications for iOS are built mainly using [MVC](https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller). Read the documantation page for [UIViewController](https://developer.apple.com/documentation/uikit/uiviewcontroller?language=objc).

Due to the fact that Objective C has somewhat of a quirky syntax, reading [this](http://blog.teamtreehouse.com/the-beginners-guide-to-objective-c-methods) page is also highly recommended before getting your pretty hands dirty. ;)

#The tutorial

*[aka this](https://pics.me.me/looks-like-its-time-to-oil-up-10217844.png)*

##Requiremets
Create an iOS application which greets the user by taking into consideration their name, gender (we assume there are only two for now) and whether the person [has an (un)healthy obsession with Japanese culture](http://www.dictionary.com/e/slang/weeaboo/). The application uses the corresponding prefix _"Mr/Ms"_ for *Normal* users and the suffixes _"-san/-chan"_ for *Weeaboo* users. Also, the greeting _"Konnichiwa"_ replaces the standard _"Hello_" for the latter. *Protip: you can refer to [this](https://developer.apple.com/library/content/documentation/Cocoa/Conceptual/Strings/Articles/FormatStrings.html) for a neat solution.*

##Creating the project

Open Xcode (which was conveniently installed for you :) and create a new project. Select **Single View App** (make sure **iOS** is selected at the top left corner). Give it a nice name and choose **Objective-C** from the *Language* dropdown. Navigate to your *Home* directory and create a new folder called `Projects` and `Create` you project there.

##Creating the UI
Make sure the `Project Navigator` is visible (press `⌘ + 1` if not) and select the `Main.storyboard`. From the `Utilities` panel (`⌥⌘ + 0`) drag and drop five **Label**-s, a **Button**, a **Text Field** and two **Swtich**-es onto the view controller. Arrange them to look something like [this](URL). *Protip: You can double-click on the respective control in order to edit its title.*

##Transmute the soul into the bare skeleton
Hooking up the actions actions/properties is really easy: while `Main.storyboard` is still selected in the `Project Navigator`, click on the two intersected rings icon in the top right. Xcode should automatically open the `ViewController.h` file. Press `^⌘ + ↑` to switch to the implementation file. Now `^ + Click` the first switch from the panel with `Main.storyboard` on the left and drag it under the `@interface` section in the `ViewController.m` file to the right. Give it a proper name. Congratulations, you have successfully created an `IBOutlet`! You can now create `@IBOutlet`-s for the rest of the controls. In order to create an `@IBAction` for the **Button**, `^ + Click` and drag under the `@implementation` section. Give the `@IBAction` a name like **on_SomeNameHere_Tap**. Here, you place the code to get executed when the user touches-up the button. It is up to you to implement the funcionality from the **Requirements** section. _Protip: Want to be a little more advanced? Check [this](https://useyourloaf.com/blog/objective-c-class-properties/) out._
