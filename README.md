# lab-sem-11

<h3><b>Parte 1</b></h3>

<h4> Paso 1 </h4>
Búsqueda de "Azure Kubernetes Service" dentro de Crear Recursos 
<img width="1333" alt="Captura de pantalla 2024-06-06 a la(s) 11 17 42 p  m" src="https://github.com/micaaprocofio/lab-sem-11/assets/163476050/18ef346e-c399-4758-83a5-ec093912c330">

Información para la creacion del Clúster
<img width="1165" alt="Captura de pantalla 2024-06-06 a la(s) 11 27 06 p  m" src="https://github.com/micaaprocofio/lab-sem-11/assets/163476050/7dfc47f8-be0c-4de5-88c7-71744b8297d7">

Se implemento correctamente el Clúster
<img width="1437" alt="Captura de pantalla 2024-06-06 a la(s) 11 46 06 p  m" src="https://github.com/micaaprocofio/lab-sem-11/assets/163476050/9a46d04d-5d59-424e-a5d3-410d598f7def">

Información general del Clúster ya creado
<img width="1437" alt="Captura de pantalla 2024-06-06 a la(s) 11 47 42 p  m" src="https://github.com/micaaprocofio/lab-sem-11/assets/163476050/7560cdb5-811a-484d-97a5-8447438ec418">

<h4> Paso 2/3 </h4>

Conexión al Clúster, establecer subscripción y descargar credenciales del Clúster
<img width="1437" alt="Captura de pantalla 2024-06-06 a la(s) 11 56 01 p  m" src="https://github.com/micaaprocofio/lab-sem-11/assets/163476050/08de6a07-d15f-465c-8d0c-423723a8245d">

Nodos configurados en la creación del Clúster
<img width="1437" alt="Captura de pantalla 2024-06-06 a la(s) 11 57 12 p  m" src="https://github.com/micaaprocofio/lab-sem-11/assets/163476050/e72e8f7f-0357-4092-95a3-fad069ad77d1">

----------------
<h3><b>Parte 2</b></h3>

<h4> Paso 1 </h4>

Creación del archivo de especificación del Deployment
<img width="1437" alt="Captura de pantalla 2024-06-07 a la(s) 12 08 56 a  m" src="https://github.com/micaaprocofio/lab-sem-11/assets/163476050/47fef97c-1916-437f-aff8-0d5ca07d816a">

Modificación del archivo de especificación del Deployment : comando vim nginx-deployment.yaml
<img width="1437" alt="Captura de pantalla 2024-06-07 a la(s) 12 10 03 a  m" src="https://github.com/micaaprocofio/lab-sem-11/assets/163476050/0de97be3-3856-4177-9f4f-f49a21ed0dd4">

Visualización del contenido del archivo
<img width="1437" alt="Captura de pantalla 2024-06-07 a la(s) 12 10 19 a  m" src="https://github.com/micaaprocofio/lab-sem-11/assets/163476050/c4b25015-31fb-4f82-a578-99e595656449">

<h4> Paso 2 </h4>

Desplegar el Deployment en el clúster de AKS
<ul>
  <li> <b>kubectl get nodes: </b> comando para asegurarse de que esta conectado al clúster de AKS</li>
  <li> <b>kubectl apply -f nginx-deployment.yaml:</b> comando para desplegar el Deployment </li>
  <li> <b>kubectl get deployments:</b> comando para verificar que el Deployment se haya desplegado correctamente </li>
</ul>
 <img width="1432" alt="Captura de pantalla 2024-06-07 a la(s) 12 11 42 a  m" src="https://github.com/micaaprocofio/lab-sem-11/assets/163476050/124482d9-77c1-4efd-80cf-e04490b2c1c5">

<h4> Paso 3 </h4>

Exponer el Deployment con un Load Balancer
<ul>
  <li> <b>touch nginx-service.yaml : </b> comando para la creacion del archivo </li>
  <li> <b>kubectl apply -f nginx-service.yaml:</b> comando para crear el servicio de Load Balancer </li>
  <li> <b>kubectl get services:</b> comando para verificar que el servicio se haya desplegado correctamente </li>
</ul>
<img width="1421" alt="Captura de pantalla 2024-06-07 a la(s) 12 15 50 a  m" src="https://github.com/micaaprocofio/lab-sem-11/assets/163476050/aa86e6dd-a47b-4d09-8b9f-8d133a9eebeb">

Modificación del archivo: comando vim nginx-service.yaml
<img width="1432" alt="Captura de pantalla 2024-06-07 a la(s) 12 14 41 a  m" src="https://github.com/micaaprocofio/lab-sem-11/assets/163476050/911f0c42-a75a-4d93-ba14-a5173c479793">

<h4> Paso 4 </h4>

Dirección IP externa del servicio de Load Balancer
<img width="1421" alt="Captura de pantalla 2024-06-07 a la(s) 12 16 23 a  m" src="https://github.com/micaaprocofio/lab-sem-11/assets/163476050/3d9b81fb-5121-4d9e-85a6-c2c9d0d63c79">

Acceder al Deployment de NGINX utilizando la dirección IP externa del servicio de Load Balancer
<img width="1421" alt="Captura de pantalla 2024-06-07 a la(s) 12 17 04 a  m" src="https://github.com/micaaprocofio/lab-sem-11/assets/163476050/e4f75dcf-5a0a-428b-a87f-5aa180b234c9">
