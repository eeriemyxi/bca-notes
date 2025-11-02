# Input Devices

## Keyboards: Keyboard Layouts

A **keyboard** is the most common input device, used to enter text, numbers, and commands. While the underlying mechanism (e.g., mechanical switch, membrane) is important, the **layout** dictates the arrangement of keys.

[insert image on different keyboard layouts QWERTY AZERTY QWERTZ here]

### QWERTY
* **Description:** The most ubiquitous layout worldwide, named for the first six keys in the top-left alphabet row.
* **Origin:** Designed by Christopher Latham Sholes in the 1870s for the Sholes and Glidden typewriter.
* **Purpose:** The layout was *not* designed for speed, but rather to **prevent typebar jams** on early mechanical typewriters by separating commonly used letter pairs (like 'TH' or 'ST').
* **Variants:** Different regions have slight variations (e.g., US vs. UK QWERTY).

### AZERTY
* **Description:** The standard layout used in **France** and other French-speaking countries.
* **Key Differences from QWERTY:**
    * `A` and `Q` are swapped.
    * `Z` and `W` are swapped.
    * `M` is moved to the right of `L`.
    * Numbers on the top row require the `Shift` key to be pressed; the unshifted keys are used for accented characters (e.g., `é`, `è`, `ç`).

### QWERTZ
* **Description:** The standard layout used in **Germany**, Austria, and much of Central Europe.
* **Key Differences from QWERTY:**
    * `Y` and `Z` are swapped. This is because `Z` is a much more common letter than `Y` in German, and `T` and `Z` often appear together.
    * Includes keys for German diacritics (e.g., `ü`, `ö`, `ä`) and the Eszett (`ß`).

### Dvorak
* **Description:** A layout designed by August Dvorak and William Dealey in the 1930s.
* **Purpose:** Designed for **ergonomics and typing speed**.
* **Design Principles:**
    * Places the most frequently used letters on the **home row** (AOEUIDHTNS) to maximize efficiency and reduce finger movement.
    * Alternates key presses between hands (rhythm).
* **Adoption:** Despite its purported benefits, it remains a niche layout due to the dominance of QWERTY.

[insert image on QWERTY vs Dvorak layout here]

---

## Pointing Devices

Pointing devices are input hardware that allow a user to control a pointer or cursor in a Graphical User Interface (GUI).

### Mechanical Mouse
* **Description:** An older mouse technology that uses a combination of mechanical and optical components.
* **Mechanism:**
    1.  A rubber-coated **steel ball** is housed on the underside.
    2.  As the mouse moves, the ball rotates.
    3.  This ball turns two perpendicular **rollers** (or shafts) inside the mouse, one for the X-axis (horizontal) and one for the Y-axis (vertical).
    4.  Each roller is attached to an **encoder wheel** (a plastic disc with slots or spokes).
    5.  An **LED** shines light through the slots of the rotating wheel towards an **optical sensor** (phototransistor).
    6.  As the wheel spins, it "chops" the light beam, creating pulses. The frequency of these pulses indicates the speed of movement, and the sequence (which sensor detects light first) indicates the direction.
* **Disadvantages:** Prone to dirt and dust buildup (the ball would pick up debris, clogging the rollers), requiring frequent cleaning. Requires a mousepad for optimal traction.

[insert image on internal mechanism of mechanical mouse here]

### Optical Mouse
* **Description:** The modern standard for mice, which uses light and a digital sensor.
* **Mechanism:**
    1.  An **LED** (Light Emitting Diode) or **Laser** illuminates the surface beneath the mouse.
    2.  A small, low-resolution **CMOS sensor** (a type of camera) captures thousands of microscopic images of the surface per second.
    3.  A **Digital Signal Processor (DSP)** analyzes this stream of images.
    4.  By comparing consecutive images, the DSP detects changes in patterns, texture, and position.
    5.  It calculates the **delta** (change) in X and Y coordinates and sends this data to the computer, which moves the cursor.
* **Advantages:** No moving parts (less wear and tear), higher precision (measured in **DPI - Dots Per Inch**), and works on most surfaces (though standard LEDs struggle on glass or highly reflective surfaces; laser mice perform better here).

### Touchpad (Trackpad)
* **Description:** A stationary pointing device common on laptop computers.
* **Mechanism:** Based on **capacitive sensing**.
    1.  The touchpad surface hides a grid of **conductive electrodes**.
    2.  This grid creates a stable electrostatic field.
    3.  When a conductor (like a human finger) approaches or touches the surface, it disrupts this field by changing the capacitance at specific (X, Y) coordinates.
    4.  A controller chip constantly monitors the capacitance of every point on the grid.
    5.  By detecting the location of the disruption, it calculates the finger's position.
* **Features:** Modern touchpads support **multi-touch**, allowing for gestures like pinching to zoom, two-finger scrolling, etc.

### Trackball
* **Description:** Essentially an "upside-down mouse." The device itself is stationary, and the user rolls a ball with their thumb or fingers.
* **Mechanism:**
    * **Mechanical:** Older trackballs used rollers and encoders, just like a mechanical mouse, to detect the ball's rotation.
    * **Optical:** Modern trackballs use a sensor system. An LED illuminates the ball (which often has a pattern of dots), and a sensor tracks the movement of these dots to determine rotation in the X and Y axes.
* **Use Cases:** Good for limited desk space (since the device doesn't move) and can be more ergonomic for some users, reducing wrist and arm strain.

[insert image on a thumb-operated trackball here]

### Joystick
* **Description:** A pointing device consisting of a stick (handle) that pivots on a base.
* **Mechanism:**
    1.  The base of the stick is mounted in a **gimbal**, allowing for at least two axes of movement (X-axis: left/right, Y-axis: forward/back).
    2.  The angle of the stick is measured by sensors, typically **potentiometers** (variable resistors) or non-contact **Hall effect sensors** (which measure magnetic field changes).
    3.  This analog data is converted to a digital signal.
* **Features:** Often includes buttons on the stick and base, a "hat switch" (D-pad), and sometimes a Z-axis (by twisting the stick) for rudder control.
* **Use Cases:** Primarily used in gaming (flight simulators, arcade games) and industrial controls (robotics, cranes).

### Digitizer (Graphics Tablet)
* **Description:** An input device that allows a user to draw, sketch, or write by hand using a special pen (stylus) on a flat pad (tablet).
* **Mechanism:** Most common technology is **Electromagnetic Resonance (EMR)**.
    1.  The tablet (pad) contains a grid of wires that transmits an electromagnetic signal.
    2.  This signal powers a resonant circuit (coil and capacitor) inside the **stylus** (this is why most styli are **passive** and require no batteries).
    3.  The stylus, now powered, returns a signal of its own to the tablet.
    4.  The tablet's grid detects this return signal to precisely calculate the (X, Y) position of the stylus tip.
* **Advanced Features:** The EMR signals also communicate **pressure sensitivity** (how hard the user is pressing), **tilt** (the angle of the stylus), and button presses from the stylus.
* **Use Cases:** Digital art, graphic design, animation, CAD/CAM, and capturing handwritten signatures.

---

## Scanners

A scanner is a device that optically scans images, printed text, or objects and converts them into a digital image.

### Hand-held Scanner
* **Description:** A compact, portable scanner that the user must manually drag across the document to be scanned.
* **Mechanism:** Contains a small scan head (light source and image sensor). The quality of the scan is dependent on the user's ability to move the scanner at a **steady, consistent speed**.
* **Relevance:** Largely obsolete for document scanning, having been replaced by smartphone apps (which use the phone's camera and software to correct for perspective) and portable "wand" scanners.

### Flat-bed Scanner
* **Description:** The most common type of desktop scanner, featuring a flat glass surface (platen) on which to place documents, books, or photos.
* **Mechanism:**
    1.  The document is placed face-down on the glass.
    2.  A **scan head** (an assembly containing a bright light source, mirrors, a lens, and an image sensor) is mounted on a mechanical arm.
    3.  This scan head moves step-by-step across the document from one end to the other.
    4.  At each step, it illuminates a thin strip of the document.
    5.  The light reflects off the document, through a system of mirrors and a lens, and onto the image sensor.
    6.  The image sensor is typically a **CCD (Charge-Coupled Device)** or **CIS (Contact Image Sensor)**.
        * **CCD:** A high-quality, light-sensitive sensor. It requires a lens and mirrors, making the scanner bulkier, but providing a greater depth of field (good for scanning 3D objects or books).
        * **CIS:** A sensor that is the same width as the scan area. It uses a row of red, green, and blue LEDs for illumination and places the sensor elements very close to the paper (no lens needed). This allows for much thinner, lighter, and more power-efficient scanners, but with a very shallow depth of field.
    7.  The sensor captures the light intensity and
        color for each pixel, which is then converted into digital data.

[insert image on diagram of flat-bed scanner CCD vs CIS here]

---

## Readers

Readers are specialized input devices that recognize specific types of marks or characters.

### OMR (Optical Mark Recognition)
* **Description:** A technology used to detect the **presence or absence** of a mark in a predefined position. It does *not* read characters.
* **Mechanism:**
    1.  A pre-printed form (e.g., a multiple-choice answer sheet) has specific "bubble" locations.
    2.  The OMR device shines a light source onto the form.
    3.  A sensor measures the amount of light reflected back.
    4.  A filled-in bubble reflects **less light** (as the dark mark absorbs light) than an empty bubble.
    5.  The device registers a "mark" if the reflected light is below a certain threshold.
* **Use Cases:** Standardized tests (e.g., SAT, GRE), surveys, ballots, lottery tickets.

### OCR (Optical Character Recognition)
* **Description:** A technology that converts images of typed, handwritten, or printed text into machine-readable text data (e.g., ASCII or Unicode).
* **Process:**
    1.  **Image Acquisition:** A document is scanned using a flat-bed scanner or camera.
    2.  **Pre-processing:** The software cleans up the image. This includes:
        * **Deskewing:** Straightening a slightly tilted image.
        * **Denoising:** Removing stray spots or "noise."
        * **Binarization:** Converting a grayscale image to black and white.
    3.  **Segmentation:** The software identifies and separates blocks of text, lines of text, individual words, and finally, individual characters (glyphs).
    4.  **Feature Extraction:** The software analyzes each character's shape, identifying features like lines, curves, loops, and intersections.
    5.  **Classification (Recognition):** These features are compared against a database of known characters using sophisticated algorithms (e.g., **pattern matching**, **feature detection**, or **neural networks**). The algorithm assigns a "best guess" character.
    6.  **Post-processing:** The system uses a built-in dictionary or language model to correct errors. For example, if it reads "qulck," it might correct it to "quick" based on context.
* **Use Cases:** Digitizing books and documents, data entry from invoices or bank statements, automated license plate recognition (ALPR).

### MICR (Magnetic Ink Character Recognition)
* **Description:** A character-recognition technology used primarily by the banking industry to streamline the processing of **checks**.
* **Mechanism:**
    1.  Checks are printed using a special **magnetic ink** (containing iron oxide) and a specific font, such as **E-13B** (used in North America) or **CMC-7** (used in Europe).
    [insert image on MICR E-13B font here]
    2.  The check is passed through an MICR reader.
    3.  The reader's "read head" first **magnetizes** the characters in the magnetic ink.
    4.  A second part of the head then reads the unique magnetic signature (waveform) given off by each character.
* **Advantages:**
    * **Security:** The magnetic ink is difficult to forge.
    * **Reliability:** The reading is highly accurate, even if the characters are obscured by stains, marks, or overwriting (which would foil OCR).
    * **Speed:** The process is extremely fast.

---

## Other Devices

### Digital Camera
* **Description:** A device that captures photographs and stores them digitally, rather than on chemical film.
* **Mechanism:**
    1.  Light from the scene passes through the **lens**, which focuses it.
    2.  The **aperture** and **shutter** control the amount of light that enters.
    3.  The light strikes an **image sensor** (either a **CCD** or, more commonly, a **CMOS** sensor).
    4.  The sensor is a grid of millions of tiny light-sensitive cells (photodiodes). Each cell (pixel) measures the **intensity** of light hitting it, generating a small electrical charge.
    5.  For color, the sensor is overlaid with a **Bayer filter**, a mosaic of Red, Green, and Blue filters, so each pixel captures data for only one color.
    6.  The analog electrical signal from the sensor is read and converted into a digital signal by an **Analog-to-Digital Converter (ADC)**.
    7.  A dedicated **Image Signal Processor (ISP)** performs **demosaicing** (reconstructing a full-color image from the Bayer filter data), white balance, noise reduction, and compression (e.g., into a JPEG file).
    8.  The final digital file is stored on a **memory card** (e.g., SD card).

### Digital Microphone
* **Description:** A microphone that converts sound directly into a digital audio stream, as opposed to an analog microphone which outputs an analog electrical signal.
* **Mechanism:**
    1.  **Transducer:** Like an analog mic, it has a diaphragm that vibrates in response to sound waves, converting acoustic energy into an analog electrical signal.
    2.  **Integrated Circuitry:** The key difference is that the digital mic also contains:
        * A **pre-amplifier** to boost the weak analog signal.
        * An **Analog-to-Digital Converter (ADC)**.
    3.  **ADC Process:** The ADC samples the analog signal thousands of times per second (e.g., 44,100 times/sec for CD quality) and quantifies its amplitude, converting the continuous analog wave into a discrete stream of binary data (a process called **Pulse-Code Modulation - PCM**).
* **Advantages:** The digital signal is less susceptible to electrical noise and interference, especially over long cable runs. They can often connect directly to computers via USB without needing a separate audio interface or sound card.
