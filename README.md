<h1>SlickNav</h1>
When we view our responsive websites on the phone, we want the navigation to change to a “hamburger” icon, and drop down when touched. To do this, we’re can the slicknav jQuery plugin which manages a lot of the transition. The plugin requires jQuery as well some JavaScript. It also requires additions to the style.css and its own CSS file.

<a href="http://slicknav.com/" target="_blank">http://slicknav.com/</a>
<h2>Step 1</h2>
Download SlickNav files

<a href="http://slicknav.com/" target="_blank">http://slicknav.com/</a>
<h2>Step 2</h2>
Add CSS + JavaScript files
<pre class="whitespace-after:2 lang:xhtml decode:true ">&lt;link href="css/slicknav.css" rel="stylesheet" type="text/css" /&gt;
     

&lt;script src="http://cdnjs.cloudflare.com/ajax/libs/modernizr/2.6.2/modernizr.min.js"&gt;&lt;/script&gt;
&lt;script src="http://ajax.googleapis.com/ajax/libs/jquery/1/jquery.min.js"&gt;&lt;/script&gt;
&lt;script src="js/jquery.slicknav.min.js"&gt;&lt;/script&gt;</pre>
Add links to the CSS file + JS file + Modernizer + jQuery library. Insert into the head of the HTML page.

Be sure to add these files to your "final web" folder. The slicknav.css file is placed in your css folder. Create a js folder for the jquery.slicknav.min.js file.

<p><strong><span style="color: #2a2a2a;">What is Modernizr?</span></strong></p>

<span style="color: #2a2a2a;">Modernizr makes it easy for you to write conditional JavaScript </span><em style="color: #2a2a2a;">and CSS</em><span style="color: #2a2a2a;"> to handle each situation, whether a browser supports a feature or not. It’s perfect for doing progressive enhancement easily.</span>
<h2>Step 3</h2>
Add id=“menu” to ul
<pre class="whitespace-after:2 lang:xhtml decode:true ">&lt;ul id="menu"&gt;</pre>
<h2>Step 4</h2>
Initialize by adding the JavaScript code before the closing body tag.
<pre class="lang:xhtml decode:true">&lt;script type="text/javascript"&gt;
$('#menu').slicknav({
label: '',
duration: 500,
prependTo:'#mobile-nav', 
});
&lt;/script&gt;</pre>
<h2> Step 5</h2>
Add an empty div for the mobile navigation before the nav tag in the HTML.
<pre class="whitespace-after:2 lang:xhtml decode:true ">&lt;div id="mobile-nav"&gt;&lt;/div&gt;</pre>
<h2> Step 6</h2>
Add CSS

Add this CSS rule to the CSS before the start of the media queries.
<pre class="whitespace-after:2 lang:css decode:true ">/* add this for SlickNav */

.slicknav_menu {
    display:none;
}
</pre>
<h2> Step 7</h2>
Add this CSS rule to the CSS in the media query for the smartphone.
<pre class="lang:css decode:true">#mobile-nav {
float: none;
padding-left: 4%;
}

.js nav {
display:none;
}

.js .slicknav_menu {
display:block;
}</pre>
<h2> Step 8</h2>
Style the navigation in the slicknav.css file. The changes can be made in the CSS below this comment
<pre class="lang:css decode:true">/* 
User Default Style
Change the following styles to modify the appearance of the menu.
*/</pre>
Change color of the navigation and also remove margin-top for columns.
