﻿# SwiftyBase

[![BuddyBuild](https://dashboard.buddybuild.com/api/statusImage?appID=59a6f3aeb749970001234046&branch=master&build=latest)](https://dashboard.buddybuild.com/apps/59a6f3aeb749970001234046/build/latest?branch=master)
[![Carthage compatible](https://img.shields.io/badge/Carthage-compatible-4BC51D.svg?style=flat)](https://github.com/Carthage/Carthage)
[![codecov](https://codecov.io/gh/mspvirajpatel/SwiftyBase/branch/master/graph/badge.svg)](https://codecov.io/gh/mspvirajpatel/SwiftyBase)
[![Version](https://img.shields.io/cocoapods/v/SwiftyBase.svg?style=flat)](http://cocoapods.org/pods/SwiftyBase)
[![License](https://img.shields.io/cocoapods/l/SwiftyBase.svg?style=flat)](http://cocoapods.org/pods/SwiftyBase)
[![Platform](https://img.shields.io/cocoapods/p/SwiftyBase.svg?style=flat)](http://cocoapods.org/pods/SwiftyBase)


SwiftyBase makes it easy to deal with new Project create in Swift.

1. [Why use the SwiftyBase](#why-use-the-swiftyBase)
2. [Requirements](#requirements)
3. [Integration](#integration)
4. [Usage](#usage)
   - [Initialization](#initialization)
   - [BaseViewController](#baseViewController)
   - [BaseView](#baseView)
   - [BaseNavigationController](#baseNavigationController)
   - [BaseImageView](#baseImageView)
   - [BaseButton](#baseButton)
5. [In Progress](#in-progress)
6. [Author](#author)


## Why use the SwiftyBase?

- In software development we all know that we have to reuse code as per as requirement so we have to utilise our code with less effort I will show you one demo on that first make one viewcontroller of baseviewcontroller then make one view of base view initialize this view in controller we can use this view in another controller too ...that’s the main purpose of baseview In storyboard or in one view controller have its own view..We all know that if we have work in owns view, then it will not use for another controller so we can implement on baseview & use it another times with simple initialize.


In Base Project included:
1. BaseViewController.swift
2. BaseView.swift
3. BaseNavigationController.swift

Utilities:

1. AppConstants 
2. AppInterFaceUtility 
3. AppLocationManager
4. AppTimer
5. AppAlert

Controls: 

1. BaseImageView - with set Url image with catch support & Clear Catch
2. BaseButton - Multiple Button with single class access
3. Full screen Image Viewer  (ImageViewer)


## Requirements

- iOS 9.0+ 
- Xcode 8	


## Integration

#### CocoaPods (iOS 9)

You can use [CocoaPods](http://cocoapods.org/) to install `SwiftyBase`by adding it to your `Podfile`:

```ruby
platform :ios, '9.0'
use_frameworks!

target 'MyApp' do
	pod 'SwiftyBase'
end
```

Note that this requires CocoaPods version 36, and your iOS deployment target to be at least 9.0:


#### Carthage (iOS 9+)

You can use [Carthage](https://github.com/Carthage/Carthage) to install `SwiftyBase` by adding it to your `Cartfile`:

```
github "mspvirajpatel/SwiftyBase"
```

#### Manually (iOS 9+)

To use this library in your project manually you may:  

1. Just drag ‘SwiftyBase/’ to the project tree



## Usage

#### Initialization

```swift
import SwiftyBase
```

#### BaseViewController

```swift
//If Create ViewContoller using BaseViewController

class ListController: BaseViewController {

    // MARK: - Attributes -
    
    // MARK: - Lifecycle -
    
    init() {

    }
    
}
```

#### BaseView

```swift
//If Create ListView using BaseView

class ListView: BaseView{
    
    // MARK: - Attributes -
    
    // MARK: - Lifecycle -
    
    override init(frame: CGRect) {
        super.init(frame:frame) 
        
    }
}

```
 

#### BaseNavigationController

```swift
//using BaseNavigationController
let listview : ListController = ListController()
        
let baseNavigation : BaseNavigationController = BaseNavigationController(rootViewController: listview)

```


#### BaseImageView

```swift
//using BaseImageView for set Image Local or Remote URL

let imgView : BaseImageView = BaseImageView(type: .profile, superView: self)
imgView.layer.setValue("imgView", forKey: ControlConstant.name)

//Set Remote URL for Download and set in Image View
imgView.setImageURL("Enter Your URL")
        
//For Full Screen Image Show on tap on Image
imgView.setupForImageViewer()

```


#### BaseButton 

```swift
//using BaseButton for set Button with case primary, secondary, radio, rounded Close, close, checkbox, dropdown, transparent 
 
let btnPrimary : BaseButton = BaseButton.init(ibuttonType: .primary, iSuperView: self)
btnPrimary.layer.setValue("btnPrimary", forKey: ControlConstant.name)
btnPrimary.setTitle("Primary Button", for: UIControlState())
        
let btnSecondary : BaseButton = BaseButton.init(ibuttonType: .secondary, iSuperView: self)
btnSecondary.layer.setValue("btnSecondary", forKey: ControlConstant.name)
btnSecondary.setTitle("Secondary Button", for: UIControlState())


```



## In Progress

- Description after some time added.(In Progress)


## Author

Viraj Patel, mspviraj@hotmail.com

## License

SwiftyBase is available under the MIT license. See the LICENSE file for more info.
