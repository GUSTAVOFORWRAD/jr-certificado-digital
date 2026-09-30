# Certificado Digital — JR Serviços Empresariais

Landing page de captação para venda de **certificados digitais Valid (ICP-Brasil)** — e-CPF e e-CNPJ, nas mídias A1, A3 e nuvem.

🔗 **Site:** https://gustavoforwrad.github.io/jr-certificado-digital/

---

## Objetivo

Gerar contato qualificado no WhatsApp. Toda a página converge para o formulário de cadastro, que monta a mensagem automaticamente e abre a conversa já preenchida com o nome, o tipo de certificado e a mídia escolhida.

**Diferencial de venda:** para emitir um certificado, o CPF/CNPJ precisa estar regular na Receita Federal. Como a JR também é contabilidade, ela regulariza a pendência e emite no mesmo atendimento — algo que uma revenda comum não faz.

## Estrutura da página

1. **Herói** — proposta de valor + cartão do certificado com a marca V/Cert
2. **e-CPF ou e-CNPJ** — qualificação do tipo de certificado
3. **A1 ou A3** — comparativo de mídia, validade e uso
4. **Diferenciais** — regularização + emissão no mesmo atendimento
5. **Cadastro** — formulário que leva ao WhatsApp
6. **Dúvidas frequentes**
7. **Chamada final**

## Detalhes técnicos

- **HTML único, sem dependências.** Nenhum framework, nenhum build. É só abrir o `index.html`.
- **Imagens embutidas** em base64 — a página não depende de nenhum servidor de imagens.
- **Duas versões de cor** (branca e azul), alternáveis pelos botões no menu. A escolha fica salva no navegador.
- **Fontes:** Be Vietnam Pro + IBM Plex Mono (Google Fonts).
- **Acessibilidade:** foco visível por teclado, textos alternativos nas imagens e respeito total à preferência de "reduzir movimento" do sistema.

### Desempenho

As animações foram construídas para não travar o scroll:

- Sem `filter: blur()` animado e sem `backdrop-filter` (os dois maiores causadores de travamento).
- A barra de progresso usa `transform` em vez de `width`, evitando recálculo de layout.
- O scroll é sincronizado com a taxa de atualização da tela (`requestAnimationFrame`).
- As animações do herói **pausam automaticamente** quando saem da tela.

## Como alterar o WhatsApp

O número fica em um único lugar, no `<script>` no final do `index.html`:

```js
var WHATSAPP = "5561981301069";   // 55 + DDD + número, só dígitos
```

Esse número alimenta todos os pontos de contato: menu, botão flutuante, formulário e chamada final.

## Hospedagem

Publicado via **GitHub Pages** a partir da branch `main`, pasta `/ (root)`. Qualquer alteração enviada para a `main` entra no ar automaticamente em poucos minutos.

---

Revenda autorizada de certificados digitais **Valid (ICP-Brasil)**. As marcas Valid e V/Cert pertencem à Valid Soluções S.A.
