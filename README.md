# Tutorial-GoogleAuth-React-Native-FIrebase


#### 1.  Buatlah project react-native baru , atau boleh langsung implementasikan pada project yang sudah ada.



### 2.  Register nama project react-native pada firebase.

### 3. Membuat HA1 Certificate untuk didaftarkan  firebase android project dengan perintah

```

keytool -exportcert -keystore debug.keystore -list -v

```
perintah ditas ditulis pada folder  "prj/android/app".

### 4. Download file "google-services.json" lalu letakan di folder "android/appp" pada project

### 5. Tambahkan Boom file sesuai dokumentasi 
detail dokumentasi boom konfigurasi dapat dilihat pada link :https://console.firebase.google.com/u/2/project/tutorialfirebase-2a512/overview

### 5. Install library react-native yang dibutuhkan 

```
npm install --save @react-native-firebase/app
npm install --save @react-native-firebase/auth
npm install --save @react-native-google-signin/google-signin

```

### 6. Dapatkan *webclientid* dari files *google-service.json*  yang sudah di donload lalu ambil client_id dengen *Type:3*.

### 7. Menambahkan library yang dibutuhkan pada di app.js

```
import React, {Component} from 'react';
import {Text, View, Button} from 'react-native';

import auth from '@react-native-firebase/auth';// tambahkan 
import {GoogleSignin} from '@react-native-google-signin/google-signin'; // tambahkan 

```

### 8. Menambahkan functions *GoogleSign.configure* dibawah list library, sehingga list program menjadi seperti berikut:

```
import React, {Component} from 'react';
import {Text, View, Button} from 'react-native';
import auth from '@react-native-firebase/auth';
import {GoogleSignin} from '@react-native-google-signin/google-signin';
GoogleSignin.configure({
  webClientId:
    '272733356002-o7944fr2622e9ut10fvv38v16h9peikp.apps.googleusercontent.com',
});  //tambahkan files konfigurasi 

```





    
