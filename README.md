# Andorid-App-Bundle


<b2>Create an upload keystore</b2>
  <p>If you have an existing keystore, skip to the next step. If not, create one by either:

Following the Android Studio key generation steps
Running the following at the command line:

On Mac/Linux, use the following command:</p>
  keytool -genkey -v -keystore ~/upload-keystore.jks -keyalg RSA -keysize 2048 -validity 10000 -alias upload
<p>On Windows, use the following command:</p>
  keytool -genkey -v -keystore %userprofile%\upload-keystore.jks -storetype JKS -keyalg RSA -keysize 2048 -validity 10000 -alias upload
