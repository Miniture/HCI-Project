# HCI-Project
What is a screen reader?

Screen readers are software that enables those who cannot see the screen to access information on computers and smartphones. The technology reads the screen aloud or converts it to Braille.


Screen readers typically support more than one language, so they can switch to a different language as long as that language is encoded in the site’s metadata.

Screen readers can be tailored to the user’s unique needs through scripting. Scripting is the ability to write programs that automate tasks in certain environments.


Users can use scripts for a more natural browsing experience, and they can also share these customizations with other users. Many screen readers have an active script-sharing community to help all users get the most from their software.


What can a screen reader do?

In addition to reading text from the computer screen, screen readers can also translate pictures and tables to help the user make sense of every element on the page.


Screen readers convert text that is displayed on a computer into a usable format for those who cannot read it. Users navigate their devices through a variety of keyboard commands and unique shortcuts. They work in one of two separate forms:
Text-to-Speech Output, where the words are read directly to the user, or
Braille Display, where the user can read the output through a tactile pad that translates the words into Braille.
What is needed for a screen reader to work?
Screen readers translate web pages by reading HTML files directly, so everything the reader needs should be included in this file. Here are some basic steps you can take to help screen readers process your pages and make your website easy to navigate for screen reader users. To get the most from this section, we recommend brushing up on your HTML if you need to.
Screen readers use HTML tags to understand the content and regions of the page, and what elements are available for the user to select. For this reason, the most effective way to make your web pages accessible is to structure your HTML code with semantically rich tags.
When we say a tag is “semantically rich,” we mean that the name of the tag itself conveys its purpose to the screen reader. Tags like <p>, <img>, <h2>, <ul>, <ol>, and <table> are all semantically rich because it’s clear what they are from the tag name itself — <p> is a paragraph, <img> is an image, and so one. On the other hand, <span> and <div> tags are generic, and not semantically rich — they could be used for any element. For these tags, you can use ARIA landmarks — we’ll cover those soon.
Writing HTML this way is important for a few reasons. First, screen readers allow users to jump between tags of the same type. A common use of this is headings, an important navigational method for screen reader users. When a screen reader detects the use of <h2>, for example, it allows users to jump between H2s, similar to how sighted users might scan a page by reading the headings.
Second, some HTML elements, such as <table>, activate specific screen reader commands. When a screen reader sees the <table> tag, it knows to let the user navigate horizontally and vertically through the table with their keyboard. This is why you should avoid making elements that look like a table, list, or button but use an unmatched tag (like <div>). Instead, use the appropriate tag when possible.
Finally, a <title> tag is also useful to screen readers. Users can set their screen readers to read the contents of this tag after the page loads to lend further context.
A screen reader needs to be told which language a web page is written in, so it knows how to pronounce words to the user with TTS.
Screen readers will first look for the lang attribute inside the <html> tag for page-wide language information. For example, if a page is written in English, its opening <html> tag would read:


<html lang="en">
In cases when foreign words appear on the page, the lang attribute can be placed inside any other tag, commonly <span> or <p>, to denote a temporary language change:


<html lang="en">
    <body>
        <p>I’m a paragraph in English.</p>
       <p>“Hello” in Spanish is <span lang=“es”>hola</span>.</p>
       <p lang="fr">Je suis un paragraphe en Français.</p>
    </body>
</html>
Use ARIA roles.
ARIA roles are values that indicate the function of a page element or region for screen readers. They may be placed inside <div> and <span> tags with the attribute role. ARIA roles include main, form, navigation, and search.
For example, if you want to indicate that a list of links is a navigation menu, you can place an ARIA landmark like so:


<div role=”navigation”>
    <ul>
        <li>Product</li>
       <li>Solutions</li>
       <li>About Us</li>
       <li>Blog</li>
    </ul>
</div>
Here, role=“navigation” is the landmark.
Also note that ARIA landmarks should only be used in <div> and <span> tags, as these are generic tags and not semantically rich. Tags like <menu>, <nav>, <form>, and <main> should not use ARIA landmarks, as their purpose is already established with their names.
While not all screen readers detect ARIA landmarks, it’s good practice to use them in any page region for which the function is unclear from the tag names alone.
Write descriptive headings and first sentences.
Similar to how sighted users skim page content visually, screen reader users can preview headings and paragraphs to see if the content is relevant to them. Therefore, it’s good practice to make your headings as descriptive as you can, and to begin paragraphs in a way that gives readers an understanding of the content to come.
Use alt text.
While it’s certainly a benefit, the main purpose of alternative text isn’t SEO — it’s to give screen readers a captioned alternative for media content. When it encounters an image, video, or other piece of media, a screen reader will default to reading alt text if it is provided. If alt text is not provided, screen readers will ignore the image or read the image file name.
To make your pages accessible, always add clear and descriptive alt text to each piece of non-text content, namely images, videos, icons, and embeds. For instance, suitable alt text for this image...

Image Source
...might be:


alt="professional baseball player Hank Aaron of the Atlanta Braves swinging a baseball bat in a baseball stadium”
For more tips on how to optimize your alt text for screen readers and search ranking, see our guide to image alt text.
Use punctuation correctly.
Here’s another tip that assists all page visitors, screen-reader-assisted and not. To simulate speech, screen reader TTS pauses for instances of periods, commas, new paragraphs, and other punctuation. For the best experience, make sure you’re implementing punctuation in the proper ways.
How to operate a screen reader (Something like a buttons on a keyboard)

A user controls their screen reader with the keyboard. A screen reader comes with a library of keyboard commands that tell the screen reader to do things like start/stop reading, jump back to re-read a section of text, spell out words, skip to different parts of a page, move the cursor/focus around, play a media file, or click a link, button, or another interactive element.

In addition to TTS, some screen readers can convert onscreen text into braille. For this function, users connect an external device, called a refreshable braille display, which generates braille characters on a pad as the screen reader scans the text. Here’s what a typical refreshable braille display looks like.

-This is all the keys on a keyboard for a JAWS, NVDA, Narrator, and VoiceOver screen reader. It's not very nice in this format but it shows it off.
Task
JAWS
NVDA
Narrator
VoiceOver
Turn screen reader on
Not available
Control + Alt + N
Windows logo + Control + Enter
Command + F5
Turn screen reader off
Insert + F4
Insert + Q
Windows logo + Control + Enter or Caps Lock + Escape
Command + F5
Stop reading
Control
Control
Control
Control
Read next item
Down Arrow
Down Arrow
Caps Lock + Right Arrow*
VO + Right Arrow
Read previous item
Up Arrow
Up Arrow
Caps Lock + Left Arrow*
VO + Left Arrow
Read next focusable item (e.g. link, button)
Tab
Tab
Tab
Tab
Activate link
Enter
Enter
Caps Lock + Enter or
Enter** or Space Bar**
VO + Space Bar or Enter
Activate button
Enter or Space Bar
Enter or Space Bar
Caps Lock + Enter or
Enter or Space Bar
VO + Space Bar or
Enter or Space Bar
Start reading continuously from this point on
Insert + Down Arrow
Insert + Down Arrow
or Numpad Plus
Caps Lock + Down Arrow
or Caps Lock + Control + R
VO + A
Go to next heading
H
H
H**
VO + Command + H
Show list of all headings
Insert + F6
Insert + F7
Caps Lock + F6
VO + U (Rotor), then Left/Right Arrow Keys
Go to next heading of level [1-6]
1-6
1-6
1-6**
Not available
Go to next landmark/region
R (JAWS 16+)
; (JAWS 15)
D
D**
Not available
Go to the main content landmark
Q
Not available
Caps Lock + N
Not available
Open Elements List or Rotor
Insert + F3
Insert + F7
Caps Lock + [F6 or F7], then Tab (twice) to the Scoping drop-down list
VO + U
Go to next table
T
T
T**
VO + Command + T
Navigate table cells
Control + Alt + Arrow Keys
Control + Alt + Arrow Keys
Control + Alt + Arrow Keys
VO + Arrow Keys
Go to next list
L
L
Not available
VO + Command + X
Go to next list item
I
I
Not available
Not available
Go to next graphic
G
G
Not available
VO + Command + G
Show list of all links
Insert + F7
Insert + F7
Caps Lock + F7
VO + U (Rotor), then Left/Right Arrow Keys
Go to next link
Not available
K
K**
VO + Command + L
Go to next unvisited link
U
U
Not available
Not available
Go to next visited link
V
V
Not available
VO + Command + V
Go to next form element
F
F
F
VO + Command + J
Go back to previous heading, landmark, table, focusable item, etc.
Shift + [H, R, T, Tab, etc.]
Shift + [H, D, T, Tab, etc.]
Shift + [H**, D**, T**, Tab, etc.]
VO + Shift + Command + [H, T, Tab, etc.]
Toggle screen reader mode
Forms Mode: (On) (Automatic when in form element), (Off) Numpad Plus
Browse/Focus Mode: Insert + Space Bar
Forms Mode^: Insert + Space Bar
Scan Mode: Caps Lock + Space Bar
Not available
Interact with (go into/out of) objects (like iframes, menus, application regions, etc.)
Not applicable
Not applicable
Not applicable
VO + Shift + Down/Up Arrows
Toggle between: Radio buttons, <select> list items, Tabs (ARIA widget), Tree view items (ARIA widget), Menu items (ARIA widget)
Arrow Keys
Arrow Keys
Arrow Keys
Arrow Keys, then [VO + Space Bar or Space Bar]
Toggle Virtual PC Cursor
Insert + Z
Not available
Not available
Not available

