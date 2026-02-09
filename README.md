# 📞 Ramais Realtime

Sistema de ramais em tempo real para visualização estruturada e busca rápida por departamentos e colaboradores.

---

## 🚀 Visão Geral

Este projeto é uma solução web em **tempo real** para consulta de ramais internos, desenvolvida com:

- **Frontend:** HTML + CSS + JavaScript
- **Backend:** Python (Flask)
- **Banco de dados:** MySQL
- **Comunicação em tempo real:** WebSocket
- **Busca:** Dinâmica por nome, departamento ou ramal

---

## 🗂️ Estrutura de Pastas

```
ramais-realtime/
│
├── templates/
│   └── index.html              # Página principal
├── static/
│   ├── style.css               # Estilos (tema HBR)
│   └── app.js                  # Lógica frontend com WebSocket
│
├── app.py                       # Aplicação Flask principal
├── requirements.txt             # Dependências Python
├── .env.example                 # Exemplo de configuração
├── pyvenv.cfg                   # Configuração do ambiente virtual
├── .gitignore                   # Arquivos ignorados pelo Git
├── README.md                    # Este arquivo
│
└── docs/                        # Documentação adicional
    ├── ARQUITETURA.md
    ├── BANCO_DADOS.md
    └── API.md
```

---

## ⚡ Início Rápido

### 1. Clone o repositório

```bash
git clone https://github.com/duarteaarthur2004/ramais-realtime.git
cd ramais-realtime
```

### 2. Configure o ambiente virtual

```bash
# Linux / macOS
python3 -m venv .venv
source .venv/bin/activate

# Windows
python -m venv .venv
.venv\Scripts\activate
```

### 3. Instale as dependências

```bash
pip install -r requirements.txt
```

### 4. Configure o banco de dados

Edite as credenciais no arquivo `.env`:

```bash
cp .env.example .env
# Edite .env com suas credenciais MySQL
```

### 5. Crie as tabelas no MySQL

Execute o script SQL em `docs/BANCO_DADOS.md` no seu banco MySQL.

### 6. Rode a aplicação

```bash
python app.py
```

A aplicação estará disponível em: **http://localhost:5000**

---

## 🕸️ Endpoints

| Método | Endpoint          | Descrição                                    |
|--------|-------------------|---------------------------------------------|
| GET    | `/`               | Página principal (HTML)                      |
| GET    | `/api/ramais/sp`  | Lista de ramais (base São Paulo)             |
| WS     | `/ws`             | WebSocket para atualizações em tempo real    |

---

## 🔍 Funcionalidades

✅ **Busca em tempo real** - Filtra por nome, departamento ou ramal  
✅ **Atualizações ao vivo** - WebSocket sincroniza mudanças instantaneamente  
✅ **Agrupamento por setor** - Organiza visualmente os ramais por departamento  
✅ **Responsivo** - Funciona perfeitamente em desktop e mobile  
✅ **Status de conexão** - Exibe status de conexão com o servidor  

---

## 📊 Exemplo de Dados

```
Setor: Comercial
├─ João Silva (1010)
├─ Maria Souza (1015)
└─ Pedro Costa (1020)

Setor: Financeiro
├─ Ana Martins (2010)
├─ Carlos Mendes (2015)
└─ Lucia Ferreira (2020)

Setor: RH
├─ Roberto Santos (3010)
└─ Fernanda Oliveira (3015)
```

---

## 🛠️ Stack Tecnológico

### Frontend
- HTML5
- CSS3 (com tema HBR)
- JavaScript vanilla (sem frameworks)
- WebSocket (built-in)

### Backend
- Python 3.13
- Flask
- Flask-SocketIO (WebSocket)
- mysql-connector-python (ou MySQLdb)

### Banco de Dados
- MySQL 5.7+

---

## 🔐 Variáveis de Ambiente

Crie um arquivo `.env` na raiz do projeto:

```env
# Banco de Dados MySQL
MYSQL_HOST=localhost
MYSQL_USER=seu_usuario
MYSQL_PASSWORD=sua_senha
MYSQL_DATABASE=ramais_db

# Flask
FLASK_ENV=production
FLASK_DEBUG=False
SECRET_KEY=sua-chave-secreta

# Servidor
HOST=0.0.0.0
PORT=5000
```

---

## 📝 Como Contribuir

1. **Fork** este repositório
2. **Crie uma branch** para sua feature: `git checkout -b feature/minha-feature`
3. **Commit** suas mudanças: `git commit -m 'feat: adicionar minha feature'`
4. **Push** para sua branch: `git push origin feature/minha-feature`
5. **Abra um Pull Request**

---

## 📚 Documentação Detalhada

Veja mais informações nos arquivos:

- 🏗️ [Arquitetura do Sistema](docs/ARQUITETURA.md)
- 🗄️ [Estrutura do Banco de Dados](docs/BANCO_DADOS.md)
- 🔌 [Documentação da API](docs/API.md)

---

## 📞 Suporte

Para dúvidas ou problemas, abra uma **Issue** no repositório.

---

## 📄 Licença

Este projeto é proprietário da HBR Aviação. Todos os direitos reservados © 2025.

---

**Desenvolvido com ❤️ por Arthur Duarte**
