# HTML Basics

## Images

---html
	<img src="images/cofee.png" alt='A coffee mug on a table' />
	<style>
		img{
			widht: 200px;
			height: 200px;
			object-fit: cover;
		}
	</style>
---

## Audio and Video

---html
	<video controls autoplay loop src="videos/ocean.mp4">
		Your Browser doesn't support videos.
	</video>
	<style>
		video{
			widht: 400px;
		}
	</style>
---

## Lists

---html
	<ul>
		<li>About me</li>
		<li>Courses</li>
			<ul>
				<li>Html</li>
				<li>JS</li>
				<li>Git</li>
			</ul>
		<li>Subscribe</li>
		<li>Contact me</li>
	</ul>
	<ol>
		<li>
			Preheat the oven.
		</li>
		<li>Place the integredents on the crust</li>
		<li>Put the pizza in the oven over 20 minutes. </li>
	</ol>
	<dl>
		<dt>HTML</dt>
		<dd>Hypertext Markup Language</dd>
		<dt>CSS</dt>
		<dd>Cascading StyleSheets</dd>
		<dt>Skills</dt>
		<dd>HTML</dd>
		<dd>CSS</dd>
		<dd>Responsive Design</dd>
	</dl>
	<style type="text/css">
		list-style-type: none;
	</style>
---


## Tables

---html
	<table>
		<thead>
			<tr>
				<th colspan="2">Expense</th>
			</tr>
			<tr>
				<th>
					Category
				</th>
				<th>
					Amount
				</th>
			</tr>
		</thead>
		<tbody>
			<tr>
				<td>Marketing</td>
				<td>$100</td>
			</tr>
			<tr>
				<td>Accounting</td>
				<td>$200</td>
			</tr>
		</tbody>
		<tfoot>
			<tr>
				<th>
					Total
				</th>
				<tr>
					$300
				</tr>
			</tr>
		</tfoot>
	</table>
	<style type="text/css">
		table, td, th{
			border: 1px solid red;
			border-collapse: collapse;
			padding: 5px;
		}
		tfoot{
			text-align: left;
		}
	</style>
---


## Containers

---html
	<div class="product">
		<p>lorem</p>
		<a href="#">Link</a>
	</div>
	<span>
		<p>lorem3</p>
	</span>
	<style type="text/css">
		.product{
			background-color: gold;
			width: 300px;
		}
	</style>
---

### Generic

- div
- span

### Semantic

1. <article> : any independent self dependent peice of content
1. <figure> : tells browser that this is an image not just regular image
1. <mark> : for highlighting the text
1. <time>

## Semantic Elements 

---html
	<div class="article">
		<h1>Heading</h1>
		<figcaption> </figcaption>
		<p>thisiasfbhjdsbfhjdbfjdsbjfbdsjfb nkdsbfhds</p>
		<time>January 1 2021 05:00</time>
	</div>
---


## Structuring a Web Page

---html
	<header>
		<nav>
			<ul>
				<li></li>
			</ul>
		</nav>
	</header>
	<main>
		<section>
			<h2>Products</h2>
			<article></article>
		</section>
		<section>
			<h2>Testimonials</h2>
			<article></article>
			<article></article>
		</section>
	</main>
	<aside></aside>
	<footer>
		<ul>
			<li></li>
		</ul>
	</footer>
---




## Relational Selectors

1. Cleaner Markup
1. Can be fragile
1. Not as fast as basic selectors

---html
	<section id="products">
		<p>jkasd akjsbd sanbasdbsa dnsabd askdjbas dkjasbd</p>
		<article>
			<p>kebfjds jsdf h isdhf i skjdf  kjsdf sdnf.</p>
		</article>
	</section>
	<p>jkd jdsab absd sabjda sdksa kjbasd d</p>
	<style type="text/css">
		#products > p, #products + p, #products ~ p{
			color: orange;
		}
	</style>
---


# Premature optimization is the root of all events.

## Pseudo Class Selectors

---html
	<article>
		<p>kasd hjads sadbs andb asdbhasd</p>
	</article>
	<ul>
		<li>Item 1</li>
		<li>Item 2</li>
		<li>Item 3</li>
		<li>Item 4</li>
		<li>Item 5</li>
		<li>Item 6</li>
	</ul>
	<style type="text/css">
		article :first-child{
			font-size: 140%;
			font-style: italic;
		}
		article p:first-of-type{
			font-size: 140%;
			font-style: italic;
		}
		article :last-child{
			font-size: 140%;
			font-style: bold;
		}
		article p:last-of-type{
			font-size: 140%;
			font-style: bold;
		}
		a:visited, a:link{
			color: dogerblue;
		}
		a:hover, a:focus{
			color: deeppink;
		}
		ul li : nth-child(odd){
			color: deeppink;
		}
		ul li : nth-child(even){
			color: deeppink;
		}
		ul li : nth-child(3n){
			color: deeppink;
		}
	</style>
---

#### Pseudo-Elements: To style of an element. Eg. First letter

#### Pseudo-Classes: To style elements in a Particular State. Eg. Hovered Anchor


## Pseudo Element Selectors

---html
	<p><span>hjdbahsbdaadbsjasbdjbasdbasdm</span>  anbjas dmasd sa dsad as d  as dsa d asd as  fa fas f sad sf a</p>
	<style type="text/css">
		p::first-letter{
			font-weight: bold;
			fonr-size: 140%;
		}
		p::first-line{
			font-weight: bold;
			fonr-size: 140%;
		}
		p::selection{
			background-color: pink
		}
		p::before{
			content: "..."
		}
	</style>
---


## Selector Specificty ( Weight )

ID Selector { #products }
Class & Attribute Selectors { .products }
Element Selector { section }

---html
	<article>
		<h1 id="products" class="highlight"> Heading </h1>
	</article>
	<style type="text/css">
		h1{
			color: dogerblue;
		}
		.highlight{
			color: deeppink;
		}
		#products{
			color: green;
		}
	</style>
---


## Inheritance

---html
	<p>kjsdn nbjdksfjksdf <strong>akjsdn</strong></p>
	<style type="text/css">
		p{
			color: dogerblue;
			border: 1px solid black;
		}
		strong{
			color: initial;
			border: inherit;
		}
	</style>
---


## Colors

- Named Colors
- RGB
- HSL
- Hexadecimal

---html
	<div class="box"></div>
	<style type="text/css">
		.box{
			height: 200px;
			width: 200px;
			background-color: rgb(230, 205, 16);
			background-color: rgba(230, 205, 16, 0.4);
		}
	</style>
---


## Gradients

---html
	<div class="box"></div>
	<style type="text/css">
		.box{
			height: 200px;
			width: 600px;
			background-color: rgb(230, 205, 16);
			background-color: rgba(230, 205, 16, 0.4);
			background: linear-gradient(to bottom right, dogerblue, yellow);
			background: linear-gradient(43deg, dogerblue, yellow, tomato);
			background: radial-gradient(circle at top left, white, yellow);
			/*gradient generator: google it*/
		}
	</style>
---


## Borders

solid, dashed

---html
	<div class="box"></div>
	<style type="text/css">
		.box{
			height: 200px;
			width: 200px;
			background-color: rgb(230, 205, 16);
			background-color: rgba(230, 205, 16, 0.4);
			background: linear-gradient(to bottom right, dogerblue, yellow);
			background: linear-gradient(43deg, dogerblue, yellow, tomato);
			background: radial-gradient(circle at top left, white, yellow);
			/*gradient generator: google it*/

			border: 10px solid royalblue;
			border: 10px solid royalblue;
			border-top: 20px solid royalblue;
			border-width: 10px 20px;
			/*trbl*/
			border-radius: 100%;
			/* search: css shape*/
		}
	</style>
---

## Shadows

---html
	<div class="box">
		<h1>Heading</h1>
	</div>
	<style type="text/css">
		.box{
			height: 200px;
			width: 200px;
			background-color: rgb(230, 205, 16);
			background-color: rgba(230, 205, 16, 0.4);
			background: linear-gradient(to bottom right, dogerblue, yellow);
			background: linear-gradient(43deg, dogerblue, yellow, tomato);
			background: radial-gradient(circle at top left, white, yellow);
			/*gradient generator: google it*/

			border: 10px solid royalblue;
			border: 10px solid royalblue;
			border-top: 20px solid royalblue;
			border-width: 10px 20px;
			/*trbl*/
			border-radius: 100%;
			/* search: css shape*/

			/*Shadows */
			box-shadow: 10px 10px;
			box-shadow: -10px -10px grey;
			/* For softer use thir value*/
			box-shadow: -10px -10px 10px grey;
			box-shadow: 0 0 30px grey; 
			/*Add Shadow to the text*/
			h1{
				color: white;
				text-shadow: 0 0 30px grey;
			}
		}
	</style>
---