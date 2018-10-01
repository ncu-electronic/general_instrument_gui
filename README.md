# GeneralInstrumentGUI
A general instrument GUI aiming for hardware manipulation.

Written in python3 and PyQt5.

## How to use:
### 1. Install dependencies:
[*pyqtgraph*](http://www.pyqtgraph.org/)

[*PyQt5*](https://pypi.python.org/pypi/PyQt5)

**Install with pip:**

`pip3 install PyQt5`, `pip3 install pyqtgraph`

**In addition**, on linux users should install ***qt5-serialport*** package for the obtain the qtserial.so shared library, this name is based on pacman package manager, it may be different on other linux distributions.

### 2. Run it:
`python3 main.py`

## Current data procotol:
Currently, data is transfering through serial port.

And at present I use one 8bit to represent a certain data number, so it'll be restrained in 0~255, there is temporarly no other thing.

**Demonstration:**

Send square waveform data by arduino, source code:
```
void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);

}

void loop() {
  // put your main code here, to run repeatedly:
  Serial.write(0x01);
  Serial.write(0x01);
  Serial.write(0x01);
  Serial.write(0x01);
  Serial.write(0x01);
  Serial.write(0x01);
  Serial.write(0x01);
  Serial.write(0x01);
  Serial.write(0x01);
  Serial.write(0x01);
  Serial.write(0x01);
  Serial.write(0xff);
  Serial.write(0xff);
  Serial.write(0xff);
  Serial.write(0xff);
  Serial.write(0xff);
  Serial.write(0xff);
  Serial.write(0xff);
  Serial.write(0xff);
  Serial.write(0xff);
  Serial.write(0xff);
  Serial.write(0xff);
}
```

## Documention:

There's some marks during developing:[*2018-01-04-marks-during-developing-oscilliscope-gui*](https://github.com/GeneralInstrumentGUI/General-Instrument-GUI/blob/master/doc/2018-01-04-marks-during-developing-oscilliscope-gui.md)