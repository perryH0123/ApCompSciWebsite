<div class="progress-container">
    <div class="progress-bar" id="progressBar"></div>
 </div>

# Perry Han
Welcome to my site!

Here, you'll find a small listing of my personal attributes.

---

<button onclick="topFunction()" id="topButton" title="Go to top">Back to top</button>
<div id="debug"><p id="debugText">0</p></div>

## Languages

- English
- Chinese
- Japanese (owo)
- Bad handwriting
- HTML
- CSS
- Markdown
- Whitney Student
- Javascript
- degen :\|
- Python
- Robot 🤖
- Java
- I need to learn JQuery 😔 dont look at the inline js

### Here's an example of some of my messy and jank code!
``` java
class Utilities {
public static ArrayList<Product> toProductArrayList(Product[] arr){
    /*List<Product> list = new ArrayList<Product>(Arrays.asList(arr));*/
    ArrayList<Product> arrList = new ArrayList<Product>();
    //I changed the for each loop to a standard for loop since it was giving me a for issues and flooding the array with null
    for (int i = 0; i < arr.length; i++){
      arrList.add(arr[i]);
    }
    return arrList;

  }

  public static double roundToHundreths(double input){
    input *= 100;
    input = Math.floor(input);
    input /= 100;
    return input;
  }
 }
```

For more details see [the full project](https://replit.com/@PerryHan/Store-Finished#Main.java).

## Some of my favorite things

- Not enough sleep
- Coding
- Bad graphic design
- Video editing
- Being bad at video games and subsequently having anger management problems

## Some images (to fulfill the grading requriements)

![Random Smiling Guy](/assets/images/istockphoto-1158245623-612x612.jpg)

![Great yearbook picture](/assets/images/image0.JPG)

<br>
## Checklist of stuff left to do

- [x] A clear topic
- [x] Two images
- [x] Two headings
- [x] Link to another webpage
- [x] Modify CSS  
- [ ] Add JS elements

<button onclick="resetColorScheme()" id="resetColors" title="Reset original page color scheme">Reset original page color scheme</button>

<style>
  #topButton{
      display: block;
      opacity: 0;
      position: fixed; /* Fixed/sticky position */
      bottom: 20px; /* Place the button at the bottom of the page */
      right: 30px; /* Place the button 30px from the right */
      z-index: 99; /* Make sure it does not overlap */
      border: none; /* Remove borders */
      outline: none; /* Remove outline */
      background-color: #808080;
      color: white; /* Text color */
      cursor: pointer; /* Add a mouse pointer on hover */
      padding: 15px; /* Some padding */
      border-radius: 5px; /* Rounded corners */
      font-size: 18px; /* Increase font size */
      transition: opacity 0.5s linear, background-color 0.5s linear, font-color 0.5s linear;
    }
    
  #debug {
        display: none;
        position: fixed;
        bottom: 20px;
        left: 20px;
        z-index: 99;
        border: 1px solid black;
    }
  
    #topButton:hover {
      background-color: #404040; /* Add a dark-grey background on hover */
      font-color: #ffffff;
    }
  
    .progress-container {
      display: block;
      padding-left: 0px;
      padding-right: 0px;
      left: 0px
      margin-right: 0px;
      display: block;
      z-index: 98;
      position: fixed;
      bottom: 0px;
      width: 100%;
      height: 8px;
      background: #fff;
    }
  
    .progress-bar {
      display: block;
      position: fixed;
      padding-left: 0px;
      padding-right: 0px;
      left: 0px;
      margin-right: 0px;
      height: 8px;
      background: #34bfed;
      width: 0%;
    
     #resetColors {
        width: 50%;
        margin: auto;
        background: #adadad;
        border-radius: 5px;
        cursor: pointer;
        transition: background-color 0.5s linear; 
     }
    
     #resetColors:hover {
        background: #636363;
     }
  
</style>
<script>
    const topBtn = document.getElementById("topButton");
    const debugText = document.getElementById("debugText");
    
    const sleep = miliseconds => {
        const currentTime = new Date().getTime();

        while (currentTime + miliseconds >= new Date().getTime()) {
        }
    }
    
    const updateDebugText = () => debugText.innerHTML = (document.documentElement.scrollTop);

    // When the user scrolls down 20px from the top of the document, show the button
    window.onscroll = function() {scrollFunction(); updateProgress()};

    const scrollFunction = () => {
      if (document.body.scrollTop > 20 || document.documentElement.scrollTop > 20) {
        topBtn.style.opacity = 0.8;
      } else {
        topBtn.style.opacity = 0;
      }
    }

    // When the user clicks on the button, scroll to the top of the document
    const topFunction = () => {
      document.body.scrollTop = 0; // For Safari
      document.documentElement.scrollTop = 0; // For Chrome, Firefox, IE and Opera
    }
  
    const updateProgress = () => {
      const winScroll = document.body.scrollTop || document.documentElement.scrollTop;
      const height = document.documentElement.scrollHeight - document.documentElement.clientHeight;
      const scrolled = (winScroll / height) * 100;
      document.getElementById("progressBar").style.width = scrolled + "%";    
    
      document.getElementById("debugText").innerHTML = scrolled;
          
    }
    
    
    
    const pageScroll = () => {
        window.scrollBy(0,1);
        scrolldelay = setTimeout(pageScroll,10);
     }
    
    const reversePageScroll = (_callback) => {
        const height = document.documentElement.scrollHeight - document.documentElement.clientHeight;
        window.scrollBy(0,-3);
        let scrollTracker = (document.body.scrollTop) ? document.body.scrollTop : document.documentElement.scrollTop;
    
        let timer = setTimeout(reversePageScroll,1);
        if ((scrollTracker/height) < 0.01){
            if (timer){
                clearTimeout(timer);
                timer = 0;
            }
            if (_callback) _callback();
        }
        
    }
    
    const resetColorScheme = () => {
        const colorBtn = document.getElementById("resetColors");
        //const audio = new Audio('audio_file.mp3');
        //audio.play();
        colorBtn.innerHTML = "おまえは もう しんでる"
        sleep(2000);
        const height = document.documentElement.scrollHeight - document.documentElement.clientHeight;
        console.log(height);
        
        /*const setColor = (className, displayValue) => {
            const elements = document.getElementsByClassName(className);
            for (i=0; i<items.length; i++){
                elements[i].style.display = displayValue;
            }          
          }*/
         const changeColors = () => {
             const pageHeader = document.getElementsByClassName("page-header");
             for(i=0; i<pageHeader.length; i++){
                pageHeader[i].style.transition = "background-color 3s linear, background-image 3s linear";
                pageHeader[i].style.backgroundColor = "#159957";
                pageHeader[i].style.backgroundImage = "linear-gradient(120deg, #155799, #159957)";
             }

            const headings = document.querySelectorAll("h1, h2, h3, h4, h5, h6");
            for(j=0; j<headings.length; j++){
                if (headings[j].cName != "project-name" || headings[j].cName != "project-tagline"){
                    headings[i].style.transition = "color 3s linear";
                    headings[j].style.color = "#159957";
                }
            }
        }
          reversePageScroll(changeColors);
        
        //alert("work in progress");
     }
 
</script>
