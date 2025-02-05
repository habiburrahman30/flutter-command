# Flutter Command

###Create Flutter MVC Boilerplate
```
mkdir -p lib/src/{base,components,configs,controllers,helpers,models,pages,routes,services,themes} && touch lib/main.dart lib/src/app.dart
```

####Step 2
```
cat >> lib/main.dart
```
```
import 'package:flutter/material.dart';
import 'src/app.dart';

void main() async {
  WidgetsFlutterBinding.ensureInitialized();
  runApp(App());
}
```
####Step 3
```
cat >> lib/src/app.dart
```
```
import 'package:flutter/material.dart';
import 'package:get/get.dart';

class App extends StatelessWidget {
  const App({super.key});

  @override
  Widget build(BuildContext context) {
    return GetMaterialApp(
      title: 'Flutter Demo',
      // initialRoute: '/',
      // initialBinding: BaseBinding(),
      debugShowCheckedModeBanner: false,
      // getPages: GetxRouteGenerator.appRoutes(),
      theme: ThemeData(
        colorScheme: ColorScheme.fromSeed(seedColor: Colors.deepPurple),
        useMaterial3: true,
      ),
      home: SplashPage(),
    );
  }
}
```
