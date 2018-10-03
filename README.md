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
  * `categorySummaryFormat` : We can customize is the summary grouped content.
    * Two forms are allowed: `%u` and `%@`.
- Dynamic notifications - Notification Content Extension `UNNotificationContentExtension`
    * `notificationActions` : We can access notificationActions as well as dynamically anywhere
    * Allows to UserInteraction touches notifications Image
    * Allows to delete action buttons from notification actions
    * `performNotificationDefaultAction` : Allows to launching application programmatically or custom control with Notification Content Extension
    * `dismissNotificationContentExtension` : Custom dismiss content extension view
  * Notification Management
    * Show notification settings under the app notification settings page
      * Deliver Quietly: These parameters show notifications only in the notification center, but notifications don’t display an alert and don’t appear on the lock screen and don’t make any sounds. But they are allowed to set a badge.
      * Turn Off...
  * Critical Alert notification: Critical notification will be delivered with sound and on screen, even if the Do not disturb mode is enable. You need to get special entitlement from [Apple](https://developer.apple.com/contact/request/notifications-critical-alerts-entitlement/).
    * Remote notifications configuration:, add a `critical: 1` property to the JSON payload
    * Local notifications configuration:, we need to configured content `UNNotificationSound.defaultCritical`
    * Override the notification volume : `UNNotificationSound.defaultCriticalSound(withAudioVolume: 1.0)`
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
- Notifications
  * Group notifications
  * Quiet notifications
  * Critical alert notifications
  * Interactive notifications


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
- 50% faster keyboard display
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
- Security code AutoFill: this allow the mobile device to scan incoming SMS messages for such codes and suggest them at the top of the default keyboard.
- Third time books app name is changed. The new name is Apple Books
- Notification Center: 
  * Group Notifications
  * Interaction
  * Settings
- Screen Time: personalized usage analytics
- Parents can manage child device remotely
- Memoji: Next level of enimoji with tongue detection
- Connections: FaceTime can GroupCall with 32 people in a single call, biggest update of FaceTime
- [Core ML 2](https://developer.apple.com/machine-learning/)
- [Safari](https://developer.apple.com/safari/whats-new/)
- More Battery info details
- 70% faster camera snap
- RAW photo editing

## watchOS 5

<http://www.apple.com/watchos-preview/>

- watchOS 5 won’t support first generation Apple Watches
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
- Rainbow: Pride edition watch band and face

## tvOS

<https://www.apple.com/apple-tv-4k/>

- Dolby Atmos and 4K HDR support
- TV App has live news
- 3rd party remote support: Crestron and Savant can control your Apple TV, including using Siri for voice search and control.
- Aerial screen saver from ISS
- Zero Sign-On: Automatically unlocks access to all the video-streaming apps that you’ve subscribed to.
- Charter Spectrum partnership


## Swift 4.2
[You can follow up all the changes in this version or future version on the official Swift CHANGELOG](https://github.com/apple/swift/blob/master/CHANGELOG.md)
- Swift 5 is coming in 2019 with ABI stability.
- Apple plan to deliver with OS than means no need to include the Swift runtime with apps which will result in smaller downloads and faster launches.
- Completed 18K pull-request
- SDK improvements
- [SE-0206 - Hashable Enhancements](https://github.com/apple/swift-evolution/blob/master/proposals/0206-hashable-enhancements.md)
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
- [SE-0143 - Conditional conformances](https://github.com/apple/swift-evolution/blob/master/proposals/0190-target-environment-platform-condition.md)
- [SE-0204 - Add last methods](https://github.com/apple/swift-evolution/blob/master/proposals/0204-add-last-methods.md)
- [SE-0207 - Contains only](https://github.com/apple/swift-evolution/blob/master/proposals/0207-containsOnly.md)

## Design

- [Apple updates Design Resources for iOS 12, adds iPad UI elements and Keynote kit](http://developer.apple.com/design/resources)
- [WWDC 2018 - Human Interface Guidelines](https://developer.apple.com/design/whats-new/?id=06042018a)
- [WWDC for Designers 2014 - 2018](https://gist.github.com/durul/b686dbe7a6f8473922a6dc5c20399499)

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
- [101 WWDC 2018 Keynote](https://developer.apple.com/wwdc18/101)
- [102 Platforms State of the Union](https://developer.apple.com/wwdc18/102)
- [103 Apple Design Awards](https://developer.apple.com/wwdc18/103)

### App Frameworks
- [201 Creating Apps for a Global Audience](https://developer.apple.com/wwdc18/201)
- [202 What's New in Cocoa Touch](https://developer.apple.com/wwdc18/202)
- [203 I Have This Idea For An App...](https://developer.apple.com/wwdc18/203)
- [204 Automatic Strong Passwords and Security Code AutoFill](https://developer.apple.com/wwdc18/204)
- [205 Advances in Research and Care Frameworks](https://developer.apple.com/wwdc18/205)
- [206 What's New in watchOS](https://developer.apple.com/wwdc18/206)
- [207 Strategies for Securing Web Content](https://developer.apple.com/wwdc18/207)
- [208 What's New in tvOS 12](https://developer.apple.com/wwdc18/208)
- [209 What's New in Cocoa for macOS](https://developer.apple.com/wwdc18/209)
- [210 Introducing Dark Mode](https://developer.apple.com/wwdc18/210)
- [211 Introduction to Siri Shortcuts](https://developer.apple.com/wwdc18/211)
- [212 Introducing MapKit JS](https://developer.apple.com/wwdc18/212)
- [214 Building for Voice with Siri Shortcuts](https://developer.apple.com/wwdc18/214)
- [215 Introducing ClassKit](https://developer.apple.com/wwdc18/215)
- [216 Managing Documents In Your iOS Apps](https://developer.apple.com/wwdc18/216)
- [217 Siri Shortcuts on the Siri Watch Face](https://developer.apple.com/wwdc18/217)
- [218 Advanced Dark Mode](https://developer.apple.com/wwdc18/218)
- [219 Image and Graphics Best Practices](https://developer.apple.com/wwdc18/219)
- [220 High Performance Auto Layout](https://developer.apple.com/wwdc18/220)
- [221 TextKit Best Practices](https://developer.apple.com/wwdc18/221)
- [222 Data You Can Trust](https://developer.apple.com/wwdc18/222)
- [223 Embracing Algorithms](https://developer.apple.com/wwdc18/223)
- [224 Core Data Best Practices](https://developer.apple.com/wwdc18/224)
- [225 A Tour of UICollectionView](https://developer.apple.com/wwdc18/225)
- [226 VoiceOver: App Testing Beyond The Visuals](https://developer.apple.com/wwdc18/226)
- [227 Optimizing App Assets](https://developer.apple.com/wwdc18/227)
- [228 What’s New in Energy Debugging](https://developer.apple.com/wwdc18/228)
- [229 Using Collections Effectively](https://developer.apple.com/wwdc18/229)
- [230 Deliver an Exceptional Accessibility Experience](https://developer.apple.com/wwdc18/230)
- [231 HomeKit Deep Dive](https://developer.apple.com/wwdc18/231)
- [232 Getting Ready for Business Chat](https://developer.apple.com/wwdc18/232)
- [233 Adding Delight to your iOS App](https://developer.apple.com/wwdc18/233)
- [234 What’s New in Safari and WebKit](https://developer.apple.com/wwdc18/234)
- [235 UIKit: Apps for Every Size and Shape](https://developer.apple.com/wwdc18/235)
- [236 AVSpeechSynthesizer: Making iOS Talk](https://developer.apple.com/wwdc18/236)
- [237 Quick Look Previews from the Ground Up](https://developer.apple.com/wwdc18/237)
- [238 What's New in TVMLKit](https://developer.apple.com/wwdc18/238)
- [239 Designing Web Content for watchOS](https://developer.apple.com/videos/play/wwdc2018/239)
- [241 Accessible Drag and Drop](https://developer.apple.com/videos/play/wwdc2018/241)


### Distribution
- [301 What's New in App Store Connect](https://developer.apple.com/videos/play/wwdc2018/301)
- [302 What's New in Managing Apple Devices](https://developer.apple.com/videos/play/wwdc2018/302)
- [303 Automating App Store Connect](https://developer.apple.com/videos/play/wwdc2018/303)
- [304 What's New in Search Ads](https://developer.apple.com/videos/play/wwdc2018/304)

### Developer Tools
- [401 What's New in Swift](https://developer.apple.com/videos/play/wwdc2018/401)
- [402 Getting the Most out of Playgrounds in Xcode](https://developer.apple.com/videos/play/wwdc2018/402)
- [403 What's New in Testing](https://developer.apple.com/videos/play/wwdc2018/403)
- [404 New Localization Workflows in Xcode 10](https://developer.apple.com/videos/play/wwdc2018/404)
- [405 Measuring Performance Using Logging](https://developer.apple.com/videos/play/wwdc2018/405)
- [406 Swift Generics](https://developer.apple.com/videos/play/wwdc2018/406)
- [407 Practical Approaches to Great App Performance](https://developer.apple.com/videos/play/wwdc2018/407)
- [408 Building Faster in Xcode](https://developer.apple.com/videos/play/wwdc2018/408)
- [409 What's New in LLVM](https://developer.apple.com/videos/play/wwdc2018/409)
- [410 Creating Custom Instruments](https://developer.apple.com/videos/play/wwdc2018/410)
- [411 Getting to Know Swift Package Manager](https://developer.apple.com/videos/play/wwdc2018/411)
- [412 Advanced Debugging with Xcode and LLDB](https://developer.apple.com/videos/play/wwdc2018/412)
- [413 Create Your Own Swift Playgrounds Subscription](https://developer.apple.com/videos/play/wwdc2018/413)
- [414 Understanding Crashes and Crash Logs](https://developer.apple.com/videos/play/wwdc2018/414)
- [415 Behind the Scenes of the Xcode Build Process](https://developer.apple.com/videos/play/wwdc2018/415)
- [416 iOS Memory Deep Dive](https://developer.apple.com/videos/play/wwdc2018/416)
- [417 Testing Tips & Tricks](https://developer.apple.com/videos/play/wwdc2018/417)
- [418 Source Control Workflows in Xcode](https://developer.apple.com/videos/play/wwdc2018/418)

### Media
- [501 Introducing Podcast Analytics](https://developer.apple.com/videos/play/wwdc2018/501)
- [502 Measuring and Optimizing HLS Performance](https://developer.apple.com/videos/play/wwdc2018/502)
- [503 Creating Photo and Video Effects Using Depth](https://developer.apple.com/videos/play/wwdc2018/503)

### Graphics and Games
- [601 Live Screen Broadcast with ReplayKit](https://developer.apple.com/videos/play/wwdc2018/601)
- [602 What’s New in ARKit 2](https://developer.apple.com/videos/play/wwdc2018/602)
- [603 Integrating Apps and Content with AR Quick Look](https://developer.apple.com/videos/play/wwdc2018/603)
- [604 Metal for OpenGL Developers](https://developer.apple.com/videos/play/wwdc2018/604)
- [605 Inside SwiftShot: Creating an AR Game](https://developer.apple.com/videos/play/wwdc2018/605)
- [606 Metal for Ray Tracing Acceleration](https://developer.apple.com/videos/play/wwdc2018/606)
- [607 Metal for Game Developers](https://developer.apple.com/videos/play/wwdc2018/607)
- [608 Metal Shader Debugging and Profiling](https://developer.apple.com/videos/play/wwdc2018/608)
- [609 Metal for Accelerating Machine Learning](https://developer.apple.com/videos/play/wwdc2018/609)
- [610 Understanding ARKit Tracking and Detection](https://developer.apple.com/videos/play/wwdc2018/610)
- [611 Metal for VR](https://developer.apple.com/videos/play/wwdc2018/611)
- [612 Metal Game Performance Optimization](https://developer.apple.com/videos/play/wwdc2018/612)

### System Frameworks
- [701 Using Accelerate and simd](https://developer.apple.com/wwdc18/701)
- [702 Your Apps and the Future of macOS Security](https://developer.apple.com/wwdc18/702)
- [703 Introducing Create ML](https://developer.apple.com/wwdc18/703)
- [704 Best Practices and What’s New with In-App Purchases](https://developer.apple.com/wwdc18/704)
- [705 Engineering Subscriptions](https://developer.apple.com/wwdc18/705)
- [706 Accessing Health Records with HealthKit](https://developer.apple.com/wwdc18/706)
- [707 New Ways to Work with Workouts](https://developer.apple.com/wwdc18/707)
- [708 What’s New in Core ML, Part 1](https://developer.apple.com/wwdc18/708)
- [709 What’s New in Core ML, Part 2](https://developer.apple.com/wwdc18/709)
- [710 What’s New in User Notifications](https://developer.apple.com/wwdc18/710)
- [711 Using Grouped Notifications](https://developer.apple.com/wwdc18/711)
- [712 A Guide to Turi Create](https://developer.apple.com/wwdc18/712)
- [713 Introducing Natural Language Framework](https://developer.apple.com/wwdc18/713)
- [714 Optimizing Your App for Today’s Internet](https://developer.apple.com/wwdc18/714)
- [715 Introducing Network.framework: A modern alternative to Sockets](https://developer.apple.com/wwdc18/715)
- [716 Object Tracking in Vision](https://developer.apple.com/wwdc18/716)
- [717 Vision with Core ML](https://developer.apple.com/wwdc18/717)
- [718 Better Apps through Better Privacy](https://developer.apple.com/wwdc18/718)
- [719 Core Image: Performance, Prototyping, and Python](https://developer.apple.com/wwdc18/719)
- [720 Wallet and Apple Pay: Creating Great Customer Experiences](https://developer.apple.com/wwdc18/720)
- [721 Implementing AutoFill Credential Provider Extensions](https://developer.apple.com/wwdc18/721)

### Design
- [801 The Qualities of Great Design](https://developer.apple.com/wwdc18/801)
- [802 Intentional Design](https://developer.apple.com/wwdc18/802)
- [803 Designing Fluid Interfaces](https://developer.apple.com/wwdc18/803)
- [804 The Life of a Button](https://developer.apple.com/wwdc18/804)
- [805 Creating Great AR Experiences](https://developer.apple.com/wwdc18/805)
- [806 Designing Notifications](https://developer.apple.com/wwdc18/806)
- [808 Prototyping for AR](https://developer.apple.com/wwdc18/808)
- [809 Apple Pencil Design Essentials](https://developer.apple.com/wwdc18/809)
- [810 Tips for Great Maps](https://developer.apple.com/wwdc18/810)
- [811 Presenting Design Work](https://developer.apple.com/wwdc18/811)

## WWDC Students
[WWDC scholarship entrants from each year](https://github.com/wwdc)

## Blogs/Newsletter
[Indie iOS Focus Weekly 177](https://indieiosfocus.com/issues/177)
