# Raspivoice User Manual

See RaspiVoiceUserManual.pdf 
alternative use the following command:

>raspivoice --help
Usage : raspivoice [OPTION] [SENTENCE]

OPTION   - Serial port, for example 'raspivoice ttyAMA0' or 'raspivoice ttyUSB' etc
           If you specified a valid serial port, raspivoice will continiously run
           while it monitors the serial port.
           Default serial baudrate is 115200
           CTL-C to exit

SENTENCE - Whatever you want it to say. Example : 'raspivoice hello world'
           Use ^m to switch for male voice. Example : 'raspivoice female ^m male
           Use ^f to switch to female or ^e to switch to eSpeak.
           Use ^f to switch to female or ^e for eSpeak.
           Regular eSpeak options goes in { } braces.
                Example : 'raspivoice ^e{v en + f5}another female voice'
           Sound files are preceeded with ^s.  Example : 'raspivoice ^s trumpets'
           Save your own custom sound files in '/usr/local/raspi-wav/wav/sounds'

Piping -   Another way to call raspivoice is to pipe the output of another appliation
           into raspivoice
           Example 'echo hello world | xargs raspivoice'
