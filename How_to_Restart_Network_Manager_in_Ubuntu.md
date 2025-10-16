<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" class="logo" width="120"/>

## How to Restart Network Manager in Ubuntu

There are several effective methods to restart the Network Manager service in Ubuntu, depending on your system version and preference for command-line or graphical tools.

**Using systemctl (Recommended for Modern Ubuntu Versions)**

- Open a terminal (Ctrl + Alt + T).
- Run the following command:

```bash
sudo systemctl restart NetworkManager
```

This command will gracefully stop and restart the NetworkManager service, which manages your network connections. You may notice the network icon disappear briefly as the service restarts[^1_1][^1_3][^1_5].

**Using the service Command (Alternative Method)**

- In the terminal, you can also use:

```bash
sudo service network-manager restart
```

This works on many Ubuntu versions and achieves the same result[^1_6].

**Using nmcli (NetworkManager Command Line Interface)**

- To turn networking off and on via NetworkManager’s CLI, use:

```bash
sudo nmcli networking off
sudo nmcli networking on
```

Or, to bring a specific connection up:

```bash
sudo nmcli connection up <connection_name>
```

Replace `<connection_name>` with the name of your network connection[^1_1].

**Using the Graphical User Interface (GUI)**

- Click the network icon in the system tray.
- Select “Turn Off” to disable networking.
- Wait a moment, then select “Turn On” to re-enable networking[^1_6].

**Verifying the Restart**

- After restarting, check the status with:

```bash
nmcli general status
```

This will confirm that NetworkManager is active and your connections are up[^1_1][^1_3].

**Cautions**

- If you are connected remotely (e.g., via SSH), restarting NetworkManager may temporarily disconnect you[^1_1][^1_3].
- For older Ubuntu versions or server environments, additional commands like `ifdown` and `ifup` may be used, but these are less common in modern Ubuntu releases[^1_3].

**Summary Table**


| Method | Command | Applies to |
| :-- | :-- | :-- |
| systemctl | `sudo systemctl restart NetworkManager` | Ubuntu 15.04+ |
| service | `sudo service network-manager restart` | Older Ubuntu |
| nmcli | `sudo nmcli networking off/on` | All with NM |
| GUI | Use network tray icon to turn off/on networking | Desktop only |

These methods will restart the Network Manager service and refresh your network connections in Ubuntu[^1_1][^1_3][^1_6].

<div style="text-align: center">⁂</div>

[^1_1]: https://greenwebpage.com/community/how-to-restart-network-services-in-ubuntu-24-04/

[^1_2]: https://askubuntu.com/questions/230698/how-to-restart-the-networking-service

[^1_3]: https://gcore.com/learning/how-to-restart-the-network-in-ubuntu

[^1_4]: https://www.reddit.com/r/Kubuntu/comments/yah4gl/need_to_restart_networkmanager_after_changing/

[^1_5]: https://help.ubuntu.com/community/NetworkManager

[^1_6]: https://monovm.com/blog/how-to-restart-network-in-ubuntu/

[^1_7]: https://unix.stackexchange.com/questions/219768/restarting-all-the-network-in-ubuntu-after-hibernating

[^1_8]: https://superuser.com/questions/1423959/ubuntu-server-fail-to-restart-networking-service-unit-network-service-not-foun

[^1_9]: https://serverfault.com/questions/1160179/networkmanager-keeps-restarting

