# Introduction

Let me start with a question. What do you find cooler?

1. Talking to your friends in real life
2. Talking to your friends via your smartphone (Messenger, WhatsApp, Viber, Messages)
3. Talking to the deceased via a psychic/Ouija board
4. Talking to the deceased via your smartphone

If your answer only contains even-numbered rows, then this is the right task for you.

# The task
Create an iOS application which allows the user to communicate with other users (the hip new word the cool kids are using nowadays is 'chatting'). The interface should allow the user to see other nearby users of the app (in the same network and in Bluetooth range).

## Apology for getting ahead of myself
The application should be written in [The Swift programming language](https://developer.apple.com/swift/). A good introduction to the language's syntax and basic concepts can be found [here](https://docs.swift.org/swift-book/GuidedTour/GuidedTour.html). **Nota bene: Please make sure you have got familiar with the basic aspects and concepts of the language (`Optionals`, `Unwrapping` etc) before diving into coding.** A good way to test simple ideas in Swift is by creating a so-called `Playground` (in Xcode `File` -> `New` -> `Playground...`). A *Hello world* can (and should) be written in one.

## What to use
The good guys at Apple Inc have provided [this](https://developer.apple.com/documentation/multipeerconnectivity) little gem, conveniently serving all our needs for the task in hand.

# Requirements
The user should be presented with an interface for creating a profile with username, password and avatar. After this is done, a list of all nearby discoverable devices running the app should be presented and the user can choose any of them to strike a conversation with. The chat interface should resemble Apple's Messages app or Facebook's Messenger app (differently coloured bubbles for the user's texts and for their interlocutor's texts). A timestamp for when the message was received should also be visible on tapping on the message.

# Switching the plane
When the user has less than 50% battery, they enter the 'dying' state. This means they become discoverable by other less than 50% battery users. The user becomes invisible for people with more than 50% battery. When the battery reaches 25% and below, the user becomes a 'hollow', which means they can chat with other hollows and 'dying'. At 10%, the user becomes 'undead'. They can communicate with all of the above and undeads. At 5% and below, the user becomes a ghost. Ghosts can haunt every other type, which means they can chat with everybody, as well as apply curses to Humans (more than 50% battery health). Curses could be various. For example:

1. Blind - the Human cannot see anyone for a given period of time
2. Silence - the Human can see, but cannot chat for a given period of time
3. Posession - the Human babbles in an unknown language (every time they try to send a message, it gets corrupted to a word-like text) for a given period of time
4. *left blank intentionally, fill with own idea*
5. *left blank intentionally, fill with own idea*

It is important to note that charging your device switches the status and one can become Human again, if charged to above 50%.
Here's a convenient reference table of the interactions between the creatures:

|        | Human | Dying | Hollow | Undead | Ghost |
|--------|-------|-------|--------|--------|-------|
| Human  |   ✓   |   ✕   |   ✕    |   ✕    |   ✕   |
| Dying  |   ✕   |   ✓   |   ✕    |   ✕    |   ✕   |
| Hollow |   ✕   |   ✓   |   ✓    |   ✕    |   ✕   |
| Undead |   ✕   |   ✓   |   ✓    |   ✓    |   ✓   |
| Ghost  |   ✓   |   ✓   |   ✓    |   ✓    |   ✓   |

# In-app purchases
The users are kindly offered Holy candles ($0.99/candle) and Saint's medallions ($2.99/medallion) to prevent ghost hauntings. Holy candles cure one curse only, while the Saint's medallions provide curse immunity. Too bad they break with use (they only provide 1 hour of immunity).

# Enduring solitude
The ethereal plane is inhabited by friendly ghastly figures, called 'spectres'. Spectres can be chatted to and randomly occur in any Human's discovery list. However, they are twice as likely to occur to Humans with the 'gift' (the gift is alloted at account creation, meaning the spectre occurence chance is 2x the normal). Spectres can give insight of the ethereal plane to the Humans (when asked), for instance how many ghosts are there nearby, what it is in the afterlife and even spells to counter ghosts (special text, sent to the 'ghost' user, which disables haunting for a given period of time).