# ADS1231 library by aerowind

## About

An Arduino library to interface the [Texas Instruments ADS1231 24-Bit ADC], an
analog-to-digital converter for weight scales. The ADS1231 is a 24-Bit, 80SPS,
1-channel delta-sigma ADC for resistive bridge sensors & weight scales.

## Usage

```shell
git clone https://github.com/hiveeyes/aerowind-ads1231
cd aerowind-ads1231
make build
```

## Hardware support
- Atmel AVR
- Atmel SAM
- Espressif ESP8266

## Caveat

You probably do not want to use this library. Have a look at the
[ThomasRyanDavies/ADS1231] Arduino library by Thomas Ryan Davies and
[other libraries for the ADS1231] instead.

## Acknowledgements

This library has been sourced from the [Arduino Forum].

- Source: Arduino Forum [Topic "SPI Load cell chip ADS1231"], [ADS1231_beta.zip].
- Author: aerowind
- Date: Jan 31, 2014

Thank you!

## Appendix

### Fixes

For compatibility with ESP8266, those compile-time errors have been fixed.

- [error: 'SREG' was not declared in this scope](https://github.com/hiveeyes/aerowind-ads1231/issues/1)
- [error: cannot convert 'volatile uint32_t*' to 'volatile uint8_t*'](https://github.com/hiveeyes/aerowind-ads1231/issues/2)

### Considerations about real world effects caused by physics

You should consider getting into the details of strain-gauge load cell sensors when
expecting reasonable results from your measurements. The range of topics is broad,
starting with a sufficient and stable power supply, over using the proper excitation
voltage, to the Seebeck effect, and temperature compensation woes.

See also:
- [Overview about real world effects](https://community.hiveeyes.org/t/analog-vs-digital-signal-gain-amplifiers/380/6)
- [Thermoelectric effect](https://en.wikipedia.org/wiki/Thermoelectric_effect) (Seebeck effect)
- Temperature compensation: [Resource collection](https://community.hiveeyes.org/t/temperaturkompensation-fur-waage-hardware-firmware/115), [DIY research](https://community.hiveeyes.org/t/temperaturkompensation-fur-waage-notig-datensammlung/245)
- [Power management for HX711](https://community.hiveeyes.org/t/stromversorgung-hx711/893)


[ADS1231_beta.zip]: https://forum.arduino.cc/uploads/short-url/mNIEHZSUA7hV1eJFrO5Fqe7koIb.zip
[Arduino Forum]: https://forum.arduino.cc/
[other libraries for the ADS1231]: https://community.hiveeyes.org/t/code-fur-ads1231/286/3
[Texas Instruments ADS1231 24-Bit ADC]: https://community.hiveeyes.org/t/ads1231-24-bit-adc-from-texas-instruments/2141
[ThomasRyanDavies/ADS1231]: https://github.com/ThomasRyanDavies/ADS1231
[Topic "SPI Load cell chip ADS1231"]: https://forum.arduino.cc/t/spi-load-cell-chip-ads1231/128267/6
