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
