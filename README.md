[![GitHub release](https://img.shields.io/github/release/appspector/flutter-plugin.svg)](https://github.com/appspector/flutter-plugin)
# ![AppSpector](https://github.com/appspector/flutter-plugin/raw/master/github-cover.png)

A plugin that integrate [AppSpector](https://appspector.com/?utm_source=flutter_readme) to your Flutter project.

With AppSpector you can remotely debug your app running in the same room or on another continent. 
You can measure app performance, view database content, logs, network requests and many more in realtime. 
This is the instrument that you've been looking for. Don't limit yourself only to simple logs. 
Debugging doesn't have to be painful!

<img src="https://github.com/appspector/appspector-flutter/raw/master/static/appspector_demo.gif" width="700px" alt="AppSpector demonstration" />

# Installation

Each app you want to use with AppSpector SDK you have to register on the web ([https://app.appspector.com](https://app.appspector.com?utm_source=flutter_readme)) and add two native applications(for iOS and Android). Application API keys will be available on the app settings page.

## Add AppSpector SDK to pubspec.yaml
```yaml
dependencies:
  appspector: '0.1.0
```

## Initialize AppSpector SDK
```dart
void main() {
  WidgetsFlutterBinding.ensureInitialized();
  runAppSpector();
  runApp(MyApp());
}

void runAppSpector() {
  var config = new Config();
  config.iosApiKey = "Your iOS API_KEY";
  config.androidApiKey = "Your Android API_KEY";
  AppSpectorPlugin.run(config);
}
```

## Build and Run
Build your project and see everything work! When your app is up and running you can go to [https://app.appspector.com](https://app.appspector.com/?utm_source=flutter_readme) and connect to your application session.


# Features

AppSpector provides many monitors that are can be different for both platforms.

### SQLite monitor
Provides browser for sqlite databases found in your app. Allows to track all queries, shows DB scheme and data in DB. You can issue custom SQL query on any DB and see results in browser immediately.

<img src="https://storage.googleapis.com/appspector.com/images/monitor-screenshots/sqlite-monitor@2x.png" width="700px" alt="SQLite monitor" />

#### HTTP monitor
Shows all HTTP traffic in your app. You can examine any request, see request/response headers and body.
We provide XML and JSON highliting for request/responses with formatting and folding options so even huge responses are easy to look through.

<img src="https://storage.googleapis.com/appspector.com/images/monitor-screenshots/network-monitor@2x.png" width="700px" alt="HTTP monitor" />

### Logs monitor
Displays all logs generated by your app.

#### Logger
AppSpector Logger allows you to collect log message only into AppSpector service.

<img src="https://storage.googleapis.com/appspector.com/images/monitor-screenshots/logs-monitor@2x.png" width="700px" alt="Logs" />

### Location monitor
Most of the apps are location-aware. Testing it requires changing locations yourself. In this case, location mocking is a real time saver. Just point to the location on the map and your app will change its geodata right away.

<img src="https://storage.googleapis.com/appspector.com/images/monitor-screenshots/location-monitor@2x.png" width="700px" alt="Location" />

### Screenshot monitor
Simply captures screenshot from the device.

### SharedPreference/UserDefaults monitor
Provides browser and editor for SharedPreferences/UserDefaults.

### Performance monitor
Displays real-time graphs of the CPU / Memory/ Network / Disk / Battery usage.

### Environment monitor
Gathers all of the environment variables and arguments in one place, info.plist, cli arguments and much more.

### Notification Center monitor (only for iOS)
Tracks all posted notifications and subscriptions. You can examine notification user info, sender/reciever objects, etc.
And naturally you can post notifications to your app from the frontend.

For mode details, you can visit [Android SDK](https://github.com/appspector/android-sdk/) and [iOS SDK](https://github.com/appspector/ios-sdk) pages.

# Feedback
Let us know what do you think or what would you like to be improved: [info@appspector.com](mailto:info@appspector.com).

[Join our slack to discuss setup process and features](https://slack.appspector.com)
