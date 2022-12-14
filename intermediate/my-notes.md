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
5. For diversity, create lighter(tints) and darker(shades) ???versions??? (resource: tints and shades)
   HOW AND WHEN TO USE COLORS
6. Use your main color to draw attention to the most important elements on
   the page
7. Use colors to add interesting accents or make entire components or sections stand out
8. You can try to use your color strategically in images and illustrations
   COLORS AND TYPOGRAPHY
9. On dark colored backgrounds, try to use a tint of the background (???lighter
   version???) for text
10. Text should usually not be completely black. Lighten if up it looks heavy and uninviting
11. Don???t make text too light! Use a tool to check contrast between text and background colors. contrast ratio needs to be at least 4.5:1 for normal text and 3:1 for large text(18px+)

## 72

when we have anchor tags and we want to style them, we need to follow this:
first, we use these 2 selectors: `.my-btn:link, .my-btn:visited {...}`
after that we use these 2 selectors: `.my-btn:hover, .my-btn:active {...}`

## 73. photos

USE GOOD IMAGES

1. Different types of images: product photos, storytelling photos, illustrations, patterns
2. Use images to support your website???s message and story. So only use relevant images!
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

1. use a good icon pack, there are tons of free and paid icons packs. resources: phosphor icons, ionicons, icons8, heroicons
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
10. Don???t confuse your users: icons need to make sense and fit the text or action!
11. Don't make icons larger than what they were designed for. If needed, enclose them in a shape

## 75. implement icons

we used some svg icons and to change its colors we used `stroke` css attribute for outline icons. for solid icons we can use `fill` attribute to give color to the icon

## 76. shadows

shadows can help users identify relationships between items in the web page or they can be used to add visual details to items
some history first: around 2010, all interfaces had skeuomophic design -> lots of shades and glossy effects and realistic effects. after ios 8 flat design (minimal) rules but caused some usability problems. after that flat design 2.0 came to existence which gave items some shadows and depth. which is still minimal but brings back shadows and depth for better usability.
shadows bring out or stimulate depth for an item in user interface. more shadow an item has the further away from the iterface the element looks or in other words shadows allow us to add 3 dimension to our element

shadows can be used on boxes and text

USE SHADOWS WELL

1. You don???t have to use shadows! Only use them if it makes sense for the
   website personality
2. Use shadows in small doses: don???t add shadows to every element!
3. Go light on shadows, don???t make them too dark!
   USE SHADOWS IN THE RIGHT SITUATIONS
4. Use small shadows for smaller elements that should stand out (to draw attention). such as input elements. we might need the user pay attention to input form or maybe we use shadows for images
5. Use medium-sized shadows for larger areas that should stand out a bit more. such as big banner or cards
6. Use large shadows for elements that should really float above the interface. modals, navigations and popup windows
7. Experiment with changing shadows on mouse interaction (click and hover). on hover show shadow or icrease shadow and on click decrease shadow to simulate being pushed to the ground or to the interface
8. Bonus: Experiment with glows (colored shadows). ex: for a button of particular color, if we give a shadow of that same color it gives an effect of glowing

# 77. implement box shadow

for container elements we use `box-shadow` and for text we use `text-shadow`. we might use shadow for text when it comes on top of some image

LOOK UP box-shadow on MDN for its properties

# 78. border-radius

USE BORDER-RADIUS WELL

1. border-radius increase playfulness and fun of the design and make it less serious
2. pay attention to the typefaces we are using. they might have some level of roundness. we need to make sure that border-radius matches that roundness
3. buttons, images, around icons, standout sections are conadidates for border-radius

# 80. whitespace

the right amount of whitespace makes designs look clean, modern and polished
it communicates how different pieces of inf are related to one another
it implies invisible relationships between the elements of a layout

WHERE TO USE WHITESPACE

1. use tons of whitespace between sections
2. use a lot of whitespace between groups of elements but not as much as sections
3. use whitespace between smaller elements
4. inside groups of elements try to use whitespace instead of lines. using lines is old skul
   HOW MUCH WHITESPACE
5. the more some elements belong together, the closer they should be. meaning if they belong to the same group they should have smaller whitespace than the whitespace that is used to another group of elements. this is called `the law of proximity`.
6. start with a lot of whitespace and then remove whitespace from there until it looks nice. too much whitespace looks detached, too little looks detached
7. match other design choices. if big text or big icons then more whitespace is needed
8. try a hard rule such as using multiples of `16px` for all spacing: 2 px, 4px, 8px, 12px, 16px, 24px, 32 px, 48px, 64px ...

## 81. visual hierarchy

visual hierarchy is about establishin gwhich elements of a design are the most important ones. it's about drawing attention to these most important elements. it's also defining a path for users to guide them through the page. combination of position, size, colors, spacing, borders and shadows are mainly used to establish a meaningful visual hierarchy between elements/components

VISUAL HIERARCHY FUNDAMENTALS

1. position important elements to closer to the top of the page, where they get more attention. let's not get confused here. it doesn't mean the important element should be at the top but it could also be closer to the top and the next important element doesn't have to be the next thing but being closer to the first one works okay
2. images need to be used mindfully since they draw attention. the larger they are more attention they get
3. whitespace creates separation, so use whitespace strategically to emphasize elements

VISUAL HIERARCHY FOR TEXT ELEMENTS

4. use font size, font weight, color and whitespace to convey importance for text elements
5. what items should be emphasized? titles, sub-titles, links, buttons, data points, icons. texts can also be de-emphasized such as lables or secondary or additional information
   VISUAL HIERARCHY BETWEEN COMPONENTS
6. emphasize an important component using background color, shadow or border or multiple of them
7. try emphasizing some component A over component B by de- emphasizing component B
8. What components to emphasize? Testimonials, call-to-action sections, highlight sections, preview cards, forms, pricing tables, important rows/columns in tables, etc.

## 83. User Experince (UX)

UX RULES FOR USABILITY
UX is how it looks as well as how it works

1. don't design complicated layouts. don't reinvent the wheel. use patterns that users know
2. make your call-to-action the most prominent element and make the descriptive. we are talking about the button here!
3. use blue text and underlined text only for links
4. animations should have a purpose and be fast: between 200 and 500ms
5. in forms, align labels and fields in a single vertical line, to make the form easier to scan
6. offer users good feedback for all actions: form errors, form success, etc [web apps]
7. place action buttons where they will create an effect (law of locality) [web apps]
   UX RULES FOR WEBSITE CONTENT
8. ues a descriptive keyword focused headline on your main page. don't be vague or fancy
9. only include relevant information, efficiently! cut out fluff and make the content 100% clear
10. use simple words! avoid technical jargon and smart-sounding words
11. break up long text with sub-headings, images, block quotes, bullet points, etc

## 85. steal like an artist

resources for inspiration: land-book.com onepagelove.com/inspiration awwwards.com screenlane.com

## components and layout patterns

## 87. elements and components

FROM ELEMENTS TO WEBPAGE
a very great point by the teacher. when i start building a website for my project and always start with white canvas and don't know what to do. his advice in this case is to never panic and just start with simple and small things and try to group some elements such as buttons titles paragraphs into components and try to create multiple components and try to group them as well. then you will have some rough idea about how to design it and work on it further. okay no so much like this <- kkkk. so we try to create components with elements and create a layout with these components. and the catch is don't just try to create a layout on your own instead use existing famous layouts which are proven to be good designs. and in the end assemble he components into layouts and compose your webpage

1. use common elements and components to convey your website's information
2. combine components into layouts using common layout patterns
3. assemble different layout areas into a complete, final page

## 99. building web application layout pt 2

we have flex container and many childs. we want them scrollable and not overflow the viewport. naturally we use `overflow: scroll` on container and this causes child elements to shrink. remember that flex-shrink for child elements is set 1 which means if necessary they are shrinkable. to avoid that we set flex-shrink to 0 on child elements and they retrieve any lost css that we gave

## OMNIFOOD project

## 105. Responsive Design Principles

WHAT IS RESPONSIVE DESIGN

- design technique to make a webpage adjust its layout and visual style to any possible screen size (window or viewport size)
- Inpractice,thismeansthatresponsivedesignmakeswebsitesusableon all devices, such as desktop computers, tablets, and mobile phones.
- It???s a set of practices, not a separate technology. It???s all just CSS!

RESPONSIVE DESIGN INGREDIENTS
[Rules for typography](./assets/resp-des-ingr.png).

1. FLUID LAYOUTS
2. RESPONSIVE UNITS
3. FLEXIBLE IMAGES
4. MEDIA QUERIES

## 106. how rem and max-width work?

`max-width` means if parent container width is bigger than max-width then the child element (which has max-width given) cannot get bigger than the max-width. that means it will not grow. if container width is smaller than child element's max-width then child element gets 100% of the width of the parent container. it will fill the width of parent container element and it will stop filling/increasing its width once parent elements gets bigger than max-width of the child element

what does **rem** mean? rem means _root element's font size_. what element is considered root element? it's html element that is root element of the document. if we don't define font-size on this `html` element then 1 rem is equal to the default browser font-size which is always 16px unless the user does change it.
changing the font-size affects all defined rem units. it may also be handy when we need to change all the sizes at once. but due to accessibility purposes we don't change it. but instead we can set root element font-size to a percentage unit.
there is a formula for coming up with a percentage that we want root element to be. if we want root element to be 10px we can come up with percentage value by dividing 10 by 16. so the formula is:

```
T / D = P
```

- T = target px value
- D = root element default value - 16px
- P = percentage value

## 113. Building how it works p1

\*\* images should be first thing we need to style becuase they don't automatically scale up or down like text. that's why we need to give them 100% width to fit into parent container

## 113. Building how it works p2

we are not allowed to add child elements to `img` tag. which should be obvious when you think about it. it's a self closing tag. so this means we cannot add `::before` pseudo element to `img` tag

## 126. Building cta section

in our css if we select buttons only with :link and :visited pseudo selectors we need to make sure that the button we are styling has href attribute. otherwise css selector doesn't select the button with no href attribute

## 130. How media queries work

we need to be careful about the order of media queries. if conflicting media queries exist the last one is applied
