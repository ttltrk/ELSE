

---

###### [改善](https://github.com/ttltrk/0C/blob/master/README.MD) - [.co.](https://github.com/ttltrk/PRG/blob/master/CODING.MD) - [manuals](https://github.com/ttltrk/PRG/blob/master/MAN.MD) - [M](https://github.com/ttltrk/ELSE/blob/master/M/M.MD) - [UX](https://github.com/ttltrk/ELSE/blob/master/M/UX/UX.MD)

---

### SSH LOGIN

---

1. generate the keys with putty generator (move with your mouse in the window)
2. save public and private key. You need to protect the private key with passwords
3. restart the application and load the private key
4. copy the content to the clipboard
5. on the target server go to your own folder and create a .ssh folder with permission 700 in the .ssh folder create a file with name authorized_keys and past the content from the clipboard and save it. change the permission of the file to 600

```sh
ls -ald .ssh .ssh/authorized_keys
```

6. check the sshd_config and according to the settings change your file name, in ```/etc/ssh```

```sh
grep authorized_keys sshd_config

AuthorizedKeysFile      .ssh/authorized_keys2
```
in this case change the name of your file to authorized_keys2

7. in putty >> ssh > auth >> load the key >> save
8. now you should launch the application pageant.exe, after start you will find it on the taskbar
9. right click and add your keys. Type your password and now you are able to login to the requested servers (with your own user) without password!
10. enjoy

---
