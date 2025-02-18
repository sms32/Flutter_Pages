import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      home: LoginScreen(),
    );
  }
}

class LoginScreen extends StatelessWidget {
  final TextEditingController usernameController = TextEditingController();
  final TextEditingController passwordController = TextEditingController();

  void login(BuildContext context) {
    String username = usernameController.text;
    String password = passwordController.text;

    if (username == "admin" && password == "admin") {
      ScaffoldMessenger.of(context).showSnackBar(
        SnackBar(content: Text("Login Successful! 🎉"), backgroundColor: Colors.green),
      );
    } else {
      ScaffoldMessenger.of(context).showSnackBar(
        SnackBar(content: Text("Invalid Username or Password ❌"), backgroundColor: Colors.red),
      );
    }
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      backgroundColor: Colors.grey[900], // Dark background
      body: Center(
        child: Container(
          width: 350,
          padding: EdgeInsets.all(20),
          decoration: BoxDecoration(
            color: Colors.grey[850], // Box background color
            borderRadius: BorderRadius.circular(20),
            boxShadow: [BoxShadow(color: Colors.black54, blurRadius: 10)],
          ),
          child: Column(
            mainAxisSize: MainAxisSize.min,
            children: [
              Text("Welcome Back", style: TextStyle(fontSize: 24, fontWeight: FontWeight.bold, color: Colors.white)),
              SizedBox(height: 20),

              TextField(
                controller: usernameController,
                decoration: InputDecoration(
                  labelText: "Username",
                  filled: true,
                  fillColor: Colors.grey[800],
                  border: OutlineInputBorder(borderRadius: BorderRadius.circular(10)),
                  labelStyle: TextStyle(color: Colors.white),
                ),
                style: TextStyle(color: Colors.white),
              ),
              SizedBox(height: 15),

              TextField(
                controller: passwordController,
                obscureText: true, // Hides password
                decoration: InputDecoration(
                  labelText: "Password",
                  filled: true,
                  fillColor: Colors.grey[800],
                  border: OutlineInputBorder(borderRadius: BorderRadius.circular(10)),
                  labelStyle: TextStyle(color: Colors.white),
                ),
                style: TextStyle(color: Colors.white),
              ),
              SizedBox(height: 20),

              ElevatedButton(
                onPressed: () => login(context),
                style: ElevatedButton.styleFrom(
                  backgroundColor: Colors.blueAccent,
                  padding: EdgeInsets.symmetric(horizontal: 40, vertical: 15),
                ),
                child: Text("Login", style: TextStyle(fontSize: 18)),
              ),
            ],
          ),
        ),
      ),
    );
  }
}
