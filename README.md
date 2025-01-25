## Инструменты для тесной интеграции qm/ct с хостовой смстемойb, большие планы на эту связку ##

### Первое что мы делаем: ставим virt-manager и spice-guest-tools-latest.exe ###

## Далее: чуть пройдемся по настройкам виртуалки, чтобы она работала в контуре Proxmox так, как нам нужно. ##



![2025-01-25_03-48-24](https://github.com/user-attachments/assets/f453117a-c12e-4251-b570-8edb8e556dbd)


![2025-01-25_04-32-18](https://github.com/user-attachments/assets/77932651-3d95-4c58-bc7d-9d0bb75ad869)


![2025-01-25_04-32-56](https://github.com/user-attachments/assets/49c6a0fa-0f00-4f66-81d9-e616396a43b4)




![2025-01-25_04-36-20](https://github.com/user-attachments/assets/e0c408f7-8e78-4e06-90ef-4a6dc5f13658)

![2025-01-25_04-37-31](https://github.com/user-attachments/assets/2506ec85-6ed4-4475-9f56-c71701310568)




![2025-01-25_04-40-24](https://github.com/user-attachments/assets/97ccd069-cfb8-4db0-922e-45d0fb0ffd59)

### Внутри виртуалки выполняем: ###

apt install qemu-guest-agent ; bash -x /etc/init.d/qemu-guest-agent  start

### После этого на хосте выполняем ###

qm guest cmd  300 get-osinfo


### ответ должен бытть что-то вроде ###


{
   "id" : "debian",
   "kernel-release" : "6.1.0-30-amd64",
   "kernel-version" : "#1 SMP PREEMPT_DYNAMIC Debian 6.1.124-1 (2025-01-12)",
   "machine" : "x86_64",
   "name" : "Debian GNU/Linux",
   "pretty-name" : "Debian GNU/Linux 12 (bookworm)",
   "version" : "12 (bookworm)",
   "version-id" : "12"
}

### Список команд: ###

qm help guest cmd
