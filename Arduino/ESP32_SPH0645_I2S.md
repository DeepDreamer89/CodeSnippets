To send the recordings of the I2s microphone SPH0645 to another system you can use a example from the arduino-audio-tools:
Github repo: pschatzmann/arduino-audio-tools/examples/examples-webserver/streams-i2s-webserver_wav/streams-i2s-webserver_wav.ino
All you have todo is replace channels from 2 to 1 and bits_per_sample from 16 to 32 in the i2s config (line 27 & 28 in the version from 21.12.2022).
The pins are connected as follow:

common name | name on ESP32 | Name on SPH0645
bck    = GPIO14 = BCLK 
ws     = GPIO15 = LRCL
data   = GPIO32 = DOUT
ground = GND    = GND
3v     = 3v3    = 3V

Per default the webserver listens on port 80 so you can connect to it with e.g. VLC:
http://X.X.X.X/