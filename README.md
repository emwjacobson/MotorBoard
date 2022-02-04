# MotorBoard

Goals for this project:

- Integreate either ESP32
- Control up to 3 stepper motors
- 6 digital inputs
  - Limit switches, User IO (Buttons)


Components:

- [Stepper Driver](https://www.lcsc.com/product-detail/Motor-Driver-ICs_Allegro-MicroSystems-LLC-A4988SETTR-T_C38437.html)
- [ESP32 Module](https://www.lcsc.com/product-detail/WiFi-Modules_Espressif-Systems-ESP32-WROVER-IE-8MB_C2934565.html)
  - This seems to be the cheapest in the WROVER-IE series. The 4MB and 16MB variants are also supported, though seem slightly more expensive on LCSC
  - The WROVER-E series is also supported. The only difference between the two is the resistor connecting the antenna output either to the PCB antenna, or the external antenna. The -E model attaches to the PCB antenna, and the -IE model attaches to the external antenna.