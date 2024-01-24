# IO-Data ICCRW2 Driver for WebUSB
## What is this?
IO-Data ICCRW2 (NFC card reader) Driver for WebUSB written in TypeScript.  
Forked from [Aruneko/WebUSB-RC-S380](https://github.com/aruneko/WebUSB-RC-S380)  
On thw Way!!


## How to install

<!--via npm  
```bash
$ npm i rc_s380_driver
# or
$ yarn add rc_s380_driver
```  
-->
via source code  
```
```


## How to use

```TypeScript
import { RCS380, ReceivedPacket } from 'iodicc2_driver'

class Sample {
    constructor(readonly rcs380: RCS380) {}

    public static async connect(): Promise<TypeFTag> {
        const device = await RCS380.connect()
        return new Sample(device)
    }

    public async sendCommand(): Promise<ReceivedPacket> {
        const command = Uint8Array.of(0x00, 0xff, 0xff, 0x01, 0x00)
        return this.rcs380.inCommRf(command, 0.01)
    }
}
```

## npm package
<!--[rc-s380-driver](https://www.npmjs.com/package/rc_s380_driver)-->

## License
MIT
