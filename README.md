# STM32F0 NRF24L01 Library

## Usage
### Receiver
`c
// SPI_HandleTypeDef hspi1
NRF24L01_SPI_Init(&hspi1); 
// Wait for NRF24 connections
while(NRF24L01_Check()){
  // Unconnected
  ...
}
// Enter receive mode
NRF24L01_RX_Mode();
// Infinite loop
while(1){
  HAL_Delay(10);
  uint8_t buf[32];
  // Receive data
  NRF24L01_RxPacket(buf)
  ...
}
`
### Transmitter
