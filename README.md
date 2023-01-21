# AVR-RC5-protocol
a simple C library for Sending RC5 Commands for AVR +  an Example test.  
## Prequistices  
The main Micro Freq. must be 8 Mhz.  
Timer 0 reserved for counting, DONT change it.  
## API  
### Macros:  
ADDR_LEN --------------> destination address bit length.(default:5)    
DATA_LEN ---------------> Command bit length.(default:6)  
MODULATION_LEN -----> How many modulated pulses are in a Half cycle?(default:32)  
OUTPUT_PORT ----------> The output GPIO of transmitter.(default:PORTA.0)  
### Functions:  
**void send_command(bool bit_toggle, uint8_t addr, uint8_t data);**  
it will generate a complete RC5 command and transmit it to output.  
bit_toggle -------------> could be 0 or 1.  
addr -------------------> The destination address(0-2^ADDR_LEN -1).  
data -------------------> The command(0-2^DATA_LEN -1).  

