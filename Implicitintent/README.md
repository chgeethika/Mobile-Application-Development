# Ex.No:3 Develop program to create a text field and a button “Navigate”. When you enter “www.google.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the google page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:
```
1.open Android Stdio and then click on File -> New -> New project.
2.Then type the Application name as “implicitintent″ and click Next. 
3.Then select the Empty Activity and click Next and click finish.
4.Click on app -> res -> layout -> activity_main.xml.
5.create a design and write a code.
5.Click on app -> java -> com.example.implicitintent -> MainActivity.
6.write the javacode and execue it.








```



## PROGRAM:
```
activity_main.xml

<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:fontFamily="sans-serif-black"
        android:text="Implicitintent"
        android:textColor="@android:color/holo_red_dark"
        android:textSize="24sp"
        app:layout_constraintBottom_toTopOf="@+id/editTextText"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.455"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.177" />

    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginBottom="4dp"
        android:text="click me"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.529"
        app:layout_constraintStart_toStartOf="parent" />

    <EditText
        android:id="@+id/editTextText"
        android:layout_width="273dp"
        android:layout_height="63dp"
        android:layout_marginTop="206dp"
        android:layout_marginBottom="320dp"

        android:ems="10"
        android:hint="enter the url"
        android:inputType="text"
        app:layout_constraintBottom_toTopOf="@+id/button"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.631"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView" />

</androidx.constraintlayout.widget.ConstraintLayout>

MainActivity.java

package com.example.implicitintent;
import static com.example.implicitintent.R.id.editTextText;
import androidx.appcompat.app.AppCompatActivity;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.content.Intent;
public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        EditText editText;
        Button button;
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        button=findViewById(R.id.button);
        editText=(EditText)findViewById(editTextText);
        button.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                String url=editText.getText().toString();
                Intent intent=new Intent(Intent.ACTION_VIEW, Uri.parse(url));
                startActivity(intent);
            }
        });

    }
}

Developed by:ch.geethika
Registeration Number :212221040032

```

## OUTPUT
![Screenshot (259)](https://github.com/chgeethika/Mobile-Application-Development/assets/142209368/afba11b9-d399-41dc-ace4-acae3f4f88f8)

![Screenshot (260)](https://github.com/chgeethika/Mobile-Application-Development/assets/142209368/9c6422bd-f0ad-4625-9a3a-9ee13430a219)

![Screenshot (253)](https://github.com/chgeethika/Mobile-Application-Development/assets/142209368/6e170046-b5f7-4a9f-9d69-4c856428c8d0)

## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the google page using Android Studio is developed and executed successfully.


