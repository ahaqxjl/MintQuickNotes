title: Split flac with cue in linux (Linux Mint 17)
tags:
- Linux
- Mint
- Ubuntu
- audio
- lossless
----
# Install tools
    sudo apt-get install cuetools shntool flac mp3info

# Split
    shntool split -t "%n.%p-%t" -f albumname.cue -o flac albumname.flac -d output
`%n` means track number, `%p` means artist, `%t` stands for track title. If `-d` is not provided, it output split files into current path

# Add tagging
    cuetag albumname.cue *.flac

# Convert
[Convert audio in Linux Mint 17](/2016/01/14/convert_audio_linux_mint_17/)