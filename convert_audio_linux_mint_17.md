title: Convert audio in Linux Mint 17
tags:
- Linux
- Mint
- ffmpeg
- audio
----
# Install ffmpeg
add ppa

    sudo apt-add-repository ppa:mc3man/trusty-media
install ffmpeg

    sudo apt-get update
    sudo apt-get install ffmpeg

# Convert to mp3
    ffmpeg -i input.ape -b:a 320k output.mp3
`-b:a 320k` means bitrate is 320k

# convert all ape to mp3 :
    for x in *.ape; do ffmpeg -i $x -b:a 320k ${x%.ape}.mp3; done
