# Nordic semiconductor eagle reference design

## Reference designs
![alt-text][dcdc_reference]

The reference designs supplied for eagle are made by following the [general pcb design guidelines][designguidenrf52] and referencing the [altium reference layout][altiumreference].
The eagle reference design is not the official reference designs, only the Altium reference designs has been tested and verified. They are available for download in Nordic's product pages.
The reference designs include eagle files as well as pdf printouts. For BOM see the altium reference designs.

* nRF51x22_qfaa
* nRF51x22_qfaa_dcdc
* nRF52832_qfaa
* nRF52832_qfaa_dcdc
* nRF52832_qfaa_nfc

## Libraries
**The libraries are not verified, only the Altium reference designs has been tested and verified.**

### Nordic_nRF
This library contains the nRF51 and nRF52 in qfn and bga packages, as well as; capacitors, inductors, and a 32MHz and 32kHz xtal. All that is needed for the core reference design. (link?)

### Nordic_misc
This library contains the rest of the components used in the sample eagle design(s) in this repository, as well as some simple antenna suggestions.

## Antenna
In the Nordic_misc library there is supplied some suggestions for antennas, please note that antenna characteristics depends greatly on the board layout. These antennas are made according to the [whitepaper][monopole] on quarter wave monopole 2.45 GHz antennas. Remember to [tune][antuning] the antenna

## NFC
An NFC listener antenna suggestion is supplied in the Nordic_misc library, this is the antenna used in the [nRF52-DK] development kit. Remember to [tune][nfctune] the antenna.


[github]: <https://github.com/NordicPlayground/nrf5-eagle-reference-design>
[designguidenrf51]: <https://devzone.nordicsemi.com/blogs/655/general-pcb-design-guidelines-for-nrf51/>
[designguidenrf52]: <https://devzone.nordicsemi.com/blogs/870/general-pcb-design-guidelines-for-nrf52/>
[referencecircuitry]: <https://infocenter.nordicsemi.com/index.jsp?topic=%2Fcom.nordic.infocenter.nrf52832.ps.v1.0%2Fref_circuitry.html&cp=1_2_0_51&anchor=concept_aqp_fd1_fq>
[altiumreference]: <http://infocenter.nordicsemi.com/index.jsp?topic=%2Fcom.nordic.infocenter.nrf52%2Fdita%2Fnrf52%2Fpdflinks%2Fref_layout.html&cp=1_5>
[nfctune]: <https://devzone.nordicsemi.com/blogs/957/nfc-tag-antenna-tuning/>
[nRF52-DK]: <http://www.nordicsemi.com/eng/Products/Bluetooth-low-energy2/nRF52-DK>
[dcdc_reference]: <nRF52832_qfaa_dcdc_reference.png>
[monopole]: <http://infocenter.nordicsemi.com/topic/com.nordic.infocenter.whitepapers/dita/whitepapers/pdflinks/nwp_008.html?cp=10_12>
[antuning]: <https://infocenter.nordicsemi.com/topic/com.nordic.infocenter.whitepapers/dita/whitepapers/pdflinks/nwp_017.html?cp=11_4>