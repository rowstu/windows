### Using USB Windows boot media

Boot USB to recover and choose command prompt, then:
```
move c:\windows\system32\utilman.exe c:\
copy c:\windows\system32\cmd.exe c:\windows\system32\utilman.exe
```
The reboot and press Ease of Access button which will open the command prompt instead of accessibility.
Then enter
```
# net user <account name> <new password>
net user user newpassword
```
Once logged back in move utilman.exe back to system32.


### Kali
Open a terminal window in /Windows/System32/Config
```
# list users
chntpw -l SAM
```
Perform action on the account
```
chntpw -u <username> SAM
```
