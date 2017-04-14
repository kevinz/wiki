## customize user data dir
`append --user-data-dir=f:\chrome_tmp`

`"C:\Program Files (x86)\Google\Chrome\Application\chrome.exe" --user-data-dir=f:\chrome_tmp`

## add registry key for opening link
reg add "HKLM\SOFTWARE\Policies\Google\Chrome" /v UserDataDir /t REG_SZ /d "f:\chrome_tmp" /f
