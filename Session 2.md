# Create an app as shown in the image below. When the Button is pressed the text from the EditText should be displayed in the TextView. Hint: Use setText() and getText().

```
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

# Create an app with two buttons and a ProgressBar. One button should increment the ProgressBar and one should decrement it. HINT: Use setProgress().

```
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
    
# Create a login screen with an email and password field, as well as a login button. The Button should create a welcoming Toast if the login information was:
1. Email: user@email.com
2. Password: ILOVEAND

```
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

# Create a new String resource in the values folder with the value "AND IS AWESOME". Create two TextViews in your layout and use this String resource in both of them. Then give the TextViews a background color, that you define in colors.xml.

```
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
