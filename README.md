# Clínica Força & Movimento — Site institucional

Site institucional em página única (single-page) para a Clínica Força & Movimento, clínica de fisioterapia em Penha de França, São Paulo.

## Como usar

Não é necessário instalar nada. Basta abrir o arquivo `index.html` diretamente no navegador (duplo clique) ou hospedar a pasta inteira em qualquer serviço de hospedagem estática (GitHub Pages, Netlify, Vercel, Hostgator, etc.).

## Estrutura de arquivos

```
Forca_e_Movimento/
│
├── index.html      → estrutura e conteúdo do site
├── style.css        → todo o design (cores, tipografia, responsividade, animações)
├── script.js         → menu mobile, scroll do header, revelar seções, FAQ (accordion)
├── assets/
│   ├── logo.png              → logotipo oficial (fundo removido, transparente)
│   ├── clinica-1.jpg         → foto real: consultório com o logo na parede
│   ├── clinica-2.jpg         → foto real: atendimento guiado na sala de tratamento
│   ├── clinica-3.jpg         → foto real: exercício de equilíbrio na sala de equipamentos
│   ├── clinica-4.jpg         → foto real: exercício com faixa elástica no espaldar
│   ├── treat-manual.jpg      → foto real: terapia manual (card "Terapia manual")
│   ├── treat-carga.jpg       → foto real: exercício com carga (card "Exercícios com e sem carga")
│   └── treat-pliometrico.jpg → foto real: exercício de equilíbrio (card "Exercícios pliométricos")
└── README.md
```

## O que já está pronto

- Header fixo com menu responsivo (hamburger no mobile), com o logo sem fundo
- Seção hero com o logo posicionado ao lado do título, CTA direto para o WhatsApp
- Seção "Clínica" com galeria de fotos reais do espaço, "Tratamentos", "Como funciona", "Benefícios"
- Banner de agendamento
- FAQ em accordion
- CTA para o Instagram
- Seção de contato com mapa (Google Maps embutido sem necessidade de chave de API)
- Seção "Avaliações no Google" com link direto para o perfil real da clínica no Google
- Botão flutuante de WhatsApp com mensagens pré-preenchidas diferentes por contexto
- Design responsivo mobile-first, com paleta extraída diretamente do logo (`#193064` navy, `#83A83F` verde, `#DD7D2F` laranja)

## Sobre a seção "Avaliações no Google"

Aqui vale uma explicação importante: um site estático em HTML/CSS/JS (sem backend, sem chave de API, como foi pedido no início do projeto) **não consegue puxar e atualizar avaliações do Google sozinho** — isso exige a Google Places API (paga, com chave própria) ou um widget de terceiros (ex: Elfsight, Trustindex, EmbedSocial), que também precisa de uma conta e uma chave/script embutido.

Por isso, o que foi implementado é uma seção que **linka diretamente para o perfil real da clínica no Google**, onde as avaliações aparecem sempre atualizadas e em tempo real — sem custo, sem chave de API e sem depender de terceiros. Também não incluí nenhuma avaliação individual "escrita" no site, porque o Google não permite raspar o texto das avaliações, e forjar avaliações não é uma opção.

Se no futuro você quiser um carrossel de avaliações embutido de fato (mostrando o texto direto no site), a forma correta é:
1. Criar uma conta gratuita em um serviço como Trustindex ou Elfsight;
2. Conectar o perfil do Google da clínica;
3. Colar o pequeno script/embed que eles fornecem no lugar da seção `#avaliacoes` do `index.html`.

## Sobre as imagens

- `logo.png`: o fundo foi removido digitalmente (recorte automático), deixando apenas o logotipo em PNG transparente — usado no header, no hero e no rodapé.
- `clinica-1.jpg` a `clinica-4.jpg`, `treat-manual.jpg`, `treat-carga.jpg`, `treat-pliometrico.jpg`: fotos reais em boa resolução, distribuídas entre a galeria da seção "Clínica" e os cards da seção "Tratamentos" (apenas nos 3 tratamentos em que havia uma foto correspondente ao conteúdo — Alongamentos e Eletroanalgesia continuam só com ícone, para não ilustrar com uma foto que não representa o tratamento). Mantidas com a mínima compressão necessária para o site carregar rápido, sem upscaling artificial.
- Uma das 8 fotos enviadas (o infográfico "Alívio da dor e mais qualidade de vida") não foi usada no site: é uma peça de marketing pronta, com título e legendas próprias, e ficaria com uma identidade visual diferente do restante do site. Guarde o arquivo original à parte caso queira usá-la em outro canal (Instagram, por exemplo) — é só pedir se quiser que eu a inclua em algum lugar específico do site.

## Pontos marcados para preenchimento posterior

Alguns campos foram deixados como placeholder porque a informação não foi fornecida. Procure por `[INSERIR...]` no arquivo `index.html`:

- Detalhes completos sobre como é feita a avaliação inicial (pergunta do FAQ)

Não foram inventados nomes de profissionais, CREFITO, convênios, horários de funcionamento, preços ou depoimentos de pacientes — adicione essas informações quando desejar.

## Personalização rápida

- **Trocar/adicionar fotos da clínica:** substitua os arquivos em `assets/clinica-1.jpg`, `clinica-2.jpg` e `clinica-3.jpg` mantendo o mesmo nome, ou edite o bloco `.clinic-gallery` no `index.html` para usar outros nomes de arquivo.
- **Cores:** todas as cores estão centralizadas no topo do `style.css`, dentro de `:root`.
- **Mensagens do WhatsApp:** os links já usam `https://wa.me/5511984463495?text=...` com mensagens diferentes para agendamento e para dúvidas gerais.
