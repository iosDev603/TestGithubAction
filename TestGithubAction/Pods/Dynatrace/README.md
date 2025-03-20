# Dynatrace

[https://www.dynatrace.com](https://www.dynatrace.com/)

Dynatrace provides the next generation intelligent application, service and infrastructure monitoring
platform.

[![CocoaPods](https://img.shields.io/badge/pod-8-blue.svg)](https://cocoapods.org/pods/Dynatrace) [![Swift Package Manager compatible](https://img.shields.io/badge/SwiftPackageManager-compatible-4BC51D.svg?style=flat)](https://github.com/Dynatrace/swift-mobile-sdk) [![Carthage compatible](https://img.shields.io/badge/Carthage-compatible-4BC51D.svg?style=flat)](https://files.dynatrace.com/mobileagent/carthage/dynatrace.json)
![License](https://img.shields.io/badge/license-Commercial-lightgrey.svg)

## Contents

* [Features](#features)
* [Installation](#installation)
* [Requirements](#requirements)
* [Documentation](#documentation)

## Features

* Intelligent application, service and infrastructure monitoring
* No manual setup required


## Installation

### Cocoapods

#### iOS

Include Dynatrace in your Podfile:

```ruby
use_frameworks!
pod 'Dynatrace', '~> 8.257'
```
This uses the default subspec `Dynatrace/xcframework`, which uses an XCFramework that contains all supported platforms.

If you want to use the static XCFramework use this:

```ruby
use_frameworks!
pod 'Dynatrace/xcframeworkStatic', '~> 8.257'
```

*DEPRECATED:* If you want to use the traditional framework use this:

```ruby
use_frameworks!
pod 'Dynatrace/framework', '~> 8.257'
```

*DEPRECATED:* If you want to use the Dynatrace static library please include the subspec `Dynatrace/lib` in your Podfile:

```ruby
pod 'Dynatrace/lib', '~> 8.257'
```

#### iOS Session Replay

For SessionReplay use the subspec:

```ruby
use_frameworks!
pod 'Dynatrace/SessionReplay', '~> 8.257'
```
This uses the subspec `Dynatrace/SessionReplayXCFramework`, which uses an XCFramework that contains all supported platforms.

*DEPRECATED:* If you want to use the traditional framework use this:

```ruby
use_frameworks!
pod 'Dynatrace/SessionReplayFramework', '~> 8.257'
```

#### tvOS

Include Dynatrace in your Podfile:

```ruby
use_frameworks!
pod 'Dynatrace', '~> 8.257'
```
This uses the default subspec `Dynatrace/xcframework`, which uses an XCFramework that contains all supported platforms.

*DEPRECATED:* If you want to use the traditional framework include this in your Podfile:

```ruby
use_frameworks!
pod 'Dynatrace/tvOS', '~> 8.257'
```

### Carthage

* Include this in your Cartfile:

```ruby
binary "https://mobileagent.downloads.dynatrace.com/ios/carthage/dynatrace.json" ~> 8.257
```

* Run  `carthage update --use-xcframeworks` (or `carthage update` for the *deprecated* traditional framework)
* Add `Dynatrace.xcframework` and `DynatraceSessionReplay.xcframework` from the Carthage/Build folder to the Frameworks, Libraries and Embedded Content section of the General tab of your Application Target and set it to Embed & Sign.
* If the static framework `DynatraceStatic.xcframework` is used, `libc++.tbd` needs to be added as linked library and `-ObjC` needs to be added to *Other Linker Flags* in Xcode

### Swift Package Manager

See the [ReadMe](https://github.com/Dynatrace/swift-mobile-sdk#readme) at the Dynatrace SPM repository on GitHub

## Requirements

* Project targeting iOS 12+ or tvOS 12+
* Latest Xcode major version

## Imports
* Swift
	* dynamic: `import Dynatrace`
	* static: `import DynatraceStatic`
* Objective-C
 	* dynamic: `#import <Dynatrace/Dynatrace.h>`
	* static: `#import <DynatraceStatic/Dynatrace.h>`

## Documentation

Detailed documentation can be found here: [Dynatrace Documentation](https://www.dynatrace.com/support/help/technology-support/operating-systems/ios/)
