# Case-1-Luma
Case 1: Luma ontwerp slimme producten Ugent

# LUMA - Slim Fietsverlichtingssysteem

**Deze repository bevat de volledige broncode, specifiek geoptimaliseerd voor de Arduino Nano.**

**LUMA** is een geavanceerd, modulair en zelfvoorzienend verlichtingssysteem voor fietsen. Het combineert veiligheid met een duurzame, gerecyclede stroomvoorziening. Het systeem beschikt over dynamische richtingaanwijzers ("Audi-stijl"), een smelheids gestuurd remlicht en een unieke opstartanimatie.

Wat LUMA uniek maakt, is het **hybride stroomsysteem**: een hergebruikte DC-motor (uit een oude schuurmachine) fungeert als krachtige dynamo. Een speciaal circuit met een **buffercondensator** stabiliseert de energie om de centrale powerbank op te laden, die vervolgens de verlichting voedt en je smartphone kan opladen via USB-C.


## Functionaliteiten

### 1. Slimme Verlichting
* **Achterlicht (Matrix 3x12):**
    * **Rijden:** Gedimd rood licht.
    * **Vertragen (Uitbollen):** Licht op naar medium rood (gedetecteerd via accelerometer).
    * **Remmen:** Fel rood remlicht.
    * **Noodstop:** Knipperend rood licht (strobe) bij hard remmen.
* **Voorlicht (Matrix 3x8 + PowerLEDs):**
    * **Dagrijverlichting (DRL):** Witte LED-matrix voor zichtbaarheid.
    * **Koplamp:** 4x High Power LEDs voor zicht in het donker (geschakeld via MOSFET).
* **Richtingaanwijzers:**
    * Dynamische "Wipe" animatie (Oranje) die van binnen naar buiten loopt.

### 2. Modulair & Waterdicht Ontwerp
* **Waterdichte Connectoren:** Het systeem maakt gebruik van hoogwaardige IP68 connectoren (YETOR). Hierdoor is de opstelling volledig modulair: lampen en knoppen kunnen eenvoudig worden losgekoppeld of vervangen.
* **3D Geprinte Behuizing:** Op maat gemaakte behuizingen met **TPU-afdichtingen** zorgen ervoor dat de elektronica in alle weersomstandigheden droog blijft.

### 3. DIY Hybrid Power (Upcycled Dynamo)
* **Custom Generator:** Een DC-motor uit een oude schuurmachine is gemonteerd als wrijvingsdynamo.
* **Stabiele Stroom:** Een circuit met een grote **buffercondensator** vlakt het fluctuerende signaal van de motor af tot een constante 5V-lading voor de powerbank.
* **Phone Charging:** Geïntegreerde USB-C uitgang aan het stuur om je telefoon op te laden tijdens het fietsen.



## Hardware & Componenten

### Elektronica
* **Microcontroller:** Arduino Nano (Code in `/code`).
* **Sensor:** MPU-6050 Accelerometer (Op zijn zijkant gemonteerd).
* **Generator:** DC Motor (Gerecycled uit schuurmachine).
* **Power Conditioning:** Buffercondensator.
* **Opslag:** Powerbank met pass-through charging support.
* **LEDs:** WS2812B Strips + 4x High Power LEDs.
* **Bediening:** 3x R16-503 Latching Drukknoppen met LED-feedback.

### Connectiviteit
We gebruiken **YETOR Waterdichte Connectoren** om de centrale unit met de randapparatuur te verbinden.
* **Product:** [YETOR Waterdichte Draadconnectoren (Amazon)](https://www.amazon.nl/YETOR-waterdichte-draadconnectoren-vrachtwagen-draadverbindingen/dp/B07S7J85BT/ref=sr_1_1_sspa?adgrpid=1335907096403061&hvadid=83494577097741&hvbmt=be&hvdev=c&hvlocphy=251367&hvnetw=s&hvqmt=e&hvtargid=kwd-83494581479747%3Aloc-14&hydadcr=26364_2804228&mcid=2555db10c2f93f9ab696e766e23b09bc&sr=8-1-spons&aref=69AhAWc195&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY)



## 3D Onderdelen (STL Bestanden)

Alle printbare onderdelen zijn te vinden in de map `/3d-onderdelen`. Het systeem maakt gebruik van een universele "Rekker & Haak" montagemethode.

### 1. Verlichtingsmodules
* **`Light_Holder.stl`**: Behuizing waar de LED-matrix in past.
* **`Light_Lens.stl`**: Transparante lens voor lichtdiffusie die op de houder klikt.

### 2. Centrale Control Unit
* **`Main_Housing_Body.stl`**: Behuizing voor de Arduino Nano, PCB en Powerbank.
* **`Main_Housing_Seal_TPU.stl`**: Een flexibele dichtingsring (**Print in TPU**) voor het waterdicht maken van de deksel.

### 3. DIY Dynamo Systeem
* **`Motor_Mount_Holder.stl`**: Robuuste klem om de schuurmachine-motor aan de voor- of achtervork te bevestigen.
* **`Friction_Wheel.stl`**: Een wrijvingswiel dat op de as van de DC-motor wordt geperst om contact te maken met de fietsband.

### 4. Bediening & Montage
* **`Button_Housing.stl`**: Behuizing voor de 3 knoppen aan het stuur.
* **`Mounting_Hook.stl`**: Universele haak voor het montagesysteem.
* **`Adjustable_Strap.stl`**: Een flexibele, verstelbare rekker (**Print in TPU**) die om het fietsframe spant en in de haak grijpt.



