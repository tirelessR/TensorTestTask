# Тестовое задание Тензор

1. Установка Foreman 5.0
hostnamectl set-hostname foreman.lab
/etc/hosts:    192.168.56.101  foreman.lab foreman
sudo dnf install -y foreman-proxy foreman-plugin-ansible foreman-proxy-plugin-ansiblesudo foreman-installer \  --enable-foreman-plugin-ansible \  --enable-foreman-proxy \  --enable-foreman-proxy-plugin-ansible

2. Регистрация managed host
/etc/hosts на .102:    192.168.56.101  foreman.lab foreman    192.168.56.102  managed.lab managed
Последующая регистрация произведена в Foreman UI

3. Шаблон с ntp
Создан фрагмент NTP_setup
Клонирован дефолтный Kickstart, в %post добавлен вызов фрагмента
Шаблон привязан к AlmaLinux 9.9
Роль disable_root кладётся в /etc/ansible/roles на основной машине

