
## 🎯 Objetivo do Curso Compreender a fundo o Protocolo de Transferência de Hipertexto (HTTP), sua arquitetura, funcionamento e evoluções, essenciais para o desenvolvimento web.

---
## 📚 Módulo 1: Conhecendo o Protocolo HTTP

### 💡 O que é HTTP? - **HTTP**: Hypertext Transfer Protocol (Protocolo de Transferência de Hipertexto).

- **Função**: Protocolo de comunicação usado para transferir dados na web (páginas HTML, imagens, scripts, etc.)
- **Arquitetura**: Modelo **Cliente-Servidor**.
- **Cliente**: Geralmente o navegador (browser), mas pode ser qualquer aplicação que faz a requisição.
- **Servidor**: Aplicação que hospeda o recurso e envia a resposta.
- **Requisição e Resposta**: O ciclo de comunicação. 
### 🔗 URLs, Domínios e Endereços 

- **URL (Uniform Resource Locator)**: O endereço de um recurso na web. - **Componentes**: Esquema (http/https), Domínio, Porta (opcional), Caminho, Query String, Fragmento.
- **Domínios**: Como o sistema de nomes funciona e sua relação com endereços IP (via DNS)
- . - **DNS (Domain Name System)**: O "GPS" da internet, traduz nomes de domínio em IPs.

### 🌐 Camadas da Internet

O protocolo HTTP vive na **Camada de Aplicação**. Para que uma mensagem HTTP chegue ao seu destino, ela precisa passar pelas camadas inferiores (Modelo TCP/IP):

| # | Camada | Protocolo Exemplo | Função Principal | Ligação com o HTTP |
|:---:|:---|:---|:---|:---|
| **4** | **Aplicação** | **HTTP**, DNS, FTP | Define o protocolo para os aplicativos (ex: navegador) trocarem dados. É onde o HTTP atua. | **O HTTP é o próprio protocolo desta camada.** |
| **3** | **Transporte** | **TCP** / UDP | Garante a comunicação **fim-a-fim** e a entrega confiável dos dados. | O HTTP depende do **TCP** para que as requisições e respostas cheguem inteiras e na ordem. |
| **2** | **Rede/Internet** | **IP** | Endereçamento e Roteamento. Define o caminho para o dado chegar ao IP de destino. | O TCP (e, por consequência, o HTTP) depende do IP para saber **para onde enviar** a mensagem. |
| **1** | **Enlace/Física** | Ethernet, Wi-Fi | Transmissão física do dado (bits) através da infraestrutura (cabos, ondas de rádio). | As bases físicas que permitem a comunicação entre os dispositivos. |

#### Detalhamento das Camadas Inferiores:

* **Camada de Transporte (TCP/UDP):**
    * **TCP (Transmission Control Protocol):** É **confiável** e orientado à conexão. Ele estabelece uma "conversa" (handshake), fragmenta a mensagem HTTP em pacotes e garante que eles cheguem na ordem correta, retransmitindo se necessário. O HTTP geralmente utiliza o TCP.
    * **UDP (User Datagram Protocol):** Mais rápido, mas **não garante** a entrega nem a ordem (não é usado primariamente para HTTP).
* **Camada de Rede/Internet (IP - Internet Protocol):**
    * Responsável pelo **endereçamento**. Cada dispositivo na rede tem um endereço IP, e esta camada decide a **melhor rota** (o caminho) para o pacote de dados viajar através de roteadores até o destino.
* **Camada de Enlace/Física:**
    * Lida com a transferência de dados localmente (em um segmento de rede). A **Camada Física** é o meio físico em si (cabos de fibra, par trançado, etc.), transformando os dados em sinais elétricos ou ópticos.

#### 💡 Importância para o HTTP

O HTTP é um protocolo de alto nível que não se preocupa com "como" o bit viaja, ele confia nas camadas inferiores:
* Se o **TCP** falhar em estabelecer a conexão, o HTTP falha (ex: "Connection Refused").
* Se o **IP** falhar em encontrar a rota, a requisição HTTP falha (ex: timeout).
---
## 🛠️ Módulo 2: O Ciclo de Requisição e Resposta ### 📨 Mensagens HTTP 

- **Requisição HTTP (Cliente -> Servidor)** 
- **Linha de Requisição**: Método HTTP + URL + Versão do Protocolo. 
- **Cabeçalhos (Headers)**: Metadados sobre a requisição (e.g., `User-Agent`, `Accept`, `Host`). 
- **Corpo (Body)**: Dados enviados ao servidor (ex: em requisições `POST` ou `PUT`). 
- **Resposta HTTP (Servidor -> Cliente)** 
- **Linha de Status**: Versão do Protocolo + Código de Status + Frase de Status. 
- **Cabeçalhos (Headers)**: Metadados sobre a resposta (e.g., `Content-Type`, `Date`, `Server`). 
- **Corpo (Body)**: O recurso solicitado (e.g., HTML, JSON, imagem). ### 🏷️ Métodos HTTP (Verbos) 
- **GET**: Solicita a representação de um recurso. (Leitura) 
- **POST**: Envia dados para criar um novo recurso. (Criação) 
- **PUT**: Atualiza um recurso existente ou o cria se não existir. (Atualização Completa) 
- **DELETE**: Remove um recurso específico. (Exclusão) 
- **PATCH**: Aplica modificações parciais a um recurso. (Atualização Parcial) 
- **HEAD**: Pede apenas os cabeçalhos (headers) da resposta, sem o corpo.

### 🚥 Códigos de Status (Status Codes) 

- **1xx - Informativo** (Continua) 
- **2xx - Sucesso** (`200 OK`, `201 Created`, `204 No Content`) 
- **3xx - Redirecionamento** (`301 Moved Permanently`, `302 Found`) 
- **4xx - Erro do Cliente** (`400 Bad Request`, `401 Unauthorized`, `403 Forbidden`, `404 Not Found`) 
- **5xx - Erro do Servidor** (`500 Internal Server Error`, `503 Service Unavailable`) 

---
## 🛡️ Módulo 3: Segurança e Evolução 
### 🔒 HTTPS: A Web Segura 
- **Diferença HTTP vs HTTPS**: 
- **HTTP**: Trafega dados em texto puro. 
- **HTTPS**: HTTP + Camada de Segurança **SSL/TLS** (dados criptografados). 
- **Certificado Digital**: Prova a identidade do servidor e contém a chave pública para a criptografia. 
- **Como funciona a Criptografia**: Chaves públicas e privadas. 

### 💨 Evoluções do HTTP 
- **HTTP/1.1**: O protocolo padrão por muito tempo. 
- **HTTP/2**: Melhorias em performance, introduzindo: - **Multiplexing**: Múltiplas requisições em uma única conexão. - **Compressão de Headers (HPACK)**. 
- **Server Push**. 
- **HTTP/3**: Usando o protocolo **QUIC** (baseado em UDP), para ainda mais performance e confiabilidade, especialmente em redes instáveis. 

--- 
## 💻 Ferramentas e Prática ### 🔍 Inspecionando o HTTP 
- Uso das **DevTools** (Ferramentas do Desenvolvedor) do navegador. 
- Aba Network: Analisando requisições, respostas, cabeçalhos e timing. 
- Uso de ferramentas como **Postman** ou **Insomnia** para testar APIs e requisições HTTP.
---