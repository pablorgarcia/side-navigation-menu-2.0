<h1>Side Navigation Menu V2, RWD</h1>

<p>CSS3 transition, box-shadow, transform properties. Responsive Web Design technologies & without JS.</p>
<a href="http://www.pablogarciafernandez.com/lab/demo/side-navigation-menu-v2.html" target="_blank">Check out the demo page</a>.

<h2>How it works</h2>

<p>We have a &lt;nav&gt; tag on the left of the screen with <code>position: fixed;</code>, a width and a fixed height.</p>
<p>Then we have a list with &lt;svg&gt; images and hidden links with <code>display: none;</code>, when we do a <code>:hover</code> over &lt;nav&gt; tag we added more <code>with</code> to the &lt;nav&gt; and a <code>display: block;</code> so that the links appear.</p>

<h3>Transition property for movement to the side navigation</h3>

<p>We have to write on the &lt;nav&gt; tag the CSS3 <code>transition</code> property:</p>
<pre>
nav {
  transition-delay: 0s;
  transition-duration: 0.4s;
  transition-property: all;
  transition-timing-function: line;
  }
</pre>

<h3>Box-shadow property for 3D effect</h3>

<p>When the screen is smaller than 1024px, the box-shadow property are going to be used at the <code>.navigation</code>.</p>

<pre>
.navigation {
	box-shadow:
	  #D4D4D4 -1px 1px,
	  #D4D4D4 -2px 2px,
	  #D4D4D4 -3px 3px,
	  #D4D4D4 -4px 4px,
	  #D4D4D4 -5px 5px,
	  #D4D4D4 -6px 6px;
}
</pre>

<p>The next step is add another box-shadow property on <code>a:hover</code>, <nav> inside.</p>

<pre>
.navigation > ul > li > a:hover{
	box-shadow:
	  #666 -1px 1px,
	  #666 -2px 2px,
	  #666 -3px 3px,
	  #666 -4px 4px
}
</pre>

<p>But in the case screen is larger than 1024px, the box-shadow property of <code>.navigation</code> is not used.</p>

<pre>
@media only screen and (min-width: 1024px) {
	.navigation { box-shadow: none; }
}
</pre>

<h3>Transform property is to correct the position</h3>

<p>We need to have the <code>.navigation</code> just the same size of the box-shadow property that we wrote before.</p>

<pre>
.navigation { transform: translate3d(4px, 0px, 0); }
</pre>

<p>And create the new position for the <code>a:hover</code>.</p>

<pre>
.navigation a:hover { transform: translate3d(6px, 0px, 0); }
</pre>

<h2>Download, Fork, Commit.</h2>

<p>If you think you can make this better, please Download, Fork, & Commit. I'd love to see your ideas.</p>

<a href="http://www.pablogarciafernandez.com/lab/side-navigation-menu-v2.html" target="_blank">Code original</a>

<a href="http://codepen.io/PableraShow/pen/hubAa" target="_blank">Demo on CodePen</a>

===================

<a href="http://pablogarciafernandez.com" title="Pablo García Fernández" target="_blank">Pablo García Fernández</a>
