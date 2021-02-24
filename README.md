# Ansible

# Выполнение ДЗ

## Результатом выполнения ДЗ стало развертывание сервера NGINX, слушающего на порту 8080, с помощью Ansible роли:

```shell
root@otus-VirtualBox:/vagrant/hw13# ansible-playbook nginx.yml

PLAY [Install & configure NGINX] *********************************************************************************************************************

TASK [Gathering Facts] *******************************************************************************************************************************
ok: [nginx]

TASK [nginx_8080 : Install EPEL Repo] ****************************************************************************************************************
ok: [nginx]

TASK [nginx_8080 : Install NGINX] ********************************************************************************************************************
ok: [nginx]

TASK [nginx_8080 : Create NGINX config file from template] *******************************************************************************************
ok: [nginx]

PLAY RECAP *******************************************************************************************************************************************
nginx                      : ok=4    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0   

```

## Проверяем результат:

```shell
root@otus-VirtualBox:/vagrant/hw13# curl http://192.168.11.150:8080
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN">
<html>
<head>
  <title>Welcome to CentOS</title>
  <style rel="stylesheet" type="text/css"> 

	html {
	background-image:url(img/html-background.png);
	background-color: white;
	font-family: "DejaVu Sans", "Liberation Sans", sans-serif;
	font-size: 0.85em;
	line-height: 1.25em;
	margin: 0 4% 0 4%;
	}
```

