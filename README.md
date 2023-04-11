# TestApp

There are 4 types of Dialogue boxes in Android studio.

1.Alert Dialog

2.DataPicker Dialog

3.TimePicker Dialog

4.Progress Dialog

I included AlertDialogue in this APP.

APP : Opens with a screen that displays 5 questions where you should be clicking on each question number, you will be displayed with a dialogue box which includes multiplechoice questions.

you should select the desired answers and you can submit.

If you want to exit from the app you can see an EXIT button on the screen(when you click on it) - An dialog box will open(click on ok).

    class MainActivity : AppCompatActivity() {

    lateinit var binding: ActivityMainBinding

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        binding = ActivityMainBinding.inflate(layoutInflater)
        setContentView(binding.root)

        supportActionBar?.hide()

        binding.tv1.setOnClickListener {
            val options = arrayOf("C", "Java", "python",)
            val builder2 = AlertDialog.Builder(this)
            builder2.setTitle("Which is your favourite programming language?")
            builder2.setSingleChoiceItems(
                options,
                0,
                DialogInterface.OnClickListener { dialog, which ->
                    // what action should be performed when user clicks on any option
                    Toast.makeText(this, "You clicked on ${options[which]}", Toast.LENGTH_SHORT)
                        .show()
                })
            builder2.setPositiveButton(
                "Submit",
                DialogInterface.OnClickListener { dialogInterface, i ->
                    // WHat action should be performed when Yes is clicked ?
                })
            builder2.setNegativeButton(
                "Decline",
                DialogInterface.OnClickListener { dialogInterface, i ->
                    //  WHat action should be performed when Yes is clicked ?
                })
            builder2.show()
        }
        binding.tv2.setOnClickListener {
            val options = arrayOf("Android development", "Web development", "Machine learning","Data science")
            val builder2 = AlertDialog.Builder(this)
            builder2.setTitle("You are intrested in ?")
            builder2.setMultiChoiceItems(
                options,
                null,
                DialogInterface.OnMultiChoiceClickListener { dialog, which, isChecked ->
                    Toast.makeText(this, "You clicked on ${options[which]}", Toast.LENGTH_SHORT)
                        .show()
                })

            builder2.setPositiveButton(
                "Submit",
                DialogInterface.OnClickListener { dialogInterface, i ->
                    // WHat action should be performed when Yes is clicked ?
                })
            builder2.setNegativeButton(
                "Decline",
                DialogInterface.OnClickListener { dialogInterface, i ->
                    //  WHat action should be performed when Yes is clicked ?
                })
            builder2.show()
        }
        binding.tv3.setOnClickListener {
            val options = arrayOf("InterviewBit", "CodeChef", "LeetCode","HackerRank")
            val builder2 = AlertDialog.Builder(this)
            builder2.setTitle("Which Platform do you mostly use ?")
            builder2.setSingleChoiceItems(
                options,
                0,
                DialogInterface.OnClickListener { dialog, which ->
                    // what action should be performed when user clicks on any option
                    Toast.makeText(this, "You clicked on ${options[which]}", Toast.LENGTH_SHORT)
                        .show()
                })
            builder2.setPositiveButton(
                "Submit",
                DialogInterface.OnClickListener { dialogInterface, i ->
                    // WHat action should be performed when Yes is clicked ?
                })
            builder2.setNegativeButton(
                "Decline",
                DialogInterface.OnClickListener { dialogInterface, i ->
                    //  WHat action should be performed when Yes is clicked ?
                })
            builder2.show()
        }
        binding.tv4.setOnClickListener {
            val options = arrayOf("OpenAI ChatGPT", "Google Bard", "MicroSoft Bing","None")
            val builder2 = AlertDialog.Builder(this)
            builder2.setTitle("Which AI bot do you use ? ")
            builder2.setSingleChoiceItems(
                options,
                0,
                DialogInterface.OnClickListener { dialog, which ->
                    // what action should be performed when user clicks on any option
                    Toast.makeText(this, "You clicked on ${options[which]}", Toast.LENGTH_SHORT)
                        .show()
                })
            builder2.setPositiveButton(
                "Submit",
                DialogInterface.OnClickListener { dialogInterface, i ->
                    // WHat action should be performed when Yes is clicked ?
                })
            builder2.setNegativeButton(
                "Decline",
                DialogInterface.OnClickListener { dialogInterface, i ->
                    //  WHat action should be performed when Yes is clicked ?
                })
            builder2.show()
        }
        binding.tv5.setOnClickListener {
            val options = arrayOf("Arya", "Aryan", "AryanShivva",)
            val builder2 = AlertDialog.Builder(this)
            builder2.setTitle("Who created this app ?")
            builder2.setSingleChoiceItems(
                options,
                0,
                DialogInterface.OnClickListener { dialog, which ->
                    // what action should be performed when user clicks on any option
                    Toast.makeText(this, "You clicked on ${options[which]}", Toast.LENGTH_SHORT)
                        .show()
                })
            builder2.setPositiveButton(
                "Submit",
                DialogInterface.OnClickListener { dialogInterface, i ->
                    // WHat action should be performed when Yes is clicked ?
                })
            builder2.setNegativeButton(
                "Decline",
                DialogInterface.OnClickListener { dialogInterface, i ->
                    //  WHat action should be performed when Yes is clicked ?
                })
            builder2.show()
        }

        binding.button.setOnClickListener {

            val builder1 = AlertDialog.Builder(this)
            builder1.setTitle("Are you Sure?")
            builder1.setMessage("Do you want to close the App")
            builder1.setIcon(R.drawable.baseline_exit_to_app_24)
            builder1.setPositiveButton(
                "Yes",
                DialogInterface.OnClickListener { dialogInterface, i ->
                    // WHat action should be performed when Yes is clicked ?
                    finish()
                })
            builder1.setNegativeButton("No", DialogInterface.OnClickListener { dialogInterface, i ->
                //  WHat action should be performed when Yes is clicked ?
            })
            builder1.show()
        }
    
