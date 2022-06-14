Flex box advanced layout:

1. There are three sections: navbar, header and boxes

Inside each of these div classes, we have added a div class container too. 

2. navbar has a logo and 3 list items, header has an image, heading and paragraph and finally, the boxes has three boxes with their own heading and paragraph. 

Point of interest:

        <div class="container">
            <div> <h1>Flexbox</h1> 
            <p>This is a practice Flexbox layout (with help from Brad Traversy's video)</p>
            </div>
            <img src="./grid.svg" alt="">
        </div>
    
Here, so that h1 and p are not considered separate items, they are put within <div> </div>, so that one item is h1+p and the other item is img 

It will make it easier to align them horizontally, without p setting up horizontally besides h1 (as we want it below h1)


3. To start with the CSS we add:
* {
    box-sizing: border-box;
    margin: 0px;
    padding: 0px;
}

And we customize the body to add font family, color, background image, and font size. 

4. Similarly img, h1 and h2 are customized too. 

To note, we also edit the items (ul) by removing its list styling, with:
list-style-type: none

5. Then we add container, and to make it responsive (when the browser is sized)

.container {
    max-width: 1100px;
    margin: 0 auto;
    padding: 0 25px; 
}

6. Now, we start with navbar section:

.navbar {
    background-color: #3474e6;
    color: white;
    height: 40 px;
}

This is done to set a different background color for this section. Additionally setting the color of the text and height. 

.logo {
    font-size: x-large;
    color: white;
    font-weight: bolder;
}

This is done to customize the logo text

a {
    color: white;
    text-decoration: none;
    font-weight: bolder;
    font-size: large;
}

This is done to customize the list item text

.navbar a:hover {
    color: lightblue;
}

To add a different color to the list item, when you hover your mouse over it

Flexbox part: 

.navbar .container{
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 100%;
}

We add this to make the elements in row, set the space-between to keep them apart, and set them to be in the center (height-wise)

.navbar ul {
    display: flex;
    margin: 20px;
}

We add this to make the list items in row. 


.navbar li {
    margin-left: 20px;
}

IMPORTANT: this is how we add space between the three list items, by adding a margin to their left. 

---------------------------

Starting with the header section:

.header {
    background-color: #0151cc;
    color: white;
    min-height: 400px;
}

customizing the header section

.header h1 {
    font-size: 3rem;
    font-weight: bold;
}
.header p {
    font-size: large;
    font-weight: bold;
}

.header img {
    max-width: 400px;
}

customizing the header elements

Flexbox part:

.header .container {
    display: flex;
    align-items: center;
    justify-content: space-between;
}

Here we add the display: flex, it sets the heading-para element and img in row orientation, align-items: puts them in center of cross axis and justify-content add space-between them 

---------------------------

Starting with boxes:

.boxes .container {
    display: flex;
    justify-content: space-around;
    align-items: flex-start;
}

Quite a simple flexbox here, just set the display: flex, to set the orientation horizontal (as all boxes are divided) and setting space around them.

.box {
    background-color: #0a51cc;
    color: white;
    margin: 20px 30px;
    border-radius: 10px;
    box-shadow: 0 3px 5px rgb(65, 61, 61);
    padding: 10px 10px;
}

customizing the boxes, by adding background color, text color, setting the margin (so it can be boxed), setting border radius for making its corner rounded, setting box shadow for a better affect and setting padding so the text within the boxes don't touch the edges. 





