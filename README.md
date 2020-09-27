# K8s_Kubelet
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
   
Master 服務的命名空間

      --master-service-namespace="default"
     
節點中可運行 Pod 數量的上限

      --max-pod=40
      
k8s的 kuberlet 回報 Node 狀態給 Master 的 間隔時間，預設為 10s

      --node-status-update-frequency=10s
      
節點註冊自身資訊至 API server。

      --register-node=true
      
分配 CIDR 位址，提供給 Pod，此適用於單機（倘若為叢集，會從 Api Server 中取得 CIDR 設定）

     --pod-cidr=""
     
設定映像檔名稱例如 eee 從何處下載例如 ccc.io，倘若遇到連線過慢或是防火牆阻擋，此參數可以解決問題，從別處取得映像檔並存入私有 Registry 儲存庫。

     --pod-infra-container-image="ccc.io/google_containers/eee:0.8.0"

容器中執行命令或是進行連接阜轉送過程誤徵會產生輸、出入串流，為了控制連線（閒置）逾時的關閉時間。

    --streaming-connection-idle-timeout=0

Pod 建立過程中，容器的映像檔可能需要從儲存庫中拉取，因為拉取過程會消耗大量頻寬，因此需要限速，倘若不限速，則可限制每秒可拉取的映像檔數量。

    --registry-qps=0
    
最多能從儲存庫拉取的映像檔案數量。

    --registry-burst=10
