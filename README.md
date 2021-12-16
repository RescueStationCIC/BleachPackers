# BleachPackers
Augmented Reality companion to Laurence Payout's 'The Bleach Packers'
More at Laurence's [website](http://www.laurencepayot.com/category/the-bleach-packers/).

This project displays a model and accompanying sound file at lat, lon and height.

## Models
Note: Test models may be downloaded from Sketchfab. Download the glTF from Sketchfab, then expand and use the following tool to create a glB file: https://alitasci.net/gltf-to-glb-packer/  

Attribution needs to be provided where required.

### Parameters
Use the following params in the url:  
 
lat: latitude  
lon: longitude  
alt: altitude - actually the height above the camera, in metres  

alternative:   
params: base64 encoded json - the above parameters formatted as a JSON object and base64 encoded

#### Examples:

* [base64](./example.base64.md)
* [json](./example.json.md)
* [url](./example.url.md)

## Debugging

Of course, you can write, debug and deploy to GitHub, but that doesn't seem fair, and clogs-up the commit messages with schoolkid errors (well, mine do!).
If you're using VSCode, then:

Use [The LiveServer Extension](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)

If you're debugging on Android devices (better for positioning,etc), then:
1. You'll need to present your local site via HTTPS - see [below](#vscode-liveserver-https) 
1. Make sure your dev machine and your device are connected to the same WiFi (need to be on same network)
1. Run live server on the dev machine, and make sure it brings up this site on localhost in Chrome.
1. Substitue the ip address of the dev machine for localhost in Chrome's address bar.
1. Connect your device to your dev machine, using USB. Ensure you have enabled on-device debugging.
1. In the Chrome address bar, use the QR Code feature to display a QR Code of the address.
1. Using your device's camera app, point it at the QR Code displayed by Chrome. When prompted choose to open the page, using the device's Chrome browser.
1. On the dev machine, in another Chrome window, use the address: chrome://inspect/#devices
1. You'll be able to see and debug the page.


### vscode-liveserver-https
How to enable HTTPS protocol on live server Visual Code

First you will need a self-signed SSL Certificate. If you don’t know how to create a self-signed SSL Certificate goto https://www.akadia.com/services/ssh_test_certificate.html and follow the steps.
[Note: If you are using Visual Code in windows, download OpenSSL and continue the process.]

After you have the private key and certificate:

- Go to your visual code project.
- Create ```.vscode``` folder inside the project. ( Don’t forget the . (period) ).
- Inside that folder create ```settings.json``` file.
- Paste the following code:

  ```json5
  {  
  "liveServer.settings.https":   
  {
  "enable": true, //set it true to enable the feature.  
  "cert": "D:\\https\\primary.crt", //full path of the certificate  
  "key": "D:\\https\\private.key", //full path of the private key  
  "passphrase": "12345"  
  }  
  }
  ```
  
- Start the Live Server and access your project using HTTPS