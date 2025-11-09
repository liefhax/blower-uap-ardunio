**HOT AIR GUN — Arduino + TRIAC**

  Hot-air gun / blower uap DIY berbasis Arduino yang mengendalikan elemen pemanas lewat TRIAC (isolasi menggunakan optotriac). Cocok untuk solder heat-shrink, desoldering, dan berbagai kebutuhan udara panas yang butuh kontrol.
  Baca semua bagian sebelum merakit / menyalakan — proyek ini berhubungan langsung dengan mains AC.

**Ringkasan fitur**
Kontrol suhu dengan setpoint (rotary encoder + LCD).
Driver TRIAC (BTA41) untuk mengendalikan elemen pemanas, di-drive via optotriac (MOC3021) untuk isolasi.
Kontrol kipas DC menggunakan MOSFET (PWM).
Indikator bunyi (buzzer) dan menu sederhana.
Proteksi dan wiring yang disarankan (fuse, snubber, isolasi).

**Skematik & wiring (intinya)**
  Mains AC → Elemen pemanas dikendalikan oleh TRIAC (BTA41).
  Gate TRIAC dikendalikan oleh MOC3021 (optotriac) untuk isolasi antara MCU dan mains.
  MCP302 di-drive oleh output Arduino melalui resistor pembatas.
  Kipas DC dikontrol oleh MOSFET (gate dari Arduino PWM).
  Sensor suhu ke Arduino melalui rangkaian pengkondisi (op-amp / divider).
  LCD + rotary encoder untuk UI.
  Selalu gunakan fuse pada jalur mains dan snubber RC pada TRIAC jika diperlukan.
  Catatan: jangan pernah hubungkan Arduino langsung ke mains tanpa isolasi (optotriac, trafo, atau rangkaian proteksi). Pastikan pengkabelan aman dan housing tahan panas.

  
**TUNE & CALIBRATE** --
First, go to the setup mode and select the Tune option.In the tune mode the internal temperature (0-1023) is displayed on the screen. Rotate the encoder to manually select the applied power to the hot air gun. Heat the gun to 500 degrees. Then tune the trim-pot to set the temperature about 900 (in the internal units). Long press to the encoder return to the menu

Then, go to the setup mode select Calibrate option. 
First, you should select one of the 3 calibration temperature (200, 300, 400) and press the encoder lightly to start calibration process. This procedure is iterative: you start with the some preset temperature value in internal units the controller heats the Hot Air Gun to this preset temperature and gets ready (beeps and question mark will be desipplyed). Then you measure the real temperature by the external thermo-couple. If the real temperature is not equal to the preset one, you should increase or decrease the internal preset temperature by rotating the encoder handle.

The controller keeps the temperature near the preset value all the time. To increment the preset temperature, turn the encoder right, to decrease - turn it left.

After all three reference temperature points will be calibrated, long press the encoder and come to main screen

That's all! now you are ready to go!



