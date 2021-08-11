# web_push_notification
Angular Web Push Notification One Signal Account

Step 1: Set Up Your OneSignal Account
Login to your OneSignal account or create a free account. Then, click on the blue button entitled New App/Website to configure your OneSignal account to fit your app or website.
Login link:- https://app.onesignal.com/login
Register link:- https://app.onesignal.com/signup

Insert the name of your app or website. Select Web Push as your platform.

Click on Next: Configure Your Platform button.

Web Configuration
Under Choose Integration, select the Typical Site option.
In the Site Setup section, enter your chosen web configuration. In my case, the configuration looks like this:

Notice for testing purposes I’m entering my localhost URL (http://localhost:4200). If you are doing the same, make sure you click on the LOCAL TESTING option. This will ensure to treat HTTP localhost as HTTPS for testing.
scroll down to the bottom of the page and click Save to save your auto-prompt selections.

Add Code to index.html file:-

<script src="https://cdn.onesignal.com/sdks/OneSignalSDK.js" async=""></script>
<script>
window.OneSignal = window.OneSignal || [];
    OneSignal.push(function() {
        OneSignal.init({
            appId: "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX",
        });
    });
</script>


Update appId with your onesignal appid.
