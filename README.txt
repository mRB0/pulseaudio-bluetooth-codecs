TL;DR: btaudio-select-codec

    Run it with no arguments and it will try to pick the best codec if
    you only have one Bluetooth audio device.


I use these scripts (mainly btaudio-select-best-codec) to switch to
the best codec supported by my bluetooth audio devices.

The devices come up using the sbc codec which is the worst audio
quality, but I can use eg sbc_xq_552 for higher audio quality. I have
to pick it manually.

These scripts require zsh and jq, and work with pulseaudio. I use them
with Ubuntu 22.04 LTS and PulseAudio 15.99.1.


btaudio-select-codec

    Switch to the selected or best codec supported by the specified
    card, or the card found by btaudio-find-bluez-card if not
    specified.

    Requires jq: https://jqlang.github.io/jq/

    Help: btaudio-select-codec -h


btaudio-list-codecs

    List audio codecs on the specified card, or the card found by
    btaudio-find-bluez-card if unspecified.

    Help: btaudio-list-codecs -h


btaudio-show-current-codec

    Show the current codec selected for the specified card, or the
    card found by btaudio-find-bluez-card if unspecified.

    Help: btaudio-show-current-codec -h


btaudio-find-bluez-card

    If only one bluez audio card is available, find it and list it to
    stdout.

    Otherwise exit with an error message.

    This script is required and used by the other scripts to find the
    card when it's not specified.


btaudio-list-bluez-cards

    List bluez cards. This is also used by other scripts.
