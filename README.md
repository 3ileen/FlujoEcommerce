# Suite de Pruebas de APIs en Postman (PetStore & eCommerce)

**Autora:** Eileen Apaza Coaquira  
**Herramienta:** Postman (Collection v2.1)  

---

## 1. Variables de Entorno (`Entorno_QA_APIs`)

| Variable | Valor | Uso |
| :--- | :--- | :--- |
| `baseUrl` | `https://petstore.swagger.io/v2` | API CRUD Usuarios (PetStore) |
| `baseDummy` | `https://dummyjson.com` | API Auth y Perfil (DummyJSON) |
| `username` | `eileen` | Usuario de prueba |
| `password` | `Clave1234` | Contraseña de prueba |
| `token` | *(Dinámico)* | Token JWT capturado tras el login |

---

## 2. Endpoints Evaluados

| # | Servicio | Método | Endpoint | Estado |
| :- | :--- | :---: | :--- | :---: |
| 1 | Crear Usuario | `POST` | `{{baseUrl}}/user` | `200 OK` |
| 2 | Consultar Usuario | `GET` | `{{baseUrl}}/user/{{username}}` | `200 OK` |
| 3 | Actualizar Usuario | `PUT` | `{{baseUrl}}/user/{{username}}` | `200 OK` |
| 4 | Login PetStore | `GET` | `{{baseUrl}}/user/login` | `200 OK` |
| 5 | Eliminar Usuario | `DELETE` | `{{baseUrl}}/user/{{username}}` | `200 OK` |
| 6 | Login eCommerce (JWT) | `POST` | `{{baseDummy}}/auth/login` | `200 OK` |
| 7 | Perfil Protegido (Bearer) | `GET` | `{{baseDummy}}/auth/me` | `200 OK` |

---

## 3. Evidencias de Ejecución

* **1. Crear Usuario (`POST /user`)**  
  ![1](images/1.png)

* **2. Consultar Usuario (`GET /user/{{username}}`)**  
  ![2](images/2.png)

* **3. Actualizar Usuario (`PUT /user/{{username}}`)**  
  ![3](images/3.png)

* **4. Login PetStore (`GET /user/login`)**  
  ![4](images/4.png)

* **5. Eliminar Usuario (`DELETE /user/{{username}}`)**  
  ![5](images/5.png)

* **6. Login eCommerce (`POST /auth/login`)**  
  ![6](images/6.png)

* **7. Perfil Protegido (`GET /auth/me`)**  
  ![7](images/7.png)