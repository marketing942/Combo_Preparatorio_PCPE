# Combo Completo — PCPE

Página de venda do combo **Curso preparatório PCPE + Apostila + Caderno de questões +
Vade Mecum digital**, lançada com o edital da PCPE (1.315 vagas, provas em 7 e 14 de
março de 2027).

É o `comboPMPE2` (mesma estrutura, mesmo preço, Everton atrás dos tablets no hero)
com a identidade visual do `comboPCPE`: destaque azul das capas, giroflex
vermelho/azul na barra do topo, no fundo, no hero e na faixa de urgência, e brasão
da Polícia Civil. A parcela continua no vermelho de promoção (`--promo`).

**Fluxo:** clique no CTA → checkout direto, sem formulário.

| | Valor |
|---|---|
| Checkout | `https://checkout.cppem.com.br/pay/combo-curso-apostila-caderno-de-questoes-vade-mecum-pcpe` |
| Preço | De R$ 688,00 por R$ 537,90 (-22%) · até 12x de R$ 56,12* (cartão, com acréscimo) |
| `utm_campaign` de fallback | `combo_completo_pcpe` |
| Evento `iniciar_checkout` | `produto: combo_completo_pcpe`, `valor: 537.9` |
| Chave de origem no storage | `cppem_origem_combo_completo_pcpe` |
| Exit popup | `prefix: cppem_combo_completo_pcpe`, `origem: exit_popup_combo_completo_pcpe` |

O botão do hero mantém o id `IPEyzyfmJhKQEYIXAlZH` da regra de clique da PixelX.
Se a regra estiver presa a outro domínio/produto, precisa ser liberada aqui.

## Assets

- `combo.webp`, `combo-resumo.webp`, `combo-questoes.webp`, `combo-vade.webp`,
  `og-combo.jpg`, `brasao-pcpe.png`: copiados do `comboPCPE` (gerados lá por
  `_build_assets.py` a partir das capas originais)
- `everton-hero.webp` e `everton-mota.jpg`: os mesmos do `comboPMPE2`

## Checklist antes do disparo

- [ ] Preço conferido: R$ 537,90 · 12x R$ 56,12 (topo, hero, oferta, barra fixa e rodapé)
- [ ] Checkout abriu com UTMs e `external_id`
- [ ] Regra de clique da PixelX disparando neste domínio
- [ ] Popup de saída testado com `ExitPopup.show()`
