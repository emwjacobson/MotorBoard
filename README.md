# MotorBoard

Goals for this project:

- Integreate ESP32
- Control up to 3 stepper motors
  - Shared pins:
    - MS1, MS2, MS3, Reset, Enable
  - Unique pins per stepper:
    - Sleep, Step, Dir
  - Total of 5 + 3(3) = 14 pins to control 3 steppers.
- Control up to 2 "hobby" servos
- 6 digital inputs
  - Limit switches, User IO (Buttons)

Decisions that need to be made:
- How will it be powered?
  - Barrel Jack? Screw Terminals?
  - Stepper motors will run off 8-35V, so 12V input should be good
- Stepper Connector
  - Leaning towards screw terminals, as they seem pretty universal
  - Could also use 4/6-pin JST connector
- Should step resolution be software controlled, or have jumpers on PCB?

Components:
- [Stepper Driver](https://www.lcsc.com/product-detail/Motor-Driver-ICs_Allegro-MicroSystems-LLC-A4988SETTR-T_C38437.html)
- [ESP32 Module](https://www.lcsc.com/product-detail/WiFi-Modules_Espressif-Systems-ESP32-WROVER-IE-8MB_C2934565.html)
  - The IE(8MB) seems to be the cheapest in the WROVER-IE series. The 4MB and 16MB variants are also supported, though seem slightly more expensive on LCSC
  - The WROVER-E series is also supported. The only difference between the two is the resistor connecting the antenna output either to the PCB antenna, or the external antenna. The -E model attaches to the PCB antenna, and the -IE model attaches to the external antenna.