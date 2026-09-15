# Consulta de Prêmios - 2026

Sistema web para consulta individual de prêmios por CPF. O colaborador informa seu CPF e visualiza apenas o seu próprio relatório de desempenho e premiação.

## 🔒 Segurança e privacidade

- Cada colaborador acessa **somente os seus próprios dados**.
- A autenticação é feita pela coluna **H da guia FDT** (CPF).
- O CPF é validado pelo algoritmo oficial (dígitos verificadores) antes da busca.
- Nenhum dado é enviado a servidores externos — todo o processamento acontece **no navegador** do usuário.

## 📋 Como usar

1. Coloque o arquivo `PREMIO.xlsx` na raiz do repositório.
2. Abra o `index.html` (via GitHub Pages ou localmente).
3. O colaborador digita o CPF no formato `000.000.000-00`.
4. O sistema carrega a planilha, localiza o colaborador e exibe o relatório.

## 📊 Estrutura da planilha

O arquivo `PREMIO.xlsx` deve conter as seguintes guias:

### `RELATORIO CONTROLADORIA`
| Coluna | Conteúdo |
|--------|----------|
| A | Índice de Retrabalho |
| B | Nome do Colaborador |
| C | Equipe |
| D–R | Métricas (Retrabalho, Produção, Dias, Valor, Resultado) |

### `FDT`
| Coluna | Conteúdo |
|--------|----------|
| C | Supervisor |
| D | Técnico (nome) |
| F | WhatsApp |
| **H** | **CPF** ← usado para autenticação |

### `TABELA DE METAS`
Contém os valores de premiação por equipe, nível e dias trabalhados.

## 🚀 Publicar no GitHub Pages

1. Crie um repositório no GitHub.
2. Faça upload dos arquivos: `index.html`, `README.md`, `PREMIO.xlsx`.
3. Vá em **Settings → Pages**.
4. Em **Source**, selecione `main` e a pasta `/ (root)`.
5. Salve. O link será algo como: `https://seu-usuario.github.io/seu-repo/`.

## ⚙️ Configuração

No `index.html`, altere o caminho da planilha se necessário:

```javascript
const ARQUIVO_PLANILHA = 'PREMIO.xlsx';
```

## 🎨 Funcionalidades

- ✅ Login por CPF com máscara e validação
- ✅ Consulta individual (cada um vê só o seu)
- ✅ Relatório detalhado com cards de Retrabalho, Produção e Resultados
- ✅ Detalhamento de Prêmio, Concessão e Meta não atingida
- ✅ Download do relatório em PDF
- ✅ Envio do resumo por WhatsApp (se cadastrado)

## 📱 Compatibilidade

Funciona em navegadores modernos (Chrome, Edge, Firefox, Safari) em desktop e mobile.

## 🔄 Atualização dos dados

Basta substituir o arquivo `PREMIO.xlsx` no repositório. A próxima consulta já trará os dados atualizados.

---

**Desenvolvido para uso interno — Gestão de Prêmios 2026**