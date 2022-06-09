<h3>Elastic Search Kurulum</h3>


[![OS](https://img.shields.io/badge/ubuntu-20.04.4-red?style=flat-square&logo=ubuntu)](https://releases.ubuntu.com/20.04/)
[![Microk8s](https://img.shields.io/badge/microk8s-1.21-red?style=flat-square&logo=canonical)](https://microk8s.io/resources)
[![Kubectl](https://img.shields.io/badge/kubectl-1.21-blue?style=flat-square&logo=kubernetes)](https://kubernetes.io/docs/tasks/tools/)
[![Helm](https://img.shields.io/badge/Helm-blue?style=flat-square&logo=helm)](https://helm.sh/)

- Kubectl komutu çalıştırılan yerde [Kubectl](https://kubernetes.io/docs/tasks/tools/) kurulu olmalı.
  - Linux: `sudo snap install kubectl --classic --channel=1.21/stable`
- Elastic CRDS yaml'ını indiriyoruz:
  `kubectl create -f https://download.elastic.co/downloads/eck/2.2.0/crds.yaml`
- Elastic operatörünü kuruyoruz:
  `kubectl apply -f https://download.elastic.co/downloads/eck/2.2.0/operator.yaml`
- Operator loglarını izleyebiliriz:
  `kubectl -n elastic-system logs -f statefulset.apps/elastic-operator`
- Monitoring için yeni bir namespace oluşturuyoruz:
  `kubectl create namespace elastic-monitoring`
  
## Kubernetes Ortamına Eklenecek YAML dosyası

- YAML dosyası:

    - [YAML](https://github.com/yusufatmc/local1/blob/main/elasticsearch.yml)
    
- Elastic Kurulumunu Kaldırma
    ```bash
    # This deletes all underlying Elastic Stack resources, included their Pods, Secrets, Services, and so on.
    
    kubectl get namespaces --no-headers -o custom-columns=:metadata.name \
       | xargs -n1 kubectl delete elastic --all -n
       
    kubectl delete -f https://download.elastic.co/downloads/eck/2.2.0/operator.yaml
    kubectl delete -f https://download.elastic.co/downloads/eck/2.2.0/crds.yaml
