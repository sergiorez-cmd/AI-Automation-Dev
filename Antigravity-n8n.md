# Antigravity + n8n MCP + n8n server Ngrok

## 1° Faça o download do Antigravity para Linux no link oficial do Google 

https://antigravity.google/download

## 2° Crie uma pasta chamada de Antrigravity no diretório /home/seu_user e descompacte o arquivo dentro
```bash
tar -xvzf Antigravity.tar.gz 
```
## 3° Acessar o diretório do /home/seu_user/Antigravity/Antigravity-x64 e executar
```bash
./antigravity
```
https://antigravity.google/docs/getting-started

## 4° Faça autenticação com uma conta de Gmail

## 5° Agora vá para Workspace e crie uma pasta para seus projetos

## 6° Crie uma conta no Ngrok e configure o n8n

https://ngrok.com

https://ngrok.com/docs/gateway/examples/n8n

https://ngrok.com/use-cases/share-localhost

## 7° Agora utilize o prompt do Antigravity para configurar o n8n-MCP
```text
Me ajude a configurar este MCP https://github.com/czlonkowski/n8n-mcp
```
* Forneça o link e chave API do seu n8n

  https://your-n8n-instance.ngrok.app

  API n8n = "pc3MiOiJuOG4iLCJqdGkiOiI3NmNjZjA4My0yOTc5LTRhNDUtYjZiNC02MTZiMjIzMzAwNGEiLCJpY"
 
* Permita as configurações automatizadas até finalizar a configuração

* Para confirmar digite o prompt `gostaria de saber se há algum servidor mcp disponível e qual diretório esta alocado?`

* Ou verifique em `Customizations >> Installed`

---

Sim, atualmente há **1 servidor MCP** configurado e disponível:

### **`n8n-mcp`**
Permite interagir diretamente com instâncias do **n8n**, automatizando o ciclo de vida de fluxos e nós. 

**Principais capacidades disponíveis:**
* **Gestão de Workflows:** Criar, obter, atualizar, validar, testar e deletar workflows (`n8n_create_workflow`, `n8n_update_full_workflow`, `n8n_validate_workflow`, `n8n_test_workflow`, etc.).
* **Exploração de Nós e Templates:** Pesquisar nós, templates oficiais e da comunidade (`search_nodes`, `get_node`, `search_templates`, `get_template`).
* **Execuções e Auditoria:** Consultar histórico de execuções (`n8n_executions`), verificar a saúde da instância (`n8n_health_check`) e auditar boas práticas (`n8n_audit_instance`).
* **Credenciais e Pastas:** Gerenciar credenciais e organização de pastas (`n8n_manage_credentials`, `n8n_manage_folders`).

---

Ran list MCP server directory
Ran list n8n-mcp contents
Ran find files in antigravity appData
Ran check n8n-mcp binary link · Exited with code 2
Ran list workspace contents
Ran check .gemini directory
Ran check config directory
Ran check config subdirectories
Ran read project configs

O servidor MCP **`n8n-mcp`** está alocado nos seguintes diretórios do seu sistema:

### 1. Definições e Schemas das Ferramentas (Metadados do Antigravity)
* **Caminho:** `/home/seu_user/.gemini/antigravity/mcp/n8n-mcp/`
* **Conteúdo:** Contém os schemas JSON de cada ferramenta disponibilizada pelo servidor (ex.: `n8n_create_workflow.json`, `search_nodes.json`, `n8n_test_workflow.json`, etc.).

### 2. Binário / Executável
* **Link no Antigravity:** `/home/seu_user/.gemini/antigravity/bin/n8n-mcp`
* **Origem da instalação (Node/npm):** `/home/seu_user/.local/share/node/bin/n8n-mcp`

Caso precise de outros servidores MCP (como GitHub, Postgres, SQLite, Slack, Figma, etc.), eles podem ser configurados nas configurações de 
plugins/MCP ou através do Agent Marketplace. Se quiser configurar um novo, é só avisar!

---

* Para conferir sua cota semanal vá `Settings >> Models`

---

## 8° Criar um Atalho para o Antigravity

Criar um arquivo Antigravity.desktop e copiar para pasta de aplicações do Debian 13
```desktop
[Desktop Entry]
Version=1.0
Type=Application
Name=Antigravity
Comment=Executa o Antigravity
Exec=/home/seu_user/Antigravity/Antigravity-x64/antigravity
Icon=utilities-terminal
Terminal=true
Categories=Utility;
```

```bash
sudo cp -a Antigravity.desktop /usr/share/applications/
```
