<h3>ElektraWeb Kurulum Öncesi Gereksinimler</h3>


[![OS](https://img.shields.io/badge/ubuntu-20.04.4-red?style=flat-square&logo=ubuntu)](https://releases.ubuntu.com/20.04/)
[![Microk8s](https://img.shields.io/badge/microk8s-1.21-red?style=flat-square&logo=canonical)](https://microk8s.io/resources)
[![Kubectl](https://img.shields.io/badge/kubectl-1.21-blue?style=flat-square&logo=kubernetes)](https://kubernetes.io/docs/tasks/tools/)
[![Helm](https://img.shields.io/badge/Helm-blue?style=flat-square&logo=helm)](https://helm.sh/)

<h4>Ön Hazırlıklar</h4>
 :mage: Sunucu oluşturma adımında listede yer alan konfigrasyon önerilerinden bir seçim yapılmalıdır.
 </n>
<center><img src='https://downloader.disk.yandex.ru/preview/ac0d24f1325ef5c41dfe4a8754c3e5694841d01040ff374dff19a6fb7b76d5c6/629f2db0/tQPrzf_yxUNargzX5cEkfIso3wZvEw2GuwkqLEPpPP6QGfX-3ll8nzjdtRKbfHJWgH5cpBEdWudgjqJEpl9ZNg%3D%3D?uid=0&filename=2022-06-07_09-50-52.png&disposition=inline&hash=&limit=0&content_type=image%2Fpng&owner_uid=0&tknv=v2&size=2048x2048'> </img> </center>

<h4>İşletim Sistemi</h4>


:mage: Kurulum Ubuntu işletim sisteminde yapılmaktadır, oluşturulan sunucular aşağıdaki sürümlere sahip bir ubuntu işletim sistemiyle kurulmalıdır.

- <a href='https://releases.ubuntu.com/20.04/' target="_blank" >Ubuntu 20.04</a>
- <a href='https://releases.ubuntu.com/jammy/' target="_blank" >Ubuntu 22.04</a>

<h4>Gerekli Lisanslar</h4>


:mage: Kurulumda ve programın çalışma rutininde aşağıdaki lisanslara ihtiyacımız olacak.

- <a href='https://www.microsoft.com/tr-tr/sql-server/sql-server-2019-pricing' target="_blank" >Microsoft SQL Server</a>
- <a href='https://www.ag-grid.com/license-pricing' target="_blank" >AG Grid (Single Application)</a>
- <a href='https://www.bryntum.com/store/scheduler/' target="_blank" >Bryntum Scheduler (Small Team)</a>


<h4>Alan Adı</h4>


:mage: Oluşturulan sunuculara yönlendirilmek üzere 4 alan adına ihtiyacımız olacak.

- app.alanadi.com
- pos.alanadi.com
- api.alanadi.com
- report.alanadi.com


<h4>Firewall Kuralları</h4>


:mage: Oluşturulan sunucular programın kurulumunda ve sonrasında yapılacak güncellemelerde bu adreslere erişebilmelidir.

- 4001.hoteladvisor.net
- ghcr.io
- security.ubuntu.com
- tr.archive.ubuntu.com
- registry.hub.docker.com
- docker.io
- *.docker.io
- docker.com
- *.docker.com
