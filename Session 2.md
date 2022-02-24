# Create an app as shown in the image below. When the Button is pressed the text from the EditText should be displayed in the TextView. Hint: Use setText() and getText().
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

# Create an app with two buttons and a ProgressBar. One button should increment the ProgressBar and one should decrement it. HINT: Use setProgress().
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
