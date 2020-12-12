% ROFIMOJI(1) Version 4.3.0 | Rofi Third-party Add-on Documentation
% Fabian Winter
% December 01, 2020

# NAME


**rofimoji** \- A character (emoji) picker for rofi

# SYNOPSIS

| **rofimoji** \[**-h**] \[**--version**] \[**--insert-with-clipboard**] \[**--copy-only**]
         \[**--skin-tone** {*neutral*,*light*,*medium-light*,*moderate*,*dark brown*,*black*,*ask*}]
         \[**--files** {*all*,*FILE* \[*FILE* ...]]} \[**--prompt** *PROMPT*]
         \[**--rofi-args** *ROFI_ARGS*] \[**--max-recent** *MAX_RECENT*]
         \[**--clipboarder** *CLIPBOARDER*] \[**--typer** *TYPER*]

# DESCRIPTION

Select, insert, or copy Unicode characters like emoji using rofi.

# OPTIONS

-h, --help

:   Prints brief usage information.

--version

:   show program's version number and exit

--insert-with-clipboard, -p

:   Do not type the character directly, but copy it to the
    clipboard, insert it from there and then restore the
    clipboard's original value

--copy-only, -c

: Only copy the character to the clipboard but do not insert it

--skin-tone=_skin-tone_, -s _skin-tone_

: Possible values: neutral, light, medium-light, moderate, dark brown, black, ask

      Decide on a skin-tone for all supported emojis. If not
      set (or set to "ask"), you will be asked for each one

--files=_FILE_ [_FILE_ ...], -f _FILE_ [_FILE_ ...]

:  Read characters from this file instead, one entry per line

--prompt _PROMPT_, -r _PROMPT_

:  Set rofimoj's prompt

--rofi-args _ROFI-ARGS_

:  A string of arguments to give to rofi

--max-recent _MAX-RECENT_

:  Show at most this number of recently used characters
   (cannot be larger than 10)

--clipboarder _CLIPBOARDER_

: Possible values: xsel, xclip, wl-copy

      Choose the application to access the clipboard with

--typer _TYPER_

: Possible values: xdotool, wtype

      Choose the application to type with

# KEYBINDINGS

(optional) Select multiple emoji with shift+enter

*enter* to insert the emoji directly

*alt+c* to copy it to the clipboard

*alt+t* to type it directly

*alt+p* to insert using the clipboard

*alt+1*, *alt+2* to insert the most recently used character (alt+2 for the second most recently one etc.)

*alt+u* to insert the Unicode codepoint

*alt+i* to copy the Unicode codepoint to the clipboard

# FILES

*~/.config/rofimoji.rc*

:   Per-user configuration file.

*/etc/xdg/xdg-i3/rofimoji.rc*

:   Global configuration file.

*~/.local/share/rofimoji/recent*

:   Stores the recently used characters

# CONFIGURATION

Args that start with "--" (eg. --version) can also be set in a config file.

Config file syntax allows: key=value, flag=true, stuff=[a,b,c] (for details, see syntax at https://github.com/fdw/rofimoji#example-config-file). If an arg is
specified in more than one place, then commandline values override values from the config file.

# WEBSITE

https://github.com/fdw/rofimoji