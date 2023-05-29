
# Ex.No:7 Develop an android application to display the place name with image using list view in android studio.


## AIM:

To create and develop the application to display the place name with image using list view in android studio

## EQUIPMENTS REQUIRED:

Android Studio(Latest Version)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as “listview″ and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Get contacts details and Display details give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:

Program to print the list of item.

## Activity_main.xml:

<?xml version="1.0" encoding="utf-8"?>

<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
              
    xmlns:app="http://schemas.android.com/apk/res-auto"
              
    xmlns:tools="http://schemas.android.com/tools"
              
    android:layout_width="match_parent"
              
    android:layout_height="match_parent"
              
    tools:context=".MainActivity">

    <ListView
        android:id="@+id/simpleListView"
        android:layout_width="match_parent"
        android:layout_height="300dp"
        android:divider="@color/material_blue_grey_800"
        android:dividerHeight="1dp"
        android:footerDividersEnabled="false" />

</LinearLayout>

## Listview.xml:

<?xml version="1.0" encoding="utf-8"?>

<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
              
    android:layout_width="match_parent"
              
    android:layout_height="match_parent">

    <ImageView
        android:id="@+id/icon"
        android:layout_width="50dp"
        android:layout_height="50dp" />
    <TextView
        android:id="@+id/textView"
        android:layout_width="fill_parent"
        android:layout_height="wrap_content"
        android:layout_gravity="center"
        android:textColor="@color/black" />

</LinearLayout>

## MainActivity.java:

package com.example.placename;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;

import android.widget.ListView;

public class MainActivity extends AppCompatActivity {

    ListView simpleList;
    String countryList[] = {"Bangalore", "Chennai", "Coimbatore", "KanyaKumari", "Kerala", "Mumbai"};
    int flags[] = {R.drawable.bangalore, R.drawable.chennai, R.drawable.coimbatore, R.drawable.kanyakumari,
            R.drawable.kerala, R.drawable.mumbai};

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        simpleList = findViewById(R.id.simpleListView);

        CustomAdapter customAdapter = new CustomAdapter(getApplicationContext(), countryList, flags);
        simpleList.setAdapter(customAdapter);
    }
}

## CustomAdapter.java:

package com.example.placename;

import android.content.Context;

import android.media.Image;

import android.view.LayoutInflater;

import android.view.View;

import android.view.ViewGroup;

import android.widget.BaseAdapter;

import android.widget.ImageView;

import android.widget.TextView;

import java.util.zip.Inflater;

public class CustomAdapter extends BaseAdapter {
    Context context;
    String countryList[];
    int flags[];
    LayoutInflater inflter;

    public CustomAdapter(Context applicationContext, String[] countryList, int[] flags) {
        this.context = applicationContext;
        this.countryList = countryList;
        this.flags = flags;
        inflter = (LayoutInflater.from(applicationContext));
    }

    @Override
    public int getCount() {
        return countryList.length;
    }

    @Override
    public Object getItem(int i) {
        return null;
    }

    @Override
    public long getItemId(int i) {
        return 0;
    }

    @Override
    public View getView(int i, View view, ViewGroup viewGroup) {
        view = inflter.inflate(R.layout.listview, null);
        TextView country = (TextView) view.findViewById(R.id.textView);
        ImageView icon = (ImageView) view.findViewById(R.id.icon);
        country.setText(countryList[i]);
        icon.setImageResource(flags[i]);
        return view;
    }
}


Developed by: Mahesh S

Registeration Number : 212221040095


## OUTPUT

![Screenshot (221)](https://github.com/MaheshS03/Mobile-Application-Development/assets/128498431/bac777ca-2374-4f1e-9406-c7c7b2e3dec0)

![Screenshot (222)](https://github.com/MaheshS03/Mobile-Application-Development/assets/128498431/b6e0531d-58ee-472a-aae8-1cab0e1ce53c)

![Screenshot (223)](https://github.com/MaheshS03/Mobile-Application-Development/assets/128498431/e349f03f-2f2f-45f8-a70e-210ecd2ae444)

![Screenshot (224)](https://github.com/MaheshS03/Mobile-Application-Development/assets/128498431/9879f2f4-25cb-4b8b-ad49-58e8d55cbf3f)

![ex7](https://github.com/MaheshS03/Mobile-Application-Development/assets/128498431/6231483c-4918-468b-b79c-1c740541c4a5)


## RESULT
Thus a Simple Android Application to create and develop the application to display the place name with image using list view in android studio is developed and executed successfully.
