# Max size for async storage and SQLite

By default on Android Async storage has a limit of 6MB. This can be increased by adding:

```java
// android/gradle.properties

AsyncStorage_db_size_in_MB=10
```

There maybe instances where the data being stored in SQLite is to large and you get the following error:

`SQLiteQuery: exception: Row too big to fit into CursorWindow requiredPos=0, totalRows=1`

```java
// MainActivity.java

import android.database.CursorWindow;
import java.lang.reflect.Field;

// In the oncreate function
try {
  Field field = CursorWindow.class.getDeclaredField("sCursorWindowSize");
  field.setAccessible(true);
  field.set(null, 100 * 1024 * 1024); //the 100MB is the new size
} catch (Exception e) {
  if (DEBUG_MODE) {
    e.printStackTrace();
  }
}

```

[Source](https://github.com/andpor/react-native-sqlite-storage/issues/364)