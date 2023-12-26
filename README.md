import 'package:flutter/material.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  // This widget is the root of your application.
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Flutter Demo',
      theme: ThemeData(
        colorScheme: ColorScheme.fromSeed(seedColor: Colors.deepPurple),
        useMaterial3: true,
      ),
      home: const MyHomePage(title: 'Flutter Demo Home Page'),
    );
  }
}

class MyHomePage extends StatefulWidget {
  const MyHomePage({super.key, required this.title});

  final String title;

  @override
  State<MyHomePage> createState() => _MyHomePageState();
}

class _MyHomePageState extends State<MyHomePage> {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        backgroundColor: Theme.of(context).colorScheme.inversePrimary,
        title: const Text("GitHub入門"),
      ),
      body: Center(
        child: Column(
          //mainAxisAlignment: MainAxisAlignment.center
          children: <Widget>[
            Container(
              height: 100,
              width: 400,
              color: Colors.black,
              child: Text(
                'これはchildです',
                style: Theme.of(context).textTheme.headlineMedium?.copyWith(
                  fontSize: 30,
                  color: Colors.white,
                ),
                textAlign: TextAlign.left,
              ),
            ),
            Container(
              height: 100,
              width: 300,
              color: Colors.pink,
              child: Text(
                'これもchildです',
                style: Theme.of(context).textTheme.headlineMedium?.copyWith(
                  fontSize: 25,
                  color: Colors.black,
                ),
                textAlign: TextAlign.left,
              ),
            ),
            Row(
              children: <Widget>[
                Container(
                  height: 200,
                  width: MediaQuery.of(context).size.width / 4,
                  color:Colors.blue,
                ),
                Container(
                  height: 200,
                  width: MediaQuery.of(context).size.width / 4,
                  color:Colors.yellow,
                ),
                Container(
                  height: 200,
                  width: MediaQuery.of(context).size.width / 4,
                  color:Colors.blue,
                ),
                Container(
                  height: 200,
                  width: MediaQuery.of(context).size.width / 4,
                  color:Colors.yellow,
                ),
              ],
            ),
            const Text(
              'トップページ',
            ),
            Text(
              'アプリケーションのトップのページです',
              style: Theme.of(context).textTheme.headlineMedium?.copyWith(
                fontSize: 36,
                color: Colors.red,
                fontWeight: FontWeight.bold,
              ),
            ),
            const Icon(
              Icons.tab,
              color: Colors.green,
            ),
            Row(
              children: <Widget>[
                Container(
                  height: 10,
                  width: MediaQuery.of(context).size.width / 4,
                  color:Colors.green,
                ),
                Container(
                  height: 10,
                  width: MediaQuery.of(context).size.width / 4,
                  color:Colors.black,
                ),
                Container(
                  height: 10,
                  width: MediaQuery.of(context).size.width / 4,
                  color:Colors.green,
                ),
                Container(
                  height: 10,
                  width: MediaQuery.of(context).size.width / 4,
                  color:Colors.black,
                ),
              ],
            ),
            Text(
              '一番下のwidgetです',
              style: Theme.of(context).textTheme.headlineMedium?.copyWith(
                fontSize: 28,
                color: Colors.purple,
                fontWeight: FontWeight.bold,
              ),
              textAlign: TextAlign.center,
            ),
          ],
        ),
      ),
      floatingActionButton: FloatingActionButton(
        backgroundColor: Colors.pink,
        child: const Icon(
          Icons.all_inbox,
          color: Colors.black,
        ),
        onPressed: () {

        },
      ),// This trailing comma makes auto-formatting nicer for build methods.
    );
  }
}
