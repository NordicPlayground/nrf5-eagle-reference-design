# Getting started with nRF5 and CadSoft EAGLE (R)

Nordic Semiconductor already provides [reference designs][altiumreference] for Altium Designer (R), but if you cant afford Altium or simply prefer EAGLE here is a quick guide on how to use the EAGLE reference design.

This quick guide assumes you are familiar with doing PCB designs in EAGLE, if not; both [Adafruit] and [SparkFun] has guides on how to get started


1. First clone or download the reference designs and libraries from [Github]
2. Select the reference-design that fits your application (if you have no idea; use *nRF52832_qfaa_dcdc*)
3. Add your own parts in the circuit diagram
4. Do the layout and routing
5. Do not modify the geometry of the rf part

Please refer to the general pcb design guidelines for [nRF51][designguidenrf51] or [nRF52][designguidenrf52]

## 1. First clone or download the reference designs and libraries from [Github]

If you are familiar with [git] this is self explanatory, if not press the (green) "Clone or download" button and then "Download ZIP". If you are not familiar with [git] it is higly reccomended to learn version control, there is a lot of guides available online.


## 2. Select the reference-design that fits your application (if you have no idea; use *nRF52832_qfaa_dcdc*)

All reference designs supplied here are for the qfn package.
If you want to use the internal ldo (not reccomended) select nRF5\*_qfaa, if you want an example of nfc antenna usage select nRF5\*_qfaa_nfc.
You probably want the nRF51x2_qfaa_dcdc or nRF52832_qfaa_dcdc, for nRF51 or nRF52 respectively.


## 3. Add your own parts in the circuit diagram

Here is the part where you do your design, use your own libraries, use libraries supplied with eagle, use parts from the Nordic_misc library, make your own parts, etc.


## 4. Do the layout and routing

This is also a part of your regular workflow. Lay out your design next to or around the reference layout.


## 5. Do not modify the geometry of the rf part

Now, the important part: Do not add components close to the rf layout. This means around where you attach the antenna (the signal named RF).
The cutout in the ground plane is there for a reason. Add cutouts to any internal layers of the pcb as well. There should be a ground plane on the bottom layer.
Add a generous amound of ground stiching vias (remember vias are free).

## 6. Done

There. You are done with your nRF5 design in eagle, dont forget to run design reviews before ordering pcbs. And dont forget to tune the antenna when you have your prototype in hand.


# Some info on the git repository

## Antenna
In the Nordic_misc library there is supplied some suggestions for antennas, please note that antenna characteristics depends greatly on the board layout. These antennas are made according to the [whitepaper][monopole] on quarter wave monopole 2.45 GHz antennas. Remember to [tune][antuning] the antenna

## NFC
An NFC listener antenna suggestion is supplied in the Nordic_misc library, this is the antenna used in the [nRF52-DK] development kit. Remember to [tune][nfctune] the antenna.

## Reference designs
![alt-text][dcdc_reference]

The reference designs supplied for eagle are made by following the [general pcb design guidelines][designguidenrf52] and referencing the [altium reference layout][altiumreference]

## Libraries

### Nordic_nRF
This library contains the nRF51 and nRF52 in qfn and bga packages, as well as; capacitors, inductors, and a 32MHz and 32kHz xtal. All that is needed for the core reference design.

### Nordic_misc
This library contains the rest of the components used in the sample eagle design(s) in the github repository, as well as some simple antenna suggestions.

[sparkfun]: <https://www.sparkfun.com/>
[adafruit]: <https://www.adafruit.com/>
[github]: <https://github.com/NordicSemiconductor/nrf5-eagle-reference-design>
[designguidenrf51]: <https://devzone.nordicsemi.com/blogs/655/general-pcb-design-guidelines-for-nrf51/>
[designguidenrf52]: <https://devzone.nordicsemi.com/blogs/870/general-pcb-design-guidelines-for-nrf52/>
[referencecircuitry]: <https://infocenter.nordicsemi.com/index.jsp?topic=%2Fcom.nordic.infocenter.nrf52832.ps.v1.0%2Fref_circuitry.html&cp=1_2_0_51&anchor=concept_aqp_fd1_fq>
[altiumreference]: <http://infocenter.nordicsemi.com/index.jsp?topic=%2Fcom.nordic.infocenter.nrf52%2Fdita%2Fnrf52%2Fpdflinks%2Fref_layout.html&cp=1_5>
[nfctune]: <https://devzone.nordicsemi.com/blogs/957/nfc-tag-antenna-tuning/>
[nRF52-DK]: <http://www.nordicsemi.com/eng/Products/Bluetooth-low-energy2/nRF52-DK>
[dcdc_reference]: <nRF52832_qfaa_dcdc_reference.png>
[monopole]: <http://infocenter.nordicsemi.com/topic/com.nordic.infocenter.whitepapers/dita/whitepapers/pdflinks/nwp_008.html?cp=10_12>
[antuning]: <https://infocenter.nordicsemi.com/topic/com.nordic.infocenter.whitepapers/dita/whitepapers/pdflinks/nwp_017.html?cp=11_4>
[git]: <https://git-scm.com/>