# Create an app which displays a Button. Clicking the Button should send an explicit Intent to start a new Activity within the app.

```java
@Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Log.v("TAG","test");

        Button button = findViewById(R.id.button);
        Intent intent = new Intent(this,MainActivity2.class);

        button.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                startActivity(intent);
            }
        });
    }
```
___
# Extend your app from the previous exercise to also send data along with the Intent, gathered from an EditText field. Have the second Activity retrieve this data and display it on the screen.

### MainActivity
```java
public class MainActivity extends AppCompatActivity {
    public static final String EXTRA_TEXT = "com.example.application.example.EXTRA_TEXT";

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Log.v("TAG","test");

        Button button = findViewById(R.id.button);

        button.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                openActivity();
            }
        });
    }
    public void openActivity(){
        EditText edit = findViewById(R.id.edittext);
        Intent intent = new Intent(this,MainActivity2.class);

        intent.putExtra(EXTRA_TEXT, edit.getText().toString());
        startActivity(intent);

    }

}
```
### MainActivity2
```java
public class MainActivity2 extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main2);

        Intent intent = getIntent();
        String text = intent.getStringExtra(MainActivity.EXTRA_TEXT);

        TextView textview = findViewById(R.id.textView);
        textview.setText(text);

    }
}
```
___