

# react-native-tele

**UPDATE**: Now is compatible with RN 0.60+ (AndroidX)



## Support
- Currently support for Android.  

## To do

 - [ ] Add ToDo

## Examples

- [Android]Simple example (https://github.com/telefon-one/react-native-replace-dialer/blob/master/examples/) 
- [Google.Play] TODO


## Installation
AndroidManifest.xml

<activity>
...
  <!-- ReplaceDialer -->
  <intent-filter>
                  <!-- Handle links from other applications -->
                <action android:name="android.intent.action.VIEW" />
                <action android:name="android.intent.action.DIAL" />
                <!-- Populate the system chooser -->
                <category android:name="android.intent.category.DEFAULT" />
                <!-- Handle links in browsers -->
                <category android:name="android.intent.category.BROWSABLE" />

                <!--SCHEME TEL-->
                <data android:scheme="tel"/>
    </intent-filter>
    <intent-filter>
    <action android:name="android.intent.action.DIAL"/>
    <category android:name="android.intent.category.DEFAULT"/>
  </intent-filter>
  <!-- ReplaceDialer -->
...
      </activity>
...

<!-- ReplaceDialer Service -->
        <service
            android:name=".TeleService"
            android:permission="android.permission.BIND_INCALL_SERVICE"
            >
            <meta-data
                android:name="android.telecom.IN_CALL_SERVICE_UI"
                android:value="true"
                />
            <intent-filter>
                <action android:name="android.telecom.InCallService" />
            </intent-filter>
        </service>
<!-- ReplaceDialer Service -->
...
<application>

- [Android](https://github.com/telefon-one/react-native-replace-dialer/blob/master/docs/installation_android.md)

## Usage

```javascript
    import {ReplaceDialer} from 'react-native-replace-dialer';

    let tReplaceDialer = new ReplaceDialer();

    if (!tReplaceDialer.isDefault()) {
      console.log('Is NOT default dialer, try to set.');
      if (tReplaceDialer.setDefault()) {
        console.log('Default dialer sucessfully set.');
      } else {
        console.log('Default dialer NOT set');
      }
    }
    
```

# react-native-replace-dialer.example



