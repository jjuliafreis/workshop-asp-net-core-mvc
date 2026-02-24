# SalesWebMvc - Informações sobre Vulnerabilidades

## ⚠️ Status Atual

Este projeto está atualmente configurado para **.NET Core 2.1**, que **chegou ao fim do suporte em 21 de agosto de 2021**.

## 🔒 Vulnerabilidades Conhecidas

O .NET Core 2.1 possui múltiplas vulnerabilidades de segurança conhecidas que **NÃO SERÃO CORRIGIDAS** pela Microsoft, incluindo:

### Vulnerabilidades Críticas:
- **GHSA-5rrx-jjjq-q2r5** (Kestrel.Core) - DoS vulnerability
- **GHSA-ghhp-997w-qr28** (Text.Encodings.Web) - XSS vulnerability

### Vulnerabilidades de Alta Severidade:
- **GHSA-hxrm-9w7p-39cc** (AspNetCore.Http)
- **GHSA-655q-9gvg-q4cm** (Http.Connections)
- **GHSA-6px8-22w5-w334** (Kestrel & WebSockets)
- **GHSA-vmch-3w2x-vhgq** (Kestrel.Transport.Sockets)
- **GHSA-5crp-9r3c-p9vr** (Newtonsoft.Json)
- **GHSA-98g6-xh36-x2p7** (System.Data.SqlClient)
- **GHSA-cmhx-cq75-c4mj** (System.Text.RegularExpressions)

### Vulnerabilidades Moderadas:
- Múltiplas vulnerabilidades em componentes do ASP.NET Core

## ✅ Ações Realizadas

1. **Atualizado a estrutura do projeto** para .NET Core 2.1 compatível:
   - Removido recursos não suportados (`Nullable`, `ImplicitUsings`)
   - Convertido `Program.cs` para a sintaxe do .NET Core 2.1
   - Criado `Startup.cs` com configuração adequada

2. **Adicionados pacotes atualizados** onde possível:
   - Newtonsoft.Json 13.0.1
   - System.Data.SqlClient 4.8.6
   - System.Text.Encodings.Web 4.7.2
   - System.Text.RegularExpressions 4.3.1

## 🚀 Recomendação Forte

**É ALTAMENTE RECOMENDADO atualizar para uma versão suportada do .NET:**

- **.NET 6 (LTS)** - Suporte até novembro de 2024
- **.NET 8 (LTS)** - Suporte até novembro de 2026 (RECOMENDADO)

### Benefícios da Atualização:

1. **Segurança**: Correções de vulnerabilidades e patches de segurança
2. **Performance**: Melhorias significativas de desempenho
3. **Recursos**: Novos recursos da linguagem e frameworks
4. **Suporte**: Suporte oficial da Microsoft

### Como Atualizar:

Para atualizar para .NET 8:
1. Alterar `<TargetFramework>` de `netcoreapp2.1` para `net8.0`
2. Atualizar pacotes NuGet
3. Ajustar código conforme necessário (geralmente mínimo)

## 📝 Nota

Enquanto o projeto permanecer no .NET Core 2.1:
- ⚠️ NÃO use em produção sem avaliar os riscos de segurança
- ⚠️ Considere a atualização como prioridade
- ⚠️ Implemente controles de segurança adicionais na infraestrutura

## 🔗 Referências

- [.NET Support Policy](https://dotnet.microsoft.com/platform/support/policy)
- [Migrating to .NET 8](https://learn.microsoft.com/dotnet/core/porting/)
- [Security Advisories](https://github.com/advisories)
