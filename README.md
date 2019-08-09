# BORN Flexbox Grid #

Enhances the useful [flex-grid](http://matthewsimo.github.io/scss-flex-grid/) to provide extra features, such as multi-base grids.

Includes SASS and LESS options, as well as a built CSS and minified file.

## Usage ##

### SASS
**Recommended:** use the node-sass|libSass [includePaths](https://github.com/sass/node-sass#includepaths) option to reference your node folder.

You can setup custom values for your grid. Follow [instructions here](http://matthewsimo.github.io/scss-flex-grid/) for a how to.
		
Additionally, you can set _$fg-columns_ as a list to generate a grid with multiple bases:
   
    $fg-columns: 10, 12, 16;

You can also set different spacing per breakpoint using _$fg-gutter_.
Note: You can skip a breakpoint if you want.
	
    $fg-gutter: (xs: 0.5rem, md: 1rem, lg: 1.5rem);

Set _$fg-use-off-half_ to true to generate -off margin positioning using half a column's width.
	    
    $fg-use-off-half: true;

Finally, import the grid into your file:

	@import 'path/to/node_modules/born-flexgrid/src/flex-grid.scss';
	

### LESS
**Recommended:** use the lessc [--include-path](http://lesscss.org/usage/) option to reference your node folder.

Usage is similar to the SASS setup. The only differences are:

1) Import the .less variant:

        @import 'path/to/node_modules/born-flexgrid/src/flex-grid.less';

2) LESS doesn't support maps, so you must setup your breakpoint variables as a list of lists:
        
        @fg-breakpoints: xs, sm 768px, md 992px, lg 1200px;

	Unlike the SASS version, _@fg-gutter_ must have the same order as _@fg-breakpoints_,
	and must have values for each breakpoint:
	            
        @fg-gutter: xs 0.5rem, sm 0.75rem, md 1rem, lg 1.5rem;