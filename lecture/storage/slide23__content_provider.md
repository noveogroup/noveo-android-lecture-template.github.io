## Content Provider

Класс для обмена данными между приложениями.

*Use case*:  
* Доступ к контактам и т.п.
* Виджеты

<br>
<br>

also [`DocumentsProvider`](https://developer.android.com/reference/android/provider/DocumentsProvider), [`FileProvider`](https://developer.android.com/reference/androidx/core/content/FileProvider?hl=en), etc.

<!-- .element: class="fragment" data-fragment-index="1" -->

------

## Работа с Content Provider

Переопределить методы:

* `onCreate()`
* `query()`
* `getType()`
* `insert()`
* `update()`
* `delete()`

<br>
<br>

Android Manifest:  
<!-- .element: class="fragment" data-fragment-index="1" -->
```
<provider 
     android:authorities="com.noveo.internship.db.exampleContentProvider" 
     android:name=".database.ExampleContentProvider"
     android:multiprocess="true"
     android:exported="false" />
```
<!-- .element: class="fragment" data-fragment-index="1" -->

