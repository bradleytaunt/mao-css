# Mao CSS Guidelines

An ever expanding CSS guideline. There aren't enough of these already right?

## All files must have follow the guidelines:

- Table of contents

- Section titles
    -- label sections with dollar signs for easy searches (ex. `$RESET`)

- Never use IDs

- Use `!important` tags on helper classes only (rules that you ALWAYS want to take over)

- No shorthand CSS (use background-color instead of just background)

- 5 return breaks between unrelated sections, 2 breaks if related

- Style parameters are written alphabetically (ex. background -> border -> color -> display etc)

- No over-nesting elements

- Tag comments on specific components

- All comments in block format

- Quasi-qualify selectors (see the `.heading` class in the example below)

- Always see if you can refactor before adding a pile-on solution


## Key variables / mixins:

- Animations

- Border Radius

- Colors

- Font sizes

- Icons

- Media queries -- ex. `$papa-bear, $mama-bear, $baby-bear`

- Resets

- zindex


## Basic Example:

```
/*------------------------------------*\
    $CONTENTS
\*------------------------------------*/
/**
 * CONTENTS............You’re reading it!
 * RESET...............Set our reset defaults
 * ELEMENTS............Configure our element defaults
 */




/*------------------------------------*\
    $RESET
\*------------------------------------*/
reset-box-model()
    border: 0
    margin: 0
    padding: 0
    outline: 0

/**
 * This comment explains what this specific
 * component will do and where it should be used.
 * Detailed comments are great!
 */
.super-reset-modal
    text-transform: uppercase




/*------------------------------------*\
    $ELEMENTS
\*------------------------------------*/
.widget
    background-color: #C0FFEE
    border: 1px solid #BADA55
    border-radius: sRadius
    color: #f8f8f8
    display: inline-block
    fontsize(18)
    padding: 10px

    /*h3*/.heading
        background-color: #ffffff
        color: #000000
        padding: 10px

```