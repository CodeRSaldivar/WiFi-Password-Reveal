One-Line Copy/Paste

cls & for /F "delims=: skip=9 tokens=2" %a in ('netsh wlan show profiles') do @for /F "tokens=*" %A in ('echo %a') do @echo. & @echo. & @echo SSID:  %A & for /F "delims=: tokens=2" %b in ('netsh wlan show profiles name^=^"%A^" key^=clear ^| findstr Content') do @for /F "tokens=*" %B in ('echo %b') do @echo Password:  %B & @echo.
