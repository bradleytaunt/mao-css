# Mao CSS Guidelines

An ever expanding CSS guideline. There aren't enough of these already right?

## All files must have follow the guidelines:

- [Table of contents](#table-of-contents)

- [Section Titles](#section-titles)

- [Never Use IDs](#never-use-ids)

- [!important Tags](#!important-tags)

- [No Shorthand](#no-shorthand)

- [Parameter Order](#parameter-order)

- [Nesting Elements](#nesting-elements)

- [Commenting](#commenting)

- [Refactor Before Reaction](#refactor-before-reaction)

- [Mixin and Variable Ideas](#mixin-and-variable-ideas)


### Table of Contents
Maintain a table of contents at the top of every stylesheet. This helps developers quickly glance through the sections of the file.

Example:

```
/*------------------------------------*\
    $CONTENTS
\*------------------------------------*/
/**
 * CONTENTS............You’re reading it!
 * RESET...............Set our reset defaults
 * ELEMENTS............Configure our element defaults
 */
```

### Section Titles
Elements should be grouped into sections based on their function / relation to each other. Be sure to label sections with dollar signs for easier searches.

Example:

```
/*------------------------------------*\
    $RESET
\*------------------------------------*/
reset-box-model()
    border: 0
    margin: 0
    padding: 0
    outline: 0
    
.reset-borders
	border: 0
	outline: 0
```

**ProTip:** Related sections should have `2 return breaks` between them. Unrelated sections should have `5 return breaks`. Also remember to include quasi-qualify selectors.

#### => Quasi-Qualify Selectors

Example:

```
.main-widget
	background-color: yellow
	
	/*h3*/.heading
		padding: 10px
```

### Never Use IDs
Goes without saying - stick to classes. This avoids super-specific selectors.

### !important Tags
Use `!important` tags on helper classes only (think of them as *trump* rules). This also avoids super-specific selectors.

### No Shorthand
**Good** Example:

```
background-color: #f8f8f8
```

**Bad** Example

```
background: #f8f8f8
```

### Parameter Order
All style parameters should be structured alphabetically. This makes it much easier for developers to read through line by line.

**Good** Example:

```
.header-widget
	background-color: #f8f8f8
	border: 1px solid #cccccc
	color: #B8E986
	display: inline-block
	padding: 10px
	width: 100%
```

**Bad** Example:

```
.header-widget
	padding: 10px
	width: 100%
	background-color: #f8f8f8
	display: inline-block
	color: #B8E986
	border: 1px solid #cccccc
```

### Nesting Elements
It's best to just follow common sense nesting rules. The biggest problem to look out for is over-nesting elements. (Remember that super-specific selector problem mentioned before?)

**Good** Example:

```
.header
	border: 1px solid #f8f8f8
	display: block
	
	ul
		li
			display: inline
			margin-right: 10px
		a
			padding: 10px
```

**Bad** Example:

```
.header
	border: 1px solid #f8f8f8
	display: block
	
	ul
		li
			display: inline
			margin-right: 10px
			
			a
				padding: 10px
```

### Commenting
All comments should be detailed and written in block format. You can never have too many comments :).

Example:

```
/**
 * This comment explains what this specific
 * component will do and where it should be used.
 * Detailed comments are great!
 */
.list-navigation
	border-radius: 4px
	display: inline
```

### Refactor Before Reaction
Always take some time to see if you can refactor old elements / code before piling more on top. Adding more styles may fix the problem but will more than likely create others. Keep it simple stupid!


### Mixin and Variable Ideas

- Animations

- Border Radius

- Colors

- Font sizes

- Icons

- Media queries -- ex. `$papa-bear, $mama-bear, $baby-bear`

- Resets

- zindex