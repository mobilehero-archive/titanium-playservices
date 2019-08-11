# @titanium/playservices

[![@titanium/playservices](https://img.shields.io/npm/v/@titanium/playservices.png)](https://www.npmjs.com/package/@titanium/playservices)


> Native modules that allows you to use Native modules that allows you to use Google Play Services with Axway Titanium native mobile apps. with Axway Titanium native mobile apps.


<p align="center">
	<h5 align="center">To provide Google Play Services for Titanium modules and applications</h6>
	<div align="center">
		<img src="https://github.com/appcelerator-modules/ti.playservices/raw/master/apidoc/diagram.png" height="170" width="449">
	</div>
</p>


* [📝 Description](#-description)
* [🚀 Getting Started](#-getting-started)
	* [Install `@titanium/playservices` in root of project](#install-titaniumplayservices-in-root-of-project)
* [Requirements](#requirements)
* [Author](#author)
* [License](#license)
* [✨Features](#features)
* [📚Learn More](#learn-more)
* [📣 Feedback](#-feedback)
* [©️ Legal](#️-legal)


## 📝 Description

This is a repackaging of the compiled iOS and Android modules for [ti.playservices](https://github.com/appcelerator-modules/ti.playservices) to allow for installation via npm.

## 🚀 Getting Started

### Install `@titanium/playservices` in root of project

```bash
npm install @titanium/playservices
```

## Requirements
- Titanium Mobile SDK 7.0.0 or later (release 12/2017)

Use `require()` to access the module from JavaScript:

```javascript
    const PlayServices = require('@titanium/playservices');
```

The `PlayServices` variable is a reference to the module. Make API calls using this reference:

```javascript
    const playServicesAvailable = PlayServices.isGooglePlayServicesAvailable();
```

It is highly recommended to detect availability issues before using Play Services:

```javascript
const PlayServices = require('@titanium/playservices');

const win = Ti.UI.createWindow({ backgroundColor: 'gray' });
const btn = Ti.UI.createButton({ title: 'CHECK PLAY SERVICES' });

btn.addEventListener('click', () => {
    PlayServices.makeGooglePlayServicesAvailable((e) => {
        if (e.success) {
            alert(`Play Services: ${PlayServices.GOOGLE_PLAY_SERVICES_VERSION_CODE}`);
            // Use Play Services
        } else {
            alert(`Play Services is not available.`);
        }
    });
});

win.add(btn);
win.open();
```

To include Play Services libraries with your native module include the module as a dependency by adding a `<module>` item to the `<modules>` element of your `timodule.xml` file:

```XML
<ti:module>
  ...
  <modules>
    <module platform="android">titanium-playservices</module>
  </modules>
  ...
</ti:module>
```

For a detailed API example please see [android/example/app.js](https://github.com/appcelerator-modules/ti.playservices/blob/master/android/example/app.js)

## Author
Axway

## License
Apache 2.0


## ✨Features

* [x] Includes Titanium native Android module: `ti.playservices 16.1.0`


## 📚Learn More

- [ti.playservices GitHub Repo](https://github.com/appcelerator-modules/ti.playservices) - Repo for ti.playservices module


## 📣 Feedback

Have an idea or a comment?  [Join in the conversation here](https://github.com/brentonhouse/titanium-playservices/issues)! 

## ©️ Legal

Modules are licensed under Apache 2.0 from https://github.com/appcelerator-modules/titanium-playservices

Alloy is developed by Appcelerator and the community and is Copyright © 2012-Present by Appcelerator, Inc. All Rights Reserved.

Alloy is made available under the Apache Public License, version 2. See their license file for more information.

Appcelerator is a registered trademark of Appcelerator, Inc. Titanium is a registered trademark of Appcelerator, Inc. Please see the LEGAL information about using trademarks, privacy policy, terms of usage and other legal information at http://www.appcelerator.com/legal.