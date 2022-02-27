# Create an app as shown in the image below. When the Button is pressed the text from the EditText should be displayed in the TextView. Hint: Use setText() and getText().

```java
@Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Log.v("TAG","test");

        Button button = findViewById(R.id.button3);
        TextView text = findViewById(R.id.textView1);
        TextView text2 = findViewById(R.id.textView2);

        button.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                text.setText(text2.getText());
            }
        });
    }
```
___
# Create an app with two buttons and a ProgressBar. One button should increment the ProgressBar and one should decrement it. HINT: Use setProgress().

```java
@Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Log.v("TAG","test");

        ProgressBar progressBar = findViewById(R.id.determinateBar);


        Button buttonPlus = findViewById(R.id.buttonPlus);
        Button buttonMinus = findViewById(R.id.buttonMinus);
        int i = 0;

        buttonMinus.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                progressBar.incrementProgressBy(-10);
            }
        });

        buttonPlus.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                progressBar.incrementProgressBy(10);
            }
        });
    }
```
___
# Create a login screen with an email and password field, as well as a login button. The Button should create a welcoming Toast if the login information was:
1. Email: user@email.com
2. Password: ILOVEAND

```java
@Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Log.v("TAG","test");

        Button login = findViewById(R.id.login);
        TextView username = findViewById(R.id.username);
        TextView password = findViewById(R.id.password);


        login.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                if(username.getText().toString().equals("user@email.com") && password.getText().toString().equals("ILOVEAND")){
                    Context context = getApplicationContext();
                    Toast loggedIn = Toast.makeText(context, "Logged in",Toast.LENGTH_LONG);
                    loggedIn.show();
                }
            }
        });
    }
```
___
# Create a new String resource in the values folder with the value "AND IS AWESOME". Create two TextViews in your layout and use this String resource in both of them. Then give the TextViews a background color, that you define in colors.xml.

```java
@Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Log.v("TAG","test");

        TextView a = findViewById(R.id.textView3);
        TextView b = findViewById(R.id.textView4);

        a.setText(R.string.string1);
        b.setText(R.string.string1);
    }
```

___

# Make an ImageView change between two images using a Switch.
```java
@Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Log.v("TAG","test");

        ImageView image1 = findViewById(R.id.imageView);
        Switch simpleSwitch = findViewById(R.id.switch1);
        image1.setImageResource(R.drawable.ic_launcher_foreground);
        simpleSwitch.setChecked(false);

        simpleSwitch.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                if (simpleSwitch.isChecked()==true){
                    image1.setImageResource(R.drawable.ic_launcher_background);
                } else {
                    image1.setImageResource(R.drawable.ic_launcher_foreground);
                }
            }
        });
    }
```
___

# Create an Activity that uses two different layouts depending on whether it is in landscape or portrait mode.

```java
@Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);

        if (getResources().getConfiguration().orientation == Configuration.ORIENTATION_PORTRAIT){
            setContentView(R.layout.activity_main);
        } else {
            setContentView(R.layout.activity_main_land);
        }
```
___

# Create a new style for an app which contains TextViews. The style should define the size, color, font and style of the text, as well as making it all CAPS.
```xml
<resources>
    <style name="style_test">
        <item name="android:gravity">center</item>
        <item name="textAllCaps">true</item>
        <item name="android:textSize">50sp</item>
        <item name="android:fontFamily">sans-serif-black</item>
        <item name="android:textColor">#fff</item>
    </style>
</resources>
```

___

# Create a theme with new colors for the app- and status bar. Apply it to the main Activity.

```xml
<resources xmlns:tools="http://schemas.android.com/tools">
    <!-- Base application theme. -->
    <style name="Theme.WeatherApp" parent="Theme.MaterialComponents.DayNight.DarkActionBar">
        <!-- Primary brand color. -->
        <item name="colorPrimary">@color/purple_500</item>
        <item name="colorPrimaryVariant">@color/purple_700</item>
        <item name="colorOnPrimary">@color/white</item>
        <!-- Secondary brand color. -->
        <item name="colorSecondary">@color/teal_200</item>
        <item name="colorSecondaryVariant">@color/teal_700</item>
        <item name="colorOnSecondary">@color/black</item>
        <!-- Status bar color. -->
        <item name="android:statusBarColor" tools:targetApi="l">?attr/colorPrimaryVariant</item>
        <!-- Customize your theme here. -->
    </style>
</resources>
```

___

# Create a calculator, that can add numbers together. It can be as simple as two EditText fields and a Button, or as complex as the image below - your choice.

<p align="center">
  <img width="200" height="auto" src="https://kasperknop.github.io/codelabs/interaction/img//68c94ac4f53a2079.png">
</p>

```java

```




