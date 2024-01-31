A sample command-line application with an entrypoint in `bin/`, library code
in `lib/`, and example unit test in `test/`.

```
import 'dart:io';

import 'package:test/test.dart';

void main(List<String> arguments) {
  print("Preparing to wait 7 seconds");
  Future<String> result = longPress();
  result.then((String value) => print(value)).catchError((error) {
    print(error);
  }).whenComplete(() => prints("complete"));

  print("completing operation");
  print("Still working ... continueing");
}

Future<String> longPress() {
  //delayed sleep(Duration(seconds: 15));
  Future<String> delayed = Future.delayed(Duration(seconds: 7), () {
    return "Sync Complete";
  });
  return delayed;
}

```
