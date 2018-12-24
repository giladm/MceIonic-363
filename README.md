# IBM Mobile messaging with Ionic 
Use IBM Watson Customer Engagement cordova SDK to build Ionic V3 projects. The sample app demonstrates the integration of IBM cordova SDK with Ionic app, as well as demonstrating cordova plugin usage. 

# Usage
- Download IBM-Mobile-push cordova SDK https://github.com/ibm-mobile-push/cordova
- git clone https://github.com/giladm/MceIonic-363
- cd MceIonic-363
- npm install
- ionic cordova platform add ios
- ionic cordova platform add android@6.4.0
##### Add mce plugin to your app. Make sure you replace with your appKeys, server URL, etc. For  plugin settings check [MCE cordova SDK documentation](https://developer.ibm.com/customer-engagement/tutorials/creating-projects-with-apache-cordova-plugin/) 
- ionic cordova plugin add ./path-to-mce-cordova-sdk/plugins/com.xtify.mce.sdk  
 --variable ANDROID_APPKEY=gcXXXX  
 --variable CUSTOM_ACTIONS="openInboxMessage"  
 --variable IOS_DEV_APPKEY=apXXXXXX  
 --variable IOS_PROD_APPKEY=apXXXXX  
 --variable SERVER_URL=https://apiX.ibm.xtify.com/3.0  
 --variable LOGLEVEL=verbose  
 --variable AUTO_INITIALIZE_LOCATION=false --force  
- ionic cordova plugin add ./path-to-mce-cordova-sdk/plugins/com.xtify.mce.sdk.gcm --variable SENDER_ID=(sender id here)
- ionic cordova resources
- ionic cordova prepare
 
 Make sure to update iOS project with your Team and provision settings
 At this point you can run the app on a device or on an emulator using ionic commands. Example:
- ionic cordova emulate ios

# Expected results
App registers with IBM Watson Customer Engagement platform and receives userId and channel Id. When selecting MCE Registration Details from the menu, the registration information is displayed.

