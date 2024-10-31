
# FV42012 Chieftain History and Development 

Welcome,

This project showcases the development and the history of how the Chieftain MBT came to be. I hope that it can be used as a website where you can go to get an overview on its history. My intended targets are any researcher, student, or just anyone curious about this topic. I hope the site serves as a gateway to understand this topic to drill down to more specific information.


### Live link:

 Chieftain MBT < https://jeddizon.github.io/fv4201_chieftain_project1/ >

![Website mockup](/assets/images/chieftainmbt-website-mockup.jpg)

---


## Features

### Page 1 (History)

This page features a brief introduction on the Chieftain before going into the development history as part of a timeline. 

![Website Intro](/assets/images/chief-intro.jpg)

The timeline includes the thinking of why it was needed, its uses, and any problems it faced during its development cycle and while it was in service. This serves as a straightforward way for anyone curious about this topic to understand its development in a chronological order.

![Timeline](/assets/images/chief-timeline.jpg)

### Page 2 (Additional Info)

This page features additional information that wasn't input into the timeline; it features 2 wars that the Chieftain took part in, along with 2 important variants.

![Additional Info page](/assets/images/chief-addnl-info.jpg)

There is also a small table showing the tank’s notable specifications. This is useful for anyone who just wants a quick look at the tank’s details.

![Chieftain Specs table](/assets/images/chief-specs.jpg)

### Page 3 (Contact Us)

This page features a disclaimer for anyone who wishes to use the information on the website to use with care as there may be inaccurate information. 

![Disclaimer](/assets/images/chief-disclaimer.jpg)

It also has contact details for the author should anyone wish to contact them (address, phone number, and email). There is a small form for any feedback that anyone that may wish to contact the author also.

![Contact Details](/assets/images/chief-contact-details.jpg)

---


## Existing Features 

### Nav Bar 

There is an identical nav bar on every page which allows users to see which page they are on at any given time and will also allow easy navigation to switch to another page as needed. 

![Nav Bar](/assets/images/chief-navbar.jpg)

### Intro

The intro section serves as a way to introduce the topic to the user before diving into the history. It is also a way to show the user what the page is about. 

### Timeline

The timeline on Page 1 allows for users to learn about the development of the Chieftain in a chronological order.

### Footer

The footer features links to relevant websites to anyone else wishing to learn more about this topic as well as links to our social media pages for more tank facts. Hovering over each link causes it to change colour and become underlined as a visual indication to the user that they can click them.

![Footer](/assets/images/chief-footer.jpg)

### Additional Info 

This showcases 2 other wars and battles the Chieftain took part in that wasn’t included in the development page. It also showcases 2 variants of the Chieftain to note.

### Specifications

Features a small table on details about the tank.

### Contact form

Showcases a form for any user who wishes to leave a comment or any feedback to the author. The user will be asked to include an email, name, and a comment if they wish to send feedback. It includes a submit and reset button to send/reset the form which changes colour to prompt users to click.

![Form](/assets/images/chief-form.jpg)

### Contact form redirect

This provides as a visual indication to the user that the author has received their comment and a way to return back to the previous pages to continue learning.  

![Redirect](/assets/images/chief-redirect.jpg)

## Features Left to Implement

See below any additional features that I would like to implement:
1. A sound recording of the Chieftain’s L11 gun firing. 
2. A small clip of a Chieftain crew training and firing from the BBC website. 
3. Include a small gallery of photos that are relevant.
4. A small map in the contact form to show where we are based. 
5. Interactable table of contents where user can jump down to specified sections (dropdown for menu headers)

---


## Testing

ChromeDevTool
  - For making the pages responsive

Links working 
  - Within page
  - External links - opens new tab

Timeline
  - Responsive as the sections move depending on the screen size

Additional Info
  - DevTools used to make text and images responsive
  - Centred text and images
  - Table can be read with no issues

Contact form
  - Works as intended; users would need to input a name, email, and comment before they can submit.
  - Submitting will bring users to a redirect page confirming that the author has received the comment.

Redirect page
  - Tells the user that the author has received the comment and provides a link back to the main page. 
---


## Responsiveness

### Desktop & Laptop

### Ipad

### Phone
 
---


## Bugs 

### W3C Markup Validation

#### Page 1:

![W3C Markup Validator Snip Page 1](/assets/images/chief-page1-validate.jpg)

Issues:
- Image labels incorrect for images
  - Fix: Replaced labels with figcaptions

- Images and figcaptions needed to be inside figure tags
  - Fix: Input figure tags

- Warn for “for” attribute inside figcaption. 
  - Fix: Removed “for” attributes.


#### Page 2:

![W3C Markup Validator Snip Page 2](/assets/images/chief-page2-validate.jpg)

Issues:
- No p element in scope but a p end tag seen. (Line 126 and 150).
  - Fix: moved closing p tag to remove figure tags

#### Page 3:

![W3C Markup Validator Snip Page 3](/assets/images/chief-page3-validate.jpg)

#### Redirect Page:

![W3C Markup Validator Snip Redirect Page](/assets/images/chief-redirect-validate.jpg)

Issues:
- Error for Missing title
  - Fix: Created heading title and made hidden


### W3C CSS Validation

![W3C CSS Validator Snip](/assets/images/w3c-css-validator.jpg)

Issues:
  - position:flex; was found in styling the redirect message. 
    - Fix: Removed. 

### Page 1

Intro: 
- Image in intro causing background padding to appear
  - Fix: went away after making image responsive & padding to the header

Timeline:
- When initially creating the timeline, the footer kept appearing in the centre of the screen.
  - Attempt: value position set to fixed and bottom to 0, but now the content is being covered by the footer at the bottom
  - Fix: style footer links with display flex.
- When putting a border around the divs, only the first div was responding
  - Fix: extra div closing tags were auto created after copying and pasting each checkpoint section.
- Timeline was not a complete line down the middle
  - Fix: adjusting max-width of checkpoint div id
- Images popping out of container when checking responsiveness
  - Fix: Object-fit & setting up a parent style for images instead of setting a different one for each  
- Timeline breaking and extending outside the page when resizing (caused when added the new breakpoint for ipad sized screens)
  - Fix: Copied styling for phone sized screens into ipad media query.



### Page 2

Additional info sections
- Images popping out of container when checking responsiveness
  - Fix: Object-fit & setting up a parent style for images instead of setting a different one for each  
- Sections, images, text, not centred when resizing
  - Fix: Used text-align & justify-content center

Spec table
- Text extending outside cell when resizing
  - Fix: Word wrap, break-word
- Rows extending past div when resizing
  - Fix: Table-layout fixed <https://stackoverflow.com/questions/4185814/fixed-table-cell-width>


### Page 3

Form
- Not centred in laptop/desktop screen
  - Fix: Made the divs in the section display into flex, and adjusted flex position to space evenly
- Not holding shape when checking responsiveness; text going out of the container & losing structure.
  - Fix: made width fit content

Contact details 
- Not centred in laptop/desktop screen
  - Fix: Made the divs in the section display into flex, and adjusted flex position to space evenly
- Not holding shape when checking responsiveness; text going out of the container & losing structure.
  - Fix: made width fit content


### Redirect 

Redirect message
- Link wont centre
  - Fix: Moved the anchor tag inside p.
- Message div extending past outside the page
  Fix: adjusted positioning and padding of div


---


## Deployment
 
This project was deployed on Github. The site to deploy can be read below:

### Steps

**Instructions copied from CodeInstitute Instructions - The benefits of early deployment**

1. Go to the **Settings** tab of your GitHub repo.
2. On the left-hand sidebar, in the **Code and automation** section, select **Pages**.
3. Make sure:

    1. **Source** is set to 'Deploy from Branch'.
    2. **Main branch** is selected.
    3. **Folder** is set to / (root).

4. Under Branch, click **Save**.
5. Go back to the **Code** tab. Wait a few minutes for the build to finish and **refresh your repo**.
6. On the right-hand side, in the **Environments** section, click on 'github-pages'.
7. Click **View deployment** to see the live site. 

### Live link:

 Chieftain MBT < https://jeddizon.github.io/fv4201_chieftain_project1/ >

---


## Credits 

### Content

- Informative Content
  - Wikipedia  < https://en.wikipedia.org/wiki/Chieftain_(tank) >
  - Tank-afv.com < https://tank-afv.com/coldwar/UK/chieftain.php >
  - Tanks Encyclopedia <https://tanks-encyclopedia.com/coldwar/uk >
  - The Tank Museum Youtube:
    - < https://www.youtube.com/watch?v=D3OF9IvtHLk >
    - < https://www.youtube.com/watch?v=yViQoJPZnMQ >

- Extra help 
  - Mentor (Julia Konovalova)
    - Feedback
    - Criticism
    - Tips and tricks for direction

- Outside Code
  - Love running code for dropdown, initial styling for logo, initial css for website.
  - Timeline: YouTube tutorial  < https://www.youtube.com/watch?v=bI3J5rUonEg&ab_channel=QuickCodingTuts >
  - Stack Overflow
    - Word wrap < https://stackoverflow.com/questions/1147877/how-to-word-wrap-text-in-html >
    - Table layout fixed < https://stackoverflow.com/questions/2259189/table-overflowing-outside-of-div >
    - Made background image darker so that the text can be read easier < https://stackoverflow.com/questions/23208200/how-to-darken-a-background-using-css >
    - To make cursor pointer a hand on hover < https://stackoverflow.com/questions/3087975/how-to-change-the-cursor-into-a-hand-when-a-user-hovers-over-a-list-item >
  - Object fit 
    - MND web docs <https://developer.mozilla.org/en-US/docs/Web/CSS/object-fit>
	  - W3schools <https://www.w3schools.com/css/css3_object-fit.asp>


### Media 

- Favicon: Flaticon <a href="https://www.flaticon.com/free-icons/military" title="military icons">Favicon: Military icons created by cube29 - Flaticon</a>
- Icons: Font Awesome < https://fontawesome.com >
- Photos: 
  - Wikimedia Commons < https://commons.wikimedia.org/wiki/Main_Page >
  - Tank-afv.com <https://tank-afv.com/coldwar/UK/chieftain.php >
  - Pexels < https://www.pexels.com >
- Colour palette combinations: 
  - Colorkit <  https://colorkit.co/palettes/ >




