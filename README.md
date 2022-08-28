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
