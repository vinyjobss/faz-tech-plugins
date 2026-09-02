# faz-tech-plugins

Marketplace pessoal de plugins do Claude Code para a Faz Tech.

## Plugins disponíveis

### coordenador-ti

Coordenador de Operações de TI: transforma demandas brutas (incidentes, projetos, ideias) em tarefas estruturadas, delegadas e priorizadas no Todoist, via MCP.

Inclui:
- Subagente `coordenador-ti` (invocado automaticamente pelo Claude quando você reporta uma demanda de TI, ou explicitamente).
- Comando `/coordenador-ti:coordenador [descrição da demanda]`.
- Configuração do servidor MCP do Todoist (pacote `todoist-mcp`).

## Como instalar

1. No Claude Code, abra o Diretório de plugins e clique em **Adicionar marketplace**.
2. Informe o repositório: `vinyjobss/faz-tech-plugins`.
3. Depois de sincronizar, instale o plugin **coordenador-ti**.
4. Antes de usar, defina a variável de ambiente `TODOIST_API_KEY` com sua chave de API do Todoist (o valor **não** fica commitado no repositório — veja `plugins/coordenador-ti/.mcp.json`, que usa `${TODOIST_API_KEY}`):

   ```powershell
   $env:TODOIST_API_KEY = "sua-chave-aqui"
   ```

   Para persistir entre sessões, defina como variável de ambiente do usuário no Windows (Configurações > Variáveis de Ambiente) em vez de exportar a cada sessão.
