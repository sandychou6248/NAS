# NAS管理員
Aimmlab NAS setting

  
## NAS 規格
* 主機：Synology DS1621xs+ * 1   
* Cache SSD： Kingston KC2500 NVMe PCIe SSD1000GB(1TB) 固態硬碟 (SKC2500M8/1000G) * 2  
* ECC RAM：Synology群暉科技 D4ECSO 2666 16G 記憶體 * 2  
* Disk：WD【金標】10TB 3.5吋企業級硬碟(WD102KRYZ) * 6  



## NAS 安裝
* Step 1：安裝硬體，硬體安裝手冊：Hardware Install Manual  
* Step 2：安裝DSM，安裝方式：DSM Installation  
    進入同一區域網路的方式   
    * 1.	將NAS網路孔插上WiFi路由器的網路孔，並用其他電腦連上此WiFi或是插上WiFi路由器的其他接孔  
    * 2.	將NAS和其他電腦接上同一台路由器或是Switch 
* Step 3：安裝完DSM，在控制台→共用資料夾→新增即可依需求將硬碟分割成需要的儲存區(目前組態為4顆10TB HDD RAID 6 共20TB)  
* Step 4：在控制台→檔案服務→NFS，啟用NFS系統，方便接下來和server對接 


## Server設定
* 依照參考網站指示安裝完後進入NAS的介面，將共用資料夾的NFS權限進行調整，目前是調整為將NFS權限統一歸類為guest，並以guest來進行資料夾讀寫權限的管理即可。  
* https://kb.synology.com/zh-hk/DSM/tutorial/How_to_access_files_on_Synology_NAS_within_the_local_network_NFS#x_anchor_id7  


## NAS外網連接
使用 http://140.113.228.124:5000 即可從外部網路連線到NAS管理介面


## NAS測速
* 使用Synology 上的Docker套件進行iperf的安裝後測速  
* 參考網站：https://cleanshadow.blogspot.com/2017/01/nas.html  

