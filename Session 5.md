# To get started, include RecyclerView in your dependencies and layout.
### activty_main.xml
```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <androidx.recyclerview.widget.RecyclerView
        android:id="@+id/rv"
        android:layout_width="match_parent"
        android:layout_height="wrap_content">
    </androidx.recyclerview.widget.RecyclerView>

</LinearLayout>
```
### build.gradle (:app)
```gradle
dependencies {

    implementation 'androidx.appcompat:appcompat:1.3.0'
    implementation 'androidx.appcompat:recyclerview:1.3.0'
}
```
___

# Decide what kind of items you want to display in the list and create the layout for a single item in your RecyclerView.
### list_items.xml
```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="50dp"
        android:layout_marginTop="20dp"
        android:text="plat : "
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <TextView
        android:id="@+id/textView2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="20dp"
        android:layout_marginEnd="50dp"
        android:text="pizza"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintTop_toTopOf="parent" />
</LinearLayout>
```
___

# Create a Plain Old Java Object to hold the data of a single item in the list.
### Plat.java
```java
public class Plat {
    private String name;

    Plat(String name) {
        this.name = name;
    }

    public String getName() {
        return name;
    }
}
```
___



