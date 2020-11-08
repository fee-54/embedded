# embedded
/*
 * File:   main.c
 * Author: Hesham
 *
 * Created on Nov. 8, 2020, 8:48 AM
 */
#include <xc.h> 
#include "config.h" //including configeations bits.
#define _XTAL_FREQ 4000000 // Delay function
#include <pic16f877a.h>
void main(void) {
    TRISB0=0; // define port 0 as an output "LED".
    RB0=0;    // has initial value "low = Turn of the LED".
    TRISB1=1; // define port 1 as an input "Switch".
    while(RB1) // while switch is on :
    {
            RB0=1; // Turn on the LED 
           /* __delay_ms(100);
            RB0=0;
            __delay_ms(100);*/
    }
    return;
}
