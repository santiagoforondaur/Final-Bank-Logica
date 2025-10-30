# Final-Bank-Logica

Resumen del proyecto

Aplicación ejemplo de un mini-banco (API REST) construida con Spring Boot. Incluye conceptos típicos de sistema bancario: clientes, cuentas, transacciones y estrategias de interés. Está organizada con capas claras: controladores (REST), servicios, repositorios  y modelos.

# Estructura relevante

- AppbankApplication — Clase principal con main() que arranca Spring Boot.

- config/OpenApiConfig — Configuración para OpenAPI/Swagger (documentación automática de la API).

- controller/BankController — Controlador REST principal con base URL: /api/bank.

- service/BankService — Interfaz que define las operaciones del dominio (gestión de clientes, cuentas, operaciones bancarias, interés y consultas).

- service/BankServiceImpl — Implementación del servicio; contiene la lógica de negocio (crear clientes, crear cuentas, depósitos, retiros, transferencias, aplicar intereses, historial de transacciones, etc.).

- service/InterestStrategy — Interfaz para estrategias de cálculo de intereses.

- service/strategies/SimpleRateStrategy, TieredRateStrategy — Implementaciones de las estrategias de interés.

- repository/JsonRepository, repository/FileManager — Clases auxiliares para persistencia simple basada en archivos JSON (dataset de ejemplo incluido en /data).

- model/* — Entidades del dominio: Customer, Account, SavingsAccount, CheckingAccount, Transaction, Money.

- exception/DomainException — Excepciones de dominio controladas por el controlador (mapeadas a respuestas HTTP legibles).

- util/JsonUtil — Utilitarios para manejo JSON.

# Dependencias importantes (pom.xml)

El proyecto usa Maven y entre otras dependencias, incluye:

- spring-boot-starter-web — para crear el API REST.

- spring-boot-starter / spring-boot parent — arranque y autoconfiguración.

- Dependencias para OpenAPI/Swagger (configuración en OpenApiConfig).

# Swagger

En el siguiente apartado vamos a mostrar como son las operaciones de registrar cliente, transferir, depositar,etc...
Para acceder al swagger ponemos en el navegador la siguiente Url: http://localhost:8080/swagger-ui.html

# (Get) Customer


<img width="207" height="329" alt="Uno" src="https://github.com/user-attachments/assets/d0ab12ee-edf7-45b9-9b73-c2fa8eddbcb1" />


# (Post) Customer 


<img width="228" height="340" alt="Dos" src="https://github.com/user-attachments/assets/c2563454-5a24-4ca7-badc-92721c60e73a" />

# (Get) CustomerId Accounts 


<img width="215" height="407" alt="Tres " src="https://github.com/user-attachments/assets/48bc7bac-6648-4f77-8cec-d2898d191615" />

# (Post) CustomerId Accounts 


<img width="253" height="374" alt="Cuatro" src="https://github.com/user-attachments/assets/71c88298-b154-4238-8a37-f57a20f6e303" />


# (Post) Transfer 



<img width="214" height="266" alt="Cinco" src="https://github.com/user-attachments/assets/6c2c57f7-a9ff-49f8-bdf4-957a83d2f75d" />



# (Post) withdraw 


<img width="256" height="377" alt="Seis" src="https://github.com/user-attachments/assets/c7a3e515-4d5a-4d9c-bc8c-1c311b33c521" />


# (Post) Deposit 


<img width="235" height="338" alt="Siete" src="https://github.com/user-attachments/assets/1149db10-5655-4586-8342-cfb11e484771" />


#  (Post) Apply Interest 


<img width="309" height="256" alt="Ocho" src="https://github.com/user-attachments/assets/baca01ed-30ab-4594-aa3d-19de30ce1845" />


# (Get) CustomerId 


<img width="194" height="338" alt="Nueve" src="https://github.com/user-attachments/assets/2c709c89-aba1-4e96-ba70-861462734117" />


# (Get) AccountId 


<img width="189" height="361" alt="Diez" src="https://github.com/user-attachments/assets/6fccd8e5-8fde-4a29-ba5b-fb86e2fd992b" />

# (Get) Transactions 


<img width="218" height="373" alt="Once" src="https://github.com/user-attachments/assets/5f009518-685c-43c7-bd69-3da869709eef" />




