# htmlwrap

A simple shell script for wrapping files in html headers.

## Installation
    
    install -m 755 htmlwrap /usr/bin

## Usage

    htmlwrap [OPTION]... [FILE]...

Make html file from output of find command

    find . -type f -name '*.jpg' -printf '<li class="list">%P</li>\n' | sed '1s/^/<ul>/; $s/$/<\/ul>/' | htmlwrap -t 'list' -d 'list of jpg files' -C -i icon.ico -k 'list jpg' -s style.css -s main.css -S clock.js -S loop.js

Get some help

    htmlwrap -h
