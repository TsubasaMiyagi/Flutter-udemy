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

全て30.0
```
margin: EdgeInsets.all(30.0)
```

垂直30.0, 水平50.0
```
margin: EdgeInsets.symmetric(vertical: 30.0, horizontal: 50.0)
```

左のみ20.0
```
margin: EdgeInsets.only(left:20)
```

上下左右指定（Left,Top,Right,Bottom）
```
margin: EdgeInsets.fromLTRB(20.0, 30.0, 40.0, 50.0)
```

### Column

[使用方法](https://qiita.com/sekitaka_1214/items/03255fd9f61685503af3)

**mainAxisSize**

```
mainAxisSize: MainAxisSize.min //max
```
　　
**mainAxisAlignment**

均等配置
```
mainAxisAlignment: MainAxisAlignment.spaceEvenly
```

中央寄せ
```
mainAxisAlignment: MainAxisAlignment.center
```

上(下)寄せ
```
mainAxisAlignment: MainAxisAlignment.start(end)
```

**crossAxisAlignment**
```
crossAxisAlignment:CrossAxisAlignment.start
```
<img width="376" alt="名称未設定18" src="https://user-images.githubusercontent.com/109131074/185045990-c2b8be3d-19d4-45de-b5ad-ad9d7e13cb56.png">


```
crossAxisAlignment:CrossAxisAlignment.end
```
<img width="373" alt="名称未設定18" src="https://user-images.githubusercontent.com/109131074/185046374-28568a31-4f10-4053-91a6-40515e02e208.png">

```
crossAxisAlignment:CrossAxisAlignment.strech
```
<img width="377" alt="名称未設定19" src="https://user-images.githubusercontent.com/109131074/185047342-d09818b5-f88f-4806-94d4-236c2ae055af.png">
widthの指定不要、親のColumnの幅に合わせて伸びる
