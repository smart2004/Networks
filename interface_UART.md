##### Universal Asinchronous Reciever-Transmitter (UART) uses for connection arrangement between digital devices

>>> RS-232 - UART:
<= RS-232 [-12V/+12V] => [MAX232] <= UART [+3.3V/0V] => MK

>>> USB - UART:
<= USB => [FL232RL] <= UART [+3.3V/0V] => [MK]

NOTE: +3.3V converts to -12V, 0V converts to +12V

NOTE: USART STM32F10X supports IrDA, smartcard ISO7816-3, onewire semiduplex mode, DMA support

>> USARTx_SR - Status Register (Flags Register)
>> USARTx_DR - Data Register
>> USARTx_CR1..3 - Configuration Register
>> USARTx_GTPR - irDA, Smartcard, module frequency pre-divider modes adjustment

