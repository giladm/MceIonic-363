ionic start MceIonic-363 tabs
cd MceIonic-363 
ionic cordova platform add ios
ionic cordova platform add  android@6.4.0
ionic cordova resources
ionic cordova prepare
ionic cordova plugin add /YourPathTo-mce-cordova-sdk/plugins/com.xtify.mce.sdk --variable ANDROID_APPKEY=replace_with_your_anroid_appKey --variable SENDER_ID=replace_with_your_senderId  --variable CUSTOM_ACTIONS="openInboxMessage" --variable IOS_DEV_APPKEY=replace_with_your_appKey --variable IOS_PROD_APPKEY=replace_with_your_appKey  --variable SERVER_URL=https://api.ibm.xtify.com/3.0 --variable LOGLEVEL=verbose --variable AUTO_INITIALIZE_LOCATION=true --force 
Make sure the following command list mce plugin> cordova plugin ls
com.xtify.mce.sdk 3.6.3 "IBM MCE Cordova Plugin"

