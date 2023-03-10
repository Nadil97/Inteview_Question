# Flutter interview Question

![Flutter Interview](/assets/img/images.png "Flutter Interview")

## What is Flutter and why it is used?
Flutter is an open-source UI software development kit created by Google. It is used to develop cross-platform applications for `Android,` `iOS`, `Linux`, `macOS`, `Windows`, `Google` Fuchsia, and the web from a single codebase.

## What are the benefits of using flutter in a project?
There are many advantages of Flutter as a cross platform mobile development framework, including the ability to create web applications that have a native look and feel on both Android and iOS devices, reduced development time and costs, and increased flexibility

## What are some of the main features of flutter?
* Hot reload
* Cross-platform development
* widget library.
* Native Performance
* Open-source.

## How does [Technology Name] compare to similar technologies in the same space?

### Flutter Vs React Native

The main difference however is in the programming language: React Native uses JavaScript, and Flutter uses Dart.

# Flutter Coding Question

## Flutter Login page Code

~~~~
import 'package:flutter/material.dart';
import 'HomePage.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      home: LoginDemo(),
    );
  }
}

class LoginDemo extends StatefulWidget {
  @override
  _LoginDemoState createState() => _LoginDemoState();
}

class _LoginDemoState extends State<LoginDemo> {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      backgroundColor: Colors.white,
      appBar: AppBar(
        title: Text("Login Page"),
      ),
      body: SingleChildScrollView(
        child: Column(
          children: <Widget>[
            Padding(
              padding: const EdgeInsets.only(top: 60.0),
              child: Center(
                child: Container(
                    width: 200,
                    height: 150,
                    /*decoration: BoxDecoration(
                        color: Colors.red,
                        borderRadius: BorderRadius.circular(50.0)),*/
                    child: Image.asset('asset/images/flutter-logo.png')),
              ),
            ),
            Padding(
              //padding: const EdgeInsets.only(left:15.0,right: 15.0,top:0,bottom: 0),
              padding: EdgeInsets.symmetric(horizontal: 15),
              child: TextField(
                decoration: InputDecoration(
                    border: OutlineInputBorder(),
                    labelText: 'Email',
                    hintText: 'Enter valid email id as abc@gmail.com'),
              ),
            ),
            Padding(
              padding: const EdgeInsets.only(
                  left: 15.0, right: 15.0, top: 15, bottom: 0),
              //padding: EdgeInsets.symmetric(horizontal: 15),
              child: TextField(

                obscureText: true,
                decoration: InputDecoration(
                    border: OutlineInputBorder(),
                    labelText: 'Password',
                    hintText: 'Enter secure password'),
              ),
            ),
            FlatButton(
              onPressed: (){
                //TODO FORGOT PASSWORD SCREEN GOES HERE
              },
              child: Text(
                'Forgot Password',
                style: TextStyle(color: Colors.blue, fontSize: 15),
              ),
            ),
            Container(
              height: 50,
              width: 250,
              decoration: BoxDecoration(
                  color: Colors.blue, borderRadius: BorderRadius.circular(20)),
              child: FlatButton(
                onPressed: () {
                  Navigator.push(
                      context, MaterialPageRoute(builder: (_) => HomePage()));
                },
                child: Text(
                  'Login',
                  style: TextStyle(color: Colors.white, fontSize: 25),
                ),
              ),
            ),
            SizedBox(
              height: 130,
            ),
            Text('New User? Create Account')
          ],
        ),
      ),
    );
  }
}


~~~~

# Question base on Given Code

## Why use extend Keyword this code ?
You can inherit from or extend a class using the extends keyword. This allows you share properties and methods between classes that are similar, but not exactly the same.

## why use overide methods ?
`@override` just points out that the function is also defined in an ancestor class, but is being redefined to do something else in the current class. It's also used to annotate the implementation of an abstract method. It is optional to use but recommended as it improves readability.

## Why use BuildContext ?
BuildContext is a locator that is used __to track each widget in a tree and locate them and their position in the tree__. The BuildContext of each widget is passed to their build method. Remember that the build method returns the widget tree a widget renders. Each BuildContext is unique to a widget.

## Why use createState() => _SomeWidgetState();
Creates the __mutable state for this widget at a given location in the tree__. Subclasses should override this method to return a newly created instance of their associated State subclass: 
```
@override State<SomeWidget> createState() => _SomeWidgetState();
```