Here's my complete list of features and updates I could learn, listen and find about iOS, tvOS, watchOS, MacOS, SDKs and developer tools that were announced at WWDC 2018. This year WWDC 2018 Focus is on performance improvements and deepening existing functionality.

The [unofficial WWDC Mac app](https://github.com/insidegui/WWDC) is good way to download the videos and keep track of what you've already watched.

## OSX → macOS 10.14 Mojave

- Dark mode: Offical Apple app and Xcode support
- Dynamic desktop: desktop subytly changes throughout the day
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
  * threadIdentifier. We use for creating own custom group notifications
  * Notification Content Extension
    * `notificationActions` : We can access notificationActions as well as dynamically anywhere
    * Allows to UserInteraction touches notifications Image
    * Allows to delete action buttons from notification actions
    * `performNotificationDefaultAction` : Allows to launching application programmatically or custom control with Notification Content Extension
    * `dismissNotificationContentExtension` : Custom dismiss content extension view
  * Notification Management
    * Show notification settings under the app notification settings page
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


## iOS 12

<https://www.apple.com/ios/ios-12-preview/>

-  App Store Connect app: replacement for the existing [iTunes Connect app](https://itunes.apple.com/us/app/app-store-connect/id1234793120?mt=8)
- iOS 12 adds multi-user Face ID with support for up to two faces
- Do Not Disturb During Bedtime
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
- Connections: Facetime can GroupCall with 32 people in a single call, biggest update of FaceTime
- Core ML 2

## watchOS 5

<http://www.apple.com/watchos-preview/>

- watchOS 5 won’t support first gen Apple Watches
- Activity competitions and awards
- New workout types: yoga and hiking  
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

## tvOS

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

## Design

[Apple updates Design Resources for iOS 12, adds iPad UI elements and Keynote kit](http://developer.apple.com/design/resources)


## Xcode 10

<https://developer.apple.com/xcode/> <br>

- Multiple source compatibility continue Swift 4 / 4.2 and 3
- Some API changes will land in later Xcode 10 betas
- Complication Mode DEBUG must be incremental
- Exclusive access to memory must be Full Enforcement (Run-time Checks in All Builds)
- Integration: BitBucket and GitLab
- New code snippets tool can accessible from Xcode Editor menu
- Run the XCTest in the command line using the xcodebuild tool
- Parallel testing by creating clones of the simulators
- Upload App to App Store with the xcodebuild tool
- Notarized App: Apple will stamp the app before uploading to App Store
- New shortcut: Select target device or simulator by CTRL+SHIFT+0
- Multi-Line Editing
- View as: Dark Appearance or System Appearance
- New color option in the action menu
- Create a SSH Key and upload them directly server accounts
- New playground interaction: Added new lines of code playground auto restart to playground session.


## Developer Tool
- Custom Insturments
- New logging API for finding memory issue ```os_signpost```. This will help Instrument for finding to the problem.


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

## WWDC 2018 Videos

[WWDC 2018 video downloader script](https://github.com/ohoachuck/wwdc-downloader)

### Featured
- 101 - WWDC 2018 Keynote
- 102 - Platforms State of the Union
- 103 - Apple Design Awards


### Developer Tools
- 401 - What's New in Swift
- 402 - Getting the Most out of Playgrounds in Xcode
- 405 - Measuring Performance Using Logging
- 418 - Source Control Workflows in Xcode


### App Frameworks
- 202 - What's New in Cocoa Touch
- 204 - Automatic Strong Passwords and Security Code AutoFill
- 206 - What's New in watchOS
- 219 - Image and Graphics Best Practices
- 220 - High Performance Auto Layout


### System Frameworks
- 710 - What’s New in User Notifications


### Designee
- 802 - Intentional Design
