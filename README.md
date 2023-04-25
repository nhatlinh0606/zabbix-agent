I. Tạo file chứa scrip

`sudo nano zabbix-agent.sh`

II. Coppy toàn bộ nội dung trong thư mục scrip dán vào thư mục zabbix-agent.sh vừa tạo
 TÌm đến dòng 21 và 22 sửa đổi thành ip private zabbix-server

`21. sed -i "s+Server=127.0.0.1+Server=12.123.13.123+g" /etc/zabbix/zabbix_agentd.conf`
`22. -i "s+ServerActive=127.0.0.1+ServerActive=12.123.13.123:10051+g" /etc/zabbix/zabbix_agentd.conf`

III. Sau khi hoàn thành 2 bước trên, thực hiện chạy scrip

`sudo bash ./zabbix-agent.sh`