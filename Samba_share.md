# How to create a Samba share

### 參考資料
>[鳥哥](http://linux.ev.ncku.edu.tw/linux_server/centos4/0370samba-centos4.php#client_win_445)

>[DOCS](https://docs.fedoraproject.org/en-US/quick-docs/samba/#sharing_a_directory_for_many_users)

>[Linux——搭建Samba(CIFS)伺服器](https://iter01.com/640334.html)

### 必裝套件
- `# dnf install policycoreutils-python-utils`
- samba：
    ```
    sudo dnf install samba
    sudo systemctl enable smb --now
    firewall-cmd --get-active-zones
    sudo firewall-cmd --permanent --zone=FedoraWorkstation --add-service=samba
    sudo firewall-cmd --reload 
    ```
- samba-common：
- samba-client： ```yum -y install samba-client```

### creat a SAMBA

## 多台需要設定的地方

### share storage
- [semba](https://docs.fedoraproject.org/en-US/quick-docs/samba/#install_and_enable_samba)
```
sudo dnf install samba
sudo systemctl enable smb --now
firewall-cmd --get-active-zones
sudo firewall-cmd --permanent --zone=FedoraWorkstation --add-service=samba
sudo firewall-cmd --reload

dnf install policycoreutils-python-utils
```
