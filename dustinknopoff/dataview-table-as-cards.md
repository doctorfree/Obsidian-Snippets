---
title: Dataview Table as Cards
date: 2021-05-20
taxonomies:
  tags:
    - css
  kind:
    - styling
extra:
  author: yungbananapeel
---

![](https://cdn.discordapp.com/attachments/840286238928797736/845044771621699634/dataview_library.jpg)

```css
/* READ ME */
/*
This css has been built to be used with dataview tables, and assumes you are not using dataviewjs. But this can easily be adapted to list view. Because this css is not supported by a js backend, text and backgrounds will not autosize (i think so anyway, i haven't found a way. if you do share on discord @yungbananapeel#2624)

I'm not that great as using css, so there is probably a lot of redundancies in the file. The Main thing to understand about using the css to manipulate the tables is  the structure of a DV table. 

Any content about a page you want returned is delivered as a child element of a span, that is nested inside of a TD.The TD's are the individual containers that make up the columns of a row. if you want to change the structure of a table on top of this file, its important to remember all the relationships between the TR>TD>SPAN>CONTENT. 

An an example images and links are returned as <a> & <img> tags as children of a div, but strings are returned as the content of the span, not as content of a child element.like so:
<span>
	<a href="mylink"> cool link </a>
	<img src="prettyPic"> picture </img>
</span>
<span>YOUR TEXT HERE</span>

TABLE STRUCTURE
<div>
	<table>
		<thead>
		</thead>
		<tbody>
			<tr>
			EACH TR CORRESPONDS TO A SINGLE PAGE RETURNED FROM YOUR QUERY.
				<td>
					EACH TD CORRESPONDS TO A COLUMN
					THEY ARE ORDERED TOP TO BOTTOM, IN ORDER FROM LEFT TO RIGHT
					<span>
					THIS SPAN IS WHERE YOUR RETURNS INFO IS (links, images, text)
					</span>
				</td>
			</tr>
		</tbody>
	</table>
</div>
*/
/* COLORS */
.CardView {
	--Name-bg: red;
	--
}
/* Hide Table Head */
.CardView thead{
	display: none;
	line-height: 0;
	height: 0px;
}
CardView table {
	border-collapse: collapse;
	border-spacing: 0;
	width: 100%;
}


/* Table wide Changes */
/* .CardView tbody {
	display: flex;
	flex-direction: row;
	flex-wrap: wrap;
} */
/* Turn all spans into flex boxes*/
.CardView span {
	display: flex;
	float: left;
	margin: 0;
	padding: 0;
	max-width: 350px;
}
/* Create a card Shape from the Table Row */
.CardView tr {
	display: block;
	text-align: justify;
	float: left;
	padding: 0;
	margin-right: 60px;
	height: 475px;
	width: 310px;
	background-color: rgb(36, 32, 32) !important;
	border: 5px solid rgb(0, 0, 0) !important;
	box-shadow: 10px 11px 19px -1px #070202;
}

.CardView td {
	display: block;
	min-height: 50px;
	padding: 15px;
}
/* First Column Box*/
.CardView td:first-child {
	min-height: 75px !important ;
	padding: auto;
	background-color: rgba(255, 255, 255, 0.863);
	border: 5px solid rgb(255, 255, 255);
}
/* First Column link */
.CardView td:first-child span a {
	text-overflow: ellipsis !important;
	word-wrap: break-word !important;
	text-overflow: ellipsis !important;
	display: block;
	line-height: 1em;
	max-height: 2em;
	font-size: 23px;
	font-weight: bold !important;
	color: rgb(207, 17, 17) !important;	
}

/* Second Column */
/* column bg */
.CardView td:nth-child(2) {
	z-index: 2;
	background-color: rgb(226, 75, 75);
	width: 175px;
	display: block;
	float: left;
	line-height: 1em;
	max-height: 2em;
}
/* column link */
.CardView td:nth-child(2) a {
	color: rgb(206, 211, 189) !important;
	font-weight: bold !important;
	width: 60px;
	word-wrap: break-word;
	text-overflow: ellipsis !important;
}

/* third column */
.CardView td:nth-child(3) {
	max-height: 50px !important;
	color: rgb(255, 81, 81) !important;
	z-index: -1;
	width: 125px;
	line-height: 1em;
	max-height: 2em;
	display: block;
	float: right;
	background-color: rgb(250, 246, 0);
}
/* third column links */
.CardView td:nth-child(3) span a {
	color: rgb(255, 81, 81) !important;
	text-align: right;
	width: 100%;
	overflow: hidden;
	display: block;
	float: right;
	font-weight: bold !important;
	word-wrap: break-word;
	text-overflow: ellipsis !important;
}
/* third column strings */
.CardView td:nth-child(3) span{
	color: rgb(255, 81, 81) !important;
	text-align: right;
	width: 100%;
	overflow: hidden;
	display: block;
	float: right;
	font-weight: bold !important;
	word-wrap: break-word;
	text-overflow: ellipsis !important;
}

/* Last Column Image */
.CardView td span img {
	display: block;
	width: 300px;
	height: 300px;
	object-fit: contain;
	margin: 0 auto;
	padding: 0;
	margin: 20px auto;
}

```