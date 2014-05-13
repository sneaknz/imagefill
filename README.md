# Imagefill plugin

A plugin that will insert a random image from a specified set and resize it to fill the parent element.

## Requirements

The plugin requires jQuery to be included in the page, and also the [http://imagesloaded.desandro.com](imagesloaded) plugin from David Desandro. A copy of the imagesloaded plugin is included with this distribution, or you can use the bundled `jquery.imageill-combined.min.js` file which already includes the plugin if you don't want to include it separately.

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

	<div class="block"></div>

	$(".block").imagefill({
		images: [
			"img/image1.jpg",
			"img/image2.jpg",
			"img/image3.jpg"
		]
	});
