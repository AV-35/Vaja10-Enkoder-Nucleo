# Enkoder z STM32G4 Nucleo-64in TIM časovnikom 

## Cilj Naloge
S  pomočjo  programskega  okolja STM32CubeIDEin  HAL  knjižnicami  terSTMStudio (ali STM32CubeIDE  v Debug pogledu) sprogramirajte  mikroprocesor  tako,  da boste merili premike  in  hitrost vrtenja enkoderja.

## Postopek inicializacije periferije
- **PA0** , **PA1**
- Premakne se za **2** inkramenta.


## Pinout
![PinOut](meida/Posnetek%20zaslona_20230131_120619.png)

## Komentar

V navodilih je napačno napisana koda, spodaj je popravljena.

```C
HAL_TIM_Encoder_Start_IT(htim2, TIM_CHANNEL_ALL);
void HAL_TIM_IC_CaptureCallback(TIM_HandleTypeDef *htim2) {}
stevec = __HAL_TIM_GET_COUNTER(htim2);
```
