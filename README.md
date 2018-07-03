Here's my complete list of features and updates I could learn, listen and find about iOS, tvOS, watchOS, MacOS, SDKs and developer tools that were announced at WWDC 2018. This year WWDC 2018 Focus is on performance improvements and deepening existing functionality.

The [unofficial WWDC Mac app](https://github.com/insidegui/WWDC) is good way to download the videos and keep track of what you've already watched.

[Apple Platform SDK API Differences](http://codeworkshop.net/objc-diff/sdkdiffs/)

[Documentation Archive](https://developer.apple.com/library/archive/navigation/#section=Platforms&topic=iOS)

[Apple Developer Documentation](https://developer.apple.com/documentation)

## OSX → macOS 10.14 Mojave

<https://www.apple.com/macos/mojave-preview/>

- Dark mode: Official Apple app and Xcode support
- Dynamic desktop: desktop subtle changes throughout the day
- Stacks: group files on your desktop
- Finder Gallery View: carousel view of files with Automator actions avail from the sidebar
- QuickLook: markup option, signatures and video trimming
- ScreenShots: see a thumbnail in the bottom right corner. You can expand the preview by double-clicking on the thumbnail, an expanded menu, with new options so you can record video
- Continuity Camera: ability to seamlessly sync messages and files, snap a picture on your iPhone from your computer, and then import that image directly into a piece of content on pages, numbers or keynote.
- Apps: News, Stocks, Voice Memos, Home come with new and redesigned App Store
  * Microsoft Office 365, Adobe Lightroom CC, and Barebones BB Edit will go back Mac App Store
- Group FaceTime: Users are able to drop in and out of videos call whenever they want
- Security protections: on camera, microphone, mail, messages, and backups
- Support for cross-platform applications in testing
- Safari: social tracking blocking such as like, share, and comment sections
- UIKit to the Mac: the new cross-platform frameworks will be available to third-party developers in 2019.

          “Are you merging macOS and iOS? No. We love the Mac”

## iOS SDK

<https://developer.apple.com/ios/>

[iOS 12.0 API Diffs](https://www.hackingwithswift.com/articles/120/ios-12-api-diffs)

- UserNotifications - new APIs for handling notifications
  * threadIdentifier. We use for creating own custom group notifications. If you do not set it, you see under the default group.
    * `threadIdentifier = nil`
  * summaryArgument. We can collect notifications under the same collect name.
    * `summaryArgument = nil`
  * summaryArgumentCount expresses the number of items that summary argument counts for in the summary.
    * `summaryArgumentCount = 3`
- Dynamic notifications - Notification Content Extension `UNNotificationContentExtension`
    * `notificationActions` : We can access notificationActions as well as dynamically anywhere
    * Allows to UserInteraction touches notifications Image
    * Allows to delete action buttons from notification actions
    * `performNotificationDefaultAction` : Allows to launching application programmatically or custom control with Notification Content Extension
    * `dismissNotificationContentExtension` : Custom dismiss content extension view
  * Notification Management
    * Show notification settings under the app notification settings page
      * Deliver Quietly: notification sent directly notification center
      * Turn Off...
  * [Critical Alert notification](https://developer.apple.com/contact/request/): Critical notification will be delivered with sound and on screen, even if the Do not disturb mode is enable.
- `UITableView`:
  * automatic cell prefetching
  * data prefetching
- Automatic Backing Store:
  * Save grayscale content for rich graphic content
  * `UIView.draw()`
  * `UIGraphicsImageRenderer`
  * `UIGraphicsImageRendererFormat.range`
- % 50 memory usage decrease for Images
- `UILabel`:
  * Uses %75 smaller backing store
- new `requestAuthorization` options `.provisional` and `.providesAppNotificationSettings`
- Coverage
  * xccov: it is a new command line tool. It helps to output formats (human-readable or JSON) more readable.
- iPhone X gives safe areas in portrait and landscape mode
- Cascade list: if Chinese first characters font does not have it, we say to use this character instead of it.
- `tableView.cellLayoutMarginsFollowReadableWidth = false`. Previously, It was true
- `tableView.insetsContentViewsToSafeArea = false`. Extending content View from edge to edge
- Automatically generate a strong password: We can define a custom password rule for sing-in our app. `UITextInputPasswordRules`
  * [Password Rules Validation Tool](https://developer.apple.com/password-rules/)
- `INRelevantShortcut` Expose Shortcuts to the Siri Watch Face
- `ASWebAuthenticationSession` handle an OAuth login flow automatically. It publishes
 instead of the `SFAuthenticationSession`.
- `INPlayMediaIntent`  Allows us to create Shortcuts to play audio and video content
- Automatic 2-factor authentication SMS codes input in the UITextfield

## watchOS SDK

<https://developer.apple.com/watchos/>

- Auto Scaling option for incomplete Assets
- Interactive Notifications
- New text styles for Fonts
- Siri Shortcuts
  * `WKRelevantShortcutRefreshBackgroundTask` : Updating your shortcuts and refresh data
- New workout builder API
  * `recoverActiveWorkoutSession()` : Automatic relaunch after crash than session and builder restore
- New Background Mode for Audio

## tvOS SDK

<https://developer.apple.com/tvos/>

- Password AutoFill
- Focus Engine enhancements `UIFocusUpdateContext`
  * `IUIFocusItemContainer` interface,
  * `UIFocusMovementHint` class,
  * `IUIFocusItemScrollableContainer` interface.
- Text Scrolling
  * `label.enablesMarqueeWhenAncestorFocused = true`
- [TVUIKit](https://developer.apple.com/documentation/tvuikit)
  * TVPosterView
  * TVCaptionButtonView
  * TVCardView
  * TVMonogramView
  * TVLockupView
- `TVDigitEntryViewController`


## iOS 12

<https://www.apple.com/ios/ios-12-preview/>

-  App Store Connect app: replacement for the existing [iTunes Connect app](https://itunes.apple.com/us/app/app-store-connect/id1234793120?mt=8)
- iOS 12 adds multi-user Face ID with support for up to two faces
- Do Not Disturb: Good morning screen & During Bedtime
- Doubling down on performance
- 2x faster app launching, share sheets
- AR
  * New App: Measure
  * Apple, Pixar and Adobe back a standardized AR file format USDZ
  * Apple unveils [ARKit 2](https://www.apple.com/newsroom/2018/06/apple-unveils-arkit-2/)
- Photos
  * The app has updated search for events, locations and people. Also, we can use multiple search parameters.
  * Send photos to your friends, also send back any photos they have that are from the same event, time, or location
- Siri Shortcuts
  * Create custom voice commands with Siri that can connect with any app.
  * User can create own activation text
- Apps: New News, New Stocks, Voice Memos
- CarPlay: 3rd party navigation apps will work with CarPlay
- Automatic Passwords
- Security code AutoFill
- Third time books app name is changed. The new name is Apple Books
- Notification Center: 
  * Group Notifications
  * Interaction
  * Settings
- Screen Time: personalized usage analytics
- Parents can manage child device remotely
- Memoji: Next level of enimoji with tongue detection
- Connections: FaceTime can GroupCall with 32 people in a single call, biggest update of FaceTime
- Core ML 2
- [Safari](https://developer.apple.com/safari/whats-new/)
- More Battery info details
- RAW photo editing

## watchOS 5

<http://www.apple.com/watchos-preview/>

- watchOS 5 won’t support first gen Apple Watches
- Activity competitions and awards
- New workout types: yoga, cadence and hiking  
- Running: rolling mile pace, steps per minute or cadence
- Webkit support, reader mode
- Podcasts
- GymKit integration with GymDevice and Apple Watch
- Air quality complication
- Automatic workout detection
- Student ID card on watch
- Walkie-Talkie app
- No longer need to say "hey siri" when raising wrist
- Siri: watch face shows directions at the appropriate times of the day and provides shortcuts to functions like directions from CityMapper.
  * Notifications interactive controls available from within them for third-party apps
- Customizable Control Center
- Third-party apps ( nike & yelp ) will come to the watch face too.
- New Notification Interface: There are two interfaces for Notification. Dynamic Interface and Interactive Interface. Dynamic Interface is for previous version watchOS Notification support.
- We can add GestureRecognizer to watchOS Notification
- New background modes: Audio
- Notification delivered with varying level of urgency
- View web pages and HTML messages from Mail and Messages

## tvOS

<https://www.apple.com/apple-tv-4k/>

- Dolby Atmos and 4K HDR support
- TV App has live news
- 3rd party remote support: Crestron and Savant can control your Apple TV, including using Siri for voice search and control.
- Aerial screen saver from ISS
- Zero Sign-On: Automatically unlocks access to all the video-streaming apps that you’ve subscribed to.
- Charter Spectrum partnership


## Swift 4.2

- Swift 5 is coming in 2019
- Apple plan to deliver with OS than means no need to include the Swift runtime with apps which will result in smaller downloads and faster launches.
- Completed 18K pull-request
- SDK improvements
- Faster builds
- % 30 less app size
- [SE-0194 Derived Collection of Enum Cases](https://github.com/apple/swift-evolution/blob/master/proposals/0194-derived-collection-of-enum-cases.md)
- [Conditional Conformance Allows Composition](https://swift.org/blog/conditional-conformance/)
- [SE-0185 Synthesizing Equatable and Hashable conformance](https://github.com/apple/swift-evolution/blob/master/proposals/0185-synthesize-equatable-hashable.md)
- [SE-0202 Random Unification](https://github.com/apple/swift-evolution/blob/master/proposals/0202-random-unification.md)
- Binary compatibility with future Swift compiler releases
- [SE-0075 - Adding a Build Configuration Import Test](https://github.com/apple/swift-evolution/blob/master/proposals/0075-import-test.md)
- There is 600 Code contributors to swift in Github
- [SE-0190 - Target environment platform condition](https://github.com/apple/swift-evolution/blob/master/proposals/0190-target-environment-platform-condition.md)
- Automatic migration to new APIs
- Nesting
  * Types
    * `UIApplication.State`
    * `UITabBar.ItemPositioning`
  * Functions
    * `rect.insetBy()`
    * `image.pngImage()`
  * Constants
    * `UIFloatRange.zero`

## Design

[Apple updates Design Resources for iOS 12, adds iPad UI elements and Keynote kit](http://developer.apple.com/design/resources)
[WWDC 2018 - Human Interface Guidelines](https://developer.apple.com/design/whats-new/?id=06042018a)

## Apple Developer Portal

- Apple has announced API to talk to both Apple Developer portal and iTunes Connect. Apple has also combined Apple Developer Portal and iTunes Connect.
- ITMS Transporter has been used for uploading apps to App Store. Now, Transporter has been supported on Linux.
- TestFlight Public Links
- AppStore Connect REST API
  * Manage TestFlight, Profiles, Certificates, Apps, Devices
  * Use of JWT for authentication
  * Support for auth tokens for iTunes transporter
  * Error handling
- You are able to create and manage certificates & provisioning profiles as you do with Fastlane match.


## Xcode 10

<https://developer.apple.com/xcode/> <br>

- Multiple source compatibility continue Swift 4 / 4.2 and 3
- Some API changes will land in later Xcode 10 betas
- Complication Mode DEBUG must be incremental
- Exclusive access to memory must be Full Enforcement (Run-time Checks in All Builds)
- Integration: BitBucket and GitLab
- New code snippets tool can accessible from Xcode Editor menu
- Run the XCTest in the command line using the xcodebuild tool
- Parallel testing by creating clones of the simulators. Clones delete automatically. Also Unit & UI parallel testing is available on iOS. Unit parallel testing is available on macOS.
  * `$ xcodebuild -project Demo.xcodeproj/ -scheme Demo -destination 'platform=iOS Simulator,OS=12.0,name=iPhone 7' clean build test CODE_SIGN_IDENTITY="" CODE_SIGNING_REQUIRED=NO -parallel-testing-worker-count 4`
- Add specific test target
- Viewing results in the test log and test report
- Upload App to App Store with the xcodebuild tool
- Notarized App: Apple will stamp the app before uploading to App Store. We have to upload an app to be notarized by Apple.
  * ``$ xcodebuild -exportNotarizedApp -archivePath <xcarchivepath> -exportPath <destinationpath>``
- New shortcut: Select target device or simulator by CTRL+SHIFT+0
- Multi-Line Editing
- View as: Dark Appearance or System Appearance
- New color option in the action menu
- Create a SSH Key and upload them directly server accounts
- New playground interaction: Add new lines of code and playground is able to auto restart to playground session and continue running it.
- Bounded String Pseudolanguage: Showing potential tripping and truncation issue with special character
- You can use `#warning` instead of `// TODO:`
- Timing Summary: Build with Timing summary
  * `$ xcodebuild -showBuildTimingSummary`
- New Xcode Localization catalog `.xcloc` extension, It is a new type of localization artifact
  * Xcode Localization catalog import `$ xcodebuild -importLocalizations -project <projectname> -localizationPath </path/to/ language.xcloc>`
  * XLIFF file import `$ xcodebuild -importLocalizations -project <projectname> -localizationPath </path/to/ language.xliff>`
- `.intentdefinition` extension, allows the localize Siri Shortcuts


## Developer Tool
- Custom Instruments Template
- New logging API for finding memory issue ```os_signpost```. This will help Instrument for finding to the problem.
  * Signposts appear in the Instruments
  * We can install Custom Templates in the Instruments
- Debug your view hierarchy by using `po yourView.value(forKey: "recursiveDescription”)!`
- Dump: print all swift objects and struct properties.  
  * `(lldb) expr dump(.....)`


## Apple Design Award Winners 2018

 - [Agenda](https://itunes.apple.com/us/app/agenda-a-new-take-on-notes/id1287445660)
 - [Bandimal](https://itunes.apple.com/app/apple-store/id1065440354?mt=8)
 - [Calzy](https://itunes.apple.com/us/app/calzy-3/id623690732?mt=8)
 - [iTranslate Converse](https://itunes.apple.com/us/app/itranslate-converse/id1241264761?mt=8)
 - [Triton Sponge](https://itunes.apple.com/us/app/triton-sponge/id1156546367?mt=8)
 - [Florence](https://itunes.apple.com/us/app/florence/id1297430468?mt=8)
 - [Playdead's INSIDE](https://itunes.apple.com/us/app/playdeads-inside/id1201642309?mt=8)
 - [Alto's Odyssey](https://itunes.apple.com/app/altos-odyssey/id1182456409?mt=8)
 - [Frost](https://itunes.apple.com/app/apple-store/id1234617736?pt=1902467&mt=8)
 - [Oddmar](https://itunes.apple.com/us/app/oddmar/id1247397901?mt=8)

## App Store Review Guidelines Diff

[WWDC 2018 Edition](https://gist.github.com/hongrich/260fc8c36aaed3f2a63c0612ba9fc910)

## SiriKit
- [Human Interface Guidelines Siri](https://developer.apple.com/design/human-interface-guidelines/ios/system-capabilities/siri/)
- [SiriKit](https://developer.apple.com/documentation/sirikit)
- [Donatin Shortcuts](https://developer.apple.com/documentation/sirikit/donating_shortcuts)
- [Deleting Donated Shortcuts](https://developer.apple.com/documentation/sirikit/deleting_donated_shortcuts)
- [Accelerating App Interactions with Shortcuts](https://developer.apple.com/documentation/sirikit/accelerating_app_interactions_with_shortcuts)

## WWDC 2018 Videos

[WWDC 2018 video downloader script](https://github.com/ohoachuck/wwdc-downloader)


### Featured
- 101 - WWDC 2018 Keynote
- 102 - Platforms State of the Union
- 103 - Apple Design Awards

### App Frameworks
- 201 - Creating Apps for a Global Audience
- 202 - What's New in Cocoa Touch
- 204 - Automatic Strong Passwords and Security Code AutoFill
- 206 - What's New in watchOS
- 208 - What's New in tvOS 12
- 209 - What's New in Cocoa for macOS
- 211 - Introduction to Siri Shortcuts
- 214 - Building for Voice with Siri Shortcuts
- 217 - Siri Shortcuts on the Siri Watch Face
- 219 - Image and Graphics Best Practices
- 220 - High Performance Auto Layout
- 222 - Data You Can Trust
- 227 - Optimizing App Assets
- 228 - What’s New in Energy Debugging
- 229 - Using Collections Effectively
- 233 - Adding Delight to your iOS App
- 235 - UIKit: Apps for Every Size and Shape
- 239 - Designing Web Content for watchOS


### Distribution
- 301 - What's New in App Store
- 303 - Automating App Store Connect


### Developer Tools
- 401 - What's New in Swift
- 402 - Getting the Most out of Playgrounds in Xcode
- 403 - What's New in Testing
- 404 - New Localization Workflows in Xcode 10
- 405 - Measuring Performance Using Logging
- 406 - Swift Generics
- 407 - Practical Approaches to Great
- 408 - Building Faster in Xcode
- 409 — What’s new in LLVM
- 411 - Getting know Swift Package Manager
- 412 — Advanced Debugging with Xcode and LLDB
- 413 - Create Your Own Swift Playgrounds Subscription
- 415 - Behind the Scenes of the Xcode Build Process
- 417 - Testing Tips & Tricks
- 418 - Source Control Workflows in Xcode


### System Frameworks
- 702 - Your Apps and the Future of macOS Security
- 704 - Best Practices and What’s New with In-App Purchases
- 707 - New Ways to Work with Workouts 
- 708 - What’s New in Core ML, Part 1
- 709 - What’s New in Core ML, Part 2
- 710 - What’s New in User Notifications
- 711 - Using Grouped Notifications
- 712 - A Guide to Turi Create
- 713 - Introducing Natural Language Framework
- 716 - Object Tracking in Vision
- 717 - Vision with Core ML

### Design
- 801 - The Qualities of Great Design
- 802 - Intentional Design
- 803 - Designing Fluid Interfaces
- 804 - The Life of a Button
- 806 - Designing Notifications

## WWDC Students
[WWDC scholarship entrants from each year](https://github.com/wwdc)

## Blogs/Newsletter
[Indie iOS Focus Weekly 177](https://indieiosfocus.com/issues/177)
