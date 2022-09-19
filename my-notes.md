# section 3

## 32

when we set some general css in body or some general parent container for all child elements to inherit not all of the css rules are inherited. only the ones that make sense will get inherited: color, font-family... inheriting border would be impractical. the ones that get inherited are: font-family, font-size, font-weight, font-style, color, line-height, letter-spacing, text-align, text-transform, text-shadow, list-style ...

## 34 css box model

content - padding - border - margin
these are the usual suspects. new one i learned
is fill area - area that gets filled with background image/color
final width and heigh of the element includes
border, padding and content width/height

## 39. CSS Theory #4: Types of Boxes

both display: block and display: inline has their problems. so just use display: inline-block.
one problem that comes to mind quickly is that margin top and bottom doesn't work for inline elements

## 53. Flexbox terminology

we got main axis. we also got cross axis. main axis is the main one, while cross axis is the secondary one.

## 54. Spacing and Aligning items

justify-content aligns items across the main axis. by default that means horizontally
align-items aligns items across the cross axis. by default that means vertically
we have align-items which aligns all items. if we want to align
one specific item we can use align-self on that child element. the property values are the same.
we can also use order property on child element to change the
order that they are in. by default all the child elements have
value of 0 for order. if we assign a value less than 0 to one
child element, it gets in the first place. if we assign greater than 0 it changes its position
to the last place.

## 55. The flex property

flex property is a shorthand for flex-grow, flex-shrink and flex-basis. they work on flex items
not on flex container. also shorthands can be used individually
default values:
flex-grow: 0
flex-shrink: 1
flex-basis: auto

flex: flex-grow(0) flex-shrink(1) flex-basis(auto);

## WEB DESIGN RULES

## 68. web design ingredients and personalities

We can all create good looking websites just by following design rules. For that we don't need to be an artist or creative. All we need to do is to follow those rules and guidelines and follow some system!.
What are INGREDIENTS? they are parts of rules that focus on specific things in web design layout that helps for the design to be considered as good. there are 10 ingredients accoriding to Jonas and each of them has rules we need to follow
Typography
Colors
Images and Illustrations
Icons
Shadows
Border-radius
Whitespace
Visual Hierarchy
User Experience
Components and Layouts

how we decide how to approach these ingredients when designing a website. answer is it depends on the website personality!

we also have [multiple personalities](./assets/website-personalities.png) for a website. depending on the purpose of the website we can lean towards the design rules that matches the one of the personalities.

## 69. Typography

Serif and Sans-serif
Serif. creates traditional and classic look and feel. conveys trustworthiness. good for long text. serif is something that sticks out of the letters such T and or X. if they have small lines sticking out then it's serif. it can be used article or online magazine

Sans-serif. modern look and feel. clean and simple. easier to choose for beginners.

[Rules for typography](./assets/01.typography.png).
TYPEFACES

1. Use only good and popular typefaces and play it safe. ex: Inter, Open Sans, Roboto, Montserrat, Work Sans, Lato (sans-serif)
   ex: Merriweather, Aleo, Playfair Display, Cormorant, Cardo, Lora (serif)
2. limit typefaces to 2. Don't use too many. it will look like ameteur. better just use one
3. choose the right typeface for website. its personality will lead you to the right typeface. decide between serif and sans-serif. experiment with all the famous and most used typefaces
   FONT SIZES AND WEIGHTS
4. when choosing font-sizes, limit choices. Use a 'type scale' tool or other pre-defined range. ex: Miner Third?
5. use a font size between 16px and 32px for 'normal' text
6. for long text (like a blog post or article), try 20px or bigger
7. for headlines, go big (50px+) and boldness of 600+, depenging on personality
8. for any font weight, don't use under 400. below 400 is too light. 400 is regular
   READING EXPERIENCE
9. it's better to use less than 75 characters per line to make it easier to read. if it's too many characters it's hard to changing lines while reading
10. for normal-sized text, use a line height between 1.5 and 2. for big text, go below 1.5. the rule is that if text font-size is small then it's line height should be larger than normal? and if text font-size is big then it's line height should be smaller than normal?
11. decrease letter spacing in headlines, if it looks unnatural!
12. experiment with all caps for short titles. make them small and bold and increase letter-spacing
13. usually, don't justify text
14. don't center long text blocks. small blocks are fine

## 70. implement typography for the website

we chose minimalist and simple website personality. we use sans-serif for clean and modern look. finding Inter sans-serif from google fonts

## 71. colors

CHOOSE THE RIGHT COLOR

1. make the main color match your website's personality: colors conver meaning
2. use a good color tone! don't choose a random tone or css named colors. resources: open color, tailwindcss colors, flat ui colors 2.
   ESTABLISH THE RIGHT COLOR SYSTEM
3. You need at least two types of colors in your color palette: a main color and a grey color
4. With more experience, you can add more colors: accent (secondary) colors (use a tool). (resource: palleton.com or coolors)
5. For diversity, create lighter(tints) and darker(shades) “versions” (resource: tints and shades)
   HOW AND WHEN TO USE COLORS
6. Use your main color to draw attention to the most important elements on
   the page
7. Use colors to add interesting accents or make entire components or sections stand out
8. You can try to use your color strategically in images and illustrations
   COLORS AND TYPOGRAPHY
9. On dark colored backgrounds, try to use a tint of the background (“lighter
   version”) for text
10. Text should usually not be completely black. Lighten if up it looks heavy and uninviting
11. Don’t make text too light! Use a tool to check contrast between text and background colors. contrast ratio needs to be at least 4.5:1 for normal text and 3:1 for large text(18px+)

## 72.

when we have anchor tags and we want to style them, we need to follow this:
first, we use these 2 selectors: `.my-btn:link, .my-btn:visited {...}`
after that we use these 2 selectors: `.my-btn:hover, .my-btn:active {...}`

## 73. photos

USE GOOD IMAGES

1. Different types of images: product photos, storytelling photos, illustrations, patterns
2. Use images to support your website’s message and story. So only use relevant images!
3. Prefer original images. If not possible, use original-looking stock images (not generic ones!). source: unsplash pexels, drawkit, undraw
   USE IMAGES WELL
4. try to show real people to trigger user's emotions
5. if nexessary, crop images, to fit your pages
6. Experiment combining photos, illustrations and patterns
   HOW TO HANDLE TEXT ON IMAGES
7. Method #1: Darker or brighten image (completely or partially, using a gradient)
8. Method #2: Position text into neutral image area
9. Method #3: Put text in a box
   SOME TECHNICAL DETAILS
10. to account for high-res screens, make image dimensions 2x as big as their displayed size. what size means is that imagine we need a picture for our page and it's place takes 300 x 450 px. when we have an image of exactly this size and normal device, there is no problem. but if we have very high res screen device to make the image look crisp it's better if we provided an image with twice the pixel ratio of the place it takes. in our case it's 600 x 900 px. it's called _Scale factor_: Actual pixels the screen contains / Pixels represented on screen
    on high res screens, scale factor is 2x or even 3x, on 'normal' screens it's just 1x (1 physical pixel = 1 design pixel)
11. compress images for a lower file size and better performance. resources: squoosh
12. when using multiple images side-by-side, make sure they have the exact same dimensions

## 74. icons

USE GOOD ICONS

1. use a good icon pack, there are tons of free and paid icons packs. resources: phosphor icons, ionicons, icons8
2. use only one icon pack. don't mix icons from different icon packs
3. use SVG icons or icon fonts becuase they scale indefinitely. don't use bitmap image formats ie jpg and png
4. adjust to website personality. roundness, weight and filled/outlined depend on typography
   WHEN TO USE ICONS
5. use icons to provide visial assistance to text
6. use icons for product feature blocks
7. use icons associated with actions, and label them (unless no space or icon is 100% clear)
8. use icons as bullet points
   USE ICONS WELL
9. To keep icons neutral, use same color as text. To draw more attention, use different color
10. Don’t confuse your users: icons need to make sense and fit the text or action!
11. Don't make icons larger than what they were designed for. If needed, enclose them in a shape
