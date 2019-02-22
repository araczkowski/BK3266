# BK3266


### Image of the BK3266 dev board

![Image 1](img/dev_1.png?raw=true "Dev1")

![Image 2](img/dev_2.png?raw=true "Dev2")


### Datasheet

![BK3266 Datasheet](doc/BK3266 Datasheet.pdf?raw=true "BK3266 Datasheet")


### BK3266 Control instruction list

<table>
  <tr>
   <td>+SNAME+
   </td>
   <td>Example: COM+SNAME+BTBLUE\r\n
<p>
"\r\n stands for carriage return and line feed, input in the debugging assistant (Enter key)"
<p>
BTBLUE is the modified name
   </td>
   <td>Modify the Bluetooth name
   </td>
   <td>COM+SNAME+XXXX\r\n
<p>
XXXX: Up to 16 characters
<p>
Correct: OK\n
<p>
Error: ERR\n
<p>
Effective after power off and restart
   </td>
  </tr>
  <tr>
   <td>+SPIN+
   </td>
   <td>Example: COM+SPIN+12345678\r\n
<p>
"\r\n stands for carriage return and line feed, input in the debugging assistant (Enter key)"
<p>
12345678 is the modified password
   </td>
   <td>Edit Bluetooth pairing password
<p>
(feature optional)
   </td>
   <td>COM+SPIN+XXXX\r\n
<p>
XXXX: Maximum 16 characters
<p>
Correct: OK\n
<p>
Error: ERR\
   </td>
  </tr>
  <tr>
   <td>TONExx
   </td>
   <td>Xx: "ON" turns on the tone
<p>
Xx: "OFF" turns off the tone
<p>
Support power-down save
<p>
Default tone
   </td>
   <td>Tone setting
   </td>
   <td>COM+TONEON\r\n
<p>
Turn on the tone
<p>
COM+TONEOFF\r\n
<p>
Turn off the tone
<p>
Effective immediately
   </td>
  </tr>
  <tr>
   <td>MTONE
   </td>
   <td>
   </td>
   <td>Query tone settings
   </td>
   <td>COM+MTONE\r\n
<p>
Open: TOMEON\n
<p>
Close: TOMEOFF\n
   </td>
  </tr>
  <tr>
   <td>GOBACKxx
   </td>
   <td>Xx: "ON" opens back
<p>
Xx: "OFF" closes back
<p>
Support power-down save
<p>
Power on by default
<p>
Power-on
   </td>
   <td>connection settings
   </td>
   <td>COM+GOBACKON\r\n
<p>
Turn on the power back
<p>
COM+GOBACKOFF\r\n
<p>
Turn off the power back
<p>
Effective immediately
   </td>
  </tr>
  <tr>
   <td>MGOBACK
   </td>
   <td>
   </td>
   <td>Query back connection settings
   </td>
   <td>COM+MGOBACK\r\n
<p>
Open: GOBACKON\n
<p>
Close: GOBACKOFF\n
   </td>
  </tr>
  <tr>
   <td>CALLxx
   </td>
   <td>Xx: "ON" to open the call function
<p>
Xx: "OFF" to turn off the call function
<p>
Support power-down save
<p>
Call on by default
   </td>
   <td>Call function settings
   </td>
   <td>COM+CALLON\r\n
<p>
Turn on the call
<p>
COM+GOBACKOFF\r\n
<p>
Turn off call
<p>
Power off restart takes effect
   </td>
  </tr>
  <tr>
   <td>MCALL
   </td>
   <td>
   </td>
   <td>Query call settings
   </td>
   <td>COM+MCALL\r\n
<p>
Open: CALLON\n
<p>
Close: CALLOFF\n
   </td>
  </tr>
  <tr>
   <td>MP3AUTOPLYxx
   </td>
   <td>U disk / TF mode:
<p>
Xx: "ON" turns on auto play
<p>
Xx: "OFF" turns off automatic playback
<p>
Support power-down save
<p>
Autoplay is enabled by default
   </td>
   <td>Auto play settings
   </td>
   <td>COM+MP3AUTOPLYON\r\n
<p>
Turn on autoplay
<p>
COM+MP3AUTOPLYOFF\r\n
<p>
Turn off autoplay
<p>
Effective immediately
   </td>
  </tr>
  <tr>
   <td>MP3AUTOPLY
   </td>
   <td>
   </td>
   <td>Query autoplay
<p>
Setting
   </td>
   <td>COM+MP3AUTOPLY\r\n
<p>
Open: MP3AUTOPLYON\n
<p>
Close: MP3AUTOPLYOFF\n
   </td>
  </tr>
  <tr>
   <td>MEQ
   </td>
   <td>
   </td>
   <td>Query EQ
   </td>
   <td>NORMAL\n
<p>
BOOST\n
<p>
TREBLE\n
<p>
POP\n
<p>
ROCK\n
<p>
CLASSIC\n
<p>
JAZZ\n
<p>
DANCE\n
<p>
R&P\n
   </td>
  </tr>
  <tr>
   <td>SETEQxx
   </td>
   <td>Xx:NORMAL
<p>
BOOST\
<p>
TREBLE
<p>
POP
<p>
ROCK
<p>
CLASSIC
<p>
JAZZ
<p>
DANCE
<p>
R&P
<p>
Support power-down save
<p>
Default "NORMAL"
   </td>
   <td>EQ settings
   </td>
   <td>COM+SETEQNORMAL\r\n
<p>
Correct: OK\n
<p>
Error: ERR\n
<p>
Effective immediately
   </td>
  </tr>
  <tr>
   <td>OT
   </td>
   <td>Example:
<p>
0015: A total of 15 songs
<p>
0001: The first song is currently played.
<p>
0328: Play time 3 minutes 28 seconds
   </td>
   <td>Open print song information
   </td>
   <td>COM+GN\r\n
<p>
Correct: MUSIC: 001500010328\n
<p>
Error: ERR\n
   </td>
  </tr>
  <tr>
   <td>CT
   </td>
   <td>Turn off song information by default
   </td>
   <td>Turn off song information
   </td>
   <td>COM+CT\r\n
<p>
Correct: OK\n
<p>
Error: ERR\n
   </td>
  </tr>
  <tr>
   <td>GN
   </td>
   <td>Xxxxxxxx: song name, up to 8 characters, when using more than 8 characters, replace with "~1"
   </td>
   <td>Get the current song play name
   </td>
   <td>COM+GN\r\n
<p>
Correct: xxxxxxxx\n
<p>
Error: ERR\n
   </td>
  </tr>
  <tr>
   <td>PR
   </td>
   <td>
   </td>
   <td>Enter pairing
   </td>
   <td>BT+PR\r\n
   </td>
  </tr>
  <tr>
   <td>AC
   </td>
   <td>
   </td>
   <td>Connect the last paired device
   </td>
   <td>BT+AC\r\n
   </td>
  </tr>
  <tr>
   <td>DC
   </td>
   <td>
   </td>
   <td>Disconnect
   </td>
   <td>BT+DC\r\n
   </td>
  </tr>
  <tr>
   <td>CA
   </td>
   <td>
   </td>
   <td>Answer the call
   </td>
   <td>BT+CA\r\n
   </td>
  </tr>
  <tr>
   <td>CJ
   </td>
   <td>
   </td>
   <td>Refuse to call
   </td>
   <td>BT+CJ\r\n
   </td>
  </tr>
  <tr>
   <td>CE
   </td>
   <td>
   </td>
   <td>Hang up the phone
   </td>
   <td>BT+CE\r\n
   </td>
  </tr>
  <tr>
   <td>CR
   </td>
   <td>
   </td>
   <td>Redial last number
   </td>
   <td>BT+CR\r\n
   </td>
  </tr>
  <tr>
   <td>PP
   </td>
   <td>
   </td>
   <td>Music play/pause
   </td>
   <td>COM+PP\r\n
   </td>
  </tr>
  <tr>
   <td>PA
   </td>
   <td>
   </td>
   <td>play music
   </td>
   <td>COM+PA\r\n
   </td>
  </tr>
  <tr>
   <td>PU
   </td>
   <td>
   </td>
   <td>Music pause
   </td>
   <td>COM+PU\r\n
   </td>
  </tr>
  <tr>
   <td>PN
   </td>
   <td>
   </td>
   <td>next track
   </td>
   <td>COM+PN\r\n
   </td>
  </tr>
  <tr>
   <td>PV
   </td>
   <td>
   </td>
   <td>previous piece
   </td>
   <td>COM+PV\r\n
   </td>
  </tr>
  <tr>
   <td>VP
   </td>
   <td>
   </td>
   <td>Volume plus
   </td>
   <td>COM+VP\r\n
   </td>
  </tr>
  <tr>
   <td>VD
   </td>
   <td>
   </td>
   <td>Volume reduction
   </td>
   <td>COM+VD\r\n
   </td>
  </tr>
  <tr>
   <td>SETTSxx
   </td>
   <td>Xx: (00-16)
<p>
Serial port settings
<p>
Support power-down save
   </td>
   <td>Set the tone volume
   </td>
   <td>COM+SETTSxx\r\n
<p>
Correct: OK\n
<p>
Error: ERR\n
   </td>
  </tr>
  <tr>
   <td>MTS
   </td>
   <td>x:(0-16)
   </td>
   <td>Query current prompt tone volume
   </td>
   <td>COM+MTS\r\n
<p>
Correct: TSx\n
<p>
Error: ERR\n
   </td>
  </tr>
  <tr>
   <td>Vxx
   </td>
   <td>Xx: (00-16)
<p>
Button, serial port
   </td>
   <td>settings
<p>
Support power-down save
<p>
Set the volume
   </td>
   <td>COM+Vxx\r\n
<p>
Correct: COM_Vxx\n
<p>
Error: ERR\n
   </td>
  </tr>
  <tr>
   <td>GV
   </td>
   <td>Xx: (00-16)
   </td>
   <td>Query current volume
   </td>
   <td>COM+GV\r\n
<p>
Correct: COM_Vxx\n
<p>
Error: ERR\n
   </td>
  </tr>
  <tr>
   <td>PWDS
   </td>
   <td>
   </td>
   <td>Soft shutdown
   </td>
   <td>COM+PWDS\r\n
   </td>
  </tr>
  <tr>
   <td>PWOS
   </td>
   <td>
   </td>
   <td>Soft boot
   </td>
   <td>COM+PWOS\r\n
   </td>
  </tr>
  <tr>
   <td>REBOOT
   </td>
   <td>This restart is equivalent to a power failure restart
   </td>
   <td>Restart
   </td>
   <td>COM+REBOOT\r\n
   </td>
  </tr>
  <tr>
   <td>MC
   </td>
   <td>
   </td>
   <td>Switch to the next working mode
   </td>
   <td>COM+MC\r\n
   </td>
  </tr>
  <tr>
   <td>MBT
   </td>
   <td>
   </td>
   <td>Bluetooth mode
   </td>
   <td>COM+MBT\r\n
   </td>
  </tr>
  <tr>
   <td>MSD
   </td>
   <td>
   </td>
   <td>TF mode (if valid)
   </td>
   <td>COM+MSD\r\n
   </td>
  </tr>
  <tr>
   <td>MAX
   </td>
   <td>
   </td>
   <td>AUX mode (if valid)
   </td>
   <td>COM+MAX\r\n
   </td>
  </tr>
  <tr>
   <td>MUD
   </td>
   <td>
   </td>
   <td>U disk mode (if valid)
   </td>
   <td>COM+MUD\r\n
   </td>
  </tr>
  <tr>
   <td>IQ
   </td>
   <td>
   </td>
   <td>Query current mode and status
   </td>
   <td>COM+IQ\r\n
   </td>
  </tr>
  <tr>
   <td>SMA
   </td>
   <td>Default play mode SMA
   </td>
   <td>Loop all
<p>
(TF/U disk mode)
   </td>
   <td>COM+SMA\r\n
<p>
Correct: COM_SMA\n
<p>
Error: ERR\n
   </td>
  </tr>
  <tr>
   <td>SMO
   </td>
   <td>
   </td>
   <td>Single loop
<p>
(TF/U disk mode)
   </td>
   <td>COM+SMO\r\n
<p>
Correct: COM_SMO\n
<p>
Error: ERR\n
   </td>
  </tr>
  <tr>
   <td>SMNO
   </td>
   <td>
   </td>
   <td>Single does not loop
<p>
(TF/U disk mode)
   </td>
   <td>COM+SMNO\r\n
<p>
Correct: COM_SMNO\n
<p>
Error: ERR\n
   </td>
  </tr>
  <tr>
   <td>SMR
   </td>
   <td>
   </td>
   <td>Shuffle Playback
<p>
(TF/U disk mode)
   </td>
   <td>COM+SMR\r\n
<p>
Correct: COM_SMR\n
<p>
Error: ERR\n
   </td>
  </tr>
  <tr>
   <td>GSM
   </td>
   <td>
   </td>
   <td>Query current MP3
<p>
Play mode
<p>
(TF/U disk mode)
   </td>
   <td>COM+GSM\r\n
<p>
All loops: COM_SMA\n
<p>
Single loop: COM_SMO\n
<p>
Single does not loop: COM_SMNO\n
<p>
Random play: COM_SMR\n
   </td>
  </tr>
  <tr>
   <td>SMPxxxx
   </td>
   <td>Xxxx: (0001-9999)
<p>
("0001" stands for the first one)
   </td>
   <td>Selection song
<p>
(TF/U disk mode)
   </td>
   <td>COM+SMP0040\r\n
   </td>
  </tr>
  <tr>
   <td>MRMP3
   </td>
   <td>x:(1-9999)
   </td>
   <td>Query the currently playing
<p>
MP3 song serial number
<p>
(in TF mode)
   </td>
   <td>COM+MRMP3\r\n
<p>
Correct: music_mun=x\n
<p>
Error: ERR\n
   </td>
  </tr>
  <tr>
   <td>MMMP3
   </td>
   <td>x:(1-9999)
   </td>
   <td>Query current mode
<p>
Number of MP3 songs
<p>
(TF/U disk mode)
   </td>
   <td>COM+MMMP3\r\n
<p>
Correct: MMMPx\n
<p>
Error: ERR\n
   </td>
  </tr>
  <tr>
   <td>MRUSB
   </td>
   <td>x:(1-9999)
   </td>
   <td>Query the currently playing
<p>
U disk song serial number
<p>
(in U disk mode)
   </td>
   <td>COM+MRUSB\r\n
<p>
Correct: music_mun=x\n
<p>
Error: ERR\n
   </td>
  </tr>
</table>



<!-- Docs to Markdown version 1.0β15 -->
