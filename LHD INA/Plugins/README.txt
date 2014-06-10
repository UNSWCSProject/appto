Release Notes

e-mail Jason Aller (jraller@ucdavis.edu) with questions.

Requirements:

jQuery version 1.4.2
jQueryUI version 1.8
Keith Wood's SVG plugin:
 * jquery.svg.js 
 * jquery.svgdom.js 
 * jquery.svganim.js -- modify to allow animation of strokeDashOffset see below

Optional:

jquery.metadata.js -- for suppying configuration from the targeted DOM element itself
 
Version 0.1

First functional version of the plugin.

Modifying jquery.svganim.js

Note: the jquery.svganim.js file will need to be modifed in order to support animating the path.

change lines 12-14:

$.each(['x', 'y', 'width', 'height', 'rx', 'ry', 'cx', 'cy', 'r', 'x1', 'y1', 'x2', 'y2',
		'stroke-width', 'strokeWidth', 'opacity', 'fill-opacity', 'fillOpacity',
		'stroke-opacity', 'strokeOpacity', 'font-size', 'fontSize'],
		
to:

$.each(['x', 'y', 'width', 'height', 'rx', 'ry', 'cx', 'cy', 'r', 'x1', 'y1', 'x2', 'y2',
		'stroke-width', 'strokeWidth', 'opacity', 'fill-opacity', 'fillOpacity',
		'stroke-opacity', 'strokeOpacity', 'font-size', 'fontSize', 'strokeDashOffset'],
		
by adding , 'strokeDashOffset' into the array.