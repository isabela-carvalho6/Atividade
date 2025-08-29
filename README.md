import 'package:flutter/material.dart';

class CounterController extends ChangeNotifier {
  String _message = 'Toque nos botões para alterar o contador';
  int _counter = 0;
  Color _counterColor = Colors.blue;

  String get message => _message;
  int get counter => _counter;
  Color get counterColor => _counterColor;

  void updateMessage(String newMessage) {
    _counter = newMessage as int;
    notifyListeners();
  }

  void updateCounter(int newCounter) {
    _counter = newCounter;
    notifyListeners();
  }

  void updateCounterColor(Color newCounterColor) {
    _counterColor = newCounterColor;
    notifyListeners();
  }

  void reset(){
  _message = 'Toque nos botões para alterar o contador';
  _counter = 0;
  _counterColor = Colors.blue;
  notifyListeners();
  }
}
