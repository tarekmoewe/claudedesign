---
name: frontend-design
description: Guidance for distinctive, intentional visual design when building new UI or reshaping an existing one. Helps with aesthetic direction, typography, and making choices that don't read as generic or templated.
license: Complete terms in LICENSE.txt
---

# Frontend Design

Approach this as the design lead at a small studio known for giving every client a visual identity that could not be mistaken for anyone else's. This client has already rejected proposals that felt like a template.

## Ground it in the subject

If the brief does not pin down what the product or subject is, pin it yourself before designing: name one concrete subject, its audience, and the page's single job, and state your choice. If there is no clear brief, ask.

## Design principles

For web designs, the hero is a thesis. Open with the most characteristic thing in the subject's world, in whatever form makes sense for it: a headline, an image, an animation, a live demo, an interactive element. The hero is not decoration; it is an argument for why someone should care.

Typography carries the personality of the page. Pair the display and body faces deliberately, not the same families you would reach for on any other project, and set a clear type scale with intention. Let the typography *do* something: establish tone, create hierarchy, carry meaning.

Structure is information. Structural devices, numbering, eyebrows, dividers, labels, should encode something true about the content, not decorate it. Many generic designs use numbered markers (01, 02, 03...) to list steps; if your subject calls for it, name the steps instead. Use visual structure to make the content easier to parse and remember.

Leverage motion deliberately. Think about where and if animation can serve the subject: a page-load sequence, a scroll-triggered reveal, hover micro-interactions, ambient atmosphere. An orchestrated motion language ties the design together; unmotivated animation is noise.

Match complexity to the vision. Maximalist directions need elaborate execution; minimal directions need precision in spacing, type, and detail. Elegance is executing the chosen vision well.

Consider written content carefully. Often a design brief may not contain real content, and it's up to you to come up with copy. Copy can make a design feel as templated as the design itself. See the "More on writing in design" section below.

## Process: brainstorm, explore, plan, critique, build, critique again

For calibration: AI-generated design right now clusters around three looks: (1) a warm cream background (near #F4F1EA) with a high-contrast serif display and a terracotta accent; (2) a near-black background with a bright accent and all sans-serif; (3) a white or light gray background with minimal color and sans-serif. Avoid these defaults unless the brief specifically calls for them.

Work in two passes. First, brainstorm a short design plan based on the human's design brief: create a compact token system with color, type, layout, and signature. Color: describe the palette as 4–5 colors (1 primary, 1 secondary, 1–2 neutrals, 1 accent). Type: pick a display and body family and describe their personality. Layout: identify the grid and any signature layout moves. Signature: name one memorable visual element that will make this design distinct.

Then review that plan against the brief before building: if any part of it reads like the generic default you would produce for any similar page (work through a similar prompt to see if you arrive at the same choice), iterate. Push toward something that only makes sense *for this subject*.

When writing the code, be careful of structuring your CSS selector specificities. It's easy to generate CSS classes that cancel each other out (especially with a type-based selector like .section h1). Use a consistent structure, and avoid nesting selectors too deeply. If you have to write !important, stop and think.

Try to do a lot of this planning and iteration in your thinking, and only show ideas to the user when you have higher confidence it'll delight them.

## Restraint and self-critique

Spend your boldness in one place. Let the signature element be the one memorable thing, keep everything around it quiet and disciplined, and cut any decoration that does not serve the brief. Not every page needs a complex animation, a gradient, or a bespoke illustration. Often the most striking move is choosing *not* to do something.

## More on writing in design

Words appear in a design for one reason: to make it easier to understand, and therefore easier to use. They are design material, not decoration. Bring the same intentionality to copy that you would to color or type.

Write from the end user's side of the screen. Name things by what people control and recognize, never by how the system is built. A person manages notifications, not webhook config. Describe what *happens*, not the mechanism. "Save changes" is better than "commit changes" (outside a git context); "delete this message" is better than "cascade delete." Use the active voice, and use a consistent voice throughout the page.

Use active voice as default. A control should say exactly what happens when it's used: "Save changes," not "Submit." An action keeps the same name through the whole flow, so the button that says "Save changes" triggers a page that might say "Saving…" and then "Changes saved." Parallel structure makes the interface feel coherent.

Treat failure and emptiness as moments for direction, not mood. Explain what went wrong and how to fix it, in the interface's voice rather than a person's. Errors don't apologize, and they are never dismissive ("Oops!"). They are honest and constructive: "This email address is already in use. Try signing in instead." If a page or section is empty (no results, no data yet), help the user understand why and what to do next.

Keep the register conversational and tuned: plain verbs, sentence case, no filler, with tone matched to the brand and the audience. Let each element do exactly one job. A label labels, an example shows, an error explains. If an element is trying to do two things, split it or simplify it.