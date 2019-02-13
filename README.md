# WiringPi

WiringPi is an implementation of most of the Arduino Wiring functions for the Raspberry Pi, this gem is a wrapper for the main wiringpi library and provides a nice OO interface with a few other handy helpers.

## Installation
```
git clone https://github.com/vimutter/WiringPi-Ruby
cd WiringPi-Ruby/ext/wiringpi
rm -fr WiringPi
git clone git://git.drogon.net/wiringPi
mv wiringPi WiringPi

cd ../..
gem build wiringpi.gemspec
gem install wiringpi-2.32.0.gem
```

## Example
```
#!/usr/bin/env ruby
gem 'wiringpi'
require 'wiringpi'

io = WiringPi::GPIO.new do |gpio|
  gpio.pin_mode(0, WiringPi::OUTPUT)
end

io.digital_write(0, WiringPi::HIGH) # Turn pin 0 on
io.delay(100)                       # Wait
io.digital_write(0, WiringPi::LOW)  # Turn pin 0 off
```

## Reference

### Pins
For a complete run-down see the [pins page](http://wiringpi.com/pins/) of the [wiringpi website](http://wiringpi.com/).
![alt text](http://wiringpi.com/wp-content/uploads/2013/03/gpio1.png "The main GPIO connector")
![alt text](http://wiringpi.com/wp-content/uploads/2013/03/gpio21.png "The secondary GPIO connector")

### More
Full details on the [wiringpi website](http://wiringpi.com/).
