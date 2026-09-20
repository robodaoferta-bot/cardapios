# Cardápios Digitais — MandaProPai

Cada loja tem uma pasta com seu cardápio digital + imagens dos produtos.

## Estrutura

```
cardapios/
  pizzaria-fornalha/
    index.html          ← página do cardápio
    img/
      calabresa.jpg     ← fotos dos produtos (quadradas, ~600x600px)
      margherita.jpg
      ...
  outra-loja/
    index.html
    img/
      ...
```

## Como usar

1. Crie a pasta da loja: `mkdir -p nome-da-loja/img`
2. Copie o `index.html` da pizzaria-fornalha como modelo
3. Edite o objeto `CONFIG` no final do HTML com os produtos da loja
4. Coloque as fotos em `img/` (JPG, quadradas, ~600x600px, máx 200KB)
5. Faça git push — GitHub Pages publica automaticamente

## URLs das imagens para o bot

Depois de publicado, as imagens ficam em:
```
https://robodaoferta-bot.github.io/cardapios/nome-da-loja/img/produto.jpg
```

Essas URLs vão no campo `image_url` da tabela `store_products` no backoffice.
O bot envia a foto quando o cliente pergunta sobre o produto.

## Dicas para as fotos

- Formato quadrado (1:1), mínimo 600x600px
- JPG com qualidade 80% (boa aparência, tamanho pequeno)
- Fundo neutro, produto centralizado
- Máximo 200KB por imagem (WhatsApp comprime, não precisa HD)
