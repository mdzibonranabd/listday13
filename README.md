# listday13
class13
import 'dart:js';

import 'package:flutter/material.dart';

void main() =>runApp(MyApp());
class MyApp extends StatelessWidget{
  @override
  Widget build(BuildContext context){
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: Text("NAME OF Items "),
        ),
        body: BodyLayout(),
      ),
    );
  }
}

class BodyLayout extends StatelessWidget{
  @override
  Widget build(BuildContext context){
    return _MyListView(context);
  }
}
Widget _MyListView(BuildContext Context) {
//   return ListView(
//     children:<Widget> [
//       ListTile(title: Text("Zibon ❤🎈"),),
//       ListTile(title: Text("MIM 👫 ♥️ SAKIB"),),
//       ListTile(title: Text("Jibon ❤️️"),),
//       ListTile(title: Text("RANA ❤️️"),),
//
//     ],
//   );
// }
  final ListItems = ['Bag', 'pan', 'shari', 'jama', 'panjabi'];
  return ListView.builder(
      itemCount: ListItems.length,
      itemBuilder: (context, index) {
        return ListTile(title: Text(ListItems[index]),);
      }
  );
}
