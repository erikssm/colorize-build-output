# colorize-build-output

Quickly find build warnings and errors in those "wall of text" build outputs by applying color to error and warning lines.

Add these lines to ~/.bashrc:
- export col_normal="$(printf '\033[0m')"
- export col_bold="$(printf '\033[0;1m')"
- export col_red="$(printf '\033[0;31m')"
- export col_bold_yellow="$(printf '\033[1;1;33m')"
- export col_bold_red="$(printf '\033[0;1;31m')"

Few tests:
- echo "test error in console build output" | sed -e "s/error/${col_bold_red}&${col_normal}/Ig" 
- echo "test warning in console build output" | sed -e "s/warning/${col_bold_yellow}&${col_normal}/Ig" 
