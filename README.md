# Dart 기본위젯

# Dart 화면구성

```dart
import 'package:flutter/material.dart';

void main() => runApp(const MyApp());

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      home: Scaffold(
        body: const SafeArea(
          child: Center(
            child: AspectRatio(
              aspectRatio: 3 / 2.5, // 이미지 비율 맞춤
              child: ColoredBlocks(),
            ),
          ),
        ),
      ),
    );
  }
}

class ColoredBlocks extends StatelessWidget {
  const ColoredBlocks({super.key});

  @override
  Widget build(BuildContext context) {
    return Container(
      decoration: BoxDecoration(
        border: Border.all(color: Colors.black, width: 1),
      ),
      child: Column(
        children: [
          Expanded(
            flex: 1,
            child: Row(
              children: [
                Expanded(
                  flex: 2,
                  child: Container(color: Colors.red),
                ),
                Expanded(
                  flex: 1,
                  child: Column(
                    children: [
                      Expanded(
                        flex: 1,
                        child: Container(color: Colors.blue),
                      ),
                      Expanded(
                        flex: 1,
                        child: Row(
                          children: [
                            Expanded(
                              flex: 1,
                              child: Container(color: Colors.black),
                            ),
                            Expanded(
                              flex: 1,
                              child: Container(color: Colors.orange),
                            ),
                          ],
                        ),
                      ),
                    ],
                  ),
                ),
              ],
            ),
          ),
          Expanded(
            flex: 1,
            child: Container(color: Colors.yellow),
          ),
        ],
      ),
    );
  }
}

```
<img src="스크린샷 2025-04-13 212055.png" width="500">

