# The Book of Margins

> *The margins, the spaces in between contain potential: an infinite canvas of what is not, yet binds what is.*
>
> — Andrey

This book is for anyone, human or AI, who lays out, draws or changes anything visual. Read it before you touch a pixel, and check your work against it before you show anyone.

## The 4 Golden Rules

1. **Respect the margins.**
2. **Respect the resolution.**
3. **Respect the symbolism.**
4. **Respect the functionality.**

They are four rules, but this is one book, because the margins tie all four together. A margin is the space around something, and you cannot respect a space without respecting what it holds: the pixels it frames, the meaning of what sits inside it, and the job that thing has to do. Bad pixels, muddled symbols or a button nobody can press break the margins as surely as an uneven gap does.

---

## Rule 1: Respect the margins

### 1.1 One gap unit
Pick **one gap** for a layout and use it everywhere: element to element, element to frame, frame to screen edge. A second, different gap needs a reason you can say out loud. If you cannot name it, it is a mistake.

### 1.2 Margins are shared
Two neighbours **share** the space between them. The gap between two tiles is the same single gap as tile to frame, not the sum of two private paddings. Sharing is caring: margins overlap where the region is shared.

### 1.3 Measure from what you see
Measure a gap from the frame's **inner edge**, and align to the line the eye actually reads. If a frame has a faint outer ring and a bright inner ring, align to the bright one. A gap that is correct on paper but wrong to the eye is wrong.

### 1.4 Equal both ways
Horizontal gaps equal vertical gaps. "Good, but taller than wide" is not good. Consistent margins say *yes, I respect the conformity.*

### 1.5 Mirror the sides
Left matches right and top matches bottom. If one side is wider, make the sides match. Don't just slide the whole layout over to hide the difference. Paired things (Light and Dark, two trays, two columns) get the same sizes and the same gaps.

### 1.6 Not too tight, not too loose
Nothing touches, crowds or overlaps an edge or a frame. A heading must not sit on a border line, and a tray must not sit on the board. But too much margin is just as wrong. Huge gaps are *i-don't-like-you-you-scare-me-stay-away* margins. Margins are good; too much is weird. When space is left over, grow the content to fill it at a whole-pixel size. Don't grow the gaps.

### 1.7 No empty reserved strips
Don't hold an empty band open "in case" something appears there later. If a label needs a home, put it inside an existing box with that box's padding. If a tray is empty, its space needs a reason to stay, such as stopping the board from jumping, and that reason should be stated.

### 1.8 Cover fully or not at all
An overlay either covers its area completely or leaves it alone. A panel that half-covers something, or a row that sticks out of its own box, looks messy. When a menu opens, **one box** holds everything, laid out as an even grid.

### 1.9 Stay inside the column
A panel is never wider than the column it belongs to. If it doesn't fit, wrap it into even rows.

### 1.10 Centre on the real thing
Centre a count on the piece it counts, a menu between the board and the screen edge, and a label on what it labels. Centre on the drawn art, not on a bounding box that happens to be bigger.

---

## Rule 2: Respect the resolution

### 2.1 One pixel grid
Everything is drawn on the game's own art-pixel grid at its pixel scale: sprites, text, frames, scrollbars, arrows, all of it. No smooth or anti-aliased lines, and no rounded rectangles drawn by the browser.

### 2.2 Whole-number zoom only
One art pixel is a whole number of screen pixels (2, 3, 4…), never 3.5. If that makes the game a little smaller at some window sizes, the smaller size is correct.

### 2.3 No half pixels
Centring something can land it half a pixel off the grid. Round it onto the grid. Arrow shafts and heads land on pixel columns, not between them.

### 2.4 Bigger font, not bigger pixels
When text needs to be larger, use a **larger pixel font** at the same pixel size. Never magnify a small font 2× or 3×. Blowing up the pixels breaks the resolution, even when the result is technically on a grid.

### 2.5 Clean diagonals
A pixel diagonal steps one pixel at a time. If a corner reads as a jagged staircase, it is wrong.

### 2.6 Match the art's resolution
An image placed in the game is resized to the exact box it fills, and its palette is reduced to what that mode allows. The 8-bit mode uses the standard EGA palette, with ordered dithering rather than noisy diffusion. A detail that has turned to speckle after shrinking is redrawn by hand.

---

## Rule 3: Respect the symbolism

### 3.1 One colour, black outline
A symbol is one colour with a black outline. No emoji and no multi-colour icons.

### 3.2 Colours mean something
A colour that stands for something keeps that meaning everywhere. A side's colour marks that side: Dark's box in Dark's colour, Light's box in Light's colour, and the side's name drawn in it. Neutral things get a neutral colour, like the colour used to show movement. Don't reuse a meaningful colour for decoration, and don't pick a colour that clashes with the frame it sits next to.

### 3.3 Faces and shapes are characters
Know what each element is before you draw it. A golem has no teeth and no nose. He looks to the side. His eyes match his piece sprite. Don't add features the character doesn't have, and don't lose the ones it does.

### 3.4 Say what is true
A symbol or label means one thing. `< >` means `< >`, not the arrow keys. Use arrows for arrow keys. Don't write "click" where people also tap. If an instruction isn't true for every user, leave it out.

### 3.5 Scenes fit their place
A picture shows the circumstance it lives in: a battle looks like a battle, and the training yard looks like the training yard.

---

## Rule 4: Respect the functionality

### 4.1 Big enough to use
On touch screens, or wherever buttons drop below a comfortable tap size, gather them into square tiles: an icon with a small label underneath. Use expandable menus rather than shrinking everything.

### 4.2 Fixed things stay fixed
Controls people look for stay in the same place. Back sits fixed at the bottom of a scrollable list, outside the scrolling part, and is still the last item when moving with the keys. A page indicator doesn't move between pages.

### 4.3 Nothing covers what you need
Decorations and demos never sit over a menu someone is using. Lines and arrows draw over frames, pieces draw over their selection frame, and nothing hides the piece it marks.

### 4.4 Every mode, every size
A change is not done until it works in every mode, including 8-bit, and at every size: wide, tall, phone, not full screen.

### 4.5 Don't drop the feature to fix the look
Every action that existed before a layout change still exists after it.

---

## Before you show anyone

Run this on every preview, in every mode and at every size, before you send it.

1. Is there **one gap**, shared between neighbours, measured from the inner edge, and equal horizontally and vertically?
2. Do the sides **mirror**? Do paired boxes have the same size?
3. Does anything **touch, crowd, overlap or poke out** of its frame or column?
4. Is anything **too loose**? Is there an empty strip with no reason?
5. Does every overlay **cover fully or not at all**?
6. Is every pixel on the **grid**, at a **whole-number zoom**, with no magnified fonts and no half pixels?
7. Is every symbol **one colour with a black outline**, and does every colour keep its **meaning**?
8. Does everything still **work**, and is it big enough to press?
9. Did you check the **8-bit** version too?

If any answer is wrong, fix it before anyone else has to point it out.
