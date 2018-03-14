###### set (OR)
    
    uint8_t set_bit = 3;
    uint8_t test_register = 0x00;
    
    test_register |= 0x01U << set_bit;

###### Clear (AND with NOT mask)
    uint8_t clear_bit = 3;
    uint8_t test_register = 0xFF;
    
    test_register &= ~(0x01U << clear_bit);

###### toggling (XOR)
    
    uint8_t toggle_bit = 3;
    uint8_t test_register = 0xFF;
    
    test_register ^= 0x01U << toggle_bit;

###### inspect (R-shift then AND with 0x01)
    uint8_t inspect_bit = 3;
    uint8_t test_register = 0xFF;
    
    uint8_t bit_status = (test_register >> inspect_bit) & 0x01U;

###### extra

[http://graphics.stanford.edu/~seander/bithacks.html](http://graphics.stanford.edu/~seander/bithacks.html)