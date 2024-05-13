## WORKSHOP ----SUMMATION OF TWO NUMBERS USING ANDROID STUDIO.


## AIM:

Summation of two numbers using Android Studio

## EQUIPMENTS REQUIRED:

Android Studio(Min. required Artic Fox)


## ALGORITHM:

Step 1: Begin the program.

Step 2: Prompt the user to input the first number.

Step 3: Prompt the user to input the second number.

Step 4: Check if both inputs are valid numbers.

Step 5: If any input is invalid, display an error message and return to step 2.

Step 6: Add the two numbers together to find their sum.

Step 7: Display the sum to the user.

Step 8: End the program

## Program:
 ```
/*
Program to implement a Hello world Activity using all lifecycles methods using Android Studio .
Developed by: NAVEENAA A K
RegisterNumber:  212222230094
*/
```

## MainActivity.java:
```java
package workshop.java;

import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.Toast;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    private EditText firstNumberEditText, secondNumberEditText;
    private Button addButton;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        firstNumberEditText = findViewById(R.id.firstNumber);
        secondNumberEditText = findViewById(R.id.secondNumber);
        addButton = findViewById(R.id.addButton);

        addButton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                calculateSum();
            }
        });
    }

    private void calculateSum() {
        String firstNumberStr = firstNumberEditText.getText().toString();
        String secondNumberStr = secondNumberEditText.getText().toString();

        if (!firstNumberStr.isEmpty() && !secondNumberStr.isEmpty()) {
            int firstNumber = Integer.parseInt(firstNumberStr);
            int secondNumber = Integer.parseInt(secondNumberStr);
            int sum = firstNumber + secondNumber;

            Toast.makeText(this, "Sum is: " + sum, Toast.LENGTH_SHORT).show();
        } else {
            Toast.makeText(this, "Please enter both numbers", Toast.LENGTH_SHORT).show();
        }
    }
}

```
## activity_main.xml:
```xml
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <EditText
        android:id="@+id/firstNumber"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="50dp"
        android:layout_centerHorizontal="true"
        android:hint="Enter first number"
        android:inputType="number"/>

    <EditText
        android:id="@+id/secondNumber"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@id/firstNumber"
        android:layout_marginTop="20dp"
        android:layout_centerHorizontal="true"
        android:hint="Enter second number"
        android:inputType="number"/>

    <Button
        android:id="@+id/addButton"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@id/secondNumber"
        android:layout_marginTop="30dp"
        android:layout_centerHorizontal="true"
        android:text="Add"/>
</RelativeLayout>
```
## Output:

![image](https://github.com/naveenaakumarasamy/WORKSHOP_SUMMATION/assets/113497406/23532cfc-8b55-492d-b11c-d2ccc34b7af5)


## Result:

Thus successfully we have added two numbers using andorid studio.
