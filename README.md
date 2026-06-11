# SFP_FLASHER

SFP/QSFP Flash Tool

QSFP-DD Pinout
| Pin | Symbol   | Description                          |
|-----|----------|--------------------------------------|
| 1   | GND      | Ground                               |
| 2   | Tx2n     | Transmitter Inverted Data Input      |
| 3   | Tx2p     | Transmitter Non-Inverted Data Input  |
| 4   | GND      | Ground                               |
| 5   | Tx4n     | Transmitter Inverted Data Input      |
| 6   | Tx4p     | Transmitter Non-Inverted Data Input  |
| 7   | GND      | Ground                               |
| 8   | ModSelL  | Module Select                        |
| 9   | ResetL   | Module Reset                         |
| 10  | Vcc Rx   | +3.3V Power Supply Receiver          |
| 11  | SCL      | 2-wire Serial Interface Clock        |
| 12  | SDA      | 2-wire Serial Interface Data         |
| 13  | GND      | GND                                  |
| 14  | Rx3p     | Receiver Non-Inverted Data Output    |
| 15  | Rx3n     | Receiver Inverted Data Output        |
| 16  | GND      | Ground                               |
| 17  | Rx1p     | Receiver Non-Inverted Data Output    |
| 18  | Rx1n     | Receiver Inverted Data Output        |
| 19  | GND      | Ground                               |
| 20  | GND      | Ground                               |
| 21  | Rx2n     | Receiver Inverted Data Output        |
| 22  | Rx2p     | Receiver Non-Inverted Data Output    |
| 23  | GND      | Grounds                              |
| 24  | Rx4n     | Receiver Inverted Data Output        |
| 25  | Rx4p     | Receiver Non-Inverted Data Output    |
| 26  | GND      | Ground                               |
| 27  | ModPrsL  | Module Present                       |
| 28  | IntL     | Interrupt                            |
| 29  | Vcc Tx   | +3.3V Power Supply Transmitter       |
| 30  | Vcc1     | +3.3V Power Supply                   |
| 31  | LPMode   | Low Power Mode                       |
| 32  | GND      | Ground                               |
| 33  | Tx3p     | Transmitter Non-Inverted Data Input  |
| 34  | Tx3n     | Transmitter Inverted Data Input      |
| 35  | GND      | Ground                               |
| 36  | Tx1p     | Transmitter Non-Inverted Data Input  |
| 37  | Tx1n     | Transmitter Inverted Data Input      |
| 38  | GND      | Ground                               |
| 39  | GND      | Ground                               |
| 40  | Tx6n     | Transmitter Inverted Data Input      |
| 41  | Tx6p     | Transmitter Non-Inverted Data Input  |
| 42  | GND      | Ground                               |
| 43  | Tx8n     | Transmitter Inverted Data Input      |
| 44  | Tx8p     | Transmitter Non-Inverted Data Input  |
| 45  | GND      | Ground                               |
| 46  | Reserved | For future use                       |
| 47  | VS1      | Module Vendor Specific 1             |
| 48  | VccRx1   | 3.3V Power Supply                    |
| 49  | VS2      | Module Vendor Specific 2             |
| 50  | VS3      | Module Vendor Specific 3             |
| 51  | GND      | Ground                               |
| 52  | Rx7p     | Receiver Non-Inverted Data Output    |
| 53  | Rx7n     | Receiver Inverted Data Output        |
| 54  | GND      | Ground                               |
| 55  | Rx5p     | Receiver Non-Inverted Data Output    |
| 56  | Rx5n     | Receiver Inverted Data Output        |
| 57  | GND      | Ground                               |
| 58  | GND      | Ground                               |
| 59  | Rx6n     | Receiver Inverted Data Output        |
| 60  | Rx6p     | Receiver Non-Inverted Data Output    |
| 61  | GND      | Ground                               |
| 62  | Rx8n     | Receiver Inverted Data Output        |
| 63  | Rx8p     | Receiver Non-Inverted Data Output    |
| 64  | GND      | Ground                               |
| 65  | NC       | No Connect                           |
| 66  | Reserved | For future use                       |
| 67  | VccTx1   | 3.3V Power Supply                    |
| 68  | Vcc2     | 3.3V Power Supply                    |
| 69  | Reserved | For Future Use                       |
| 70  | GND      | Ground                               |
| 71  | Tx7p     | Transmitter Non-Inverted Data Input  |
| 72  | Tx7n     | Transmitter Inverted Data Input      |
| 73  | GND      | Ground                               |
| 74  | Tx5p     | Transmitter Non-Inverted Data Input  |
| 75  | Tx5n     | Transmitter Inverted Data Input      |
| 76  | GND      | Ground                               |

Control Signals
| Name    | Function             | Description                                                                                                                                                                                                 |
|---------|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ModPrsL | Output, asserted low | Pull-up by host when no transceiver/cable is present. Connected to ground inside the transceiver. Hence, asserted low when a transceiver/cable is plugged in.                                               |
| ModSelL | Input, asserted Low  | Module Select input pin, terminated high in the module. Only when held low by the host, the module responds to 2-wire serial communication commands. Enables multiple modules to share a single 2-wire bus. |
| ResetL  | Input, asserted Low  | Reset input pin, pulled high in the module. A low level on the ResetL pin for longer than the minimum length initiates a module reset. When de-asserted the transceiver starts initialization.              |
| LPMode  | Input, asserted high | Low Power Mode input, pulled up inside the module. Hardware control signal for forcing the transceiver into low-power state. Can be overwritten by low-power mode command.                                  |
| ePPS    | Input                | Not implemented                                                                                                                                                                                             |
| IntL    | Output, asserted low | Interrupt Low is an open-collector output, terminated high in the host system. A “Low” indicates a possible module operational fault or a status critical to the host system, e.g. temperature alarm.       |
