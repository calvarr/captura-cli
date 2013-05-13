captura-cli
===========

Utilitar pentru captura desktop, camera web si nu numai

Autori:

calvarr: https://github.com/calvarr
bionel: https://github.com/bionel

===========
Dependinte:
	dialog sau/si xdialog,gdialog,kdialog etc.
	ffmpeg sau avconv
	sed,awk,grep,curl
	scrot
	fbdev
	cvlc sau mplayer
	wmctrl
===========
Configurare fbdev (captura TTY):
chmod a+rw /dev/fb0

===========
Stream nesecurizat:
	- pentru a reda streamul webcam, desktop, tty (player http://localhost:9003/stream.mjpeg)
	- Pentru a difuza streamul webcam, desktop, tty in reteaua externa:
	testam daca este deschis portul 9003:
$ telnet IP_extern 9003
	tunelizam prin ssh:
ssh nume@IPextern -R 9003:127.0.0.1:9003
	redam:
player http://IPextern:9003/stream.mjpeg

