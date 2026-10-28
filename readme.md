# The Book of Margins

> *The margins, the spaces in between contain potential: an infinite canvas of what is not, yet binds what is.*
>
> — Andrey

This book is for anyone, human or AI, who lays out, draws or changes anything visual: a game, a website, an app, a document. Read it before you touch a pixel, and check your work against it before you show anyone.

The rules are general. The examples come from Monster Chess, where they were learned. Your project will have its own pixels, colours and meanings, so translate each example into the terms of the thing you are working on.

## The 4 Golden Rules

1. **Respect the margins.**
2. **Respect the resolution.**
3. **Respect the symbolism.**
4. **Respect the functionality.**

They are four rules, but this is one book, because the margins tie all four together. A margin is the space around something, and you cannot respect a space without respecting what it holds: the pixels it frames, the meaning of what sits inside it, and the job that thing has to do. Bad pixels, muddled symbols or a button nobody can press break the margins as surely as an uneven gap does.

---

## Rule 1: Respect the margins

**Margin and padding are the same thing seen from two sides of a border.** Padding is the margin inside a border: the space between the border and what it holds. Margin is the padding outside a border: the space between the border and its neighbours. Both are empty space that keeps things apart, so every rule in this book applies to both. When this book says "margin", it means either one.

### 1.1 One gap unit
Pick **one gap** for a layout and use it everywhere: element to element, element to frame, frame to screen edge. A second, different gap needs a reason you can say out loud. If you cannot name it, it is a mistake.

### 1.2 Margins are shared
Two neighbours **share** the space between them. The gap between two cards is the same single gap as card to container, not the sum of two private paddings. *Sharing is caring: margins overlap where the region is shared.*

*Example:* in a menu grid, the space between two tiles equals the space between a tile and the frame, measured once.

### 1.3 Measure from what you see
Measure a gap from a frame's **inner edge**, and align to the line the eye actually reads. If a border has a faint outer edge and a strong inner one, align to the strong one. A gap that is correct in the code but wrong to the eye is wrong.

*Example:* side boxes lined up with the faint outer ring of the board's frame looked two pixels off, because the eye reads the bright ring as the edge.

### 1.4 Equal both ways
Horizontal gaps equal vertical gaps. "Good, but taller than wide" is not good. *Consistent margins say yes, I respect the conformity.*

### 1.5 Mirror the sides
Left matches right and top matches bottom. If one side is wider, make the sides match. Don't just slide the whole layout over to hide the difference. Paired things (two sidebars, two columns, two players' panels) get the same sizes and the same gaps.

### 1.6 Not too tight, not too loose
Nothing touches, crowds or overlaps an edge or a frame. A heading must not sit on a border line. But too much margin is just as wrong. Huge gaps are *i-don't-like-you-you-scare-me-stay-away* margins. Margins are good; too much is weird. When space is left over, grow the content to fill it. Don't grow the gaps.

### 1.7 No empty reserved space
Don't hold an empty band open "in case" something appears there later. If a label needs a home, put it inside an existing box with that box's padding. If an empty area has to stay, for example so the layout doesn't jump, say why.

### 1.8 Cover fully or not at all
An overlay, modal or menu either covers its area completely or leaves it alone. A panel that half-covers something, or a row that sticks out of its own box, looks messy. When a menu opens, **one box** holds everything, laid out as an even grid.

### 1.9 Stay inside the column
A panel is never wider than the column it belongs to. If it doesn't fit, wrap it into even rows.

### 1.10 Centre on the real thing
Centre a label on what it labels, a badge on the item it counts, and a block in the space it actually has. Centre on the visible content, not on a bounding box that happens to be bigger. Text inside a box sits with equal space above and below.

---

## Rule 2: Respect the resolution

Every project has a native resolution: the grid its art is drawn on, the device pixels of the screen, the size its images were made for. Work on that grid.

### 2.1 Draw on the native grid
Everything sits on the project's grid. In pixel art, that is the art-pixel grid at its scale, and that covers sprites, text, frames, scrollbars and arrows alike, with no smooth lines and no browser-rounded corners. On a regular site, it means crisp edges on whole device pixels, with no blurry half-pixel borders.

### 2.2 Whole-number scaling only
Scale by whole numbers. One art pixel is 2, 3 or 4 screen pixels, never 3.5. If that makes something a little smaller at some window sizes, the smaller size is correct.

### 2.3 No half pixels
Centring can land something half a pixel off the grid. Round it back onto the grid. Lines and arrowheads land on pixel columns, not between them.

### 2.4 Bigger font, not bigger pixels
When text needs to be larger, use a **larger font**, not a magnified small one. Never blow up a font, an icon or an image 2× or 3× to make it bigger. It breaks the resolution, even when the result is technically on a grid.

### 2.5 Clean diagonals and corners
A pixel diagonal steps one pixel at a time. If a corner reads as a jagged staircase, it is wrong.

### 2.6 Images fit their box
An image is made or resized for the exact box it fills, and for the palette or quality the medium allows. Don't stretch, upscale or shrink it until it turns to noise. A detail that has turned to speckle after shrinking is redrawn.

*Example:* the 8-bit mode uses the standard EGA palette, with ordered dithering rather than noisy diffusion.

---

## Rule 3: Respect the symbolism

### 3.1 Learn the project's language first
Before you draw, colour or label anything, find out what the project's colours, shapes, icons and characters already mean. Every project has its own symbolism: a brand colour, a status colour, an icon style, a mascot. Your job is to keep that meaning consistent, not to invent a new one.

*Example:* in Monster Chess, orange means Light, magenta means Dark, and cyan, a light blue, is the neutral colour. A deeper blue would sit too close to purple and blur into Dark. Warm orange or yellow for light and magenta or purple for dark is a pairing that carries well to other projects. On a store site, the same roles might be the brand colour, the sale colour and the neutral UI colour.

### 3.2 Colours mean something
A colour that stands for something keeps that meaning everywhere. Don't reuse a meaningful colour for decoration. Give neutral things a neutral colour, and don't pick a colour that clashes with what it sits next to.

*Example:* each side's box is framed in that side's colour, and the side's name is drawn in it. The narrator's box is neutral.

### 3.3 One icon style
Icons share one consistent style. No emoji and no mixing of icon sets.

*Example:* Monster Chess icons are one colour with a black outline.

### 3.4 Characters stay in character
Know what each element is before you draw it. Don't add features a character, logo or mark doesn't have, and don't lose the ones it does.

*Example:* the golem has no teeth and no nose, looks to the side, and his eyes match his piece sprite.

### 3.5 Say what is true
A symbol or label means one thing. `< >` means `< >`, not the arrow keys. Use arrows for arrow keys. Don't write "click" where people also tap. If an instruction isn't true for every user, leave it out.

### 3.6 Pictures fit their place
An image shows the context it lives in.

*Example:* a battle scene looks like a battle, and the training yard looks like the training yard.

---

## Rule 4: Respect the functionality

### 4.1 Big enough to use
On touch screens, or wherever controls drop below a comfortable tap size, gather them into larger targets: square tiles with an icon and a small label, or expandable menus. Don't shrink everything to make it fit.

### 4.2 Fixed things stay fixed
Controls people look for stay in the same place. Back sits fixed at the bottom of a scrollable list, outside the scrolling part, and is still the last item when moving with the keys. A page indicator doesn't move between pages.

### 4.3 Nothing covers what you need
Decorations, banners and demos never sit over a menu someone is using. Highlights and markers never hide the thing they mark.

*Example:* the move line draws over the selection frame, and the piece draws over its frame.

### 4.4 Every mode, every size
A change is not done until it works in every mode and theme (dark, light, 8-bit, whatever the project has) and at every size: wide, tall, phone, not full screen.

### 4.5 Don't drop the feature to fix the look
Every action that existed before a layout change still exists after it.

---

## Before you show anyone

Run this on every preview, in every mode and at every size, before you send it.

1. Is there **one gap**, shared between neighbours, measured from the inner edge, and equal horizontally and vertically?
2. Do the sides **mirror**? Do paired boxes have the same size?
3. Does anything **touch, crowd, overlap or poke out** of its frame or column?
4. Is anything **too loose**? Is there empty space with no reason? Is text centred in its box?
5. Does every overlay **cover fully or not at all**?
6. Is everything on the **native grid**, at **whole-number scaling**, with no magnified fonts or images and no half pixels?
7. Does every colour, icon and character keep its **meaning** in this project?
8. Does everything still **work**, and is it big enough to press?
9. Did you check **every mode and size**?

If any answer is wrong, fix it before anyone else has to point it out.
