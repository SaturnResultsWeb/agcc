# Design brief: AGCC home page

Status: CONFIRMED by user 2026-10-16. Produced by `/impeccable shape home page`, 2026-10-16.
Reads with: `PRODUCT.md`, `DESIGN.md` (seed), `current-site-audit.md`.

Visual probe step skipped: this harness has no built-in image generation.

## 1. Feature summary

The home page of the Alderney Gambling Control Commission, built as a pitch demo for a full site rebuild. It has to make Alderney read as a modern, transparent, firm, world-class regulator in the first screen, then route four audiences (operators, players, compliance professionals, press and government) to what they need in one step. It must not be boring: calm system, a few high-contrast moments.

## 2. Primary user action

**Check whether a gambling company or website is licensed in Alderney**, right on the home page. Everything else (routes, pitch, news) supports the authority that makes that check meaningful.

## 3. Design direction

- **Colour strategy:** Committed (per DESIGN.md). Aubergine Ink fields carry 30 to 60 percent of the page. The surface changes temperature at least three times down the scroll.
- **Scene sentence:** A compliance officer in a bright London or Malta office checks an operator between meetings, while a frustrated player on a phone in their kitchen pastes a casino URL to see if it's real, both in ordinary daylight wanting a fast, certain answer. This forces light paper for reading, with deep ink fields reserved for statements and the register.
- **Anchor references:** Bank of England (typographic calm, data literacy), GOV.UK (task-first routing, search as a tool), Jersey Finance (place-led jurisdiction pitch).
- **Style:** `minimalist-ui`, adapted (see DESIGN.md Overview). Never Boring Rule applies in full.
- **Signature moment:** **The register unfolds.** The register chapter opens like a ledger as it enters view and as you type: rows, status words and licence details resolve line by line.

## 4. Scope

- **Fidelity:** high-fi.
- **Breadth:** one page (home), desktop and mobile.
- **Interactivity:** interactive prototype. Search works for real against bundled register data; nav menus open; routes expand. Other pages are not built (links point to the current site's URLs so the demo stays honest).
- **Build:** single self-contained static HTML prototype (`home.html`), like Midtown's. Port to Next.js after approval.
- **Time intent:** polish until it is pitch-ready.

## 5. Layout strategy

Eight chapters. No two consecutive chapters share a structure.

1. **Header (Paper).** Slim utility line (phone, email, "Make a complaint", search shortcut) over a main bar: a newly drawn AGCC mark and wordmark left (rebrand concept; the current logo is not reused), audience-first nav right (Operators, Players, Licence register, Legislation, News, About). Menus open as wide, typographic panels, not dropdown link soup.
2. **Hero (Aubergine Ink, full-bleed).** Split. Left: very large serif statement (two to three lines max) for authority. Right: the register console, a single large field "Company or website" with an instant answer area. Fine Alderney outline linework and coordinates (49.71° N, 2.20° W) sit in the field as quiet chart graphics. Two small secondary routes under the console: "Apply for a licence", "Make a complaint".
3. **Audience routes (Granite Paper).** A typographic index, not cards: four large serif rows (For operators, For players, For compliance teams, For press and government). Each row reveals its three or four real tasks in columns on hover or focus, and is always fully visible on mobile.
4. **The register (Aubergine Ink, full-bleed): signature chapter.** A ledger of all 20 eGambling licensees in tabular figures: company, licence category (1, 2, 1 and 2), number of websites, link through. Filter by category. Unfolds line by line as it enters view. Ledger header in small mono metadata (counts as facts, not a hero stat bar). Footnote links to the other registers (Core Service Provider Associates, Category 1 and 2 Associates, Hosting Providers, Temporary Licensees, Recently Licensed, UN and EU Sanctions).
5. **Why Alderney (Paper, photography).** Asymmetric editorial composition: one decisive warm, desaturated coastal photograph offset against a large island map drawn in linework, with three or four concise claims as a numbered list alongside. Link to the jurisdiction page.
6. **How licensing works (Island Stone band).** A four-step operator path (Enquire, Apply, Due diligence, Licensed) laid out horizontally on desktop and joined by one fine chart line, vertical on mobile. Each step: short serif title, one or two plain sentences, the key document or form linked. Ends with "Start an application" and "See fees". Steps and wording to be taken from the live Applications & Guidance and Regulation Framework pages, not invented.
7. **News and notices (Granite Paper).** A plain dated list (tabular dates, serif headlines), latest three real headlines plus notices. No slider.
8. **Closing chapter and footer (Aubergine Ink).** Large serif sign-off, contact block (St Anne's House address, phone, email, the "complaints cannot be dealt with over the phone" rule stated plainly with the routes that do work), and footer links.

## 6. Key states (register search)

- **Idle:** prompt plus two or three example chips drawn from real data ("Betway Alderney", "jackpotcity.com").
- **Typing:** instant, debounced results under the field, max six rows, best match first. Matches company names and website addresses. Input normalised (strip `https://`, `www.`, paths, case).
- **Licensed match:** status word "Licensed in Alderney" with icon, company name, category explained in words ("Category 1: B2C operator"), the matched website highlighted, link to the licensee.
- **Company with no listed websites:** "Licensed. No consumer websites listed." (many licensees show N/A).
- **No match:** "Not on the AGCC register." Followed by what to do: check the spelling, it may be licensed elsewhere, how to report a site claiming an Alderney licence. Never alarmist, never ambiguous.
- **Partial or very short input:** wait for two characters; no flashing results.
- **Keyboard:** arrow keys move through results, Enter opens, Escape clears. Results announced via `aria-live="polite"`.
- **Mobile:** console stacks under the statement and stays in the first screen; results expand in place, never in a modal.
- **Reduced motion:** ledger and results appear without line-by-line motion, opacity only.

## 7. Interaction model

- Hero console is the first focus target after the skip link.
- Results resolve line by line (short stagger, 30 to 50ms), ease-out, under 250ms each. Retyping interrupts cleanly.
- Register chapter: rows resolve as the band enters view (once). Category filter re-sorts with a quick crossfade.
- Audience index: rows reveal tasks on hover/focus with a calm transition; whole row is not a link, each task is.
- Nav panels open on click (and hover on fine pointers), close on Escape and outside click.
- Buttons press to scale(0.97). Hover effects gated behind `(hover: hover)`.
- No scroll-jacking, no pinned sections, no auto-rotation.

## 8. Content requirements

- **Real data:** full eGambling licensee list and websites from the live register (captured 2026-10-16: 20 companies, 87 unique websites after de-duplication). Bundle as JSON inside the page with a "register as at" date.
- **Real headlines:** the three current news posts (Christopher Blythe OBE appointed Commissioner; Leadership transition; Guernsey financial crime lead signed as new Commissioner).
- **Real contact facts:** from `current-site-audit.md`.
- **Hero statement:** draft options during craft, in the PRODUCT.md voice (short, declarative, no superlatives such as "Global leader").
- **Why Alderney claims:** to be written from the live `/alderney-egambling` page; no invented facts or numbers.
- **Microcopy:** search placeholder, the four result states above, filter labels, route task names in visitor language ("Check a licence", "Make a complaint", "Set a limit on your play", "Apply for a licence", "Fees", "Forms and ICS guidelines", "Legislation", "AML/CFT resources", "Sanctions lists", "Reports", "Press and notices").
- No em dashes in UI copy.

## 9. Recommended references for craft

`brand.md` (register), `typeset.md` (font selection away from the reflex-reject list), `layout.md` (chapter variance), `animate.md` (ledger unfold, results stagger), `harden.md` (search edge cases), `adapt.md` (mobile console), `audit.md` (WCAG 2.2 AA).

## 10. Open questions

1. Resolved: extra section is "How licensing works" (chapter 6).
2. Resolved: logo is redrawn as a new mark for the concept.
3. **Photography:** stock Alderney coastal imagery for now; does the agency have licensed Alderney photos to use instead?
4. **Other registers:** include Hosting Providers and Associates in the home search too, or link only? (Default: eGambling licensees in search, others linked.)
