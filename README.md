# LLC
#include <stdio.h>
#include <stdint.h>

// IEEE 802.2 LLC Header
struct llc_header {
    uint8_t dsap;     // Destination Service Access Point
    uint8_t ssap;     // Source Service Access Point
    uint8_t control;  // Control field
};

int main() {

    struct llc_header frame;

    frame.dsap = 0x06;    // hedef servis
    frame.ssap = 0x06;    // kaynak servis
    frame.control = 0x03; // Unnumbered Information frame

    printf("DSAP: 0x%X\n", frame.dsap);
    printf("SSAP: 0x%X\n", frame.ssap);
    printf("Control: 0x%X\n", frame.control);

    return 0;
}
