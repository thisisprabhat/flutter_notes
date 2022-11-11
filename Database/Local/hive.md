# Steps to add Hive to a project


## Step 1 : Add Required dependencies in pubspec.yaml file

>In dependencies:

```yaml
dependencies:
  flutter:
    sdk: flutter
  cupertino_icons: ^1.0.2

  // These are added 
  hive: ^2.2.3
  hive_flutter: ^1.1.0
  path_provider: ^2.0.11

  ```
  >Also in dev_dependencies
  ```yaml
  dev_dependencies:
  flutter_test:
    sdk: flutter
  flutter_lints: ^2.0.0

  # These are added
  hive_generator: ^2.0.0
  build_runner: ^2.3.2
  ```
## Step 2 : Initializing Hive in main.dart

```dart
import 'package:flutter/material.dart';
import 'package:hive_app/home_page.dart';
import 'package:hive_flutter/hive_flutter.dart';
import 'package:path_provider/path_provider.dart' as path_provider;

Future<void> main() async { //main function is converted in to future and async

//The below line is for getting document path using path_provider package
  final appDocumentaryDirectory = await path_provider.getApplicationDocumentsDirectory();
// In the below line hive is initialized with the directory
  Hive.init(appDocumentaryDirectory.path);
  runApp(const MyApp());
}
```
