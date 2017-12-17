
shellinabox
===========

This is an unofficial fork of the project **Shell In A Box**. The fork was created because
the original project was not maintained anymore and we cannot contact the original
repository owners.

About shellinabox-Hangul
-----------------

Shellinabox-Hangul is forked version of [Shellinabox](https://github.com/shellinabox/shellinabox) to fix Hangul typing bug.
This version solve Hangul bug typed like "ㅌ테텟테스슽스트".

Shell In A Box implements a web server that can export arbitrary command line
tools to a web based terminal emulator. This emulator is accessible to any
JavaScript and CSS enabled web browser and does not require any additional
browser plugins.

![Shell In A Box preview](/misc/preview.gif?raw=true)

More information:

* [Manual page](https://github.com/shellinabox/shellinabox/wiki/shellinaboxd_man)
* [Official site](https://code.google.com/p/shellinabox)
* [Official wiki](https://code.google.com/p/shellinabox/wiki/shellinaboxd_man)


Build
-----------------

For building **shellinabox** from source on Debian or RHEL based systems use commands
listed below. This will create executable file `shellinaboxd` in project directory.

1. Install dependencies

   ```
    apt-get install git libssl-dev libpam0g-dev zlib1g-dev dh-autoreconf
   ```
   
   or
   
   ```
   yum install git openssl-devel pam-devel zlib-devel autoconf automake libtool
   ```

2. Clone source files and move to project directory

   ```
    git clone https://github.com/mango-tree/shellinabox.git && cd shellinabox
   ```

3. Run autotools in project directory

   ```
    autoreconf -i
   ```

4. Run configure and make in project directory

   ```
    ./configure && make
   ```

Known Issues
------------

* The openssl package is required for HTTP/SSL support.
  Shell-in-a-box may be used without SSL such that the login session
  is not encrypted.  To enable automatic creation of self-signed
  certificates or to use a generated certificate, install openssl.

* On Debian Jessie, the default openssl package does not include the
  utilities necessary for Shell-in-a-box to generate self-signed
  certificates.  Upgrade openssl to install a version of the tools
  that support certificate creation.

