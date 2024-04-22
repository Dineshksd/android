1.CREATE LOGIN PAGE AND DISPLAY TOAST MESSAGE

Acitvity_main.xml:

<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout
 xmlns:android="http://schemas.android.com/apk/res/android"
 xmlns:app="http://schemas.android.com/apk/res-auto"
 xmlns:tools="http://schemas.android.com/tools"
 android:layout_width="match_parent"
 android:layout_height="match_parent"
 tools:context=".MainActivity">
<LinearLayout
android:layout_width="match_parent"
android:layout_height="match_parent"
android:orientation="vertical"
android:padding="16dp">
<ImageView
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:layout_gravity="center_horizontal"
 android:layout_marginBottom="16dp"
 android:src="@drawable/ic_launcher_foreground"
 android:importantForAccessibility="no" />
 <EditText
 android:id="@+id/etUsername"
 android:layout_width="match_parent"
 android:layout_height="wrap_content"
 android:layout_marginBottom="8dp"
 android:hint="Username"
 android:importantForAutofill="no"
 android:inputType="text"
 android:minHeight="48dp"
 tools:ignore="HardcodedText" />
 <EditText
 android:id="@+id/etPassword"
 android:layout_width="match_parent"
 android:layout_height="wrap_content"
 android:layout_marginBottom="16dp"
 android:hint="Password"
 android:importantForAutofill="no"
 android:inputType="textPassword"
 android:minHeight="48dp"
 tools:ignore="HardcodedText" />
<Button
 android:id="@+id/button1"
 android:layout_width="match_parent"
 android:layout_height="wrap_content"
 android:text="Login"
 tools:ignore="HardcodedText" />
<TextView
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:text="Don't have an account? Register"
 android:layout_gravity="center_horizontal"
 android:layout_marginTop="16dp"
 tools:ignore="HardcodedText" />
<TextView
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:text="Forgot Password?"
 android:layout_gravity="center_horizontal"
 android:layout_marginTop="8dp"
 tools:ignore="HardcodedText" />
</LinearLayout>
</androidx.constraintlayout.widget.ConstraintLayout>
MainActivity.java:
package com.example.ex_1;
import androidx.appcompat.app.AppCompatActivity;
import android.app.Activity;
import android.view.View;
import android.view.Menu;
import android.widget.*;
import android.os.Bundle;

public class MainActivity extends AppCompatActivity {
 @Override
 protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main);
 Button b1 = (Button) findViewById(R.id.button1);
 b1.setOnClickListener(new View.OnClickListener() {
 @Override
 public void onClick(View arg0) {
 Toast.makeText(getBaseContext(), "success",
 Toast.LENGTH_LONG).show();
 }
 });
 }
}


2.DEMONSTRATE INTENT EXPLICIT

Activity_main.xml:
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout
 xmlns:android="http://schemas.android.com/apk/res/android"
 xmlns:app="http://schemas.android.com/apk/res-auto"
 xmlns:tools="http://schemas.android.com/tools"
 android:background="@android:color/darker_gray"
 android:layout_width="match_parent"
 android:layout_height="match_parent"
 tools:context=".MainActivity">
 <TextView
 android:id="@+id/textView"
 android:layout_width="137dp"
 android:layout_height="33dp"
 android:fontFamily="sans-serif"
 android:gravity="center_horizontal"
 android:text="INTENT"
 android:textAlignment="center"
 android:textSize="20dp"
 android:textStyle="bold"
 app:layout_constraintBottom_toBottomOf="parent"
 app:layout_constraintHorizontal_bias="0.491"
 app:layout_constraintLeft_toLeftOf="parent"
 app:layout_constraintRight_toRightOf="parent"
app:layout_constraintTop_toTopOf="parent"
 app:layout_constraintVertical_bias="0.227" />
 <Button
 android:id="@+id/btnActivity1"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:layout_marginStart="164dp"
 android:layout_marginLeft="164dp"
 android:layout_marginEnd="148dp"
 android:layout_marginRight="148dp"
 android:text="Next"
 app:layout_constraintBottom_toBottomOf="parent"
 app:layout_constraintEnd_toEndOf="parent"
 app:layout_constraintHorizontal_bias="0.09"
 app:layout_constraintStart_toStartOf="parent"
 app:layout_constraintTop_toTopOf="parent"
 app:layout_constraintVertical_bias="0.459"
 tools:text="Next" />
</androidx.constraintlayout.widget.ConstraintLayout>
Activity_main2.xml:
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout
 xmlns:android="http://schemas.android.com/apk/res/android"
 xmlns:app="http://schemas.android.com/apk/res-auto"
 xmlns:tools="http://schemas.android.com/tools"
 android:background="@color/white"
 android:layout_width="match_parent"
 android:layout_height="match_parent"
 tools:context=".MainActivity2">
 <TextView
 android:id="@+id/textView2"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:layout_marginTop="298dp"
 android:layout_marginBottom="414dp"
 android:text="This is Next Page"
 android:textSize="34dp"
 android:fontFamily="sans-serif"
 android:textAppearance="@style/TextAppearance.AppCompat.Display2"
 app:layout_constraintBottom_toBottomOf="parent"
 app:layout_constraintEnd_toEndOf="parent"
 app:layout_constraintHorizontal_bias="0.572"
 app:layout_constraintStart_toStartOf="parent"
 app:layout_constraintTop_toTopOf="parent"/>
 <TextView
 android:id="@+id/textView"
 android:layout_width="137dp"
 android:layout_height="33dp"
 android:fontFamily="sans-serif"
 android:gravity="center_horizontal"
 android:text="INTENT-2"
 android:textAlignment="center"
 android:textSize="20dp"
 android:textStyle="bold"
 app:layout_constraintBottom_toBottomOf="parent"
 app:layout_constraintHorizontal_bias="0.491"
 app:layout_constraintLeft_toLeftOf="parent"
 app:layout_constraintRight_toRightOf="parent"
 app:layout_constraintTop_toTopOf="parent"
 app:layout_constraintVertical_bias="0.227" />
</androidx.constraintlayout.widget.ConstraintLayout>

MainActivity.java:
package com.example.ex_2;
import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.view.View;
import android.widget.Button;
import android.os.Bundle;
public class MainActivity extends AppCompatActivity {
 @Override
 protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main);
 Button butActivity2 = findViewById(R.id.btnActivity1);
 butActivity2.setOnClickListener(new View.OnClickListener() {
 @Override
 public void onClick(View view) {
 Intent ActivIntent = new
 Intent(MainActivity.this,MainActivity2.class);
 startActivity(ActivIntent);
 }
 });
 }
}

MainActivity2.java:
package com.example.ex2;
import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
public class MainActivity2 extends AppCompatActivity {
 @Override
 protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main2);
 }
}


3.Develop an application for student Registration confirmation 
using intent Explicit

<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
 xmlns:tools="http://schemas.android.com/tools"
 android:layout_width="match_parent"
 android:layout_height="match_parent"
 tools:context=".MainActivity">
 <EditText
 android:id="@+id/editTextName"
 android:layout_width="match_parent"
 android:layout_height="wrap_content"
 android:hint="Name" />
 <EditText
 android:id="@+id/editTextEmail"
 android:layout_width="match_parent"
 android:layout_height="wrap_content"
 android:layout_below="@id/editTextName"
 android:layout_marginTop="84dp"
 android:hint="Email" />
 <Button
 android:id="@+id/buttonRegister"
 android:layout_width="wrap_content"
 android:layout_height="126dp"
 android:layout_below="@id/editTextEmail"
 android:layout_alignParentStart="true"
 android:layout_alignParentEnd="true"
 android:layout_alignParentBottom="true"
 android:layout_marginStart="156dp"
 android:layout_marginTop="277dp"
 android:layout_marginEnd="142dp"
 android:layout_marginBottom="224dp"
 android:text="Register" />
</RelativeLayout>
 Activity_confirmation.xml
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
 xmlns:tools="http://schemas.android.com/tools"
 android:layout_width="match_parent"
 android:layout_height="match_parent"
 tools:context=".ConfirmationActivity">
 <TextView
 android:id="@+id/textViewConfirmation"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:layout_centerInParent="true"
 android:textSize="18sp"
 android:textStyle="bold"/>
</RelativeLayout>


MainActivity.java
package com.example.reg_explicit;
import android.content.Intent;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import androidx.appcompat.app.AppCompatActivity;
public class MainActivity extends AppCompatActivity {
 EditText editTextName, editTextEmail;
 Button buttonRegister;
 @Override
 protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main);
 editTextName = findViewById(R.id.editTextName);
 editTextEmail = findViewById(R.id.editTextEmail);
 buttonRegister = findViewById(R.id.buttonRegister);
 buttonRegister.setOnClickListener(new View.OnClickListener() {
 @Override
 public void onClick(View v) {
 // Get the input from EditText fields
 String name = editTextName.getText().toString();
 String email = editTextEmail.getText().toString();
 Intent intent = new Intent(MainActivity.this, ConfirmationActivity.class);
 // Pass data to ConfirmationActivity
 intent.putExtra("NAME", name);
 intent.putExtra("EMAIL", email);
 startActivity(intent);
 }
 });
 }
}

ConfirmationActivity.java:

package com.example.reg_explicit;
import android.content.Intent;
import android.os.Bundle;
import android.widget.TextView;
import androidx.appcompat.app.AppCompatActivity;
public class ConfirmationActivity extends AppCompatActivity {
 TextView textViewConfirmation = findViewById(R.id.textViewConfirmation);
 @Override
 protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_confirmation);
 Intent intent = getIntent();
 String name = intent.getStringExtra("NAME");
 String email = intent.getStringExtra("EMAIL");
 String confirmationMessage = "Registration confirmed!\nName: " + name + "\nEmail: " + email;
 textViewConfirmation.setText(confirmationMessage);
 }
}


4.NAVIGATE TO DIFFERENT WEBSITES USING INTENT IMPLICIT

<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
 xmlns:tools="http://schemas.android.com/tools"
 android:layout_width="match_parent"
 android:layout_height="match_parent"
 android:padding="8dp"
 tools:context=".MainActivity">
 <Button
 android:layout_width="170dp"
 android:layout_height="54dp"
 android:layout_alignParentStart="true"
 android:layout_alignParentTop="true"
 android:layout_alignParentEnd="true"
 android:layout_alignParentBottom="true"
 android:layout_marginStart="125dp"
 android:layout_marginTop="383dp"
 android:layout_marginEnd="108dp"
 android:layout_marginBottom="286dp"
 android:onClick="GetUrlFromIntent"
 android:text="Go!!"
 tools:ignore="TouchTargetSizeCheck" />
 <EditText
 android:id="@+id/editTextText2"
 android:layout_width="267dp"
 android:layout_height="53dp"
 android:layout_alignParentStart="true"
 android:layout_alignParentTop="true"
 android:layout_alignParentEnd="true"
 android:layout_alignParentBottom="true"
 android:layout_marginStart="81dp"
 android:layout_marginTop="222dp"
 android:layout_marginEnd="55dp"
 android:layout_marginBottom="448dp"
 android:ems="10"
 android:inputType="text"
 android:minHeight="48dp"
 android:hint="Username"
 tools:ignore="TouchTargetSizeCheck" />
 <EditText
 android:id="@+id/editTextText3"
 android:layout_width="262dp"
 android:layout_height="58dp"
 android:layout_alignParentStart="true"
 android:layout_alignParentTop="true"
 android:layout_alignParentEnd="true"
 android:layout_alignParentBottom="true"
 android:layout_marginStart="88dp"
 android:layout_marginTop="283dp"
 android:layout_marginEnd="53dp"
 android:layout_marginBottom="382dp"
 android:ems="10"
 android:inputType="text"
 android:hint="Password" />
</RelativeLayout>

MainActivity.java

package com.example.login;
import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
public class MainActivity extends AppCompatActivity {
 @Override
 protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main);
 
}
 public void GetUrlFromIntent(View view) {
 String url = "http://www.google.com";
 Intent i = new Intent(Intent.ACTION_VIEW);
 i.setData(Uri.parse(url));
 startActivity(i);
 }
}

AndroidManifest.xml:

<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
 xmlns:tools="http://schemas.android.com/tools">
 <uses-permission android:name="android.permission.INTERNET"/>
 <application
 android:allowBackup="true"
 android:dataExtractionRules="@xml/data_extraction_rules"
 android:fullBackupContent="@xml/backup_rules"
 android:icon="@mipmap/ic_launcher"
 android:label="@string/app_name"
 android:roundIcon="@mipmap/ic_launcher_round"
 android:supportsRtl="true"
 android:theme="@style/Theme.Login"
 tools:targetApi="31">
 <activity
 android:name=".MainActivity"
 android:exported="true">
 <intent-filter>
 <action android:name="android.intent.action.MAIN" />
 <category android:name="android.intent.category.LAUNCHER" />
 </intent-filter>
 </activity>
 </application>
</manifest>

5.PASSING MESSAGES FROM ONE ACTIVITY TO ANOTHER USING INTENT.

<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
 xmlns:tools="http://schemas.android.com/tools"
 android:layout_width="match_parent"
 android:layout_height="match_parent"
 tools:context=".MainActivity">
 <EditText
 android:id="@+id/editTextPhone"
 android:layout_width="match_parent"
 android:layout_height="wrap_content"
 android:hint="Phone Number" />
 <EditText
 android:id="@+id/editTextMessage"
 android:layout_width="match_parent"
 android:layout_height="wrap_content"
 android:layout_below="@id/editTextPhone"
 android:hint="Message" />
 <Button
 android:id="@+id/buttonSend"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:layout_below="@id/editTextMessage"
 android:text="Send"
 android:onClick="sendMessage" />
</RelativeLayout>

MainActivity.java
import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.EditText;
import androidx.appcompat.app.AppCompatActivity;
public class MainActivity extends AppCompatActivity {
 private EditText editTextPhone, editTextMessage;
 @Override
 protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main);
 editTextPhone = findViewById(R.id.editTextPhone);
 editTextMessage = findViewById(R.id.editTextMessage);
 }
 public void sendMessage(View view) {
 String phoneNo = editTextPhone.getText().toString();
 String message = editTextMessage.getText().toString();
 Uri uri = Uri.parse("smsto:" + phoneNo);
 Intent intent = new Intent(Intent.ACTION_SENDTO, uri);
 intent.putExtra("sms_body", message);
 startActivity(intent);
 }
}

6.DEMONSTRATE DATE PICKER

MainActivity.java 

package com.example.datepickerexample; 
import androidx.appcompat.app.AppCompatActivity; 
import android.app.DatePickerDialog; 
import android.os.Bundle; 
import android.view.View;
import android.widget.Button;
import android.widget.DatePicker; 
import android.widget.TextView; 
import java.util.Calendar; 
public class MainActivity extends AppCompatActivity { 
private TextView tvSelectedDate; 
private Button btnDatePicker; 
@Override 
protected void onCreate(Bundle savedInstanceState) { 
super.onCreate(savedInstanceState); 
setContentView(R.layout.activity_main); 
tvSelectedDate = findViewById(R.id.tvSelectedDate); 
btnDatePicker = findViewById(R.id.btnDatePicker); 
btnDatePicker.setOnClickListener(new View.OnClickListener() { 
@Override 
public void onClick(View v) { showDatePickerDialog(); 
} }); }
private void showDatePickerDialog() { 
Calendar calendar = Calendar.getInstance(); 
int year = calendar.get(Calendar.YEAR); 
int month = calendar.get(Calendar.MONTH); 
int dayOfMonth = calendar.get(Calendar.DAY_OF_MONTH); 
DatePickerDialog datePickerDialog = new DatePickerDialog( this, new 
DatePickerDialog.OnDateSetListener() {
@Override
public void onDateSet(DatePicker view, int year, int month, int dayOfMonth) { 
String selectedDate = dayOfMonth + "/" + (month + 1) + "/" + year;
tvSelectedDate.setText("Selected Date: " + selectedDate);
} },
year, month, dayOfMonth ); 
datePickerDialog.show();
}
}


7.DEMONSTRATE TIME PICKER

<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout
 xmlns:android="http://schemas.android.com/apk/res/android"
 xmlns:tools="http://schemas.android.com/tools"
 android:id="@+id/idRLContainer"
 android:layout_width="match_parent"
 android:layout_height="match_parent"
 android:orientation="vertical"
 tools:context=".MainActivity">
 <TextView
 android:id="@+id/idTVHeading"
 android:layout_width="match_parent"
 android:layout_height="wrap_content"
 android:layout_above="@id/idTVSelectedTime"
 android:layout_centerInParent="true"
 android:layout_margin="20dp"
 android:gravity="center"
 android:padding="10dp"
 android:text="Time Picker Dialog"
 android:textAlignment="center"
 android:textColor="@color/black"
 android:textSize="20sp"
 android:textStyle="bold" />
 <TextView
 android:id="@+id/idTVSelectedTime"
 android:layout_width="match_parent"
 android:layout_height="wrap_content"
 android:layout_above="@id/idBtnPickTime"
 android:layout_centerInParent="true"
 android:layout_margin="20dp"
 android:gravity="center"
 android:padding="10dp"
 android:text="Time"
 android:textAlignment="center"
 android:textColor="@color/black"
 android:textSize="20sp"
 android:textStyle="bold" />
 <Button
 android:id="@+id/idBtnPickTime"
 android:layout_width="223dp"
 android:layout_height="wrap_content"
 android:layout_centerInParent="true"
 android:layout_marginStart="20dp"
 android:layout_marginLeft="20dp"
 android:layout_marginTop="20dp"
 android:layout_marginEnd="20dp"
 android:layout_marginRight="20dp"
 android:layout_marginBottom="20dp"
 android:text="Pick Time"
 android:textAllCaps="false" />
</RelativeLayout>

MainActivity.java

package com.example.timepick;
import android.app.TimePickerDialog;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;
import android.widget.TimePicker;
import androidx.appcompat.app.AppCompatActivity;
import java.util.Calendar;
public class MainActivity extends AppCompatActivity {
 private Button pickTimeBtn;
 private TextView selectedTimeTV;
 @Override
 protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main);
 pickTimeBtn = findViewById(R.id.idBtnPickTime);
 selectedTimeTV = findViewById(R.id.idTVSelectedTime);
 pickTimeBtn.setOnClickListener(new View.OnClickListener() {
 @Override
 public void onClick(View v) {
 final Calendar c = Calendar.getInstance();
 int hour = c.get(Calendar.HOUR_OF_DAY);
 int minute = c.get(Calendar.MINUTE);
 TimePickerDialog timePickerDialog = new TimePickerDialog(MainActivity.this,
 new TimePickerDialog.OnTimeSetListener() {
 @Override
 public void onTimeSet(TimePicker view, int hourOfDay,
 int minute) {
 selectedTimeTV.setText(hourOfDay + ":" + minute);
 }
 }, hour, minute, false);
 timePickerDialog.show();
 }
 });
 }
}

8.Develop an application for event management using Picker view

<!-- activity_main.xml -->
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
 xmlns:tools="http://schemas.android.com/tools"
 android:layout_width="match_parent"
 android:layout_height="match_parent"
 android:orientation="vertical"
 android:padding="16dp"
 tools:context=".MainActivity">
 <EditText
 android:id="@+id/eventNameEditText"
 android:layout_width="match_parent"
 android:layout_height="wrap_content"
 android:hint="Event Name"
 android:minHeight="48dp" />
 <DatePicker
 android:id="@+id/datePicker"
 android:layout_width="wrap_content"
 android:layout_height="273dp" />
 <TimePicker
 android:id="@+id/timePicker"
 android:layout_width="wrap_content"
 android:layout_height="256dp" />
 <Button
 android:id="@+id/createEventButton"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:text="Create Event" />
</LinearLayout>

MainActivity.java:

package com.example.events;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.DatePicker;
import android.widget.EditText;
import android.widget.TimePicker;
import android.widget.Toast;
import androidx.appcompat.app.AppCompatActivity;
import java.util.Calendar;
public class MainActivity extends AppCompatActivity {
 @Override
 protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main);
 final EditText eventNameEditText = findViewById(R.id.eventNameEditText);
 final DatePicker datePicker = findViewById(R.id.datePicker);
 final TimePicker timePicker = findViewById(R.id.timePicker);
 Button createEventButton = findViewById(R.id.createEventButton);
 createEventButton.setOnClickListener(new View.OnClickListener() {
 @Override
 public void onClick(View v) {
 String eventName = eventNameEditText.getText().toString();
 int year = datePicker.getYear();
 int month = datePicker.getMonth();
 int day = datePicker.getDayOfMonth();
 int hour = timePicker.getHour();
 int minute = timePicker.getMinute();
 Calendar calendar = Calendar.getInstance();
 calendar.set(year, month, day, hour, minute);
 String eventDateTime = calendar.getTime().toString();
 Toast.makeText(MainActivity.this, "Event Name: " + eventName + "\nDate and 
Time: " + eventDateTime, Toast.LENGTH_LONG).show();
 }
 });
 }
}

9.DEMONSTRATE DATA PERSISTENT USING SHARED PREFERENCES

Mainactivity1.java:

package com.example.shar;
import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
public class MainActivity extends AppCompatActivity {
 @Override
 protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main);
 Button butActivity2 = findViewById(R.id.btnActivity1);
 butActivity2.setOnClickListener(new View.OnClickListener() {
 @Override
 public void onClick(View view) {
 Intent ActivIntent = new
 Intent(MainActivity.this, MainActivity2.class);
 startActivity(ActivIntent);
 }
 });
 }
}

MainActivity2.java

package com.example.shar;
import android.content.SharedPreferences;
import android.os.Bundle;
import android.widget.EditText;
import android.widget.TextView;
import androidx.appcompat.app.AppCompatActivity;
public class MainActivity2 extends AppCompatActivity {
 private SharedPreferences sharedPreferences;
 private TextView textView;
 private EditText editText;
 @Override
 protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main);
 textView = findViewById(R.id.textView);
 sharedPreferences = getSharedPreferences("MyPrefs", MODE_PRIVATE);
 if (sharedPreferences.contains("message")) {
 String message = sharedPreferences.getString("message", "");
 textView.setText(message);
 } else {
 textView.setText("No message stored");
 }
 SharedPreferences.Editor editor = sharedPreferences.edit();
 editor.putString("message", "ANDROID-APP-II");
 editor.apply();
 }
}

Activitymain.xml:

<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android"
 xmlns:app="http://schemas.android.com/apk/res-auto"
 xmlns:tools="http://schemas.android.com/tools"
 android:layout_width="match_parent"
 android:layout_height="match_parent"
 tools:context=".MainActivity">
 <Button
 android:id="@+id/btnActivity1"
 android:layout_width="wrap_content"
 android:layout_height="48dp"
 android:layout_marginStart="16dp"
 android:layout_marginTop="32dp"
 android:layout_marginEnd="24dp"
 android:text="Go"
 app:layout_constraintBottom_toBottomOf="parent"
 app:layout_constraintEnd_toEndOf="parent"
 app:layout_constraintHorizontal_bias="0.512"
 app:layout_constraintStart_toStartOf="parent"
 app:layout_constraintTop_toTopOf="parent"
 app:layout_constraintVertical_bias="0.173"
 tools:ignore="HardcodedText" />
 <TextView
 android:id="@+id/textView"
 android:layout_width="245dp"
 android:layout_height="59dp"
 android:layout_marginStart="100dp"
 android:layout_marginEnd="100dp"
 android:text="Name"
 android:textSize="20sp"
 app:layout_constraintBottom_toBottomOf="parent"
 app:layout_constraintEnd_toEndOf="parent"
 app:layout_constraintHorizontal_bias="0.509"
 app:layout_constraintStart_toStartOf="parent"
 app:layout_constraintTop_toTopOf="parent"
 tools:ignore="HardcodedText,TextSizeCheck" />
</androidx.constraintlayout.widget.ConstraintLayout>

Activitymain2.xml:

<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android"
 xmlns:app="http://schemas.android.com/apk/res-auto"
 xmlns:tools="http://schemas.android.com/tools"
 android:layout_width="match_parent"
 android:layout_height="match_parent"
 tools:context=".MainActivity2">
 <TextView
 android:id="@+id/textView"
 android:layout_width="291dp"
 android:layout_height="56dp"
 android:layout_marginStart="100dp"
 android:layout_marginEnd="100dp"
 android:text="Name"
 android:textSize="20dp"
 app:layout_constraintBottom_toBottomOf="parent"
 app:layout_constraintEnd_toEndOf="parent"
 app:layout_constraintHorizontal_bias="0.35"
 app:layout_constraintStart_toStartOf="parent"
 app:layout_constraintTop_toTopOf="parent"
 app:layout_constraintVertical_bias="0.407" />
</androidx.constraintlayout.widget.ConstraintLayout>

10.DEVELOP APPLICATION TO STORE AND RETRIEVE DATA USING FILES

MainActivity.java

import android.content.Context;
import android.os.Bundle;
import android.support.v7.app.AppCompatActivity;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;
import java.io.BufferedReader;
import java.io.FileInputStream;
import java.io.FileOutputStream;
import java.io.InputStreamReader;
public class MainActivity extends AppCompatActivity {
 EditText editText;
 TextView textView;
 Button saveButton;
 private static final String FILE_NAME = "example.txt";
 @Override
 protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main);
 editText = findViewById(R.id.edit_text);
 textView = findViewById(R.id.text_view);
 saveButton = findViewById(R.id.save_button);
 saveButton.setOnClickListener(new View.OnClickListener() {
 @Override
 public void onClick(View v) {
 saveData();
 }
 });
 loadData();
 }
 private void saveData() {
 String text = editText.getText().toString();
 FileOutputStream fos = null;
 try {
 fos = openFileOutput(FILE_NAME, Context.MODE_PRIVATE);
 fos.write(text.getBytes());
 editText.getText().clear();
 textView.setText("Data saved to file.");
 } catch (Exception e) {
 e.printStackTrace();
 } finally {
 try {
 if (fos != null)
 fos.close();
 } catch (Exception e) {
 e.printStackTrace();
 }
 } }
 private void loadData() {
 FileInputStream fis = null;
 try {
 fis = openFileInput(FILE_NAME);
 InputStreamReader isr = new InputStreamReader(fis);
 BufferedReader br = new BufferedReader(isr);
 StringBuilder sb = new StringBuilder();
 String text;
 while ((text = br.readLine()) != null) {
 sb.append(text).append("\n");
 }
 textView.setText(sb.toString());
 } catch (Exception e) {
 e.printStackTrace();
 } finally {
 try {
 if (fis != null)
 fis.close();
 } catch (Exception e) {
 e.printStackTrace();
 }
 }
 }
}

Activity_main.xml

<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
 xmlns:tools="http://schemas.android.com/tools"
 android:layout_width="match_parent"
 android:layout_height="match_parent"
 android:padding="16dp"
 tools:context=".MainActivity">
 <EditText
 android:id="@+id/edit_text"
 android:layout_width="match_parent"
 android:layout_height="wrap_content"
 android:hint="Enter text here"/>
 <Button
 android:id="@+id/save_button"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:layout_below="@id/edit_text"
 android:layout_marginTop="16dp"
 android:text="Save"/>
 <TextView
 android:id="@+id/text_view"
 android:layout_width="match_parent"
 android:layout_height="wrap_content"
 android:layout_below="@id/save_button"
 android:layout_marginTop="16dp"/>
</RelativeLayout>

11.IMPLEMENTATION OF SQLITE IN ANDROID APPLICATION

<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
 xmlns:tools="http://schemas.android.com/tools"
 android:layout_width="match_parent"
 android:layout_height="match_parent"
 android:padding="16dp"
 tools:context=".MainActivity">
 <EditText
 android:id="@+id/editTextName"
 android:layout_width="match_parent"
 android:layout_height="wrap_content"
 android:hint="Enter Name" />
 <EditText
 android:id="@+id/editTextAge"
 android:layout_width="match_parent"
 android:layout_height="wrap_content"
 android:layout_below="@id/editTextName"
 android:layout_marginTop="16dp"
 android:hint="Enter Age"
 android:inputType="number" />
 <Button
 android:id="@+id/buttonAdd"
 android:layout_width="match_parent"
 android:layout_height="wrap_content"
 android:layout_below="@id/editTextAge"
 android:layout_marginTop="16dp"
 android:text="Add Student" />
 <ListView
 android:id="@+id/listViewStudents"
 android:layout_width="match_parent"
 android:layout_height="wrap_content"
 android:layout_below="@id/buttonAdd"
 android:layout_marginTop="16dp" />
</RelativeLayout>

MainActivity.java

import android.content.ContentValues;
import android.database.Cursor;
import android.database.sqlite.SQLiteDatabase;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.ListView;
import android.widget.SimpleCursorAdapter;
import android.widget.Toast;
import androidx.appcompat.app.AppCompatActivity;
public class MainActivity extends AppCompatActivity {
 private EditText editTextName, editTextAge;
 private Button buttonAdd;
 private ListView listViewStudents;
 private DatabaseHelper dbHelper;
 @Override
 protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main);
 editTextName = findViewById(R.id.editTextName);
 editTextAge = findViewById(R.id.editTextAge);
 buttonAdd = findViewById(R.id.buttonAdd);
 listViewStudents = findViewById(R.id.listViewStudents);
 dbHelper = new DatabaseHelper(this);
 buttonAdd.setOnClickListener(new View.OnClickListener() {
 @Override
 public void onClick(View v) {
 String name = editTextName.getText().toString();
 String age = editTextAge.getText().toString();
 if (!name.isEmpty() && !age.isEmpty()) {
 long result = dbHelper.insertData(name, Integer.parseInt(age));
 if (result != -1) {
 Toast.makeText(MainActivity.this, "Student added successfully", 
Toast.LENGTH_SHORT).show();
 displayStudents();
 editTextName.setText("");
 editTextAge.setText("");
 } else {
 Toast.makeText(MainActivity.this, "Failed to add student", 
Toast.LENGTH_SHORT).show();
 }
 } else {
 Toast.makeText(MainActivity.this, "Please enter name and age", 
Toast.LENGTH_SHORT).show();
 }
 }
 })
 displayStudents();
 }
 private void displayStudents() {
 Cursor cursor = dbHelper.getAllData();
 String[] fromColumns = {DatabaseHelper.COL_NAME, DatabaseHelper.COL_AGE};
 int[] toViews = {android.R.id.text1, android.R.id.text2};
 SimpleCursorAdapter adapter = new SimpleCursorAdapter(this,
 android.R.layout.simple_list_item_2, cursor, fromColumns, toViews, 0);
 listViewStudents.setAdapter(adapter);
 }
}

DatabaseHelper.java

import android.content.ContentValues;
import android.content.Context;
import android.database.Cursor;
import android.database.sqlite.SQLiteDatabase;
import android.database.sqlite.SQLiteOpenHelper;
public class DatabaseHelper extends SQLiteOpenHelper {
 private static final String DATABASE_NAME = "students.db";
 private static final int DATABASE_VERSION = 1;
 public static final String TABLE_NAME = "students";
 public static final String COL_ID = "_id";
 public static final String COL_NAME = "name";
 public static final String COL_AGE = "age";
 public DatabaseHelper(Context context) {
 super(context, DATABASE_NAME, null, DATABASE_VERSION);
 }
 @Override
 public void onCreate(SQLiteDatabase db) {
 String createTableQuery = "CREATE TABLE " + TABLE_NAME + " (" +
 COL_ID + " INTEGER PRIMARY KEY AUTOINCREMENT, " +
 COL_NAME + " TEXT, " +
 COL_AGE + " INTEGER)";
 db.execSQL(createTableQuery);
 }
 @Override
 public void onUpgrade(SQLiteDatabase db, int oldVersion, int newVersion) {
 db.execSQL("DROP TABLE IF EXISTS " + TABLE_NAME);
 onCreate(db);
 }
 public long insertData(String name, int age) {
 SQLiteDatabase db = this.getWritableDatabase();
 ContentValues contentValues = new ContentValues();
 contentValues.put(COL_NAME, name);
 contentValues.put(COL_AGE, age);
 return db.insert(TABLE_NAME, null, contentValues);
 }
 public Cursor getAllData() {
 SQLiteDatabase db = this.getReadableDatabase();
 return db.query(TABLE_NAME, null, null, null, null, null, null);
 }
}

12.DEVELOP AN ANDROID APPLICATION FOR SMS MESSAGING

<RelativeLayout 
xmlns:android="http://schemas.android.com/apk/res/android"
 xmlns:tools="http://schemas.android.com/tools"
 android:layout_width="match_parent"
 android:layout_height="match_parent"
 tools:context=".MainActivity">
 <EditText
 android:id="@+id/editTextPhone"
 android:layout_width="match_parent"
 android:layout_height="wrap_content"
 android:hint="Phone Number"/>
 <EditText
 android:id="@+id/editTextMessage"
 android:layout_width="match_parent"
 android:layout_height="wrap_content"
 android:layout_below="@id/editTextPhone"
 android:hint="Message"/>
 <Button
 android:id="@+id/buttonSend"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:layout_below="@id/editTextMessage"
 android:text="Send"/>
</RelativeLayout>

MainActivity.java

package com.example.myapplication;
import android.Manifest;
import android.content.pm.PackageManager; 
import android.os.Bundle;
import android.telephony.SmsManager;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.Toast;
import androidx.appcompat.app.AppCompatActivity;
import androidx.core.app.ActivityCompat;
import androidx.core.content.ContextCompat;
public class MainActivity extends AppCompatActivity {
 private EditText editTextPhone, editTextMessage;
 private Button buttonSend;
 private static final int PERMISSION_REQUEST_CODE = 1;
 @Override
 protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main);
 editTextPhone = findViewById(R.id.editTextPhone);
 editTextMessage = findViewById(R.id.editTextMessage);
 buttonSend = findViewById(R.id.buttonSend);
 buttonSend.setOnClickListener(new View.OnClickListener() {
 @Override
 public void onClick(View v) {
 if (checkPermission()) {
 sendSMS();
 } else {
 requestPermission();
 }
 }
 });
 }
 private void requestPermission() {
 ActivityCompat.requestPermissions(this, new 
String[]{Manifest.permission.SEND_SMS}, PERMISSION_REQUEST_CODE);
 }
 private boolean checkPermission() {
 int result = ContextCompat.checkSelfPermission(getApplicationContext(), 
Manifest.permission.SEND_SMS);
 return result == PackageManager.PERMISSION_GRANTED;
 }
 private void sendSMS() {
 String phoneNo = editTextPhone.getText().toString();
 String message = editTextMessage.getText().toString();
 try {
 SmsManager smsManager = SmsManager.getDefault();
 smsManager.sendTextMessage(phoneNo, null, message, null, null);
 Toast.makeText(getApplicationContext(), "SMS sent successfully", 
Toast.LENGTH_LONG).show();
 } catch (Exception ex) {
 Toast.makeText(getApplicationContext(), "SMS sending failed", 
Toast.LENGTH_LONG).show();
 ex.printStackTrace();
 }
 }
 @Override
 public void onRequestPermissionsResult(int requestCode, String permissions[], int[] 
grantResults) {
 super.onRequestPermissionsResult(requestCode, permissions, grantResults);
 switch (requestCode) {
 case PERMISSION_REQUEST_CODE: {
 if (grantResults.length > 0 && grantResults[0] == 
PackageManager.PERMISSION_GRANTED) {
 sendSMS();
 } else {
 Toast.makeText(getApplicationContext(), "Permission denied", 
Toast.LENGTH_LONG).show();
 }
 }
 }
 }
}

AndroidManifest.xml:

<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
 xmlns:tools="http://schemas.android.com/tools">
 <uses-feature
 android:name="android.hardware.telephony"
 android:required="false" />
 <uses-permission android:name="android.permission.SEND_SMS">
 </uses-permission>
 <application
 android:allowBackup="true"
 android:dataExtractionRules="@xml/data_extraction_rules"
 android:fullBackupContent="@xml/backup_rules"
 android:icon="@mipmap/ic_launcher"
 android:label="@string/app_name"
 android:roundIcon="@mipmap/ic_launcher_round"
 android:supportsRtl="true"
 android:theme="@style/Theme.MyApplication"
 tools:targetApi="31">
 <activity
 android:name=".MainActivity"
 android:exported="true">
 <intent-filter>
 <action android:name="android.intent.action.MAIN" />
 <category android:name="android.intent.category.LAUNCHER" />
 </intent-filter>
 </activity>
 </application>
</manifest>

13.DEVELOP AN APPLICATION USING VARIOUS BASIC VIEW

<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
 xmlns:tools="http://schemas.android.com/tools"
 android:layout_width="match_parent"
 android:layout_height="match_parent"
 android:padding="16dp"
 tools:context=".MainActivity">
 <TextView
 android:id="@+id/textView"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:text="Hello, World!"
 android:textSize="24sp"
 android:layout_centerHorizontal="true"
 android:layout_marginTop="32dp"/>
 <EditText
 android:id="@+id/editText"
 android:layout_width="match_parent"
 android:layout_height="wrap_content"
 android:layout_below="@id/textView"
 android:layout_marginTop="16dp"
 android:hint="Enter your name"
 android:minHeight="48dp" />
 <Button
 android:id="@+id/button"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:text="Click Me"
 android:layout_below="@id/editText"
 android:layout_centerHorizontal="true"
 android:layout_marginTop="16dp"/>
 <ImageView
 android:id="@+id/imageView"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:src="@drawable/ic_launcher_foreground"
 android:layout_below="@id/button"
 android:layout_centerHorizontal="true"
 android:layout_marginTop="16dp"/>
 <CheckBox
 android:id="@+id/checkBox"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:text="I agree to the terms and conditions"
 android:layout_below="@id/imageView"
 android:layout_centerHorizontal="true"
 android:layout_marginTop="16dp"/>
</RelativeLayout>

MainActivity.java:

package com.example.basicviewsapp;
import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.CheckBox;
import android.widget.EditText;
import android.widget.Toast;
public class MainActivity extends AppCompatActivity {
 @Override
 protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main);
 final EditText editText = findViewById(R.id.editText);
 Button button = findViewById(R.id.button);
 final CheckBox checkBox = findViewById(R.id.checkBox);
 button.setOnClickListener(new View.OnClickListener() {
 @Override
 public void onClick(View v) {
 String name = editText.getText().toString();
 if (!name.isEmpty()) {
 Toast.makeText(MainActivity.this, "Hello, " + name + "!", 
Toast.LENGTH_SHORT).show();
 } else {
 Toast.makeText(MainActivity.this, "Please enter your name", 
Toast.LENGTH_SHORT).show();
 }
 }
 });
 checkBox.setOnClickListener(new View.OnClickListener() {
 @Override
 public void onClick(View v) {
 if (checkBox.isChecked()) {
 Toast.makeText(MainActivity.this, "Checkbox checked", 
Toast.LENGTH_SHORT).show();
 } else {
 Toast.makeText(MainActivity.this, "Checkbox unchecked", 
Toast.LENGTH_SHORT).show();
 }
 }
 });
 }
}

14.IMPLEMENTATION OF LIST VIEW AND SCROLL VIEW

<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
 android:layout_width="match_parent"
 android:layout_height="match_parent">
 <ScrollView
 android:layout_width="match_parent"
 android:layout_height="match_parent"
 android:layout_alignParentStart="true"
 android:layout_alignParentTop="true"
 android:layout_alignParentEnd="true"
 android:layout_alignParentBottom="true"
 android:layout_marginStart="-5dp"
 android:layout_marginTop="140dp"
 android:layout_marginEnd="5dp"
 android:layout_marginBottom="-140dp">
 <LinearLayout
 android:layout_width="match_parent"
 android:layout_height="wrap_content"
 android:orientation="vertical">
 <ListView
 android:id="@+id/list_view"
 android:layout_width="match_parent"
 android:layout_height="285dp" />
 </LinearLayout>
 </ScrollView>
</RelativeLayout>

List_item.xml:

<?xml version="1.0" encoding="utf-8"?>
<TextView xmlns:android="http://schemas.android.com/apk/res/android"
 android:id="@+id/text_view"
 android:layout_width="match_parent"
 android:layout_height="wrap_content"
 android:padding="16dp"
 android:textSize="16sp" />
 
MainActivity.java:

package com.example.scrollv;
import android.app.Activity;
import android.os.Bundle;
import android.widget.ArrayAdapter;
import android.widget.ListView;
public class MainActivity extends Activity {
 @Override
 protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main);
 ListView listView = findViewById(R.id.list_view);
 String[] data = new String[]{"Item 1", "Item 2", "Item 3", "Item 4", "Item 5", "Item 6", 
"Item 7", "Item 8", "Item 9", "Item 10"};
 ArrayAdapter<String> adapter = new ArrayAdapter<>(this, R.layout.list_item, 
R.id.text_view, data);
 listView.setAdapter(adapter);
 }
}








