# Design — Project Identity

> This document is project-long-lived. Tokens are not changed without
> the Architect's approval. Developers MUST use these tokens
> instead of improvising their own colors/spacings.

## Style Direction

Helles, freundliches Fintech: Flächen aus #F4F5FA und weißen Karten, ein einziges lebendiges Grün (#6CC57C bis #179F2F) als Akzent, Tinte-Dunkelblau #23233C als Text — seriös wie eine Banking-App, aber leicht und mit verspielten Illustrationen.

## Colors

- `--color-bg`: **#F4F5FA**
- `--color-bg-alt`: **#F4F4F4**
- `--color-bg-dashboard`: **#ECF1FA**
- `--color-surface`: **#FFFFFF**
- `--color-surface-alt`: **#DCE5F4**
- `--color-fg`: **#23233C**
- `--color-fg-strong`: **#1C1C1C**
- `--color-fg-black`: **#000000**
- `--color-muted`: **#A5A5A5**
- `--color-muted-alt`: **#8D8D8D**
- `--color-placeholder`: **#898888**
- `--color-accent`: **#6CC57C**
- `--color-accent-soft`: **#61D27C**
- `--color-accent-strong`: **#179F2F**
- `--color-accent-surface`: **#6CC57CA3**
- `--color-accent-overlay`: **#6CC57C78**
- `--color-on-accent`: **#FFFFFF**
- `--color-dark-surface`: **#23233C**
- `--color-dark-bar`: **#2B2B2B**
- `--color-ink-navy`: **#181461**
- `--color-border`: **#707070**
- `--color-divider`: **#1C1C1C33**
- `--color-nav-inactive`: **#BBC7DB**
- `--color-warning-line`: **#C48B30**
- `--color-social-facebook`: **#0F279E**

## Typography

- `font_family`: Inter, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif
- `font_family_display`: Aleo, Georgia, 'Times New Roman', serif
- `font_family_calendar`: Ubuntu, -apple-system, 'Segoe UI', Roboto, sans-serif
- `font_family_login`: Actor, Inter, -apple-system, sans-serif
- `heading_weight`: 700
- `body_weight`: 400
- `text-25`: Aleo 700 25px/30px (Login Slide, Zeilenumbruch-Variante 25px/32px)
- `text-24`: Aleo 700 24px/29px (Screen-Titel, z. B. 'Add an appointment')
- `text-20`: Aleo 700 20px/25px (Login-CTA)
- `text-16-display`: Aleo 700 16px/19px (Abschnittstitel, Tabs aktiv)
- `text-16`: Inter 400 16px/19px (Formular-/Such-/Button-Text, 'Search' liegt bei opacity 0.2)
- `text-14-display`: Aleo 700 14px/17px (Listentitel, 'Modify')
- `text-14`: Inter 400 14px/17px (Feldtext Login)
- `text-13`: Inter 400 13px/17px ('Forgot you password?')
- `text-12-caps`: Inter 100 12px/15px, letter-spacing 2.4–2.8px, uppercase (Kicker 'MONTHLY EXPENSES', 'WEEKLY REPORT', 'ADD EXPENSE')
- `text-12`: Inter 400 12px/14px (Untertitel Liste, 'Customize Plan')
- `text-11`: Ubuntu 700 11px/12px, letter-spacing 0.3px (Kalender-Zeitspalte, Aleo-700-Variante in Time Management)
- `text-10`: Inter 400 10px/13px (Fließtext Onboarding-Slide)
- `text-9`: Inter 100 9px/11px, letter-spacing 1.8px, uppercase (Kategorie- und Datumslabel in Transaktionsliste)
- `text-7`: Aleo 700 7px/5px (Bottom-Tab-Bar-Labels, 'Earned/10AM-11AM' via Ubuntu 700 7px/10px)
- `text-login-field`: Actor 400 14px/18px (E-Mail-/Passwortwert im Login, zentriert)

## Spacing Scale

- `--space-0`: 4px
- `--space-1`: 8px
- `--space-2`: 12px
- `--space-3`: 16px
- `--space-4`: 20px
- `--space-5`: 24px
- `--space-6`: 40px

## Border-Radii

- `--radius-sm`: 3px
- `--radius-input`: 5px
- `--radius-md`: 8px
- `--radius-social`: 10px
- `--radius-lg`: 12px
- `--radius-button`: 18px
- `--radius-card`: 20px
- `--radius-pill`: 999px

## Components

### Button — Primary (gefüllt)

Zwei Ausführungen aus den Frames, beide exakt übernommen. (a) Formular-CTA: 334–336×43, bg=accent #6CC57C, radius input 5px, shadow 0/3 blur 16 #00000014, Label Inter 400 16px/19px #FFFFFF ('Add Expense', 'Add Appointment', 'Add a new appointment'); Trefferfläche per hitSlop auf min. 44px Höhe aufziehen (Figma-Maß 43px bleibt optisch). (b) Login-CTA: 333×54, bg=fg #23233C, radius button 18px, Label Aleo 700 20px/25px #FFFFFF zentriert ('Login'). (c) Slide-CTA 'Next': 115×42, bg=accent, radius md 8px, Label Inter 400 15px/19px #FFFFFF; daneben 'Skip step' als reiner Text-Button Inter 400 15px/19px #B4B4B4, Trefferfläche 44px hoch. Zustände (Frames zeigen default; Rest im Frame-Stil ergänzt): default wie oben; hover (nur Web-Build) bg=accent-soft #61D27C bei grünen CTAs, bei dunklem CTA #2E2E4F; active/pressed bg=accent-strong #179F2F bzw. #1B1B33, translateY 1px, shadow auf 0/1 blur 4 #00000014 reduziert; focus 2px Outline #23233C mit 2px Offset; disabled bg=accent bei opacity 0.4 (Label #FFFFFF bleibt), dunkler CTA bg=#23233C bei opacity 0.4, shadow entfernt, kein Pointer-Event; loading = Label ersetzt durch 16px-Spinner #FFFFFF, Breite unverändert. Immer align center, kein Textumbruch.

### Button — Icon/Quadrat

Kompakter Icon-Button der Header: 32×32, bg=#23233C, radius md 8px, Chevron nach links als weißer Stroke 2px (Money Management 2/3, bei 47,55); ebenso 3-Dot-Menü als reine Icon-Fläche 3×14 mit drei Ellipsen 3×3 #23233C im Abstand 5px (x=372 in der Zeile, Trefferfläche 44×44). Hover #2E2E4F, active #1B1B33 + translateY 1px, disabled opacity 0.4.

### Button — Back-Chevron (Header)

Assset 'noun-back-1227057' 11×18 als PNG, keine Neuerstellung; Farbe #181461, Position 40,29 (Time Management) bzw. 22,25 (Money Management). Trefferfläche 44×44 mit hitSlop, Icon bleibt 11×18. Active: opacity 0.6, kein Farbwechsel — das Icon ist ein exportiertes Bild.

### FloatingAddButton

Kreis 64×63, zentriert über der Bottom-Bar (x=179 in 413, y=778), fill=linear-gradient(180deg, #6CC57C 0%, #179F2F 100%), stroke 4px #FFFFFF innen, shadow 0/3 blur 40 #00000029. Plus-Zeichen: zwei Linien 3px #FFFFFF, 20×20, zentriert (y=799/808, x=203/212). Hover: Gradient leicht heller (Start #7BCE8A), shadow 0/6 blur 40 #00000033; active: scale 0.96 + shadow 0/2 blur 16 #00000029; disabled: opacity 0.4, Gradient flach #6CC57C. Trefferfläche = Kreis (64px ≥ 44px).

### BottomTabBar

Navbar-Block 413×118 am unteren Rand (y=778), darin weiße Bar 413×77 ab y=819, fill #FFFFFF, shadow 0/3 blur 20 #60719329. Vier Items: Icon 19–22px, Label Aleo 700 7px/5px. Inaktives Item: Icon+Label #BBC7DB. Aktives Item (Frames zeigen keinen aktiven Zustand — ergänzt im Frame-Stil): Icon+Label #6CC57C, zusätzlich 3px Indikator-Strich #6CC57C, 20px breit, 4px über dem Label. Labels: 'Home' (36,862), 'Products' (87,862), 'Liked' (297,862), 'Today' (354,862) — x-Zentren 46/101/306/364. Trefferfläche je Item 44px hoch, ganze Bar-Breite/4. Icons: 'noun_Home_1191731' und 'Icon feather-user-check' sind exportierte PNGs; 'shop' und 'noun_Favorite_1481179' rendert Figma leer → im Frame-Stil nachzeichnen (19×19 bzw. 20×18, gleiche Strichstärke wie die übrigen Icons).

### Input / SearchField

334×43, bg=#FFFFFF, radius input 5px, shadow 0/3 blur 16 #00000014, kein Border. Text links: 16px-Icon (#23233C, 'noun_Search_860389' 16×16 bei x=55–57) bzw. Kalender-Icon 15×16; Label/Platzhalter Inter 400 16px/19px #1C1C1C, im Suchfeld zusätzlich opacity 0.2 (echter Platzhalter), Eingabetext opacity 1. Rechts-Icon (Suche) 16×16 #1C1C1C. Vertikaler Pitch der Feldstapel: 63px (y=149 → 212 → 275 → 338). Zustände: default wie oben; focus shadow 0/0 blur 0 2px #6CC57C (Frames zeigen keinen Focus — ergänzt) + Label #23233C; filled Text #1C1C1C opacity 1; disabled bg #F4F5FA, Text #A5A5A5, shadow entfernt. Trefferfläche 43px Höhe, per hitSlop auf 44px.

### LoginInput

336×54, bg=#FFFFFF, radius 5px, shadow 0/10 blur 10 #0D4E810D (zweite Variante #0D158108), kein Border. Wert zentriert: Actor 400 14px/18px #23233C ('mauricio@divelement.io' bei 64,339; Passwort als '***********'). Rechts-Icons: 'check' 17×17 und 'view' 19×12 bei x=329, #23233C (in Figma leer gerendert → im Frame-Stil zeichnen, 1.5px Stroke, runde Kappen). Zustände ergänzt: focus + 1px Border #6CC57C innen; error 1px Border #C48B30 + Hilfetext Inter 400 12px/14px #C48B30; disabled bg #F4F5FA, Wert #A5A5A5, Icons opacity 0.4.

### Card / Panel

Weiße Karte: bg #FFFFFF, radius card 20px, Padding 24px rundum, kein Border, kein Shadow (Quick Categories 330×276 bei 45,453) — Innenraster 3 Spalten à 55px, Spaltenabstand 54px, Zeilenabstand 37px. Kopfzeile der Karte: text-12-caps #000000, zentriert, margin-bottom 28px. Variante 'flache Panel': 414×406 oben am Screen (Money Management) bzw. 414×138 (Add Expense), fill #FFFFFF, darüber liegender Inhalt. Variante 'Kalenderkarte' (Time Management - 2): 414×629 fill #F4F5FA, oben ausgespart (Notch über der weißen Fläche), radius card 20px an den oberen Ecken.

### CategoryTile (Quick Categories)

55×55, bg #FFFFFF, 1px dashed Border #000000 innen, radius lg 12px (zweite Reihe: gleiche Maße). Icon 29–42px #000000 zentriert (home 42×39, dish-spoon-knife 41×29, briefcase 41×34, friends 40×30, shopping-bag 36×42, gas-station 37×39). Diese sechs Icons rendert Figma leer → im Frame-Stil nachzeichnen: 1.5–2px gleichmäßiger Stroke, keine Füllungen außer kleinen Akzentflächen, optische Größe innerhalb der 55px-Kachel. Zustände: default dashed #000000; hover Border solid #6CC57C + Icon #6CC57C; active bg #6CC57C bei opacity 0.12; disabled Icon #A5A5A5, Border #A5A5A5 dashed. Trefferfläche = 55px.

### TransactionRow

Zeile 378×83 auf 414 Breite (Thumbnail bei x=28–30, Betrag rechtsbündig bei x=307/308). Thumbnail 53×53 weißer gerundeter Rahmen (radius lg) mit Illustration (exportierte PNGs illustration-53x53…4). Textblock bei x=103: Kategorie text-9 uppercase #000000 (letter-spacing 1.8px), Titel Inter 100 12px/15px #000000, Datum text-9 uppercase #000000. Betrag rechts Inter 100 14px/18px #000000, rechtsbündig. Hover: Hintergrund #F4F5FA; active: #ECF1FA. Keine Divider in den Frames — Abstand zwischen Zeilen 30px.

### BarChart + Legende

7 Balken, Breite 9px, Abstand 30px (x=78,117,157,198,238,277,318), Höhe max. 300px, oben und unten abgerundet (radius pill). Track/Legende hell: Balkenhintergrund #F4F4F4 (inaktiv), Expenses #6CC57C, Deposit #2B2B2B; Stapel von unten nach oben. Legende unter dem Chart (y=358): Swatch 13×13 radius sm 3px (#6CC57C bzw. #2B2B2B), Label text-9 uppercase #000000, Abstand Swatch→Label 5px.

### Tabs (Upcoming / Past, Upcoming / Deposit-Varianten)

Gruppe 336×38. Aktives Label Aleo 700 16px/19px #23233C links; inaktives Label Inter 400 16px/19px #1C1C1C rechtsbündig. Unterstreichung 51×2 fill #23233C unter dem aktiven Label; darunter 1px-Linie 336 breit, stroke 0.5px #1C1C1C opacity 0.2. Umschalten = 150ms Crossfade der Labels + Unterstreichung mit gleicher Breite. Trefferfläche je Tab 44px hoch.

### ListRow (Quick Adds / Appointments)

Zeile 336×90, Thumbnail 69×69 links (exportierte Bilder image-69x69), Textblock bei x=121 (82px Abstand zum Thumbnail): Titel Aleo 700 14px/17px #1C1C1C, Untertitel Inter 400 12px/14px #1C1C1C opacity 0.4, optionaler dritter Wert '10AM - 11AM' Ubuntu 700 7px/10px #23233C. Rechts 3-Dot-Menü (drei Ellipsen 3×3 #23233C, Abstand 5px, Treffer 44×44). Trennlinie 336×1, stroke 0.5px #1C1C1C opacity 0.2, 3px unter der Zeile. Hover bg #F4F5FA, active bg #ECF1FA.

### Divider / Line

Haarlinie 0.5–1px, Farbe #1C1C1C bei opacity 0.2 (Listen) bzw. #707070 bei opacity 0.18 (Zeitspalte im Kalender) bzw. #C48B30 bei opacity 0.18 (Akkentlinie der Terminkarte). Breiten: 336px (Liste), 286px (Terminkarte), 22px (Zeitspalten-Stummel).

### AppointmentCard (Kalender)

Karte 286×118, fill accent-surface #6CC57CA3, kein Radius (Frames zeigen eckige Karten), links 20px Einzug zum Thumbnail. Inhalt: Titel 'Work' Ubuntu 700 11px/12px #23233C, Uhrzeit '10AM - 11AM' Ubuntu 700 7px/10px #23233C mit clock-Icon 11×11 #23233C davor (in Figma leer gerendert → nachzeichnen), Beschreibung 'Besprechung' Ubuntu 400 10px/12px #000000 opacity 0.42, Avatar 56×56 rund rechts (exportiertes Bild). Vertikaler Rhythmus 30px zwischen den Karten. Hover: fill #6CC57CB8, active: #6CC57CD9. Lesbarkeit: Text bleibt #23233C/#000000 auf #6CC57CA3 — dunkler Text auf Grün, niemals heller Text auf dem Grün.

### CalendarStrip

Wochentagszeile (Ubuntu 400 15px/20px #000000, letter-spacing 0.4px) bei y=175, Datumszeile bei y=223, Spaltenraster 52px ab x=34. Ausgewählter Tag: Ellipse 42×42 fill #6CC57C (um 181,213, also Versatz −11,−10 zur Zahl), Zahl #000000 — Kontrast Grün/Text bleibt wie im Frame. Monatstitel '15-21 April 2019' Ubuntu 400 13px/15px #000000, zentriert, mit Chevron-Buttons 8×14 (Treffer 44×44). Zustände: anderer Tag = nur Text, hover Zahl #23233C + dünner Punkt 4px #6CC57C darunter, active = Ellipse wie oben.

### Header (Screen Header)

Zwei Varianten. (a) Weißer Header 414×126, fill #FFFFFF, shadow 0/3 blur 16 #0000001A, Titel Aleo 700 24px/29px #23233C links bei x=18,y=62, links Menü-Icon 18×15 (in Figma leer → nachzeichnen, 2px Stroke #181461), rechts User-Icon 27×27 #181461 bei x=367,y=25. (b) Leichtgewichtiger Header ohne Fläche: Back-Chevron 11×18 #181461 links, Ziel-Icon 27×27 #23233C rechts, darunter Titel Aleo 700 16px/19px #1C1C1C bei y=80. Erste Inhaltszeile immer 23–24px unter dem Header-Ende. Sticky, mit Safe-Area-Insets; kein Verlauf, keine Border — nur der Shadow trennt.

### OnboardingSlide

Vollflächiges Bild 414×896 (exportierte PNGs, z. B. 'jo-sonn…' mit Überlagerung #6CC57C 47% und Panel #F4F5FA darüber; Variante 'undraw_workout_gcgu' 242×190 auf bg #F4F5FA). Indikator-Punkte 10×10, Abstand 21px: aktiv #61D27C, inaktiv #E3E3E3 (Position 186/207/228, y=617). Titel Aleo 700 25px/30–32px, zentriert, #23233C oder #6CC57C (Slide 2) — Textblock 324px breit bei x=45. Subtext Inter 400 10px/13px #A5A5A5, zentriert. Fußzeile: 'Skip step' Inter 400 15px/19px #B4B4B4 links, grüner 'Next'-Button 115×42 radius 8 rechts. Zustände: Skip hover #6CC57C, active opacity 0.6; Punkte sind nicht klickbar, nur Anzeige; Slide-Wechsel 250ms Slide-in von rechts.

### SocialLoginButton

82×51, bg #FFFFFF, radius social 10px, shadow 0/0 blur 10 #0000000F, kein Border, Icon zentriert: Facebook 12×24 #0F279E (exportiertes PNG 'facebook-2'), zweite Kachel 82×51 mit 'search (1)' 24×24 (exportiertes PNG). Abstand zwischen den Kacheln 21px (x=115/218 bei y=649). Hover: shadow 0/4 blur 12 #00000014; active: translateY 1px, shadow entfernt; disabled: opacity 0.4. Trefferfläche 82×51 ≥ 44px.

### AvatarBadge

Kreis 51×51 fill #6CC57C, shadow 0/3 blur 6 #00000029, Initial Aleo 700 32px/41px #FFFFFF (Beispiel 'R' bei 311,82, also 15px Einzug). Keine Zustände — reine Anzeige.

### TextButton (inline)

Inline-Aktionen: 'Forgot you password?' Inter 400 13px/17px #8D8D8D zentriert, 'Don't have an account? sign up' Aleo 700 13px/17px #898888C9 zentriert (jeweils Trefferfläche 44px hoch). Hover #23233C, active #23233C opacity 0.7, focus 2px Outline #23233C. 'Modify' in Listen: Aleo 700 14px/17px #23233C mit Pencil-Icon 12×12 direkt dahinter.

### MenuPanel (Dashboard-Menü)

Panel im Kartenstil: bg #FFFFFF, radius card 20px, Padding 0; Zeilen 336×56 mit 1px-Trennlinie #1C1C1C opacity 0.2 zwischen den Zeilen, Label Aleo 700 14px/17px #1C1C1C, links Icon 20×20 #23233C, rechts Chevron 8×14 #23233C. Hover bg #F4F5FA, active bg #ECF1FA, disabled Label #A5A5A5. Erste Zeile oben, letzte ohne Trennlinie.

## Layout Principles

- Ein einziger Viewport: 414×896, Portrait, nicht responsiv. Keine Breakpoints, kein max-width-Container, kein Desktop-Raster — jede Fläche wird auf 414px Breite gebaut.
- Horizontale Ränder 39–41px links und rechts; Inhaltsbreite 334–336px, mittig zentriert. Alle Formularfelder, Karten und Listen halten diese Spalte.
- Vertikaler Rhythmus der Feldstapel: Felder 43px hoch, Pitch 63px (y=149 → 212 → 275 → 338); Karten-Padding 24px; Abstände zwischen Abschnitten 20px, zwischen Gruppen 24px, zwischen Listenzeilen 30px.
- Screens stapeln sich wie in den Frames: Login/Onboarding → Dashboard → Money Management → zurück über den Back-Chevron (11×18, #181461) oben links im Header. Kein Top-Nav-Tab, kein Hamburger außer in Variante (a) von 'Header'.
- Bottom-Tab-Bar als fester Fuß: Block 413×118 ab y=778, weiße Bar 413×77 ab y=819 mit shadow 0/3 blur 20 #60719329; der FloatingAddButton (64×63) liegt zentriert in der Aussparung der Karte darüber (y=778).
- Sichere Bereiche: oben 44px, unten 34px einrechnen; der scrollende Inhalt endet 118px über dem unteren Rand, damit die Bar nichts überdeckt. Screens klippen Inhalt (overflow hidden) wie die Frames.
- Oberer Screen-Bereich ist weiß (#FFFFFF) bis y=406 bzw. 138, darunter folgt der Screen-Grund (#F4F4F4 für Money Management, #F4F5FA für Dashboard/Login/Zeit) — die Kante ist gerade, nicht abgerundet.
- Elevation-Hierarchie: Felder 0/3 blur 16 #00000014 (Login: 0/10 blur 10 #0D4E810D), Social-Kacheln 0/0 blur 10 #0000000F, Bottom-Bar 0/3 blur 20 #60719329, Floating-Button 0/3 blur 40 #00000029, Header 0/3 blur 16 #0000001A. Karten tragen keinen Shadow, sie trennen über Weiß gegen den Grund.
- Typografie-Einsatz strikt nach Frame: Inter für UI, Formulare, Kicker und Labels; Aleo für Überschriften, Listentitel, Buttons mit Versalien-Anmutung und Zahlen; Ubuntu ausschließlich in den Kalender-Screens (Time Management); Actor ausschließlich für die Login-Feldwerte.
- Uppercase-Mikrolabels mit letter-spacing: 2.4–2.8px bei 12/14px-Kickern, 1.8px bei 9px-Kategorielabels; Zahlen stehen in Aleo/Inter 100–500, nie fett außer in Listentiteln.
- Lesbarkeit: dunkler Text (#23233C/#1C1C1C/#000000) auf dem Grün #6CC57C — wie in den Frames; über Bildern liegt entweder eine weiße Fläche oder das grüne Overlay mit weißem Text (Login-Fußzeile, Oppacity-Varianten #6CC57CA3/#6CC57CD9). Grün ist nie Hintergrund für grünen Text.
- Alle Figma-Assets werden als exportierte Bilder eingebunden (die in Figma leer gerenderten Icons ausgenommen: home, dish-spoon-knife, briefcase, friends, shopping-bag, gas-station, shop, Favorite, Search, Map, filters, dots, clock, menu, check, view — diese im Frame-Stil mit gleicher Strichstärke nachzeichnen, 24er-Raster, Farben #000000/#23233C/#BBC7DB). Keine selbst erfundenen Illustrationen.
- Zustände, die die Frames nicht zeigen, sind additiv und dürfen die Frame-Maße nicht verändern: active-Tab (#6CC57C + Indikator), Hover/Pressed/Disabled, Focus-Ring #23233C 2px — nur im Web-Verifikationsbuild sichtbar, in der mobilen App über Pressed/Disabled abgebildet.
- Bilder und Icons skalieren nie unabhängig vom Frame-Maß (z. B. Avatar 56×56, Thumbnail 69×69, Transaktions-Illustration 53×53) — feste px-Werte, keine Flex-Skalierung.

## Source Frames

This design was taken from the Figma frames below. They are the reference; the tokens above were read from them. Each frame's spec carries its exact positions, sizes, colours, fonts and texts; `design/figma/README.md` is the index.

Platform: mobile app (`mobile-app`) — design viewport 414×896 (phone, portrait) — one viewport, the design is not responsive.

- **Money Management** · businesshandler — spec `design/figma/money-management.md` — `design/figma/money-management.png` — https://www.figma.com/design/edl4sapqOV1QVVleWmFCt3/?node-id=0-2446
- **Money Management 2** · businesshandler — spec `design/figma/money-management-2.md` — `design/figma/money-management-2.png` — https://www.figma.com/design/edl4sapqOV1QVVleWmFCt3/?node-id=0-2573
- **Money Management 3** · businesshandler — spec `design/figma/money-management-3.md` — `design/figma/money-management-3.png` — https://www.figma.com/design/edl4sapqOV1QVVleWmFCt3/?node-id=0-2673
- **Time Management** · businesshandler — spec `design/figma/time-management.md` — `design/figma/time-management.png` — https://www.figma.com/design/edl4sapqOV1QVVleWmFCt3/?node-id=0-803
- **Time Management - 2** · businesshandler — spec `design/figma/time-management-2.md` — `design/figma/time-management-2.png` — https://www.figma.com/design/edl4sapqOV1QVVleWmFCt3/?node-id=0-3047
- **Time Management - 3** · businesshandler — spec `design/figma/time-management-3.md` — `design/figma/time-management-3.png` — https://www.figma.com/design/edl4sapqOV1QVVleWmFCt3/?node-id=0-1029
- **Login** · businesshandler — spec `design/figma/login.md` — `design/figma/login.png` — https://www.figma.com/design/edl4sapqOV1QVVleWmFCt3/?node-id=0-81
- **Login Slide** · businesshandler — spec `design/figma/login-slide.md` — `design/figma/login-slide.png` — https://www.figma.com/design/edl4sapqOV1QVVleWmFCt3/?node-id=0-20
- **Login Slide 2** · businesshandler — spec `design/figma/login-slide-2.md` — `design/figma/login-slide-2.png` — https://www.figma.com/design/edl4sapqOV1QVVleWmFCt3/?node-id=0-208
- **Dashboard** · businesshandler — spec `design/figma/dashboard.md` — `design/figma/dashboard.png` — https://www.figma.com/design/edl4sapqOV1QVVleWmFCt3/?node-id=0-681
- **Dashboard Menu** · businesshandler — spec `design/figma/dashboard-menu.md` — `design/figma/dashboard-menu.png` — https://www.figma.com/design/edl4sapqOV1QVVleWmFCt3/?node-id=0-2973
- **Dashboard Stats** · businesshandler — spec `design/figma/dashboard-stats.md` — `design/figma/dashboard-stats.png` — https://www.figma.com/design/edl4sapqOV1QVVleWmFCt3/?node-id=0-900
