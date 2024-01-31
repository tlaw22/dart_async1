A sample command-line application with an entrypoint in `bin/`, library code
in `lib/`, and example unit test in `test/`.


```
import 'dart:io';

import 'package:test/test.dart';

void main(List<String> arguments) {
  print("Preparing to wait 15 seconds");
  longPress();
  print("completing operation");
  print("Operation complete!");
}

longPress() {
  // sleep(Duration(seconds: 15));
Future.delayed(Duration(seconds: 7), () {
  print('Async Complete'); 
});

  print('Sync Complete');
}
```
