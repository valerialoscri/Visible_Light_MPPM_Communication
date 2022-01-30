This code properly works using LFTX and LFRX daughterboards in transmitting and receiving USRP.
Connect the transmitting TX USRP to the optical transmitter, properly including a bias tee and eventually an amplifier for allowing the signal to correctly feed the LED.
Connect the receiving RX USRP to the optical receiver, properly including a transimpedance amplifier and eventually, a conditioning circuit in order to avoid receiver saturation.
Set the same communication parameters (sample rate, order of modulation, synchronization frame length etc.) in transmitting and receiving device ( MAIN_RX.vi and MAIN_TX.vi) files. Set the picture format (size, color flag, pulse duration, etc.) too.
Run continuously MAIN_RX.vi
Load the picture to transmit in the input path of MAIN_TX.vi 
Run MAIN_TX.vi
Received picture appears in the dedicated area of MAIN_RX.vi after the loading bar is fully charged. Quality of the picture depends on distance between transmitter and receiver and by external noise. In case of extremely poor Signal to Noise Ratio condition, synchronization and, consequently, image transfer could fail. If it happens, try to increase the order of PPM modulation and pulse duration.  Transferring rate depends on sample rate (set a maximum value of 2Msample/s) and the order of modulation (the higher the order, the slower the communication).
