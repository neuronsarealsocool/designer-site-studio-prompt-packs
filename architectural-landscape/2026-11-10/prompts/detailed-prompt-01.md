You are a senior creative developer, motion designer, and WordPress block-theme engineer.

Build a premium, cinematic real-estate website for a fictional luxury property brand named “Architectural Landscape.”

The visual and motion direction should closely follow the supplied reference screenshots and the existing golden-hour landscape/property assets inside \`/assets/images\`, without copying the original reference brand, wording, logo, or exact layout.

The result must feel like one continuous vertical world rather than separate full-screen images placed underneath each other.

Important visual direction:  
This project should be created in an orangish-yellow golden-hour tone from the beginning.

Do not create a purple/lavender/pink version first.  
Do not use purple as the base theme.  
Do not add orange tint over purple assets when real orange/golden assets exist.  
Use the newly supplied orange, yellow, amber, golden-hour images as the primary source of truth.

Do not ask me to manually identify the image files. Inspect the assets, determine their intended roles, and proceed using your best judgment.

\======================================================================  
1\. PRIMARY OBJECTIVE  
\======================================================================

Create:

1\. A working front-end preview that can be opened and reviewed immediately.  
2\. A production-ready WordPress block theme containing the same experience.  
3\. Gutenberg-editable blocks for all meaningful content and images.  
4\. Smooth, stable parallax and scroll-based motion without visual jumps, seams, layout shifts, or mobile glitches.

The website should use the generated assets in \`/assets/images\`, including these visual categories where available:

\- Orange/yellow cloud sky background.  
\- Central mountain with modern glass residence.  
\- Orange/golden mountain or rocky landscape cutout.  
\- Orange cloud \+ mountain PNG for hero parallax.  
\- Left-aligned mountain landscape in golden-hour tone.  
\- Golden mist / cloud continuation images.  
\- Transparent PNG foreground layers.  
\- 4:3 residence images for property cards.  
\- Any additional related golden-hour real-estate or landscape assets found in the directory.

Do not generate new images.  
Do not download external stock imagery.  
Do not use old purple/lavender images unless there is no suitable orange/golden replacement.

\======================================================================  
2\. FIRST STEP: INSPECT AND MAP THE ASSETS  
\======================================================================

Before writing the interface:

1\. Recursively inspect \`/assets/images\`.  
2\. Collect:  
   \- Filename  
   \- File type  
   \- Width and height  
   \- Aspect ratio  
   \- Whether the image contains a real alpha channel  
   \- Whether it belongs to the orange/golden set or an older purple set  
   \- Approximate visual role  
3\. Create an asset manifest at:  
   \`/docs/asset-manifest.md\`

Assign each relevant image one of these roles:

\- hero-sky  
\- hero-building-mountain  
\- hero-cloud-mountain-parallax  
\- hero-foreground-mountain  
\- hero-mist-overlay  
\- transition-landscape-one  
\- transition-landscape-two  
\- story-background  
\- section-background  
\- residence-alpine-glasshouse  
\- residence-cliff-residence  
\- residence-desert-courtyard  
\- residence-additional-one  
\- residence-additional-two  
\- residence-additional-three  
\- optional-estate-image

Use visual inspection rather than relying only on filenames.

Transparent PNGs should normally be rendered as independent parallax layers.

Opaque landscape images should normally be used as full-width backgrounds or continuation panels.

Important:  
Do not assume a PNG is transparent just because the file extension is \`.png\`. Check whether it has a real usable alpha channel.

Record the recommended \`object-position\`, scale, and parallax depth for each image in the manifest.

\======================================================================  
3\. BRAND DIRECTION  
\======================================================================

Brand name:  
Architectural Landscape

Brand positioning:  
A private real-estate advisory and curated collection of architecturally significant residences in extraordinary landscapes.

Personality:

\- Refined  
\- Quietly confident  
\- Cinematic  
\- Contemporary  
\- Private  
\- International  
\- Design-led  
\- Warm  
\- Architectural  
\- Never flashy or sales-heavy

The page should feel like:

\- Golden hour  
\- Warm architectural lighting  
\- Amber mist  
\- Sunlit stone  
\- Desert/coastal luxury  
\- Premium editorial real estate

Suggested color system should be sampled from the supplied golden-hour graphics.

Use these only as fallback values:

\- Deep umber: \#160E08  
\- Burnt cedar: \#3A1D0C  
\- Warm bronze: \#8C4A16  
\- Ember orange: \#D86A1F  
\- Golden amber: \#F2A93B  
\- Sunlit yellow: \#FFD77A  
\- Sand mist: \#F4D7A1  
\- Warm ivory: \#FFF4DF  
\- Soft parchment: \#F6E6C8  
\- Dark text: \#21170E

Avoid using these as the main palette:

\- Violet  
\- Purple  
\- Lavender  
\- Pink-magenta  
\- Blue-purple shadows

Create reusable CSS custom properties for all colors, spacing, typography, radii, shadows, container widths, and motion durations.

Typography:

\- Elegant modern sans-serif.  
\- Large editorial headings.  
\- Clean, readable body text.  
\- Avoid decorative luxury serif clichés unless a suitable bundled font already exists.  
\- Do not depend on Google Fonts at runtime.  
\- Bundle any permitted webfonts locally or use a strong system-font fallback.

\======================================================================  
4\. GLOBAL VISUAL TONE  
\======================================================================

The site should not look like orange images placed inside an old purple UI.

Use a cohesive golden-hour visual system.

Important:

\- Navigation glass should be warm dark brown / deep umber, not purple.  
\- Buttons should use warm ivory and deep brown text.  
\- Section backgrounds should use warm mist, parchment, amber haze, or deep umber.  
\- Text highlight effects should brighten toward warm ivory or pale gold.  
\- Cards should use warm dark overlays, not violet overlays.  
\- Metrics section should transition into a soft warm parchment background.  
\- Footer should use deep umber or burnt cedar.  
\- Borders should be warm bronze, amber, or soft ivory with low opacity.  
\- Shadows should feel warm and cinematic, not blue/purple.

Remove or avoid:

\- Purple overlays  
\- Violet tints  
\- Lavender backgrounds  
\- Blue-purple shadows  
\- Pink/purple gradient masks  
\- Any visual treatment that makes the site feel lavender

Replace them with:

\- Amber gradients  
\- Warm mist  
\- Soft golden haze  
\- Deep brown/navy-black contrast  
\- Sunlit orange highlights

Keep contrast accessible.

\======================================================================  
5\. PAGE STRUCTURE AND CONTENT  
\======================================================================

Build the following sections.

\----------------------------------------------------------------------  
A. Floating navigation  
\----------------------------------------------------------------------

Create a floating translucent navigation bar similar in spirit to the reference:

Left:  
\- Simple geometric Architectural Landscape symbol  
\- “Architectural Landscape”

Navigation:  
\- Home  
\- Philosophy  
\- Residences  
\- Approach  
\- Contact

Right:  
\- “Private consultation” button

Behavior:

\- Floating glass panel.  
\- Rounded shape.  
\- Subtle backdrop blur.  
\- Warm deep-umber / burnt-cedar glass tone.  
\- Becomes slightly more compact while scrolling.  
\- Remains readable over every background.  
\- Mobile navigation must be accessible and fully functional.  
\- Do not use the Aether Lane name or logo.  
\- Do not place the navigation inside an animated transform layer.

\----------------------------------------------------------------------  
B. Cinematic parallax hero  
\----------------------------------------------------------------------

Build a layered hero using the supplied golden-hour image assets.

Use the fewest layers required for a clean, cinematic result.

Recommended layer order:

1\. Orange/yellow cloud sky background.  
2\. Large split headline behind the central mountain/building.  
3\. Central mountain and glass residence.  
4\. Orange cloud \+ mountain PNG parallax layer, if it blends cleanly.  
5\. Warm mist / cloud seam overlay.  
6\. Hero copy and navigation.

Do not stack multiple opaque 16:9 landscape images in the hero.  
Do not create hard horizontal image boundaries.  
Do not cover the central residence with unrelated cloud layers.  
Do not add fake orange tint over purple images if real orange assets exist.

Suggested copy:

Eyebrow:  
PRIVATE RESIDENCES. EXTRAORDINARY PERSPECTIVES.

Heading split into two editable parts:

Left phrase:  
Live beyond

Right phrase:  
the expected.

Supporting text:  
Architectural Landscape curates architecturally distinct homes in remarkable settings for people who value privacy, design, and a deeper sense of place.

Buttons:  
\- Explore the collection  
\- Speak with an advisor

Optional small labels:  
\- Elevated living, thoughtfully placed  
\- Private residences across exceptional landscapes

Desktop headline composition:

\- Place “Live beyond” on the left side of the mountain.  
\- Place “the expected.” on the right side of the mountain.  
\- Keep both phrases on approximately the same visual baseline.  
\- The mountain should sit between and partially in front of the two text groups.  
\- The text must feel like one sentence passing behind the mountain.  
\- Part of the text may be naturally obscured by the mountain silhouette.  
\- Do not cover so much text that the phrase becomes unreadable.  
\- Do not place the entire heading as one oversized block fully in front of the scene.  
\- Do not add a translucent rectangle behind the headline.

Required hero layer order:

\- Sky: lowest  
\- Headline: above sky  
\- Central mountain/building: above headline  
\- Mist and parallax clouds: above lower mountain edge where useful  
\- Navigation and clickable content: highest interactive layer

Example desktop logic:

\[ Live beyond \]       \[central mountain/building\]       \[ the expected. \]

The mountain should visually overlap the final portion of the left phrase and the opening portion of the right phrase.

Typography:

\- Large editorial type.  
\- Warm ivory, pale gold, or soft cream.  
\- Avoid cold pure white if it clashes with the golden palette.  
\- \`font-size: clamp(4.5rem, 8.8vw, 10rem)\`  
\- Tight line height around \`0.86–0.94\`  
\- Slight negative letter spacing.

Mobile behavior:

\- Stack the phrase into two readable lines.  
\- Keep the mountain subtly overlapping the text.  
\- Do not force the desktop left/right arrangement onto narrow screens.  
\- Prevent clipping.

Hero motion:

\- Use a tall scroll scene of approximately 170–220vh.  
\- Keep the visual composition sticky for part of the scroll.  
\- Sky moves the least.  
\- Central residence moves slightly faster than the sky.  
\- Orange cloud/mountain parallax layer moves slightly faster.  
\- Mist moves independently and gently.  
\- Supporting copy fades and moves upward before the next section.  
\- Avoid exaggerated zooming.  
\- The scene should feel like the viewer is slowly moving through a warm golden landscape.

Suggested relative movement:

\- Sky: 0 to 4–8vh  
\- Headline: 0 to \-8vh  
\- Central residence mountain: 0 to \-12/-16vh  
\- Cloud/mountain parallax PNG: 0 to \-18/-26vh  
\- Mist: 4vh to \-5vh with subtle opacity adjustment  
\- Supporting content: fade and move upward near the end

Use transforms and opacity only.

Avoid animating:

\- \`top\`  
\- \`bottom\`  
\- \`height\`  
\- \`margin\`  
\- z-index  
\- background-position on huge images

Decorative parallax layers must use:

\`\`\`css  
pointer-events: none;

**\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\***

**Old Prompts**

**1st Used in Video**

You are a senior creative developer, motion designer, and WordPress block-theme engineer.

Build a premium, cinematic real-estate website for a fictional luxury property brand named “Architectural Landscape.” The visual and motion direction should closely follow the supplied reference screenshots and the existing landscape assets inside \`/assets/images\`, without copying the original reference brand, wording, logo, or exact layout.

The result must feel like one continuous vertical world rather than separate full-screen images placed underneath each other.

Do not ask me to manually identify the image files. Inspect the assets, determine their intended roles, and proceed using your best judgment.

\======================================================================  
1\. PRIMARY OBJECTIVE  
\======================================================================

Create:

1\. A working front-end preview that can be opened and reviewed immediately.  
2\. A production-ready WordPress block theme containing the same experience.  
3\. Gutenberg-editable blocks for all meaningful content and images.  
4\. Smooth, stable parallax and scroll-based motion without visual jumps, seams, layout shifts, or mobile glitches.

The website should use the generated assets in \`/assets/images\`, including the following visual categories where available:

\- Purple and pink sunset sky background.  
\- Central mountain with a modern glass residence.  
\- Foreground mountain or rocky landscape cutout.  
\- Left-aligned mountain landscape.  
\- Purple cloud and mist continuation images.  
\- Transparent PNG foreground layers.  
\- Any additional related landscape assets found in the directory.

Do not generate new images and do not download external stock imagery.

\======================================================================  
2\. FIRST STEP: INSPECT AND MAP THE ASSETS  
\======================================================================

Before writing the interface:

1\. Recursively inspect \`/assets/images\`.  
2\. Collect:  
   \- Filename  
   \- File type  
   \- Width and height  
   \- Aspect ratio  
   \- Whether the image contains an alpha channel  
   \- Approximate visual role  
3\. Create an asset manifest at:  
   \`/docs/asset-manifest.md\`

Assign each relevant image one of these roles:

\- hero-sky  
\- hero-building-mountain  
\- hero-foreground-mountain  
\- hero-mist-overlay  
\- transition-landscape-one  
\- transition-landscape-two  
\- story-background  
\- section-background  
\- optional-estate-image

Use visual inspection rather than relying only on filenames.

Transparent PNGs should normally be rendered as independent parallax layers. Opaque landscape images should normally be used as full-width backgrounds or continuation panels.

Record the recommended \`object-position\`, scale, and parallax depth for each image in the manifest.

\======================================================================  
3\. BRAND DIRECTION  
\======================================================================

Brand name:  
Architectural Landscape

Brand positioning:  
A private real-estate advisory and curated collection of architecturally significant residences in extraordinary landscapes.

Personality:

\- Refined  
\- Quietly confident  
\- Cinematic  
\- Contemporary  
\- Private  
\- International  
\- Design-led  
\- Never flashy or sales-heavy

Suggested color system should be sampled from the supplied graphics.

Use these only as fallback values:

\- Deep ink: \#100B24  
\- Midnight violet: \#241B55  
\- Horizon violet: \#695AC7  
\- Lavender mist: \#BCA8EE  
\- Soft rose: \#F2B6D4  
\- Cloud white: \#F7F4FC  
\- Pale background: \#EEE8F8  
\- Body text: \#211A34

Create reusable CSS custom properties for all colors, spacing, typography, radii, shadows, container widths, and motion durations.

Typography:

\- Elegant modern sans-serif.  
\- Large editorial headings.  
\- Clean, readable body text.  
\- Avoid decorative luxury serif clichés unless a suitable bundled font already exists.  
\- Do not depend on Google Fonts at runtime.  
\- Bundle any permitted webfonts locally or use a strong system-font fallback.

\======================================================================  
4\. PAGE STRUCTURE AND CONTENT  
\======================================================================

Build the following sections.

\----------------------------------------------------------------------  
A. Floating navigation  
\----------------------------------------------------------------------

Create a floating translucent navigation bar similar in spirit to the reference:

Left:  
\- Simple geometric Architectural Landscape symbol  
\- “Architectural Landscape”

Navigation:  
\- Home  
\- Philosophy  
\- Residences  
\- Approach  
\- Contact

Right:  
\- “Private consultation” button

Behavior:

\- Floating glass panel.  
\- Rounded shape.  
\- Subtle backdrop blur.  
\- Becomes slightly more compact while scrolling.  
\- Remains readable over every background.  
\- Mobile navigation must be accessible and fully functional.  
\- Do not use the Aether Lane name or logo.

\----------------------------------------------------------------------  
B. Cinematic parallax hero  
\----------------------------------------------------------------------

Build a layered hero using the supplied image assets.

Recommended layer order:

1\. Purple sunset sky.  
2\. Distant clouds or mountains.  
3\. Central mountain and glass residence.  
4\. Foreground mountain range.  
5\. Mist or cloud overlay.  
6\. Hero copy and navigation.

Suggested copy:

Eyebrow:  
PRIVATE RESIDENCES. EXTRAORDINARY PERSPECTIVES.

Heading:  
Live beyond the expected.

Supporting text:  
Architectural Landscape curates architecturally distinct homes in remarkable settings for people who value privacy, design, and a deeper sense of place.

Buttons:  
\- Explore the collection  
\- Speak with an advisor

Optional small top labels:  
\- Elevated living, thoughtfully placed  
\- Private residences across exceptional landscapes

Hero motion:

\- Use a tall scroll scene of approximately 180–230vh.  
\- Keep the visual composition sticky for part of the scroll.  
\- Sky moves the least.  
\- Central residence moves slightly faster than the sky.  
\- Foreground mountain moves faster than the residence.  
\- Mist moves independently and gently.  
\- Copy fades and moves upward before the next section.  
\- Avoid exaggerated zooming.  
\- The scene should feel like the viewer is slowly moving through the landscape.

Suggested relative movement:

\- Sky: 4–8vh  
\- Distant landscape: 8–12vh  
\- Residence mountain: 12–18vh  
\- Foreground mountain: 20–30vh  
\- Mist: 16–24vh with subtle opacity adjustment

Use transforms only for animated movement. Avoid animating layout properties such as \`top\`, \`height\`, or \`margin\`.

\----------------------------------------------------------------------  
C. Overlapping mountain transition  
\----------------------------------------------------------------------

The next landscape must visually overlap the hero in the same way as the reference.

Requirements:

\- Begin the transition before the hero scene fully ends.  
\- Use negative vertical overlap where appropriate.  
\- Align the horizon, cloud density, color temperature, and scale.  
\- No rectangular image boundary should be visible.  
\- No black, gray, empty, or transparent-looking strip may appear.  
\- Use CSS masking and gradient blending where needed.  
\- Preserve the visible upper silhouette of the mountain for the parallax effect.  
\- Left-aligned mountain forms should enter naturally.  
\- Clouds should cover any unavoidable seam.

Use techniques such as:

\- \`mask-image: linear-gradient(...)\`  
\- \`-webkit-mask-image\`  
\- matching background-color behind the images  
\- overlapping fog pseudo-elements  
\- large feathered gradients  
\- carefully tuned \`object-position\`  
\- 8–18vh visual overlap

Do not place text directly on the mountain transition until sufficient readable mist or negative space is available.

\----------------------------------------------------------------------  
D. Scroll-highlighted brand statement  
\----------------------------------------------------------------------

Create a spacious mist-filled section inspired by the reference.

Use this original copy:

“At Architectural Landscape, every residence is selected for the way it lives — how light moves through it, how the landscape frames it, and how it feels long after arrival.”

Behavior:

\- Large centered paragraph.  
\- Text begins at low opacity.  
\- Individual words or short phrases progressively brighten as the user scrolls.  
\- The highlighted text should feel synchronized with scrolling, not like a timed animation.  
\- Completed words remain bright.  
\- Non-highlighted words remain softly visible.  
\- Maintain high readability over the mist background.  
\- Keep the background subtly moving at a lower parallax speed.

Do not animate each character separately. Highlight by word or short phrase to avoid visual noise.

\----------------------------------------------------------------------  
E. Brand principles strip  
\----------------------------------------------------------------------

Create a quiet two-row strip of small labels, not a loud marquee.

Example labels:

\- Perspective  
\- Privacy  
\- Architecture  
\- Stewardship  
\- Provenance  
\- Place  
\- Detail  
\- Discretion  
\- Longevity  
\- Craft

Use simple custom line icons or restrained symbols.

The strip may drift horizontally by a very small amount during scrolling, but it must not distract from the statement.

\----------------------------------------------------------------------  
F. Results section  
\----------------------------------------------------------------------

Transition from lavender mist into a soft pale surface.

Heading:  
Measured by trust, not volume.

Supporting text:  
A private advisory built around considered selection, discreet representation, and enduring client relationships.

Use editable sample metrics:

\- 120+  
  Residences represented

\- 18  
  Private markets

\- 14  
  Years of advisory experience

\- 98%  
  Client referral rate

Treat these as placeholder brand metrics that can be changed in Gutenberg.

Animation:

\- Numbers reveal softly when entering the viewport.  
\- Use a subtle count-up only when reduced motion is not enabled.  
\- Vertical separators on desktop.  
\- Stacked layout on mobile.  
\- Do not use aggressive bouncing or spinning animations.

\----------------------------------------------------------------------  
G. Signature residences  
\----------------------------------------------------------------------

Add a section containing three featured-estate cards.

Example content:

1\. Alpine Glasshouse  
   Dolomites, Italy  
   A transparent retreat shaped around uninterrupted mountain light.

2\. The Cliff Residence  
   Big Sur, California  
   A coastal home positioned between architecture, rock, and open horizon.

3\. Desert Courtyard  
   AlUla, Saudi Arabia  
   A quiet residence built around shade, stone, and protected interior gardens.

Use existing relevant images from \`/assets/images\` where possible.

When there are not enough suitable estate images:

\- Reuse the strongest landscape assets using different crops.  
\- Do not download replacement images.  
\- Keep image fields editable in Gutenberg.

Card interaction:

\- Minimal image scale.  
\- Slight text movement.  
\- Soft border or highlight.  
\- No large 3D tilt effect.  
\- Entire card must be keyboard accessible.

\----------------------------------------------------------------------  
H. Horizon approach  
\----------------------------------------------------------------------

Create four steps:

01 — Understand    
We begin with how you want to live, not a list of available properties.

02 — Curate    
A considered shortlist shaped by architecture, location, privacy, and long-term value.

03 — Secure    
Discreet representation from first viewing through negotiation and completion.

04 — Steward    
Ongoing support for ownership, introductions, and future acquisitions.

Use a clean editorial layout with a restrained scroll reveal.

\----------------------------------------------------------------------  
I. Final cinematic call to action  
\----------------------------------------------------------------------

Return to a darker violet landscape treatment.

Heading:  
Your next horizon begins here.

Text:  
Speak privately with our advisory team about the residence, setting, or opportunity you are seeking.

Buttons:  
\- Request a consultation  
\- View residences

Include a minimal footer with:

\- Architectural Landscape  
\- Residences  
\- Advisory  
\- Journal  
\- Contact  
\- Privacy  
\- Instagram  
\- LinkedIn

\======================================================================  
5\. MOTION SYSTEM  
\======================================================================

Use a consistent, premium motion language.

Preferred implementation:

\- GSAP  
\- ScrollTrigger  
\- Lenis or an equivalent lightweight smooth-scroll system  
\- Bundle dependencies locally in the final WordPress theme  
\- Do not depend on remote CDNs

Coordinate smooth scrolling and ScrollTrigger correctly.

Mandatory behavior:

\- Refresh ScrollTrigger after images and fonts are ready.  
\- Recalculate on resize and orientation changes.  
\- Prevent animation initialization before required elements exist.  
\- Destroy and reinitialize instances safely when Gutenberg previews update.  
\- No duplicate event listeners.  
\- No repeated RAF loops.  
\- No console warnings.  
\- No horizontal overflow.  
\- No sudden jumps while assets decode.  
\- No blank space between pinned sections.  
\- No flash of incorrectly positioned layers on page load.

Use a reusable animation controller rather than one-off scripts for every section.

Example data attributes:

\- \`data-parallax-speed\`  
\- \`data-scroll-fade\`  
\- \`data-scroll-highlight\`  
\- \`data-stagger\`  
\- \`data-pin-section\`  
\- \`data-counter\`

Animations must degrade gracefully if JavaScript is unavailable.

Reduced-motion behavior:

\- Disable smooth scrolling.  
\- Remove pinning where it harms navigation.  
\- Render all text fully visible.  
\- Use minimal fades only.  
\- Keep all content accessible.

Mobile behavior:

\- Reduce parallax movement by at least 50%.  
\- Avoid long pinned scenes.  
\- Prevent viewport-height bugs by using \`svh\` or a safe CSS fallback.  
\- Preserve important mountain silhouettes.  
\- Adjust image focal points using breakpoint-specific CSS variables.  
\- Maintain at least 44px touch targets.

\======================================================================  
6\. SEAMLESS LANDSCAPE CONTINUITY  
\======================================================================

This is a critical requirement.

Every landscape section must appear to continue from the previous section.

For each transition:

1\. Compare the previous section’s bottom 15–20% with the next section’s top 15–20%.  
2\. Match:  
   \- Lavender hue  
   \- Fog density  
   \- Contrast  
   \- Image scale  
   \- Mountain direction  
   \- Horizon position  
3\. Use cloud overlays to bridge visual differences.  
4\. Do not cut a mountain peak at the top edge unless it is intentionally hidden by mist.  
5\. Do not introduce trees at the top edge when the previous section ends in clouds.  
6\. The first visible area of the following section should resemble the final cloud region of the preceding section.  
7\. Test every seam at common widths:  
   \- 1440px  
   \- 1280px  
   \- 1024px  
   \- 768px  
   \- 390px

Use a development-only debug mode that can outline image layers and show their boundaries. Disable the debug mode in production.

\======================================================================  
7\. FRONT-END PREVIEW  
\======================================================================

Create a preview that can be reviewed without WordPress.

Suggested structure:

/preview  
  index.html  
  assets/  
    css/  
    js/

/src  
  styles/  
  scripts/

/assets/images

The preview and WordPress theme should reuse the same source styling and animation modules wherever practical.

Provide commands such as:

\- \`npm install\`  
\- \`npm run dev\`  
\- \`npm run build\`  
\- \`npm run theme:zip\`

Do not create a prototype that must later be completely rewritten for WordPress.

The front-end markup should already mirror the block markup and component structure that will be used in the theme.

\======================================================================  
8\. WORDPRESS BLOCK THEME  
\======================================================================

Create a complete block theme named:

Architectural Landscape

Suggested theme directory:

\`/wordpress/architectural-landscape\`

Include at minimum:

\- \`style.css\`  
\- \`functions.php\`  
\- \`theme.json\`  
\- \`screenshot.png\`  
\- \`templates/front-page.html\`  
\- \`templates/index.html\`  
\- \`templates/page.html\`  
\- \`templates/single.html\`  
\- \`parts/header.html\`  
\- \`parts/footer.html\`  
\- \`/patterns\`  
\- \`/blocks\`  
\- \`/assets/css\`  
\- \`/assets/js\`  
\- \`/assets/images\`  
\- \`/languages\`  
\- \`README.md\`

Use the current stable WordPress block-theme conventions available in the project environment.

Create Gutenberg blocks for:

1\. \`horizon/parallax-hero\`  
2\. \`horizon/scroll-statement\`  
3\. \`horizon/principles-strip\`  
4\. \`horizon/metrics\`  
5\. \`horizon/residence-grid\`  
6\. \`horizon/approach\`  
7\. \`horizon/cinematic-cta\`

Each block should provide appropriate editable controls.

Text editing:

\- RichText fields for headings and body copy.  
\- Editable button labels and URLs.  
\- Optional eyebrow text.  
\- Correct heading-level controls where relevant.

Image editing:

\- MediaUpload controls.  
\- Alt-text support.  
\- Focal-point controls when useful.  
\- Separate fields for each hero layer.  
\- Ability to replace every supplied image later.  
\- Preview the parallax composition inside the editor without running the full heavy animation.

Design controls:

\- Background color where appropriate.  
\- Text color.  
\- Section spacing.  
\- Optional animation intensity: Off, Subtle, Standard.  
\- Optional section height.  
\- Alignment and content width.  
\- Toggle for gradient seam overlay.

Avoid exposing dozens of unnecessary controls. Preserve the intended design while keeping content editable.

For advanced visual blocks, use block locking or content-only editing so users cannot accidentally destroy the layer structure while still being able to change text, links, and media.

Register an editable full-page pattern called:

“Architectural Landscape — Cinematic Homepage”

Use the supplied assets as the default images for the pattern or the dynamic block fallbacks.

\======================================================================  
9\. THEME.JSON AND EDITOR PARITY  
\======================================================================

Define in \`theme.json\`:

\- Brand color palette  
\- Typography scale  
\- Fluid font sizes  
\- Content width  
\- Wide width  
\- Spacing scale  
\- Button styles  
\- Border radii  
\- Shadows  
\- Default block gaps  
\- Heading styles  
\- Link styles

The Gutenberg editor should visually resemble the front end.

Load editor styles.

Do not make the user guess what the final page will look like.

\======================================================================  
10\. PERFORMANCE  
\======================================================================

The hero must remain visually rich without becoming unstable.

Requirements:

\- Preload only the true hero-critical image.  
\- Use responsive image sizes.  
\- Supply width and height attributes.  
\- Use \`srcset\` and WordPress image functions where applicable.  
\- Lazy-load below-the-fold images.  
\- Use \`decoding="async"\` where appropriate.  
\- Avoid animating huge blur filters.  
\- Use \`will-change\` only on currently animated elements.  
\- Remove \`will-change\` after animations where practical.  
\- Use transform and opacity for motion.  
\- Compress or recommend compression for oversized images without replacing originals.  
\- Avoid more than one full-resolution copy of the same image being rendered simultaneously.  
\- Prevent cumulative layout shift.  
\- Do not autoplay large video backgrounds.

Create \`/docs/performance-notes.md\` containing any asset optimization recommendations.

\======================================================================  
11\. ACCESSIBILITY  
\======================================================================

Meet practical WCAG requirements.

Include:

\- Semantic landmarks  
\- Skip link  
\- Visible keyboard focus  
\- Accessible mobile navigation  
\- Correct heading structure  
\- Meaningful alt-text defaults  
\- Decorative images hidden from assistive technology  
\- Sufficient contrast  
\- Reduced-motion support  
\- Buttons and links with clear names  
\- No scroll-jacking that prevents keyboard or native scrolling  
\- No content that is visible only through animation

\======================================================================  
12\. DEVELOPMENT QUALITY  
\======================================================================

Use:

\- Semantic HTML  
\- Modern CSS  
\- Modular JavaScript  
\- Clear naming  
\- Reusable motion helpers  
\- Defensive null checks  
\- Proper cleanup functions  
\- WordPress escaping and sanitization  
\- Namespaced PHP functions  
\- Translation-ready strings  
\- No hardcoded production URLs  
\- No jQuery unless there is a strong technical reason  
\- No page-builder dependency  
\- No Elementor dependency  
\- No ACF dependency  
\- No external CDN dependency

The theme should be installable and usable independently.

\======================================================================  
13\. REQUIRED DOCUMENTATION  
\======================================================================

Create:

1\. \`/README.md\`  
   \- Project overview  
   \- Preview setup  
   \- Build commands  
   \- WordPress installation  
   \- Gutenberg editing instructions

2\. \`/docs/asset-manifest.md\`  
   \- Asset roles and dimensions

3\. \`/docs/motion-system.md\`  
   \- Parallax values  
   \- ScrollTrigger structure  
   \- Reduced-motion behavior  
   \- Mobile adjustments

4\. \`/docs/theme-editing-guide.md\`  
   \- How to edit copy  
   \- How to replace image layers  
   \- How to change metrics  
   \- How to reorder sections safely

5\. \`/docs/qa-checklist.md\`  
   \- Responsive checks  
   \- Seam checks  
   \- Keyboard checks  
   \- Performance checks

\======================================================================  
14\. DEFINITION OF DONE  
\======================================================================

Do not consider the task complete until:

\- The preview runs locally.  
\- The page forms one continuous visual journey.  
\- The hero uses actual files from \`/assets/images\`.  
\- The foreground mountain overlaps the hero naturally.  
\- The continuation sections do not show hard image boundaries.  
\- There is no strange blank area on the right side.  
\- Mountains remain left aligned where required.  
\- Clouds fill the remaining width naturally.  
\- The first and last edges of adjacent images feel connected.  
\- Scroll highlighting works in both directions.  
\- Navigation remains usable throughout.  
\- Mobile layouts do not break.  
\- Reduced-motion mode works.  
\- The WordPress theme activates without errors.  
\- All primary text and images are editable in Gutenberg.  
\- The homepage pattern can be inserted and edited.  
\- The browser console contains no errors.  
\- The site does not depend on remote assets.  
\- A production theme ZIP can be generated.

\======================================================================  
15\. EXECUTION ORDER  
\======================================================================

Work in this order:

Phase 1:  
Inspect images and write the asset manifest.

Phase 2:  
Create design tokens, page structure, and static composition.

Phase 3:  
Build the layered hero and seamless image transitions.

Phase 4:  
Add parallax, smooth scrolling, text highlighting, counters, and section reveals.

Phase 5:  
Complete responsive, accessibility, and performance work.

Phase 6:  
Create the WordPress block theme and editable Gutenberg blocks.

Phase 7:  
Run final visual and technical QA.

At the end, provide:

\- A concise summary of what was built.  
\- The asset-role mapping.  
\- Commands to run the preview.  
\- The WordPress theme location.  
\- The generated theme ZIP location.  
\- Any remaining issues that could not be resolved.

Start by inspecting \`/assets/images\`. Do not begin with generic placeholder layouts.

—------------------

**Assets Change Prompt**

You are working on the existing Architectural Landscape parallax website / WordPress block theme.

The page structure, Gutenberg blocks, parallax functionality, smooth scroll, text highlight effects, counters, navigation behavior, and responsive logic are already working well.

Do not rebuild the project from scratch.

Your task is to update the visual direction from the previous purple/lavender concept to the new orangish-yellow golden-hour concept using the newly added image assets in \`/assets/images\`.

\======================================================================  
PRIMARY GOAL  
\======================================================================

Replace the purple/pink/lavender image set and overall webpage tone with the new orange, yellow, amber, golden-hour image set.

The final website should feel warm, premium, cinematic, sunlit, and architectural.

The site should no longer feel violet/lavender/purple.

Keep the existing functionality intact.

Do not remove or break:

\- Smooth scroll  
\- Parallax hero  
\- ScrollTrigger timelines  
\- Text highlighting on scroll  
\- Residence cards  
\- Metrics animation  
\- Gutenberg editability  
\- WordPress block theme structure  
\- Existing block names  
\- Existing editable controls  
\- Existing responsive behavior  
\- Reduced-motion behavior

Only update images, color tokens, visual tone, and residence card content/images where needed.

\======================================================================  
ASSET INSPECTION  
\======================================================================

Start by inspecting \`/assets/images\`.

Do not rely only on filenames.

For every image, identify:

\- Dimensions  
\- Aspect ratio  
\- File type  
\- Whether it has a real alpha channel  
\- Whether it belongs to the old purple set or the new golden/orange set  
\- Best use case

Update \`/docs/asset-manifest.md\` with the new mapping.

The new orange/golden assets should take priority.

Do not use old purple images unless there is no suitable orange replacement.

Expected new asset categories include:

1\. Orange/yellow cloud sky background.  
2\. Orange cloud \+ mountain PNG for hero parallax.  
3\. Orange/golden mountain or mist continuation images.  
4\. 4:3 residence image for:  
   \- Dolomites, Italy — Alpine Glasshouse  
5\. 4:3 residence image for:  
   \- Big Sur, California — The Cliff Residence  
6\. 4:3 residence image for:  
   \- AlUla, Saudi Arabia — Desert Courtyard  
7\. Three additional new residence/property photos that were recently added to the images folder.

Use visual inspection to decide which photo goes where.

\======================================================================  
COLOR SYSTEM UPDATE  
\======================================================================

Replace the current purple/lavender palette with a warm golden-hour palette.

Create or update CSS variables and \`theme.json\` colors.

Suggested palette:

\- Deep umber: \#160E08  
\- Burnt cedar: \#3A1D0C  
\- Warm bronze: \#8C4A16  
\- Ember orange: \#D86A1F  
\- Golden amber: \#F2A93B  
\- Sunlit yellow: \#FFD77A  
\- Sand mist: \#F4D7A1  
\- Warm ivory: \#FFF4DF  
\- Soft parchment: \#F6E6C8  
\- Dark text: \#21170E

Use the actual image colors as the source of truth.

The palette should feel like:

\- Golden hour  
\- Warm architectural lighting  
\- Amber mist  
\- Sunlit stone  
\- Desert/coastal luxury  
\- Premium editorial real estate

Remove or heavily reduce:

\- Purple overlays  
\- Violet tints  
\- Lavender backgrounds  
\- Blue-purple shadows  
\- Pink/purple gradient masks

Replace them with:

\- Amber gradients  
\- Warm mist  
\- Soft golden haze  
\- Deep brown/navy-black contrast  
\- Sunlit orange highlights

\======================================================================  
GLOBAL DESIGN TONE  
\======================================================================

Update the page background, section transitions, overlays, buttons, borders, nav tint, and text colors to match the new images.

The page should not look like orange images placed inside an old purple UI.

Important:

\- Navigation glass should become warm dark brown / deep umber, not purple.  
\- Buttons should use warm ivory and deep brown text.  
\- Section backgrounds should use warm mist / parchment / amber haze.  
\- Text highlight effects should brighten toward warm ivory or pale gold.  
\- Cards should use warm dark overlays, not violet overlays.  
\- Metrics section should transition into a soft warm parchment background.  
\- Footer should use deep umber or burnt cedar.

Keep contrast accessible.

\======================================================================  
HERO SECTION UPDATE  
\======================================================================

The hero should keep the same working parallax structure, but swap to the new golden-hour imagery.

Important: do not break the hero functionality.

Use the new orange/yellow cloud sky image as the main sky/background layer.

Use the new orange cloud \+ mountain PNG from \`/assets/images\` for the hero parallax foreground/transition layer.

This new orange cloud \+ mountain PNG should replace the previous purple cloud/mountain layer.

Do not add a fake orange tint over purple images if a real orange asset exists.

Remove the old tint workaround if it was added only to make purple images feel warmer.

Hero layer logic should remain:

1\. Golden cloud sky background.  
2\. Large heading behind the central mountain/building.  
3\. Central mountain/building or hero subject.  
4\. Orange cloud \+ mountain PNG parallax layer.  
5\. Warm mist / cloud seam overlay.  
6\. Navigation and clickable content above all decorative layers.

Use the new orange cloud \+ mountain PNG carefully:

\- It should enhance the parallax depth.  
\- It should not cover the central residence awkwardly.  
\- It should not create a hard rectangular edge.  
\- It should not introduce purple tones.  
\- It should not create a visible seam.  
\- It should help merge the hero into the next section.

If the orange cloud \+ mountain PNG is transparent, use it as an independent parallax layer.

If it is not actually transparent, use it only where it can fill the viewport naturally without revealing edges.

Do not stack multiple opaque 16:9 images in the hero.

Use the fewest layers needed for a clean result.

\======================================================================  
HERO HEADLINE  
\======================================================================

Keep the existing improved headline concept:

Left phrase:  
Live beyond

Right phrase:  
the expected.

The mountain/building should sit between the two text groups and visually overlap the heading.

Do not revert to a single oversized heading block placed fully in front of the scene.

The text should still feel embedded into the image.

Update text color if needed:

\- Warm ivory  
\- Pale gold  
\- Soft cream

Avoid pure white if it feels too cold against the new golden palette.

\======================================================================  
HERO TRANSITION  
\======================================================================

The hero should transition into the next section using warm mist and the new orange cloud/mountain layer.

The transition must have:

\- No purple seam  
\- No hard horizontal image line  
\- No rectangular image boundary  
\- No sudden color shift  
\- No black/white gap  
\- No unrelated layer covering the residence  
\- No duplicate mountain layer glitch

Use CSS gradients/masks in warm tones if needed.

Suggested warm seam treatment:

\`\`\`css  
background:  
  radial-gradient(  
    ellipse at 50% 100%,  
    rgba(255, 216, 146, 0.86) 0%,  
    rgba(230, 142, 54, 0.38) 45%,  
    transparent 76%  
  );