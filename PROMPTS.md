# Build Prompts

This project was built using Claude Code CLI. Here's the prompt sequence to recreate it:

## Initial Setup

```
I want to update the website to have a few things. I essentially want to have a site
that looks at an image and gives you a color palette in real time. and as you are
dragging a picker, you can see the shadcn/ui update in real time.
```

## Refining the Flow

```
I just want the image viewer, and a dropper to drag around. I want the dropper to,
in realtime, adjust the shadcn UI toolkit. so, the flow is essentially, i upload an
image, it becomes a surface where I can use a picker, hover over portions of the
image, and see the color palette change in the UI toolkit.
```

## Adding Color Harmonies

```
I will also want to add in 3 standard color selections, like analogous, etc.
you pick three.
```

**Result:** Analogous, Complementary, Triadic harmony modes

## Layout Refinement

```
I want the middle surface as the selection surface. the right will be for me to
view the toolkit change. the left will be a place where I can see past color
selections.
```

## Palette Generation

```
I want it to spawn a color palette when I pick one color. when I select, it should
provide a whole palette.
```

```
analogous, complementary, triadic needs to update the selected palette based on
that color profile definition.
```

## Design Polish

```
Ill want a simplified version of this. again, use shadcn for everything right now:
https://paper.design/
```

## Additional Features

```
I need a refresh button also so I can reset my color selections
```

```
keep the image uploader but have it seed an image from a photo of the day from like
national geographic. for every photo coming from there - keep it as a thumbnail
below the selected image
```

```
when i use a random image, and it selects the image, and I go into color picker
mode, i want to have a button next to reset and random and upload
```

```
link shadcn in the footer so that people can see it
```

## Key Principles

- **Start simple**: Basic functionality first (image + color picker)
- **Iterate quickly**: Add features one at a time
- **Be specific**: Describe the exact flow you want
- **Reference designs**: Link to sites with the aesthetic you want
- **Test as you go**: Verify each feature works before adding more

## Tech Stack Used

- Pure HTML/CSS/JavaScript (single file)
- Tailwind CSS (via CDN)
- shadcn/ui design system
- Canvas API for color extraction
- Picsum Photos API (free, no key required)

## Tips for Using This Approach

1. **Start with the core feature** - In this case: "pick colors from image"
2. **Add UI polish gradually** - Layout → styling → animations
3. **Request specific changes** - "Left panel for history" vs "add a sidebar"
4. **Reference real sites** - Linking to paper.design gave clear design direction
5. **Iterate on features** - Single color → full palette → harmony modes

---

Want to build something similar? Start with the first prompt and work your way down!
