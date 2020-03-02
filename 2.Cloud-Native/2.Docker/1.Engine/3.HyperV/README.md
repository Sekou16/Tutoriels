# Hyper-V


https://vmarena.com/installing-hyper-v-on-windows-server-2019/

https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/about/

:one: - [BCD (Boot Configuration Data)](https://docs.microsoft.com/en-us/windows-hardware/manufacture/desktop/bcdedit-command-line-options) Set Hyper-V Auto

Utiliser `PowerShell` pour mettre à jour le type de démarrage de l'`Hypervisor`  (i.e. Auto/Off)

```
PS > bcdedit /set HypervisorLaunchType Auto
```

Installer Hyper-V (et redemarrer) sur Windows Standard ou Windows Server 

```
PS > Install-WindowsFeature -Name Hyper-V -IncludeManagementTools -Restart
```


![image](images/bcedit-auto.png)

:three: - S'assurer que Docker est démarré

![image](images/docker-logo.png)


:four: - S'assurer que le service HyperV est démarré 

![image](images/docker-desktop-vm.png)

:five: - S'assurer que le service HyperV est démarré 

![image](images/Hyper-V_Manager.png)

:six: - S'assurer que le service HyperV est démarré 

![image](images/Hyper-V_Services.png)
