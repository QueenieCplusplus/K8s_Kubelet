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
      
