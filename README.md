Private Portfolio
=========================

By Edgardo Lopez
-------------------------

## Table of Contents
==============================
*   [The Purpose](#the-purpose)
*   [Critera](#criteria)
*   [Installation](#installation)
*   [Usage](#usage)
*   [The Process](#the-process)
*   [What Was Done Differently](#differently)
*   [Built With](#built-with)
*   [Contributing](#contributing)
*   [Project Status](#project-status)
*   [Disclaimer](#disclaimer)
*   [Website](#website)
==============================

#   [The Purpose](#the-purpose)

There are two purposes:  One, to show my personal portfolio for the others to see when introducing myself.  Two, to contribute on a more public usage by showing how the portfolio was made to aid those making their own portfolio.

#   [Critera](#criteria)

    CRITERIA:

    GIVEN I need to sample a potential employee's previous work

    WHEN I load their portfolio
    THEN I am presented with the developer's name, a recent photo or avatar, and links to sections about them, their work, and how to contact them

    WHEN I click one of the links in the navigation
    THEN the UI scrolls to the corresponding section

    WHEN I click on the link to the section about their work
    THEN the UI scrolls to a section with titled images of the developer's applications

    WHEN I am presented with the developer's first application
    THEN that application's image should be larger in size than the others

    WHEN I click on the images of the applications
    THEN I am taken to that deployed application

    WHEN I resize the page or view the site on various screens and devices
    THEN I am presented with a responsive layout that adapts to my viewport

#   [Installation](#installation)

Head on over to the GitHub:

When you have a folder location, issue the command:  

```bash
git clone {link of the project}
```
Remember to use a program such as Powershell and have a program like Visual Studio Code to be able to open and edit the project.

#   [Usage](#usage)

Using the file generated as my portfolio as a sample, you are able to click on the various texts that allow you to navigate throughout the page.

((SHOW SCREENSHOT))

The top portion of it located at the right side are links that will traverse throughout the page.  Clicking the "Resume" link will pop out a new page, which will display my resume.  At the bottom portion of the page, you are also able to click on the links below (clicking on my email will get you to the email app that will allow you to contact me via email.  GitHub will send you over to my GitHub portfolio that's in the system).

((SHOW SCREENSHOT WITH SMALLER WINDOW))
In addition to this, you are also able to change the sizing of the window to indicate the format change that's happening on the page itself (it is using media queries).



#   [The Process](#the-process)

In order to have this executed as the criteria's agends, I needed to make the following:

    -CSS file
    -HTML file

We'll go through the process since it is going to take a while to explain everything.  Let's start with the HTML:

The first step I needed to do was make the skeleton of the site.  Here, I decided to write what section we need.
These are as follows:

<!-- Header -->
<!-- Section -->
<!-- Section/Content -->
<!-- Section/Article/Aside -->
<!-- Section/Article/Div -->

Once I made the skeleton, I then decided to take care on what was inside the content:

//* ======================= Global Declaration ======================= *//
Throughout the page, we needed to have a global representation on all the elements that are found here.  The coding
I used are as follows:

/* ====================== Start of Universal Declaration ====================== */
* {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
    background-color: rgb(165, 168, 202);
}

We also had repeated values found on the code.  It needed to be changed into a root so that if we change the value, it'll change the overall code itself:

:root{

    --main-lightteal-color: #67d6d6; /*use:  var(--main-white-color); */
    --font-family-one: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif; /*use: var(--font-family-one); */
    --display-inline: inline-block; /*use: var(--display-inline); */
    --font-color-one: teal;    /*Use: var(--font-color-one); */
    --dark-color: #252525; /*use: var(--dark-color); */

}

Within the code, we used 'a' and 'p' for the links and the paragraphs that we're adding.  That also had its own structure.  I made sure that they have the overall color and font-family with them:

a {
    color: teal;     /* Changing the link color to this */
    text-decoration: none;              /* This is to ensure if there's a line or not */
}

p {
    font-family: var(--font-family-one);
}


/* ====================== End of Universal Declaration ====================== */


//* ======================= Header ======================= *//
There are two sections we needed to do.  The first one dealt with the title, which is going to be my full name.
Next, we needed to have an unordered list and have it display it side to side.  We then also needed to do an
elemental guidance on it.  They have their own respected values as well as the margins needed:

/* ====================== Start of Header ====================== */

header {

    padding: 20px 0px 20px 0px;
    font-family: var(--font-family-one);
    background-color: var(--dark-color);
    color: var(--dark-color);

}

header h1 {

    padding: 5px 5px 5px 35px;
    display: var(--display-inline);
    font-size: 48px;
    background-color: teal;

}

header nav {
    background-color: var(--dark-color);
    padding-top: 15px;
    margin-right: 70px;
    float: right;
    font-family: var(--font-family-one);
    font-size: 20px;
}

header nav ul {
    list-style-type: none;
    background-color: var(--dark-color);
}

header nav ul li {
    background-color: var(--dark-color);
    display: var(--display-inline);
    margin-left: 25px;
}

/* We're in the header, going to nav, that's inside ul, in the li, and any text that has 'a' in it */
header nav ul li a {
    background-color: var(--dark-color);
    border-bottom-style: solid;     /* Adding solid line on the bottome of text */
    padding: 0px 10px 0px 10px;                   /*Adding spacing around the text */
    font-size: 25px;
}

/* ====================== End of Header ====================== */



//* ======================= Banner ======================= *//
In this section, we have a picture background as well as a sentence that is overlaid on top of it.  We needed to make sure that the positioning was correct:

/* =========== Start of Banner =========== */

The following is identifying what the image of the banner is as well as the size.  I also set this to be relative so that it is on the background.

.banner {
    height: 250px;
    position: relative;
    margin-bottom: 25px;
    background-image: url("../images/blue-banner.jpg");
    background-size: cover;
    background-position: center;
}

The following code is then used for the text.  Ther are two sections we needed to do.  The first one deals with the positioning where the word is going to be at:

.bottom-right {
    position: absolute;         /* This will cause the text to be inside the image */
    padding: 10px;              /* Have some spacing around the text */
    background-color: teal;   /* Have a background set behind the color */
    bottom: 16px;               /* Move it from the bottom */
    right: 60px;                /* Move it from the right */
}

This is then followed by the format of the h2 that's being identified in this section.  Here's the code:

.bottom-right h2 {
    font-size: 35px;            /* Change the size of the font */
    color: var(--dark-color);             /* Color of the text */
    font-family: var(--font-family-one);
    background-color: teal;

}

/* =========== End of Banner =========== */


//* ======================= Content ======================= *//

In this area, we're going to make new session that deals with the three articles.  When I observed the requirements for the criteria, I noticed that each are separated in a section that is the same thing on the properties.  I made sure that each section is defined.  First, we started out with this:

/* =========== Start of Section Declaration =========== */

section {
    padding: 30px;
}

/* =========== End of Section Declaration =========== */

This is declaring that all the sections is going to have a padding of 30 pixels around it.

Next, we did the content.  Properties:

/* =========== Start of Content =========== */

.content {
    margin-left: 20px;   
}

.content h2 {
    font-family: var(--font-family-one);
    text-align:right;
    font-size: 35px;
    top: 8px;
    right: 16px;
}

/* =========== End of Content =========== */

Next, I then identified the articles.  There are three, but they are going to have  the same property:

/* =========== Start of Article Declaration =========== */

article {
    margin-bottom: 20px;
    margin-left: 20px;
}

/* =========== End of Article Declaration =========== */

Finally, we have the properties from within the articles.  There are two sections:  One is the aside and the other is the contents.  Here are the declarations for it:

/* =========== Start of Article Design =========== */

.about-me, .work, .contact-me {
    overflow: auto;
    margin: 0 0 30px 20px;
}



.about-me aside, .work aside , .contact-me aside {
    width: 150px;
    display: var(--display-inline);
    padding: 10px 10px 5px 10px;
    float: left;

}

.about-me div, .work figure , .contact-me nav {
    
    float: left;
    display: var(--display-inline);
    border-left-style: solid;
    padding: 10px 0 10px 40px;
}

.contact-me nav {
    padding-top: 40px;
    padding-bottom: 40px;
    font-family: var(--font-family-one);
}

.contact-me nav ul li {
    display: var(--display-inline);
    margin-left: 25px;
}

.contact-me nav ul li a {
    border-bottom-style: solid;     /* Adding solid line on the bottome of text */
    padding: 10px 10px 5px 10px;                   /*Adding spacing around the text */
    font-size: 20px;
    color: var(--dark-color);
    font-weight: bold;
}

/* =========== End of Article Design =========== */

There's one more that needs to be emphasized:  The flex wraps.  I needed to make separate sections to have it behave accordingly.  Here are the few that I've used so far:

On the header, there are 3 children divs that are affected.  Identified to this being a parent, I applied the flex wrap:

header {

    padding: 20px 0px 20px 0px;
    font-family: var(--font-family-one);
    background-color: var(--dark-color);
    color: var(--dark-color);

    /*This is what's needed to have the text move.  Remember the following:
    
    display:flex causes the purple line
    justify-content: space-between adds spacing on the contents
    flex-wrap:wrap: if there is no space, it'll go to another line

    */
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;

}

The article (with the three sections) also have flex wraps.  Here's the code for it:

article {
    margin-bottom: 20px;
    margin-left: 20px;

    /*I'm making an attempt to have the flex property added here.  If we do, all the contents within the article should fall in place*/
    display: flex;
    /*We're not aligning the contents here.  The columns are to the left and the contents are at the side of the right*/
    /*justify-content: space-between;*/
    flex-wrap: wrap;

}

There's yet another flex-wrap that I used:

.work figure {
    flex: 2;
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;

}

All the way to the bottom of the contact is another flex-wrap.  Here's the code:

.contact-me nav ul {

    
    /*Something worth noting about this:  With the justify-content, we had the value of the space defined before.  When we applied it on the HEADER, we shifted THIS list so that it is taken to the right.  If we decrease the size, the space in between THIS content and the HEADER will decrease.  Now the question is:  

    Why did we needed another justify-content here?  Is it by default?*/
    /*Adding the purple line on it: 

    */
    display: flex;
    /* Contents will go below if the screen is small */
    flex-wrap: wrap;
    /*There are two more commands being used.  Pay attention carefully:
    
    align-items is like the justify-conent, but on the opposite axis.  flex-box operates in the main axis.  We need to be careful since the line above works, by default, on the horizontal axis and the one below follows the vertical axis.  But if we were to define the flex-direction to column, then the main and cross would be flipped.

    Keep in mind that the flex-direction is "row" by default.  Change this to "column" if you want it to be flipped.

    ;*/
    align-items: center;

    /*This sets how a list item is styled (bullet points, dashes, etc.) and positioned (indented or outdented).  Changed the value to none to hide the bullet points. */

    /* Though another question:  We already defined this to be none in the main section.  Why do we need this here? */

    list-style: none;
}


With this, we have the css structure of the code.  


#  [What Was Done Differently](#differently)

From the previous section to the updated, there were a few changes made.  First, I have the media query involved.  With the constant evolution in technology, one of the few things that needed to be done is have an accesability from both Desktop and Mobile devices in case someone were to look at the portfolio from either said devices.  The code itself has a way to reconstruct so that it is neatly laid out as much as possible to show on a different sized screen.

As more of my work is being added to the system, I changed the properties from "Flex" properties to "Grid".  This will ensure to have a better layout when adding new information in the system.  With this, I was also able to understand the properties of the "Grid" and was able to show a much neater presentation on the page overall.

#   [Built With](#built-with)

    *HTML
    *CSS

#  [Contributing](#contributing)
Made with ❤️ by [Edgardo Lopez]

#  [Project Status](#project-status)

As stated on the "What Was Done Differently", there are portions of the file that have been changed since assigned.  As I continue to grow as a developer, I'll be inputing additional of my work from GitHub on the portfolio as well as reconstructing the layout of the page (such as the previous change when using Grid instead of Flex).  Keep an eye out for any updates on the portfolio itself!

#  [Disclaimer](#disclaimer)

The project is open for anyone to use.  As stated on the purpose, it's to help out those that are starting in making a portfolio of their own.

#   [Website](#website)