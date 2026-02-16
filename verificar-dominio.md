# Verificação passo a passo: antirretico.thaciosiqueira.com.br

## Passo 1 — Site no Netlify
- [ ] Abrir https://antirretico.netlify.app/ (aba anônima ou outro dispositivo)
- Resultado: carrega? (sim = deploy OK; não = problema no deploy)

## Passo 2 — Domínio no Netlify
- [ ] Clicar no projeto **antirretico.thaciosiqueira.com.br** no dashboard
- [ ] Ir em **Domain management** (ou **Site configuration** → **Domains**)
- Anotar:
  - O domínio **antirretico.thaciosiqueira.com.br** está na lista?
  - Há avisos (DNS, certificado)?
  - Qual valor o Netlify pede para colocar no DNS? (ex.: CNAME → antirretico.netlify.app)

## Passo 3 — DNS no provedor do domínio
- [ ] Onde o domínio **thaciosiqueira.com.br** está registrado? (Registro.br, GoDaddy, Cloudflare, etc.)
- [ ] Abrir a área de **DNS** / **DNS Management** / **Zona DNS**
- [ ] Procurar registro para **antirretico** (subdomínio):
  - Deve existir: **CNAME** → **antirretico.netlify.app** (ou o que o Netlify indicar)
  - Ou, se o Netlify pedir A/ALIAS, anotar os valores

## Passo 4 — Teste no Terminal
Rodar e anotar o resultado:
```bash
curl -I https://antirretico.thaciosiqueira.com.br/ 2>&1
```

## Passo 5 — Cache / outro navegador
- [ ] Testar em aba anônima
- [ ] Ou em outro navegador / celular em 4G (sem Wi‑Fi da casa)

---
Quando tiver o resultado do **Passo 2** (o que aparece em Domain management) e, se possível, do **Passo 4** (saída do curl), envie e seguimos daí.
