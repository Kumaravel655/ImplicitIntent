# ImplicitIntent
Develop program to create a text field and a button “Navigate”. When you enter “www.google.com” and press navigate button it should open google page using Implicit Intents and to create two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.

## AIM:
To create a layout,click button,open google page using Implicit Intents and display factorial number using Explicit Intents in Android Studio.

## EQUIPMENTS REQUIRED: 
Android Studio(Min. required Artic Fox)

## ALGORITHM: 
Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as “ex.no.2″ and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: open google page using Implicit Intents and display factorial number using Explicit Intents in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
/*
Program to print the text “Implicit Intents”.
Developed by:Kumaran.B
Registeration Number :212220230026
*/
```
### MainActivity.java
```java
package com.example.exp2implicit;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.content.Intent;
import android.net.Uri;

import android.widget.Button;
import android.widget.EditText;
import android.view.View;

public class MainActivity extends AppCompatActivity {
    Button button;
    EditText editText;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        button = findViewById(R.id.button);
        editText =  findViewById(R.id.editText);

        button.setOnClickListener(new View.OnClickListener(){
            @Override
            public void onClick(View view) {
                String url=editText.getText().toString();
                Intent intent=new Intent(Intent.ACTION_VIEW, Uri.parse(url));
                startActivity(intent);
            }
        });

    }
    }
```
### activity_main.xml
```java
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <EditText
        android:id="@+id/editText"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginEnd="8dp"
        android:layout_marginStart="8dp"
        android:layout_marginTop="60dp"
        android:ems="10"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.575"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        android:autofillHints="" />


    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="156dp"
        android:layout_marginTop="204dp"
        android:layout_marginEnd="8dp"
        android:text="@string/visit"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.031"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/editText" />



</androidx.constraintlayout.widget.ConstraintLayout>
```
## output
![image](https://user-images.githubusercontent.com/75235334/165320159-1bb8af49-dc57-4c7c-b429-3935c49faed7.png)

![image](https://user-images.githubusercontent.com/75235334/165319841-a07b9343-44b9-47f5-b6b3-2bca1ddff856.png)
## result
Thus a Simple Android Application to open google page using Implicit Intents and display factorial of the same number using Explicit Intents using Android Studio is developed and executed successfully.
