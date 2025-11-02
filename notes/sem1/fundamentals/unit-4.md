# Output Devices

An output device is any piece of computer hardware that converts information from electronic data into a human-perceptible form. This output can be visual (monitors), physical (printers), or auditory (speakers).

---

## Monitors (Visual Display Units - VDU)

Monitors are the most common visual output device, displaying data processed by the computer's video card. The display quality is determined by factors like resolution (number of pixels), refresh rate (how often the image is redrawn), response time (how quickly a pixel can change color), and the underlying panel technology.

### Liquid Crystal Display (LCD)

LCDs use a backlight (traditionally a CCFL - Cold Cathode Fluorescent Lamp) that passes light through a layer of liquid crystals. These crystals are aligned or twisted by an electric current to either block the light or allow it to pass through red, green, and blue (RGB) sub-pixels, which combine to form the final image.

[insert image on how an LCD panel works here]

* **Active Matrix (TFT):** Modern LCDs use Thin-Film Transistor (TFT) technology. This is an active-matrix display where each pixel is controlled by one to four dedicated transistors. This provides faster response times and better image quality (brighter, sharper) compared to older passive-matrix displays.
* **Panel Types:** The orientation of the liquid crystals defines the panel type:
    * **TN (Twisted Nematic):** Inexpensive and known for very fast response times, making them popular for gaming. They suffer from poor color reproduction and significant color shift when viewed from an angle (poor viewing angles).
    * **IPS (In-Plane Switching):** Offer the best color accuracy and the widest viewing angles. They are favored by graphic designers and professionals. Their main trade-offs are slower response times and "IPS glow" (a glow on dark scenes) compared to other types.
    * **VA (Vertical Alignment):** Provide a good balance. They offer much better contrast ratios (deeper blacks) and viewing angles than TN panels, but typically have slower response times than both TN and IPS, which can lead to "ghosting" in fast-moving scenes.

### Light Emitting Diode (LED) Display

This term is a common source of confusion. In most consumer electronics, an "LED monitor" is **not** a true LED display.

* **1. LED-Backlit LCD:** This is what 99% of "LED monitors" are. It is simply an **LCD panel** (like the one described above) that uses **LEDs** as its backlight instead of the older, bulkier CCFLs.
    * **Advantages over CCFL:** Thinner designs, lower power consumption, better brightness, and improved contrast ratios.
    * **Local Dimming:** A feature in higher-end LED-backlit displays where zones of LEDs can be dimmed or brightened independently, allowing for deeper blacks in dark areas of the screen.

* **2. True LED (OLED/MicroLED):** These are **emissive** displays. Each individual pixel is a tiny LED (or **O**rganic **L**ED) that produces its own light. There is no backlight.
    * **Advantages:** Since each pixel can be turned off completely, this technology achieves "perfect" black levels and an almost infinite contrast ratio. They also have exceptionally vibrant colors and instantaneous response times.

### Plasma Display Panel (PDP)

Plasma displays are an emissive technology, now considered obsolete and replaced by LCD and OLED.

* **Mechanism:** Each pixel is composed of three tiny cells (for RGB) containing a noble gas (like neon and xenon). When an electric current is applied, the gas turns into a **plasma**, which emits ultraviolet (UV) light. This UV light then strikes a phosphor coating on the cell, causing the phosphor to glow and produce visible light.
* **Pros:** At their peak, they offered superior contrast ratios (deep blacks, similar to OLED) and excellent response times with no motion blur.
* **Cons:** High power consumption, significant heat generation, heavy, and susceptible to **"burn-in"** (permanent image retention).

---

## Printers

Printers are output devices that generate a hard copy (a physical, permanent representation) of electronic data on a medium, usually paper.

### Impact vs. Non-Impact Printers

Printers are broadly classified based on how they transfer the image to the paper.

#### Impact Printers

These printers create an image by physically **striking** an ink-soaked ribbon against the paper. A "hammer" or "pin" mechanism forces the contact.

* **Characteristics:**
    * Noisy operation.
    * **Key Advantage:** Can print on multi-part forms (carbon-copy or carbonless copy paper) because the physical force transfers the image through multiple layers.
    * Low print quality (for graphics).
    * Low cost per page.
* **Examples:** Dot-matrix printers, Daisy-wheel printers.

#### Non-Impact Printers

These printers form an image **without** making direct physical contact with the paper. They use various technologies like spraying ink, fusing toner, or using heat.

* **Characteristics:**
    * Very quiet operation.
    * Cannot be used for multi-part forms.
    * Capable of high-resolution photo-quality output.
    * Generally faster for high-quality output.
* **Examples:** Inkjet, Laser, Thermal printers.

---

### Types of Printers

#### Dot-Matrix Printer (Impact)

* **Mechanism:** Uses a print head that moves back and forth across the page. The print head contains a matrix of small **pins** (e.g., 9-pin for draft quality or 24-pin for "Near Letter Quality" - NLQ). These pins are fired selectively by electromagnets to strike an inked ribbon, forming characters from a pattern of dots.
* [insert image on dot-matrix printer mechanism here]
* **Use Case:** Largely obsolete in consumer use, but still vital in industrial and business environments (e.g., logistics, auto garages, accounts departments) for printing invoices, shipping forms, and receipts that require multi-part copies.

#### Inkjet Printer (Non-impact)

* **Mechanism:** Sprays microscopic droplets of liquid ink onto the paper from a print head containing hundreds of tiny nozzles.
* **Technologies:**
    * **1. Thermal Bubble (e.g., HP, Canon):** A resistor in the nozzle chamber rapidly heats the ink, creating a steam bubble. This bubble expands, forcing a droplet of ink out of the nozzle. When the resistor cools, the bubble collapses, pulling more ink into the chamber.
    * **2. Piezoelectric (e.g., Epson):** A piezoelectric crystal is located in the ink chamber. When an electric current is applied, the crystal vibrates or flexes, creating pressure that ejects the ink droplet. This method provides more precise control over the droplet size.
* [insert image on thermal bubble vs piezoelectric inkjet here]
* **Use Case:** Ideal for high-quality color printing, especially photographs. Common for home use and small offices. Initial hardware cost is low, but the cost of ink cartridges (consumables) can be high.

#### Laser Printer (Non-impact)

* **Mechanism:** A complex process based on electrostatics (xerography).
    1.  **Charging:** A primary charge roller applies a uniform negative (or positive) electrostatic charge to a photosensitive **drum**.
    2.  **Writing (Exposing):** A laser beam is scanned across the drum, "writing" the image. Where the laser hits, it neutralizes the charge, creating an "electrostatic image."
    3.  **Developing:** The drum rotates past a developer roller, which holds **toner** (a fine, dry powder) with the same charge as the drum. The toner is repelled by the charged areas but attracted to the neutralized areas (where the laser wrote).
    4.  **Transferring:** The paper is fed past the drum and given a strong opposite charge, which pulls the toner from the drum onto the paper.
    5.  **Fusing:** The paper passes through a **fuser** unit (a pair of hot rollers), which melts and presses the toner, permanently bonding it to the paper.
* [insert image on laser printer printing process here]
* **Use Case:** Best for high-volume, high-speed text and monochrome graphics printing (e.g., large offices, libraries). Offers a very low cost per page and extremely fast print speeds. Color laser printers exist but are more complex and expensive.

#### Thermal Printer (Non-impact)

* **Mechanism:** Uses heat to create an image.
    * **1. Direct Thermal:** The print head contains heating elements that pass over special **thermochromic** (heat-sensitive) paper. The paper turns black in the areas that are heated. **No ink, toner, or ribbon is required.**
    * **2. Thermal Transfer:** The print head heats a wax or resin-based **ribbon**, melting it onto the paper. This is more durable than direct thermal and can print in color (using CMY sections of the ribbon).
* **Use Case:**
    * **Direct Thermal:** Overwhelmingly used for receipts (Point-of-Sale systems), shipping labels, barcodes, and tickets. The print fades over time, especially when exposed to heat or sunlight.
    * **Thermal Transfer:** Used for durable labels, ID badges, and high-quality barcodes that need to last.

---

## Other Output Devices

### Plotters

A plotter is a specialized printer used for **vector graphics**. While a regular printer prints in a raster (dot-by-dot) fashion, a plotter draws continuous, smooth lines using a pen, marker, or cutting tool.

* **Types:**
    * **Pen Plotters:** The classic type.
        * **Flatbed Plotter:** The paper is held stationary, and a robotic arm moves a pen (or multiple pens of different colors) in both X andY axes over the paper.
        * **Drum Plotter:** The paper is rolled back and forth on a drum (providing the Y-axis) while the pen moves side-to-side on a carriage (providing the X-axis).
    * **Electrostatic/Thermal Plotters:** Modern large-format plotters that operate more like a very wide laser or thermal printer, creating a raster image for large outputs.
* [insert image on drum plotter vs flatbed plotter here]
* **Use Case:** Used for large-scale, high-precision drawings, such as architectural blueprints, engineering designs (CAD), manufacturing schematics, and billboards.

### Voice Output Systems

These systems (also known as voice synthesizers) convert digital text data into audible, spoken language. This process is called **Text-to-Speech (TTS)**.

* **Mechanism (Simplified):**
    1.  **Text Pre-processing (Normalization):** The system analyzes the text, expanding abbreviations (e.g., "Dr." -> "Doctor," "123" -> "one hundred twenty-three") and interpreting punctuation for pauses and intonation.
    2.  **Phonetic Conversion:** Converts the normalized text into a sequence of **phonemes** (the basic, distinct units of sound in a language).
    3.  **Waveform Generation (Synthesis):** Generates the final audio waveform.
        * **Concatenative Synthesis:** Stitches together small snippets of pre-recorded human speech (phones, diphones) stored in a large database.
        * **Neural Synthesis (Modern):** Uses deep learning models (like Tacotron or WaveNet) to generate highly realistic, natural-sounding, and expressive speech from scratch.
* **Use Case:** Accessibility tools for the visually impaired (screen readers), virtual assistants (Siri, Google Assistant, Alexa), GPS navigation, and public announcement systems.

### Projectors

A digital projector is an optical device that receives a video signal and projects the corresponding image onto a surface (like a screen or wall).

* **Key Technologies:**
    * **DLP (Digital Light Processing):** Uses a **DMD** (Digital Micromirror Device) chip, which is a semiconductor covered in millions of microscopic mirrors. Each mirror represents a pixel and can be rapidly tilted to either reflect light through the lens (pixel ON) or away from it (pixel OFF).
        * **Single-chip DLP:** Uses a high-speed spinning color wheel (RGB) to create sequential color.
        * **3-chip DLP:** Uses three separate DMD chips (one each for R, G, B), offering superior color and no "rainbow effect." Used in high-end cinema projectors.
    * **LCD (Liquid Crystal Display):** Uses a powerful lamp that shines light through a dichroic mirror system, splitting the light into its red, green, and blue components. Each color channel passes through its own small, high-temperature LCD panel, which controls the brightness for each pixel. The three colored images are then recombined in a prism before passing through the main lens.
* [insert image on DLP vs 3LCD projector technology here]
* **Use Case:** Business presentations, classroom education, home cinema, and large-venue displays (e.g., concerts, auditoriums).
