![alt text](https://cdn3.macworld.co.uk/cmsdata/features/3523633/swift_1200home_thumb800.jpg "Logo Title Text 1")

# Swift iOS Guide
iOS Tips and Useful Things to Remember


## The Basics
Default projects come with the following:
  - a ViewController.swift file, which contains the code focused on controlling the UI and views of your application. imports UIKit, inherits UIViewController (MVC pattern)
  - a Main.storyboard file, which is essentially an XML file that contains the markup to represent existing system components. this file is used to design the look of your application
  - Assets.xcassets, where your static media files should go (images, appicons, you know - assets)
  - LaunchScreen.storyboard, your launch screen for your application
  - AppDelegate.swift, the lifecycle methods for the entire app. imports UIKit, inherits UIResponder, UIApplicationDelegate
  - Info.plist, contains specfic flags about your application

## Connecting UI to Code
Connecting your user interface to the core logic of the application is step one of even building for iOS.

#### Connect Storyboard Element to Function Call or Value
  - While holding *control* click down and then drag to the UI element that you would like to attach behavior to (should be inside of a ViewController that you are targeting!)
  - In Xcode a popup should then appear. provide it with a name (this wil be used to refer to it in code)
  - Here you select an Outlet (holds data to change appearance, etc.) or an Action(holds function to handle behavior). it should then say @IBOutlet if you selected an Outlet, and @IBAction if you selected an action.
  - make sure to properly de-register old events, properties from an item. it may cause a system error. to fix, right click on the item in question and break the connections to variables that no longer exist.
  - 
  
## Common Types

UIImage - refers to a type that is an image. has a .image property that contains the image buffer.

UIImageView - a type that contains a View and holds an image.

UIText - havent come across this yet, but probably has a .text property with the text buffer.

Markdown is a lightweight markup language based on the formatting conventions that people naturally use in email.  As [John Gruber] writes on the [Markdown site][df1]


## Classes
Classes are incredibly important in Swift. You essentially define classes in Swift files (.swift) then extend Native functionality such as UIViewController, etc. You can then attach the behavior of the class to a specific object or view.


## String Interpolation
String interpolation like Javascript's `${variable_name}` is done with `"\(variable_name)"`


## Swift Language Quirks

### IIFE

swift```
let logoView: UIImageView = {
        return UIImageView(image: UIImage(named: "logo"))
    }()
```

