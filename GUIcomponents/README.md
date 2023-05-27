# Ex.No: 2 To develop an application that uses GUI Components with Fonts and Colors. 


## AIM:

To create an application that uses GUI Components with Fonts and Colors using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:
Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as HelloWorld and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Display message give in MainActivity file.

Step 7: Save and run the application.


## PROGRAM:
Program to print the text “GUIcomponent”.
## Activity_main.xml:
<?xml version="1.0" encoding="utf-8"?>

<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"

xmlns:app="http://schemas.android.com/apk/res-auto"                                                                                     

xmlns:tools="http://schemas.android.com/tools"    

android:layout_width="match_parent"

android:layout_height="match_parent"    

tools:context=".MainActivity">
    

    <Button   
        android:id="@+id/colorButton"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_centerHorizontal="true"
        android:layout_marginStart="120dp"
        android:text="Change Color"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/fontButton"
        app:layout_constraintVertical_bias="0.082" />

    <Button
        android:id="@+id/fontButton"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@id/colorButton"
        android:layout_centerHorizontal="true"
        android:layout_marginStart="120dp"
        android:layout_marginTop="120dp"
        android:text="Change Font"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView" />

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@id/fontButton"
        android:layout_centerHorizontal="true"
        android:text="Hello World!"
        android:textSize="40sp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.435"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.325" />

</androidx.constraintlayout.widget.ConstraintLayout>

## MainActivity.java:
package com.example.myapplication;

import androidx.appcompat.app.AppCompatActivity;

import android.graphics.Color;

import android.graphics.Typeface;

import android.os.Bundle;

import android.view.View;

import android.widget.Button;

import android.widget.TextView;

public class MainActivity extends AppCompatActivity {

    private Button colorButton;
    
    private Button fontButton;
    
    private TextView textView;
    
    @Override
    
    protected void onCreate(Bundle savedInstanceState) {
    
        super.onCreate(savedInstanceState);
        
        setContentView(R.layout.activity_main);
        
        colorButton = findViewById(R.id.colorButton);
        
        fontButton = findViewById(R.id.fontButton);
        
        textView = findViewById(R.id.textView);
        
        colorButton.setOnClickListener(new View.OnClickListener() {
        
            @Override
            
            public void onClick(View v) {
            
                changeTextColor();
                
            } });

        fontButton.setOnClickListener(new View.OnClickListener() {
        
            @Override
            
            public void onClick(View v) {
            
                changeFont();
                
            }
        });
    }
    private void changeTextColor() {
    
        int randomColor = Color.rgb(
        
                (int) (Math.random() * 256),
                
                (int) (Math.random() * 256),
                
                (int) (Math.random() * 256)
        );
        textView.setTextColor(randomColor);
    }
    private void changeFont() {
    
        Typeface[] fontStyles = new Typeface[]{
        
                Typeface.DEFAULT,
                
                Typeface.DEFAULT_BOLD,
                
                Typeface.MONOSPACE,
                
                Typeface.SANS_SERIF,
                
                Typeface.SERIF
                
        };

        int randomIndex = (int) (Math.random() * fontStyles.length);
        Typeface selectedFont = fontStyles[randomIndex];
        textView.setTypeface(selectedFont);}
   }


Developed by: Mahesh.S

Registeration Number : 212221040095


## OUTPUT
![Screenshot (186)](https://github.com/MaheshS03/Mobile-Application-Development/assets/128498431/0069e359-b928-4d0e-9df8-78e0371230bc)

![Screenshot (187)](https://github.com/MaheshS03/Mobile-Application-Development/assets/128498431/9d107a8d-d8b9-4d95-9f18-c374cea0c6ba)

![Screenshot (189)](https://github.com/MaheshS03/Mobile-Application-Development/assets/128498431/b96a144c-7f70-4ba9-bc29-d8bb58579818)

![Screenshot (190)](https://github.com/MaheshS03/Mobile-Application-Development/assets/128498431/ad89b626-094c-4907-a2a5-826d45bb6ae8)

![ex2 1](https://github.com/MaheshS03/Mobile-Application-Development/assets/128498431/1a3e1c8c-bcc6-4e51-ad5d-f1064c1973a4)

![ex2 2](https://github.com/MaheshS03/Mobile-Application-Development/assets/128498431/0560cd67-33bd-48e2-8190-bf4253102145)

![ex2 3](https://github.com/MaheshS03/Mobile-Application-Development/assets/128498431/bd0a2f05-782e-4b65-a4a0-080e62194db5)

![ex2 4](https://github.com/MaheshS03/Mobile-Application-Development/assets/128498431/4b887e3b-525b-480a-90ba-fdb6d8e05956)


## RESULT
Thus a Simple Android Application that uses GUI Components with Fonts and Colors using Android Studio is developed and executed successfully.


