 * Install [Wlink](https://github.com/ch32-rs/wlink)
 * Install MRS toolchain make sure that ```riscv-none-embed-``` is in path
```bash
meson setup --cross-file cross.ini build
ninja -C build
```

NO connection:
 - UI 0x042c 0x0437
```
             0b10000110111
               |||||||||||
               ||||||||||└- RB_UIF_BUS_RST
               |||||||||└-- RB_UIF_TRANSFER
               ||||||||└--- RB_UIF_SUSPEND
               |||||||└---- RB_UIF_HST_SOF
               ||||||└----- RB_UIF_FIFO_OV
               |||||└------ RB_U_SIE_FREE
               ||||└------- RB_U_TOG_OK
               |||└-------- RB_U_IS_NAK
```
 - 

Connection:
 - UI 0x042c 0x0433
SystemClk:96000000
main
UI 0x042c 0x0433
        - 0b10000110011