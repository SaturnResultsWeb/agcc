# Current site audit: gamblingcontrol.org (captured 2026-10-16)

Source facts for the home page rebuild demo. Everything below was read from the live site.

## Identity
- Name: Alderney Gambling Control Commission (AGCC)
- Hero line: "Global Leader in eGambling Regulation"
- Mission: "To ensure and maintain the integrity of electronic gambling activities regulated by the Commission."
- Platform: Wix
- Logo: plum/aubergine square mark + "ALDERNEY / Gambling Control Commission" serif wordmark

## Brand colour actually in use
- Plum: #885682 (rgb 136,86,130), most used accent
- Deep aubergine: #601A58, #300D2C
- Slate ink: #1E242E, #2D3643; grey #414141, #737882
- Fonts: Times New Roman headings, Helvetica/Arial body (system defaults, no real type system)

## Primary navigation (and children)
- FAQs
- Regulation Framework: eGambling Licence, Core Service Provider Associate Certificate, Associate Certificate, Hosting Certificate, Temporary eGambling Licence, Key Individual Certificate, Legislation, AML/CFT Resources, Fees
- Applications & Guidance: Forms, ICS Guidelines, Current Applicants
- Licences & Certificates: eGambling Licensees, Core Service Provider Associates, Category 1 & 2 Associate Certificates, Hosting Providers, Temporary eGambling Licensees, Recently Licensed, UN & EU Sanctions
- Legislation
- Players: Limitation on Play, Player Complaints, Submit a Complaint
- About Us: Approach, Organisation, Notices, Reports, News, Careers
- Contact

## Home page sections today
1. Hero: headline + full-width coastal photo of Alderney
2. Mission statement + "Find out more about us"
3. Six numbered tiles: Compliance (Regulation Framework), Industry (Applications & Guidance), Licencees (Current Licences & Certificates), Legal (Legislation), Information (Players), Find out more (FAQs)
4. Stats: 70+ Licences & Certificates, 100+ URLs, 20+ Game Providers, 10+ Hosting Facilities
5. Recent News slider (4 pages):
   - The AGCC announces the appointment of Mr Christopher Blythe OBE as Commissioner
   - AGCC Announces Leadership Transition
   - Alderney's Gambling Regulator Signs Guernsey's Financial Crime Lead as New Commissioner
6. "Why Alderney?" + More info (/alderney-egambling)
7. Footer

## Contact / footer
- St Anne's House, Queen Elizabeth II Street, Alderney, Channel Islands, GY9 3TB
- +44 (0)1481 825500 · info@agcc.gg
- Complaints cannot be dealt with over the phone (form, email or post)
- Links: Privacy Policy, Cookie Policy, Service Providers, Sitemap

## Problems worth fixing
- No clear routes per audience (operators/applicants vs players vs public/press); six tiles mix them
- Licence register (the most important public utility) is buried under a nav label
- Search is a small box with no prominence
- Default system fonts, thin underline-heavy nav, generic stock coastline
- Stats are vague ("100+ URLs") and say little about the regulator's standing
- News is a slider (hidden content, poor accessibility)

## Note on the generated MASTER.md
`design-system/alderney-gambling-control-commission/MASTER.md` came back as the category default
(navy + gold, IBM Plex Sans, "Trust & Authority"). That is exactly the "finance/regulator = navy + gold"
reflex we are trying to avoid. Keep it as the UX/accessibility baseline (checklists, contrast, anti-patterns),
but the palette and type will be overridden in DESIGN.md, starting from the real plum brand.
