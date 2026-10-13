# AVR-Assembler
A little BASH helper script to automate the process of assembling assembly code using avrdude in Linux

## Prerequisites
- The GNU Assembler utilities (`avr-as`, `avr-ld`, `avr-objcopy`)
- `avrdude`
- A supported microcontroller (tested using the Arduino Nano)

## Usage

1. Download the script from the Releases Page.
2. Open a terminal and change the working directory to the one containing the script
3. Run `chmod +x avr-assembler` to make the script executable
4. Run `./avr-assembler [name of assembly source code with extension]`
   e.g. `./avr-assembler clear_sreg.s`

## Optional - Put it in Shell PATH
This is mainly if you want to run the script without going into the script's working directory (so you can run `avr-assembler` instead of `./avr-assembler`)

1. In your file explorer, copy this file path `~/.local` and paste it in the box containing the directory path
2. Create a new folder called `bin` if it doesn't exist.
3. Move the `avr-assembler` script here.
4. In the terminal, type `nano ~/.bashrc`. Feel free to change this command if you use a different text editor or shell.
5. At the end of the file, paste this command `export PATH="$HOME/.local/bin:$PATH"`
6. Save and exit the file.
7. Reload bash by typing `source ~/.bashrc`.
8. To test, try assembling a program with `avr-assembler` instead of `./avr-assembler`.
