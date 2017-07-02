# Easy install FreePBX on VPS with Cent OS

[![Video Manual](https://i1.ytimg.com/vi/A6mxdvIMLEc/hqdefault.jpg)](https://www.youtube.com/watch?v=A6mxdvIMLEc "Video Manual")

Original Post: http://www.cameronbackus.com/2016/04/09/easy-install-freepbx-on-digital-ocean.html

## Pre-requsites

* SELinux is disabled (it is in DigitalOcean by default)
* A CentOS 7 droplet (of any size)

## Lets get started

* First we need to clone/get the script found in github repo
`wget https://raw.githubusercontent.com/lgg/easy-freepbx-install/master/install_freepbx.sh`
* Next, run the script
`sh install_freepbx.sh`
* The Script will run for a bit, afterwards, choose your options for MariaDB - **DO NOT USE A ROOT PASSWORD**.
* The Script will run for a bit more, you then will be able to choose if you would like any more Asterisk modules to be installed.

The script will then finish and you can browse to the FreePBX WebGUI using the droplet IP address.

## Troubleshooting

* MODULENAME tampered
If you get such errors in FreePBX web interface:
```
MODULENAME tampered
MODULENAME/file is wrong
```
run `fwconsole ma upgrade MODULENAME`
also try
`fwconsole a ma refreshsignatures`

## Credits

* Original script belongs to [Cameron](https://github.com/cameronbackus/)
