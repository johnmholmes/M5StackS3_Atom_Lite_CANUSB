# AtomS3 Lite OpenLCB / GridConnect Bridge

> **Disclaimer**  
> This project is provided for **educational and reference purposes only**.  
> It is not intended for commercial use, safety-critical systems, or production environments.  
> Use at your own risk. The author accepts no liability for any damage, data loss, or issues arising from the use of this software or hardware configuration.

Bidirectional bridge between OpenLCB/LCC (CAN @ 125 kbit/s) and JMRI GridConnect protocol for the **M5Stack AtomS3 Lite**.

## This is a tool to allow you to test Can nodes on a work bench only. It may not be able to cope with to many nodes starting up all at once. I created this to allow me to test nodes when away from my layout. But have shared it to assist others who are trying to get into OpenLCB.

## Hardware Options

### 1. Grove Port (Unit Mini CAN)
| Signal  | GPIO |
|---------|------|
| CAN TX  | 2    |
| CAN RX  | 1    |
| RGB LED | 35   |

### 2. Atomic Port ABC / toUnit Base
| Signal  | GPIO |
|---------|------|
| CAN TX  | 5    |
| CAN RX  | 6    |
| RGB LED | 35   |

> Alternative pairs on the base: `7/8` or `38/39`

## LED Status
- **White** – Boot
- **Green** – CAN ready / Transmit
- **Blue**  – Receive
- **Red**   – CAN initialisation failed

## Usage

1. Select board: **M5Stack-AtomS3**
2. Install **FastLED** library
3. In the sketch, uncomment the pin set that matches your hardware (Grove or Base)
4. Upload
5. In JMRI set connection type to **GridConnect** (baud rate is largely ignored because of native USB)

**Note:** After closing JMRI you may need to press the reset button on the AtomS3 Lite before reconnecting.

