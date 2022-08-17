# Flutter Day1
## 40 Flutter Layout Challenge
https://www.udemy.com/course/flutter-bootcamp-with-dart/

### Container
[Container class - widgets library - Dart API](https://api.flutter.dev/flutter/widgets/Container-class.html)

## SafeArea
1. option + return
2. wrap with Widget
3. widget → SafeAreaに変更

<img width="387" alt="名称未設定16" src="https://user-images.githubusercontent.com/109131074/184904794-292e217b-7e05-4b06-a828-712a9b3d21d0.png">

```Dart
class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        backgroundColor: Colors.teal,
        body: SafeArea(
          child: Container(
            color: Colors.white,
            child: Text('Hello'),
          ),
        ),
      ),
    );
  }
}
```

### margin,padding
[EdgeInsets class - painting library - Dart API](https://api.flutter.dev/flutter/painting/EdgeInsets-class.html)

上下左右30.0
```

margin:EdgeInsets.all(30)
```

垂直30.0,水平50.0
```

margin: EdgeInsets.symmetric(vertical: 30, horizontal: 50)
```

左のみ20.0
```

margin:EdgeInsets.only(left:20)
```

上下左右指定（Left,Top,Right,Bottom）
```

margin:EdgeInsets.fromLTRB(20.0, 30.0, 40.0, 50.0)
```

