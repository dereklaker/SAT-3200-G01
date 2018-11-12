# Lab 1
## OS Drive
	Use RAID 1+0, no spare
	CTRL+S to open ROM configuration
## OS configuration
	Language: English
	Install RHEL to /dev/sda
	Hostname: 3200-g01
	Root: correct horse battery staple
	Use all space
	Install compact smart array as device for boot loader
	Mount USB
## OS Configuration II
	Red Hat Basic Install
	`system-config-network`
	Update system with `yum update -y`
	Installed zsh
	`wget -O .zshrc https://git.grml.org/f/grml-etc-core/etc/zsh/zshrc`
## Add user
	`useradd -m -s /bin/zsh -G wheel,tty,input, zorro`
	Pass: correct horse battery staple
	`visudo`
## Iron information
	HP Proliant DL385G5
## Misc information
	Serial #: 2ux841009w
	Port 14 for the switch
	Installed PowerPath via `rpm -ivh ./path/to/RPM`
