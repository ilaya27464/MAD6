# MAD_wrokshop6

## Design and develop an android application using MapView Control in android.

## AIM:
To design and develop an android application using MapView Control in android.
```
/*
Submitted by: ILAYARAJA M
Register number: 212221040057
*/
```
## activity_main.xml:
```
<?xml version="1.0" encoding="utf-8"?> 
<manifest xmlns:android="http://schemas.android.com/apk/res/android" 
 package="com.example.locationmap"> 
 <!-- 
 The ACCESS_COARSE/FINE_LOCATION permissions are not required to 
use 
 Google Maps Android API v2, but you must specify either coarse or 
fine 
 location permissions for the "MyLocation" functionality. 
 --> 
 <uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" 
/> 
 <application 
 android:allowBackup="true" 
 android:icon="@mipmap/ic_launcher" 
 android:label="@string/app_name" 
 android:roundIcon="@mipmap/ic_launcher_round" 
 android:supportsRtl="true" 
 android:theme="@style/Theme.Locationmap>
 <meta-data 
 android:name="com.google.android.geo.API_KEY" 
 android:value="AIzaSyC4dxumPEProewZiUZ8G8sHiQD-FlsgJK4" /> 
 <activity 
 android:name=".MapsActivity" 
 android:exported="true" 
 android:label="@string/title_activity_maps"> 
 <intent-filter> 
 <action android:name="android.intent.action.MAIN" /> 
 <category android:name="android.intent.category.LAUNCHER" 
/> 
 </intent-filter> 
 </activity> 
 </application> 
</manifest> 
```

## MainActivity.java:
```
package com.example.locationmap; 
import android.os.Bundle; 
import androidx.fragment.app.FragmentActivity; 
import com.example.locationmap.databinding.ActivityMapsBinding; 
import com.google.android.gms.maps.CameraUpdateFactory; 
import com.google.android.gms.maps.GoogleMap; 
import com.google.android.gms.maps.OnMapReadyCallback; 
import com.google.android.gms.maps.SupportMapFragment; 
import com.google.android.gms.maps.model.LatLng; 
import com.google.android.gms.maps.model.MarkerOptions; 
public class MapsActivity extends FragmentActivity implements 
OnMapReadyCallback { 
 private GoogleMap mMap; 
 private ActivityMapsBinding binding; 
 @Override 
 protected void onCreate(Bundle savedInstanceState) { 
 super.onCreate(savedInstanceState); 
 binding = ActivityMapsBinding.inflate(getLayoutInflater()); 
 setContentView(binding.getRoot()); 
 // Obtain the SupportMapFragment and get notified when the map is 
ready to be used. 
 SupportMapFragment mapFragment = (SupportMapFragment) 
getSupportFragmentManager() 
 .findFragmentById(R.id.map); 
 mapFragment.getMapAsync(this); 
 }
 @Override 
 public void onMapReady(GoogleMap googleMap) { 
 mMap = googleMap; 
 // Add a marker in Sydney and move the camera 
 LatLng saveethacollege = new LatLng(13.030126090531084, 
80.01646935874139); 
 mMap.addMarker(new 
MarkerOptions().position(saveethacollege).title("Marker in Chennai")); 
 mMap.moveCamera(CameraUpdateFactory.newLatLng(saveethacollege)); 
 } 
```

## OUTPUT:
![image](https://github.com/ashmistalin/MAD_wrokshop6/assets/103128410/ffddd6ea-5447-48ca-8ade-f51de829f974)


## RESULT:
Thus an android application using Mapview Control is created. 
