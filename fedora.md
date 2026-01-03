# Fedora

## Change Fedora (43) kernel

>[!NOTE]
>Applies to other Fedora versions also

Print default kernel:

    sudo grubby --default-kernel

Change default kernel:

    # List kernel indices
    sudo grubby --info=ALL | grep -E "^kernel|^index"
    # Set the new index
    sudo grubby --set-default-index=1

## Release Upgrade

    sudo dnf system-upgrade download --releasever=43
