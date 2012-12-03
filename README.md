A wicd network manager template for the eduroam network in Göttingen
====================================================================

Installation
------------

Copy the file `eduroam_goettingen` to your wicd templates folder.
The exact path might differ depending on which Linux distribution you're using.
On Arch Linux you would type:

    sudo cp eduroam_goettingen /etc/wicd/encryption/templates

Next, activate the new template by simply issuing the following command:

    sudo echo 'eduroam_goettingen' >> /etc/wicd/encryption/templates/active

That's it. You should now be able to select "eduroam_goettingen" from the
encryption type select box.



__Note:__ The template assumes that the following certificate is installed on
your system: `/usr/share/ca-certificates/mozilla/Deutsche_Telekom_Root_CA_2.crt`

You can verify the location of the certificate on your system with:

    locate .crt | grep -i telekom

If this certificate is located somewhere else on your system, either open
an issue here on github and I will make the certificate path editable or
edit the path manually yourself in the template.

Oh, and because we all like screenshots:

<img src="https://raw.github.com/epegzz/wicd_eduroam_goettingen/master/screenshot.png">
