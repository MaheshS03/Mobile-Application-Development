# Ex.No:3 Develop program to create a text field and a button “Navigate”. When you enter “www.google.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the google page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as implicit inetent and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Display message give in MainActivity file.

Step 7: Save and run the application.



## PROGRAM:
Program to print the text “Implicitintent”.

## Activity_main.xml:
<?xml version="1.0" encoding="utf-8"?>

<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"

    xmlns:app="http://schemas.android.com/apk/res-auto"
    
    xmlns:tools="http://schemas.android.com/tools"
    
    android:layout_width="match_parent"
    
    android:layout_height="match_parent"
    
    tools:context=".MainActivity">

    <EditText
        android:id="@+id/urlEditText"
        android:layout_width="292dp"
        android:layout_height="67dp"
        android:layout_marginStart="56dp"
        android:layout_marginTop="108dp"
        android:hint="Enter URL"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <Button
        android:id="@+id/navigateButton"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_gravity="center"
        android:text="Navigate"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/urlEditText" />
       

</androidx.constraintlayout.widget.ConstraintLayout>

## MainActivity.java:

package com.example.myapplication;

import androidx.appcompat.app.AppCompatActivity;

import android.content.Intent;

import android.net.Uri;

import android.os.Bundle;

import android.view.View;

import android.widget.Button;

import android.widget.EditText;

public class MainActivity extends AppCompatActivity {
    EditText editText;
    Button button;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        button = findViewById(R.id.navigateButton);
        editText = (EditText) findViewById(R.id.urlEditText);
        button.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                String url=editText.getText().toString();
                Intent intent = new Intent(Intent.ACTION_VIEW, Uri.parse(url));
                startActivity(intent);
            }
        });
    }
}

Developed by: Mahesh S

Registeration Number : 212221040095


## OUTPUT

![Screenshot (206)](https://github.com/MaheshS03/Mobile-Application-Development/assets/128498431/017fb3e9-8099-4b8b-8cfa-a9786f4c784f)

![Screenshot (209)](https://github.com/MaheshS03/Mobile-Application-Development/assets/128498431/9259aeb4-3334-49e6-aec6-74e3ea5a2756)

![ex3 1](https://github.com/MaheshS03/Mobile-Application-Development/assets/128498431/dfda0209-a41e-4c12-bfbf-1c7c43312a31)

![ex3 2](https://github.com/MaheshS03/Mobile-Application-Development/assets/128498431/a4e5f4ff-7958-40b4-ab60-8121949b1f3d)


## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the google page using Android Studio is developed and executed successfully.


