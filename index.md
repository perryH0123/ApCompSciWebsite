# Perry Han
Welcome to my site!

Here, you'll find a small listing of my personal attributes.

---

<button onclick="topFunction()" id="topButton" title="Go to top">Back to top</button>
<style>
  #topButton {
      display: block; /* Hidden by default */
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
      transition-property: opacity;
      transition-duration: 0.5s;
    }
  
    #topButton:hover {
      background-color: #555; /* Add a dark-grey background on hover */
      font-color: #ffffff;
    }
</style>
<script>
    topBtn = document.getElementById("topButton");

    // When the user scrolls down 20px from the top of the document, show the button
    window.onscroll = function() {scrollFunction()};

    const scrollFunction = () => {
      if (document.body.scrollTop > 20 || document.documentElement.scrollTop > 20) {
        topBtn.style.opacity = 0.6;
      } else {
        topBtn.style.opacity = 0;
      }
    }

    // When the user clicks on the button, scroll to the top of the document
    const topFunction = () => {
      document.body.scrollTop = 0; // For Safari
      document.documentElement.scrollTop = 0; // For Chrome, Firefox, IE and Opera
    }
</script>

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
- Python
- Robot 🤖
- Java

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

![Pretty Sky](/assets/images/IMG-4661.jpg)

<br>
## Checklist of stuff left to do

- [x] A clear topic
- [x] Two images
- [x] Two headings
- [x] Link to another webpage
- [x] Modify CSS  
