# Google-AdMob-Xamarin
Add advertise to Xamarin with Google AdMob

💣STEP BY STEP ADD ADVERTISE ON XAMARIN APPLICATION

Step 1: Create Google Admob account for your Google Play Application
![admob1](https://user-images.githubusercontent.com/75094927/135495894-49d2d73f-b931-413a-8b6d-1ab5d2651f6d.png)

Step 2: Choose your advertise type 
![admob2](https://user-images.githubusercontent.com/75094927/135495944-5ed1d944-c7d6-4cfc-ba58-19385009a5dd.png)

Step 3: Create Keys for your Google Play app
![admob3](https://user-images.githubusercontent.com/75094927/135496079-2a08944c-59a8-4e61-a446-7ae5e3d9dd53.png)



Now Let's go Visual Studio:

Step 4: We need to download MarcTron.Admob Package on  your project : [Package Name: MarcTron.Admob]

Step 5:
Setup for Android:
▶️In step 3.photo, first key we use in Android.xml file:   
           
           <application>
        <!-- Sample AdMob app ID: ca-app-pub-3940256099942544~3347511713 --> This ID is Example
        <meta-data
            android:name="com.google.android.gms.ads.APPLICATION_ID"
            android:value="ca-app-pub-3940256099942544~3347511713"/>
    </application>
  You must write your key in android:value = "" part! 
  
  
▶️ We need to write this code in MainActivity.cs script in OnCreate() Method:
      
        MobileAds.Initialize(ApplicationContext);

  Note: Also need this  => using Android.Gms.Ads;
  
Setup for IOS:

In Info.plist you need to add this code in <dict> </dict> part:
         
          <key>GADApplicationIdentifier</key>
          <string>ca-app-pub-3940256099942544~3347511713</string>
          <key>GADIsADManagerApp</key>
          <true/>

Open AppDelegate.cs Script and this code in FinishedLaunching() Method:

           MobileAds.SharedInstance.Start(CompletionHandler);
           
           // Create a CompletionHandler Method
           private void CompletionHandler(InitializationStatus status)
           { 
           
           }

    
    

Last Step:
    Open your Xaml page and also in ContentPage Like this: 
    
          <ContantPage xmlns:s="clr-namespace:MarcTron.Plugin.Controls;assembly=Plugin.MtAdmob">
          
  Then write in ContantPage this Code and also look at step 3 beacuse we use this keys:
   
          <admob:MTAdView AdsId="ca-app-pub-3940256099942544/6300978111"/>


🥇Well Done your advertise is ready!! Now make money 🤑🤑🤑🤑🤑 

![Screenshot_1631640751](https://user-images.githubusercontent.com/75094927/135500250-bd86bc5e-868b-4df0-a6bb-ea87d816f191.png)



