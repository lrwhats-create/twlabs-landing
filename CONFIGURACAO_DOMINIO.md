# TWLabs.ai - Configuração de Domínio

> Documentação completa da configuração do domínio twlabs.ai
> Última atualização: 2026-01-06

---

## 📋 Informações Gerais

| Item | Valor |
|------|-------|
| **Domínio Principal** | twlabs.ai |
| **Domínio com WWW** | www.twlabs.ai |
| **Plataforma de Hospedagem** | Cloudflare Pages |
| **Canonical URL** | https://twlabs.ai/ |
| **Status** | ✅ Ativo e Funcionando |

---

## 🌐 Configuração DNS (Cloudflare)

### Registros DNS Configurados:

| Tipo | Nome | Conteúdo | Proxy | TTL |
|------|------|----------|-------|-----|
| **CNAME** | twlabs.ai | twlabs.pages.dev | ✅ Proxied | Auto |
| **CNAME** | www | twlabs.pages.dev | ✅ Proxied | Auto |
| **MX** | @ | route1.mx.cloudflare.net (78) | ❌ DNS only | Auto |
| **MX** | @ | route2.mx.cloudflare.net (99) | ❌ DNS only | Auto |
| **MX** | @ | route3.mx.cloudflare.net (55) | ❌ DNS only | Auto |
| **TXT** | @ | v=spf1 include:_spf.mx.cloudflare.net ~all | ❌ DNS only | Auto |
| **TXT** | _dmarc | v=DMARC1; p=none; | ❌ DNS only | 1 hr |
| **TXT** | @ | google-site-verification=... | ❌ DNS only | 1 hr |
| **CNAME** | cf2024-1._domainkey | [DKIM record] | ❌ DNS only | Auto |

**Total de Registros DNS**: 10

---

## 🚀 Cloudflare Pages - Custom Domains

### Domínios Configurados:

| Domínio | Status | SSL | Configuração |
|---------|--------|-----|--------------|
| **twlabs.ai** | ✅ Active | ✅ Enabled | Domínio principal |
| **www.twlabs.ai** | ✅ Active | ✅ Enabled | Subdomínio www |

### URL do Projeto Pages:
- `twlabs.pages.dev`

---

## 📄 SEO e Indexação

### Sitemap
- **URL**: https://twlabs.ai/sitemap.xml
- **Última modificação**: 2026-01-05
- **Frequência de atualização**: monthly
- **Prioridade**: 1.0

### Tag Canonical
```html
<link rel="canonical" href="https://twlabs.ai/">
```

### Google Search Console
- **Propriedade**: sc-domain:twlabs.ai
- **Status de Indexação**: ✅ URLs indexados
- **Última solicitação de indexação**: 2026-01-05
  - https://twlabs.ai/ - ✅ Indexado
  - https://www.twlabs.ai/ - ✅ Indexação solicitada

---

## 📧 Configuração de Email (Cloudflare Email Routing + Purelymail)

### Contas de Email Criadas:
1. **brain@twlabs.ai** - Email principal
2. **lt@twlabs.ai** - Email secundário
3. **mj@twlabs.ai** - Email secundário

### Registros DNS de Email:
- ✅ MX records configurados (Cloudflare)
- ✅ SPF configurado
- ✅ DMARC configurado
- ✅ DKIM configurado

### Provedor de Email:
- **Serviço**: Purelymail
- **Credenciais**: Ver `/media/twrs/4TB/TWLabs.ai/.credentials/PURELYMAIL_CREDENTIALS.md`

---

## ✅ Status de Verificação

### Testes Realizados (2026-01-05/06):

| Teste | Status | Observações |
|-------|--------|-------------|
| **DNS CNAME www** | ✅ Pass | Registro configurado corretamente |
| **Custom Domain Pages** | ✅ Pass | Ativo com SSL habilitado |
| **Acesso via www.twlabs.ai** | ✅ Pass | Site carrega corretamente |
| **Acesso via twlabs.ai** | ✅ Pass | Site carrega corretamente |
| **Redirecionamento HTTPS** | ✅ Pass | Automático via Cloudflare |
| **SSL/TLS** | ✅ Pass | Certificado válido |
| **Sitemap acessível** | ✅ Pass | https://twlabs.ai/sitemap.xml |
| **Google Search Console** | ✅ Pass | Indexação solicitada com sucesso |

---

## 🔧 Resolução de Problemas

### Problema Original:
**Google Search Console** reportou erro de redirecionamento para www.twlabs.ai

### Causa Raiz:
- CNAME DNS `www` estava faltando
- Custom Domain `www.twlabs.ai` não estava registrado no Cloudflare Pages

### Solução Implementada:
1. ✅ Adicionado CNAME `www → twlabs.pages.dev` no DNS Cloudflare
2. ✅ Adicionado `www.twlabs.ai` como Custom Domain no Cloudflare Pages
3. ✅ Atualizado sitemap.xml com data 2026-01-05
4. ✅ Solicitada re-indexação no Google Search Console

### Data da Correção:
**2026-01-05**

---

## 📊 Informações Técnicas

### Cloudflare Account ID:
```
869651ccbc0e109d72a363c9ca7a0aa5
```

### Zone ID (twlabs.ai):
```
e9f94cae71dfbac99ce1e3bad69f7e08
```

### Nameservers Cloudflare:
- `carlos.ns.cloudflare.com`
- `vicki.ns.cloudflare.com`

---

## 📝 Histórico de Alterações

| Data | Alteração | Responsável |
|------|-----------|-------------|
| 2026-01-05 | Configuração inicial do domínio | Claude Code |
| 2026-01-05 | Correção www: DNS CNAME + Custom Domain | Claude Code |
| 2026-01-05 | Atualização sitemap lastmod | Claude Code |
| 2026-01-05 | Solicitação indexação Google | Claude Code |

---

## 🔗 Links Úteis

- **Site Principal**: https://twlabs.ai
- **Site com WWW**: https://www.twlabs.ai
- **Sitemap**: https://twlabs.ai/sitemap.xml
- **Cloudflare Dashboard**: https://dash.cloudflare.com/869651ccbc0e109d72a363c9ca7a0aa5/twlabs.ai
- **Cloudflare Pages**: https://dash.cloudflare.com/869651ccbc0e109d72a363c9ca7a0aa5/pages/view/twlabs
- **Google Search Console**: https://search.google.com/search-console?resource_id=sc-domain:twlabs.ai

---

## ⚠️ Notas Importantes

1. **Canonical URL**: Sempre usar `https://twlabs.ai/` (sem www) como canonical
2. **Redirecionamento**: www.twlabs.ai funciona mas canonical aponta para versão sem www
3. **DNS Propagação**: Alterações DNS podem levar até 48h para propagar globalmente
4. **Indexação Google**: Solicitações de indexação são processadas em fila prioritária
5. **Credenciais Email**: NUNCA commitar arquivos .credentials/ no Git

---

**Documentação gerada automaticamente por Claude Code**
