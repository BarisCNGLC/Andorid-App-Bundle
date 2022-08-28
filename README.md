# Andorid-App-Bundle


## Step 1 - Create an upload keystore
  
On Mac/Linux, use the following command:
 ```bash
 
  keytool -genkey -v -keystore ~/upload-keystore.jks -keyalg RSA -keysize 2048 -validity 10000 -alias upload
 ```

On Windows, use the following command:
  ```bash
 keytool -genkey -v -keystore %userprofile%\upload-keystore.jks -storetype JKS -keyalg RSA -keysize 2048 -validity 10000 -alias upload
  ```
## Step 2 - Reference the keystore from the app
Create a file named [project]/android/key.properties that contains a reference to your keystore:
  ```bash
  storePassword=<password from previous step>
keyPassword=<password from previous step>
keyAlias=upload
storeFile=<location of the key store file, such as /Users/<user name>/upload-keystore.jks>
```
## Step 3 - Configure signing in gradle

Configure gradle to use your upload key when building your app in release mode by editing the [project]/android/app/build.gradle file.
  <h6> 1. Add the keystore information from your properties file before the android block:</h6>
   
   ```bash
   
      def keystoreProperties = new Properties()
   def keystorePropertiesFile = rootProject.file('key.properties')
   if (keystorePropertiesFile.exists()) {
       keystoreProperties.load(new FileInputStream(keystorePropertiesFile))
   }

   android {
         ...
   }
   ```
  


