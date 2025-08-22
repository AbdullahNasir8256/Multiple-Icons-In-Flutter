# Multiple-Icons-In-Flutter


import 'dart:io';

import 'package:flutter/material.dart';

void main() {
  runApp(const MyApp());

}
class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      theme:ThemeData(colorScheme:ColorScheme.fromSeed(
        seedColor: const Color.fromARGB(255, 255, 255, 255),
        brightness: Brightness.dark),),
     home: Scaffold(
      appBar: AppBar(
        title: Text("--Online Banking--"),
        centerTitle: true,
      ),
      floatingActionButton: Column(
        mainAxisAlignment: MainAxisAlignment.end,
        children: [

          FloatingActionButton(onPressed: () {
          print('Thumbs Up');
          },
          child:Icon(Icons.thumb_up_alt_sharp),
          ),
          SizedBox(height: 20,),
          FloatingActionButton(onPressed: () {
          print('Location');
          },
          child:Icon(Icons.add_location_alt_rounded),
          ),
          SizedBox(height: 20,),
        ],
      ),
    bottomNavigationBar: NavigationBar(destinations: [NavigationDestination(
      icon: Icon
    (Icons.home),
     label: 'Home'
     ),
     NavigationDestination(
      icon: Icon
    (Icons.delete),
     label: 'Delete'
     ),
        NavigationDestination(
      icon: Icon
    (Icons.person),
     label: 'Profile'
     ),
    ],
    onDestinationSelected: (int value) {
      print(value);
    },
    selectedIndex: 0,
    ),
     

     ),
    ); 
}
}


