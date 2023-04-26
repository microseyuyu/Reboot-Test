# Reboot test

## how to use？

1. put script *cycletest.service* into  */lib/systemd/system* 
2. follow the step blow:

```
systemctl daemon-reload
systemctl enable cycletest.service (enable the service to start on reboot)
systemctl start cycletest.service (start the service, should reboot in 30s)
```

3. This script could only count times, it CANNOT set times.If you want to stop the test just log in and type ```systemctl stop cycletest.service```
4. the results will appear in ```/``` called ```cycle-count```