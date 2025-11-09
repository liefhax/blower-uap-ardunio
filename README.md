HOT AIR GUN — Arduino + TRIAC
Hot-air gun / blower uap DIY berbasis Arduino yang mengendalikan elemen pemanas lewat TRIAC (isolasi menggunakan optotriac). Cocok untuk solder heat-shrink, desoldering, dan berbagai kebutuhan udara panas yang butuh kontrol.
Baca semua bagian sebelum merakit / menyalakan — proyek ini berhubungan langsung dengan mains AC.

Ringkasan fitur
Kontrol suhu dengan setpoint (rotary encoder + LCD).
Driver TRIAC (BTA41) untuk mengendalikan elemen pemanas, di-drive via optotriac (MOC3021) untuk isolasi.
Kontrol kipas DC menggunakan MOSFET (PWM).
Indikator bunyi (buzzer) dan menu sederhana.
Proteksi dan wiring yang disarankan (fuse, snubber, isolasi).

Skematik & wiring (intinya)
Mains AC → Elemen pemanas dikendalikan oleh TRIAC (BTA41).
Gate TRIAC dikendalikan oleh MOC3021 (optotriac) untuk isolasi antara MCU dan mains.
MCP302 di-drive oleh output Arduino melalui resistor pembatas.
Kipas DC dikontrol oleh MOSFET (gate dari Arduino PWM).
Sensor suhu ke Arduino melalui rangkaian pengkondisi (op-amp / divider).
LCD + rotary encoder untuk UI.
Selalu gunakan fuse pada jalur mains dan snubber RC pada TRIAC jika diperlukan.
Catatan: jangan pernah hubungkan Arduino langsung ke mains tanpa isolasi (optotriac, trafo, atau rangkaian proteksi). Pastikan pengkabelan aman dan housing tahan panas.

