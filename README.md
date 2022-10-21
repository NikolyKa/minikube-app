# minikube-app
<h2>В репозитории описан манифест файл, который запускается через kubectl в кластере
поднятом на minikube.</h2>
<h2>Для запуска необходимо установить ```minikube``` и ```kubectl``` </h2>

<h3>С помощью команды ```minikube start``` создается кластер k8s.</h3>

<h3>После успешного создания кластера, командой ```kubectl get nodes``` проверяем наличие 
созданного нода.</h3>

<h3>Командой</h3> ```kubectl run app-kuber --image=nikolyka/kuber --port=8000``` <h3> создаем pod

с названием ```k8s-app``` на имедже "nikolyka/kuber" и открываем порт 8000 контейнеру.</h3>
<h3>Либо командой ```kubectl apply -f minikube-app.yml``` проделываем то же самое

на основе манифест файла.</h3>

<h3>После создания пода, командой ```kubectl get pods``` проверяем начилие созданного пода.</h3>

<h3>Командой ```kubectl port-forward app-kuber 8080:8000``` можем присвоить порт

8080 нашего компьютера порту 8000 пода, после чего заходим на ```localhost:8080``` 

и проверяем работоспособность. </h3>