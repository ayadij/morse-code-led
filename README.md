# Morse Code
2016 BYU CS 224 Lab 5


### Description:
Write an MSP430 assembly program that outputs an alphanumeric message in Morse Code using an LED and a transducer (magnetic speaker). Use the watchdog as an interval timer whose interrupt service routine (ISR) pulse width modulates (PWM) the transducer device creating a tone. Use a .string assembler primitive to store the message. Use Switch #1 to toggle the tones on and off.

### Learned:
- Gained experience programming in assembly language.
- Learned how to use single-step and break points to debug assembly code.
- Written an interrupt service routine (ISR).
- Used indirect addressing modes of registers as pointers.
- Communicated with asynchronous routines using global variables.
- Debounced a mechanical switch.
- Demonstrated the use "callee-save" protocol when calling subroutines.
- Linked symbolic values together from different program files.


### Specs:
- 1 point	Your Morse Code Machine is written in MSP430 assembler and contains header comments that include your name and a declaration that the completed assignment is your own work.
- 2 points	A Watchdog Timer Interrupt Service Routine (ISR) creates Morse Code DOTs and DASHes using the development board speaker. The red LED (D6) is on and the speaker pulses with a square wave during a DOT and DASH. The red LED is off and the speaker is not pulsed during silent spacing elements. The Watchdog ISR also toggles the green LED (D5) on and off every second.
- 2 points	The International Morse Code standard is used to repeatedly output the string message "HELLO CS 124 WORLD " at a default rate of 5 words per minute ( 193 elements @5 WPM = approximately 46.32 seconds). Each DOT is one element, each DASH is three elements, intra-character spacing is one element, inter-character spacing is three elements, and inter-word spacing is seven elements.
- 2 points	The output message is stored in program memory using the .string assembler directive and accessed character by character using an indirect auto-increment assembly instruction. (Allowable characters include A-Z and 0-9.) The characters are translated to DOTs and DASHes using a table defined in an external assembly file.
- 2 points	Depressing Switch #1 (SW1) generates a Port 1 interrupt. The Watchdog ISR debounces Switch #1 which then turns (toggles) the speaker ON/OFF. (The red LED continues to blink out the Morse Code message.)
- 1 point	All program constants are defined using the .equ assembly directive. All subroutines use correct callee-save protocol. Only .bss section variables (not registers) are used to pass values between your main program and interrupt service routines (ie. ISRs are also callee-save subroutines).
 
https://students.cs.byu.edu/~clement/cs224/labs/L06a-morse/morse.php?BeforeYouBegin=1&Proceed=1
