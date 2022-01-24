[//]: # (header-start)


<h1 align="center">
	<a href="https://brenton.house/saying-goodbye-to-axway-amplify-titanium-31a44f3671de">
		Axway Amplify End-of-Life Announcement
	</a>	
</h1>
<h2 align="center">
	👇 &nbsp; See API FAQ below  &nbsp; 👇
</h2>	


<a href="https://brenton.house/saying-goodbye-to-axway-amplify-titanium-31a44f3671de">
	<p align="center">
		<img src="https://cdn.secure-api.org/images/RIP-Axway-Amplify-Titanium.png" alt="RIP Axway Amplify Titanium (2010 - 2022)" width="80%" />
	</p>
</a>	
<p align="center">
	<a href="https://brenton.house/saying-goodbye-to-axway-amplify-titanium-31a44f3671de">
			🪦 &nbsp; RIP Axway Amplify Titanium (2010 - 2022)
	</a>
</p>
<p align="center">
	<a href="https://brenton.house/saying-goodbye-to-axway-amplify-titanium-31a44f3671de">
			🪦 &nbsp; RIP Axway Amplify Cloud Services (2012 - 2022)
	</a>
</p>

<hr>
<a href="https://brenton.house/saying-goodbye-to-axway-amplify-titanium-31a44f3671de">
	<h4 align="center">
🛑 &nbsp;&nbsp; All products affected by the announcements will not be supported by Axway effective their EOL dates in 2022.
</h4>

<h4 align="center">
Some Open-Source versions of Axway products will live on after End-of-Life (EOL) Axway Amplify product announcements.  However, some products are closed-source and will NOT continue after the shut down in 2022.  
	</h4>
</a>
<p>&nbsp;</p>

> 👉 &nbsp;&nbsp; Stay tuned for more info as plans are being made to save the Titanium project and move it under the control of a independent group of developers.

<p>&nbsp;</p>
<hr>

## API FAQ:

* [API Best Practices](https://brenton.house)
* [What is API Security?](https://brenton.house/what-is-api-security-5ca8117d4911)
* [Top API Trends for 2022](https://brenton.house/top-10-api-integration-trends-for-2022-49b05f2ef299)
* [What is a Frankenstein API?](https://brenton.house/what-is-a-frankenstein-api-4d6e59fca6)
* [What is a Zombie API?](https://brenton.house/what-is-a-zombie-api-6e5427c39b6a)
* [API Developer Experience](https://brenton.house/keys-to-winning-with-an-awesome-api-developer-experience-62dd2fa668f4)
* [API Cybersecurity 101](https://brenton.house/what-is-api-security-5ca8117d4911)
* [YouTube API Videos](https://youtube.com/brentonhouse)
* [YouTube API Shorts Videos](https://youtube.com/apishorts)



<p>&nbsp;</p>
<hr>

<p>&nbsp;</p>
<p>&nbsp;</p>

[//]: # (header-end)


# @titanium/playservices

[![@titanium/playservices](https://img.shields.io/npm/v/@titanium/playservices.png)](https://www.npmjs.com/package/@titanium/playservices)
[![Dependabot Status](https://api.dependabot.com/badges/status?host=github&repo=mobilehero-archive/titanium-playservices)](https://dependabot.com)

> Native modules that allows you to use Native modules that allows you to use Google Play Services with Axway Titanium native mobile apps. with Axway Titanium native mobile apps.


<p align="center">
	<h5 align="center">To provide Google Play Services for Titanium modules and applications</h5><br/>
	<div align="center">
		<img src="https://github.com/appcelerator-modules/ti.playservices/raw/master/apidoc/diagram.png" width="75%">
	</div>
</p>

---

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