# HW Android_Studio и ADB

 1. Отобразить подключённый девайс в консоли.
```
adb devices
```
 2. Вывести адрес приложения todolist в системе Android.
```
adb shell pm list packages | findstr todolist
```
 3. Установить .apk файл приложениия todolist на телефон с компьютера через  ADB.
```
adb install /001_ToDoList-master/app/build/outputs/apk/debug/app-debug.apk
```
 4. Сделать скриншот запущенного приложения todolist и сразу скопировать на компьютер в одной команде.
```
adb shell screencap /mnt/sdcard/Download/test.png
adb pull /mnt/sdcard/Download/test.png C:\Users\user\Downloads\test.png
```
 5. Вывести в консоль логи приложения todolist.
```
adb logcat | findstr -rnw "com.android.todolist"
```
 6. Скопировать логи приложения todolist на компьютер.
```
adb logcat | findstr -rnw "com.android.todolist" > C:\Users\user\Downloads\todolist.log
```
 7. Удалить приложение todolist с телефона через ADB.
```
adb uninstall "com.android.todolist"
```
