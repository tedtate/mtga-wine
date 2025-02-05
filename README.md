# MTGA Wine

Run MTG Arena on your Mac!

## Requirements

- Wine Stable 3.0.5
- XCode Command Line Tools
- Homebrew
- xquartz
- cabextract
- zenity
- winetricks

## Quick Start

### Installing dependencies and prerequisites

Check to see if you have XCode Command Line Tools installed by running `xcode-select -p` in the terminal. If it is installed, you'll be presented with the tools path. If it is not installed, run `xcode-select --install` in the terminal.

A script has been supplied to install Homebrew, xquartz, cabextract, zenity, winetricks, and wine in one shot. This script is very naive and may not be ideal in all circumstances. If you have any concerns, please open the script and execute the commands manually.

```bash
bin/prerequisites.sh
```

### Build and wrap

Run the build script to create the Wine bottle, install the remaining dependencies and MTG Arena, and make a Mac application wrapper.

```bash
bin/build.sh
bin/make-wrapper.sh
```

### Enjoy

If all has gone well, an executable Mac application will be deposited in 'out/MTGA.app'. You may move this to your Applications directory and run it as you would any other application. You may also remove the 'tmp' directory to free up space.

## Troubleshooting

The scripts are all fairly simple and do not provide much in the way of fault tolerance. If something doesn't seem to be working during the build, you may try to remove `&> /dev/null` from the wine commands to watch the output for obvious issues. 

## Contributing

If you would like to help make this project better, please feel free to make a pull request. 

## Acknowledgments

Inspiration for the wrapper came from this project: https://github.com/p-sam/hori-mini-wired-gamepad-remote-play
