### Using USB Windows boot media

Boot USB to recover and choose command prompt, then:
```
cd c:\windows\system32
rename utilman.exe utilman.exe.orig
copy cmd.exe utilman.exe
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
Use interactive mode
```
chntpw -i SAM
```
