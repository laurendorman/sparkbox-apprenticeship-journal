# Build Responsively
with Ben Callahan

## RWD 101
*An introduction to Responsive Web Design.*

**Three Core Techniques**
- A Fluid Foundation
- Flexible Content
- Media Queries

**Fluid Foundation** - Honor the proportions of the design by creating percentage-based layout instead of fixed-width, pixel-based layout.

**Flexible Content** - Once we have a layout which is based on proportions, the content must also respond.

**Media Queries** - When our content and our design are no longer working in harmony, we need to make a larger shift in layout.

## RWD Workflow
*The One Deliverable Workflow.*

Content / UX / Design / Front-End / Back-End

**Content & Planning**
- Content Audit
- Information Architecture
- Content Priority Guides
- Content Prototypes
- Static Wireframes
- Interactive Wireframes

**Dissecting Design**
- Establish the Aesthetic
  - Style Comparisons
  - Flat or Textured
  - Illustration vs Photography
  - Style Prototypes
- Solve the Problem
  - Static Design Tools: Photoshop, Sketch, Sketch Books
  - HTML/CSS
  - Layouts vs Modules: Atomic Design
- Refine the Solution
  - Design Pairing

## Serving RWD Styles

In HTML
`<meta name="viewport" content="width=device-width; initial-scale=1.0">`

In CSS
`@viewport { width: device-width;}`

Modifier - `only` or `not`
Media Types - `all` / `screen` / `print` / `speech`
Media Feature - `(min-/max-)width` / `(min-/max-)height` / `device-width` / `device-height` / `orientation` / `aspect-ratio` / `device-aspect-ratio` / `color` / `color-index` / `monochrome` / `resolution` / `scan` / `grid`

## CSS Preprocessing

**Resources**
[LibSass][] - A C implementation, for faster pre-processing
[Structuring and Serving Styles for Older Browsers][]
[Rob Tarr's Media Query Bookmarklet][]
[Pure][] - A CSS grid with a minimal footprint, a good starting point
[SMACSS][] - Scalable and Modular Architecture for CSS

## Creating Flexibility

**What Needs to Flex**
- Grid
- Layout
- Typography
- Images
- Tables
- Videos

**Resources**
[Srcset and Sizes][] by Eric Portis
[Content Choreography][] by Trent Walton
[Off Canvas][] by Jason Weaver

[LibSass]: http://libsass.org/
[Structuring and Serving Styles for Older Browsers]: http://seesparkbox.com/foundry/structuring_and_serving_styles_for_older_browsers
[Rob Tarr's Media Query Bookmarklet]: http://seesparkbox.com/foundry/media_query_bookmarklet
[Pure]: http://purecss.io/
[SMACSS]: https://smacss.com/
[Srcset and Sizes]: http://ericportis.com/posts/2014/srcset-sizes/
[Content Choreography]: http://trentwalton.com/2011/07/14/content-choreography/
[Off Canvas]: http://jasonweaver.name/lab/offcanvas/