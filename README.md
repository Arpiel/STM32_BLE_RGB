# STM32_BLE_RGB
* STM32WB55 제품으로 구동되는 BLE 지원 RGB LED 등 프로젝트
* 타겟 보드: NUCLEO-WB55RG
* 개발 환경: CubeIDE 1.13

# 구현
* TIM1 채널 1/2/3이 각각 3색 LED의 각각의 색상에 연동됨. UUID는 FF02/FF03/FF04로 세팅됨
* TIM1채널은 PWM출력이 세팅되어 있으며 0~255의 값을 입력해 출력 밝기를 변경가능함.
* UUID FF05에 0/1 값을 전송하는 것으로 TIM1채널의 PWM출력이 가능함
* 내부 플래시메모리 영역에 RGB 설정값을 저장하고 있으며 전원 분리후 재부팅 시 해당 플래시메모리 영역을 읽어와 다시 작동함.

<p align="center">
  
![he](https://github.com/Arpiel/STM32_BLE_RGB/assets/41049703/8096a3fd-26f7-4280-8978-b5bbac6faf5c)

# 버전별 변경사항

## Version 1.1.1
오류수정(특정 기능 동작에 오류가 있던 점)

## Version 1.1
신규기능 추가(PWM ON/OFF제어, 마지막 기록값 불러오기)

## Version 1.0
초기기능 구현(PWM 제어 LED)
