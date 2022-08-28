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
## Reference the keystore from the app
Create a file named [project]/android/key.properties that contains a reference to your keystore:
  ```bash
  storePassword=<password from previous step>
keyPassword=<password from previous step>
keyAlias=upload
storeFile=<location of the key store file, such as /Users/<user name>/upload-keystore.jks>
```
