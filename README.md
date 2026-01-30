# e7020e_project

# TOTP with automatic password input

## Members

- Gabriel Axheim Gustafsson (gabaxh-2@student.ltu.se)
- Patrik Wall (walpat-1@student.ltu.se)
- Simon Pergel (isoepe-1@student.ltu.se)


## High level specification
Our TOTP fob is designed to be able to automatically input the password calculated by behaving like a keyboard when you click the button once and it's connected to the USB, holding the button down will instead make it behave like a usb memory thus allowing a user to insert a new secret onto the device. When the password has been sent the display will show a "Success" message letting the user know that it's safe to remove the device. When the device is only powered by battery the device will show the one time password on the display instead, holding down the button will instead show the secret stored on the device.
- Button
  - Click, USB powered: calculate & act as keyboard (enters password automatically)
  - Click, battery powered: calculate password and show it on the display
  - Hold, USB powered: allow insertion of secrets
  - Hold, battery powered: display secret
- Display
  - If button was clicked show password (battery)
  - If button was clicked send password (usb)
    - Show successful message when password was "sent"
  - If button was held & connected to USB
    - Restart USB connection & act as a USB memory
    - Allow a user to store new secret

NOTE: This is still not set in stone, currently talking about it and might change
### Hardware Features
- 1x Real time clock (32kHz crystal)
- 1x Button
- 1x USB connector
- 1x Display
- 1x Battery connector (5V)

### Software Features
- Allow setting & getting time
- Set shared secret
- Encrypt secret
- Deep sleep (1mA during idle)

### Additional features
- Battery powered while not connected to USB
- Allowing the TOTP to switch between different behaviour
  - Might need to terminate USB connection for this to work
  - Acting as a keyboard
  - Acting as a USB memory
- *LED displaying remaining battery

Features starting with * might be included depending on difficulty and time required to complete said feature

## Grading
- Gabriel
  - Expected contributions towards grade 4?
  - Expected contributions towards grade 5?

- Simon
  - Expected contributions towards grade 4?
  - Expected contributions towards grade 5?
 
- Patrik
  - Expected contributions towards grade 4?
  - Expected contributions towards grade 5?


