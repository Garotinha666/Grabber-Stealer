# Grabber/Stealer

## ⚠️ Aviso Legal

Este projeto é disponibilizado **exclusivamente para fins educacionais, acadêmicos e de pesquisa**.

O código demonstra técnicas relacionadas a:
- Análise de armazenamento local de dados
- Manipulação de chaves de criptografia
- Uso da API criptográfica do Windows (DPAPI)
- Inspeção de perfis de navegadores
- Processamento de arquivos locais

**Qualquer uso não autorizado deste código em sistemas, contas ou dispositivos sem permissão explícita é ilegal e antiético.**

Os autores e mantenedores **não se responsabilizam** por qualquer uso indevido deste material.

---

## 📌 Visão Geral do Projeto

Este projeto tem como objetivo demonstrar, em nível técnico, como determinadas aplicações desktop e navegadores baseados em Chromium armazenam dados criptografados localmente em sistemas Windows.

O código aborda conceitos como:
- Extração de chaves de criptografia a partir de arquivos `Local State`
- Descriptografia utilizando AES no modo GCM
- Varredura de diretórios e múltiplos perfis de usuário
- Uso de threads para paralelização
- Registro detalhado de logs
- Estrutura de envio de dados via webhook (conceitual)

A implementação é **específica para Windows** e utiliza APIs nativas do sistema operacional.

---

## 🧩 Dependências

Todas as dependências externas estão listadas no arquivo `requirements.txt`.

### Bibliotecas Externas
- **pycryptodome** – Implementação de algoritmos criptográficos (AES)
- **pywin32** – Acesso à DPAPI do Windows (`win32crypt`)

### Biblioteca Padrão do Python
Os seguintes módulos fazem parte da biblioteca padrão do Python e **não exigem instalação adicional**:
- os
- sys
- re
- json
- base64
- urllib
- datetime
- subprocess
- threading
- logging
- sqlite3
- time

---

## 🐍 Versão do Python

- Python **3.8 ou superior**
- Compatível até Python **3.12**

---

## 🖥️ Requisitos de Sistema

- **Sistema Operacional:** Windows 10 ou superior
- **Arquitetura:** x64
- **Variáveis de Ambiente Necessárias:**
  - `%APPDATA%`
  - `%LOCALAPPDATA%`

Esses requisitos são necessários devido ao uso da:
- DPAPI do Windows
- Estrutura de diretórios dos navegadores Chromium

---

## 📁 Estrutura do Projeto

```text
project/
│
├── main.py              # Lógica principal de análise
├── requirements.txt     # Dependências externas
└── README.md            # Documentação do projeto
