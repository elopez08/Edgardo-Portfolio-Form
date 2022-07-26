# Run Buddy, Inc

## Purpose
A website that offers fitness training services. 


    ? = is the task still being issued
    X = the task is there, but it has an error (not similar)
    Y = yes!  The criteria is met!

    CRITERIA:

    [?]GIVEN I need to sample a potential employee's previous work

    [?]WHEN I load their portfolio
    THEN I am presented with the developer's name, a recent photo or avatar, and links to sections about them, their work, and how to contact them

    [Y]WHEN I click one of the links in the navigation
    THEN the UI scrolls to the corresponding section

    [?]WHEN I click on the link to the section about their work
    THEN the UI scrolls to a section with titled images of the developer's applications

    [?]WHEN I am presented with the developer's first application
    THEN that application's image should be larger in size than the others

    [?]WHEN I click on the images of the applications
    THEN I am taken to that deployed application

    [?]WHEN I resize the page or view the site on various screens and devices
    THEN I am presented with a responsive layout that adapts to my viewport

## THE PROCESS
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


/* Make sure you write down on what you did to have the color overlay of the picture.  We also need to describe what we did in terms of setting the picture in the frame. */


With this, we have the css structure of the code.  



## Built With
* HTML
* CSS

## Website
https://lernantino.github.io/run-buddy/

## Contribution
Made with ❤️ by [Edgardo Lopez]

### ©️2019 Run Buddy, Inc 
