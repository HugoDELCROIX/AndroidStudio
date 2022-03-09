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

