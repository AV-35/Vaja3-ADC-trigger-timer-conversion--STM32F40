# vaja3_ADC_pretvorba

1. Cilj naloge: S pomočjo programskega okolja STM32CubeIDE in HAL knjižnicami sprogramirajte mikroprocesor tako, da bo izvajal ADC pretvorbe sprožene s časovnimi prekinitvami (interrupt).

2. Postopek inicializacije periferije.  
  - Uporabljena razvojna plošča je **STM32F401C-DISCO**
  - Izbran pin je **PA1** na plošči je to tudi **PA1**.  
  - Poleg pina se izpiše **ADC_IN1**
  - Ko spremenimo APB1 Timmer na 16 MHz se spremenijo tudi  APB1 peripheral clocks, APB2 peripheral clocks itd.
  - Če želimo frekvenco nastaviti na **1 kHz** moramo v polje Prescaler zapisati **16 000**.
  - Za spreminjanje stanje LED je uporabljena komanda **HAL_GPIO_TogglePin(GPIOD, GPIO_PIN_12);**

## Pinout

![Pinout](media/Posnetek%20zaslona%202022-10-07%20102403.png)








## Komentar
Pri točki **e** je sampling time 28 saj opcije za 28,5 ni.  

Namesto **TIM 1** moramao izbrati **TIM 2** saj **TIM 1** nima opcije **Timer trigger out event** (Pri External Trigger Conversion Source pod ADC1) medtem, ko **TIM 2** jo ima.

Koda ne dela na STM32F401C-DISCO.Deluje pa na Nucleo razvojni plošči. Video posnetek za Nucle se nahaj pod mapo Nucleo/media