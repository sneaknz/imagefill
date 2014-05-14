# Imagefill plugin

A plugin that will insert a random image from a specified set and resize it to fill the parent element. See an example at <a href="http://code.sneak.co.nz/imagefill/">http://code.sneak.co.nz/imagefill/</a>.

## Requirements

The plugin requires jQuery to be included in the page, and also the [imagesloaded](http://imagesloaded.desandro.com) plugin from David Desandro. A copy of the imagesloaded plugin is included with this distribution, or you can use the bundled `jquery.imagefill-combined.min.js` file which already incorporates the plugin if you don't want to include it separately.

## Options
 
 <table>
 	<tr>
		<th>images</th>
		<td>An array of strings that are paths to images (required)</td>
	</tr>
	<tr>
		<th>loader</th>
		<td>Whether to show the loading animation (optional). Default is true.</td>
	</tr>
	<tr>
		<th>loaderHtml</th>
		<td>The HTML for the 'loading' animation (optional). Default is `'<div class="imagefill-loader"><div class="bounce1"></div><div class="bounce2"></div><div class="bounce3"></div></div>'`</td>
	</tr>
</table>

## Usage

After including jQuery, add the necessary files for the plugin:

	<link href="imagefill.css" rel="stylesheet" />
	<script src="imagesloaded.js"></script>
	<script src="jquery.imagefill.js"></script>
	
Or if you are using the combined script that includes the `imagesloaded` plugin:

	<link href="imagefill.css" rel="stylesheet" />
	<script src="jquery.imagefill-combined.min.js"></script>
	
To use the plugin simply call it against the element you wish to insert an image into:

	<div class="block"></div>

	$(".block").imagefill({
		images: [
			"img/image1.jpg",
			"img/image2.jpg",
			"img/image3.jpg"
		]
	});

## To-do

- TODO: Check for image load status, and if an error then select another from the array. Test with bad references to local images and also with internet disabled for web-based images.
- CONSIDER: Add options for loader animations and/or colouring.
