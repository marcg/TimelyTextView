TimelyTextView
==============

Animated TextView like Timely app

Intital commit for Animated TextView present in the Timely(Alarm) App.
This is just an addition to the concept explained by Sriram Ramani here : http://sriramramani.wordpress.com/2013/10/14/number-tweening/

I have just figured out missing bits & pieces and made a simple library out of it. Please thank Sriram if this helped you. Also please note I have been very busy and this was the outcome  of just 2hrs of work on a lazy Monday afternoon, so there might be a few bugs. It would be great if anyone else wants to contribute and take this to the next level. Have a few ideas in mind already, feel free to get in touch and send Pull Requests.


Usage :

XML Layout -

        <com.example.timelytextview.NumberView  xmlns:app="http://schemas.android.com/apk/res-auto"
                android:id="@+id/textView1"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:textSize="40sp"
                android:textAppearance="?android:attr/textAppearanceLarge" 
                app:animate="once" 
                app:count="down"
           />
   

Java -

         public class MainActivity extends Activity {
         NumberView mNumView;
                   @Override
                   protected void onCreate(Bundle savedInstanceState) {
                         super.onCreate(savedInstanceState);
                         setContentView(R.layout.activity_main);
                         mNumView = (NumberView) findViewById(R.id.textView1);
                         mNumView.setAnimationType("loop");
                         mNumView.setCountType("up");
                   }
        }

        

The animate and count parameters control the looping and counter. 

animate = once, loop (loop will make the numbers count infintely in a loop from 0-9, once would count only once)

count = up, down (up will count the numbers from 0-9 while down will count from 9-0)



P.S : I suck at UI and animations and don't really know much, so if there are any bugs/performance issues I am to blame. Feel free to point them out to me so that I can fix them. It would be even better if you fix them ! 
