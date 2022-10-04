# vaja3_ADC_pretvorba

1. Cilj naloge: S pomočjo programskega okolja STM32CubeIDE in HAL knjižnicami sprogramirajte mikroprocesor tako, da bo izvajal ADC pretvorbe sprožene s časovnimi prekinitvami (interrupt).

2. Postopek inicializacije periferije.  
  - Uporabljena razvojna plošča je **STM32F401C-DISCO**
  - Izbran pin je **PA1** na plošči je to **PA1**.  
  - Poleg pina se izpiše **ADC_IN1**
  - Ko spremenimo APB1 Timmer na 16 MHz se spremenijo tudi  APB1 peripheral clocks, APB2 peripheral clocks itd.
  - Če želimo frekvenco nastaviti na **1 kHz** moramo v polje Prescaler zapisati **16 000**.
  - Za spreminjanje stanje LED je uporabljena komanda **HAL_GPIO_TogglePin(GPIOD, GPIO_PIN_12);**








# Komentar
pri točki **e** je sampling time 28 saj opcije za 28,5 ni.