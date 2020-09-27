# K8s_Kubelete
Software for Node

* 參數表


綁定主機 IP 位址，設定為 0.0.0.0. 表示全部網路介面。

      --address=0.0.0.0

啟動 http restfult server，此伺服器提供了取得本 Node 上執行的 Pod 清單與 Pod 狀態，利於 Web 管理。

      --enable-server=false
      
      --port=10250 # http server 上的連接阜
      
設定 Master （apiserver） 位址清單，以 ip:port 表示。

      --api-servers=[]
      
TLS 憑證位於的目錄，預設為 /var/run/kubernetes。

      --cert-dir="/var/run/kubernetes"
      
隨機產生用戶端（使用者端）錯誤的機率，僅用於測試，預設為 0，即不產生錯誤。

      --chaos-chance=0
      
雲端供應商的設定檔路徑

      --cloud-config=""
      
雲端供應商的名稱

      --cluster-provider=""
      
叢集 DNS 的 IP 服務

      --cluster-dns=<nil>
      
Kuberlet 設定檔路徑或是目錄名稱

      --config=""
      
Docker endpoint 位址

      --docker-endpoint="unix:///var/run/docker.sock"
      
容器的類型，預設為 docker

      --container-runtime="docker"
      
根據 Node.Spec.PodCIDR 值來配置 cbr0

      --configure-cbr0=true
    
覆寫真實的主機名稱

      --hostname-override=""
      
建立 Pod 所需剩餘磁碟空間的下限，單位為 MB，當剩餘磁碟空間低於此值時， kuberlet 拒絕建立新的 Pod，預設值為 256 MB。

      --low-diskspace-threshhold-mb=256
      
設定映像檔佔用磁碟空間比值，超過門檻便會處理不用的影像檔，Garbage Collection 釋放磁碟空間，需搭配上敘設定的剩餘磁碟空間下限。

      --image-gc-high-threshhold=90
      
