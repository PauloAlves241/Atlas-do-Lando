# Atlas Cartográfico do Império do Lando e Laucidônia

Site estático, responsivo e compatível com GitHub Pages, construído a partir do mapa provincial de 2023 fornecido ao projeto.

## Sistema de coordenadas landesas

- Marco zero: **Sefante**, capital da província de Erena.
- Posição no mapa-base: pixel X 838, Y 637.
- Longitude positiva: leste de Sefante.
- Longitude negativa: oeste de Sefante.
- Latitude positiva: norte de Sefante.
- Latitude negativa: sul de Sefante.
- Escala operacional: 10 pixels por grau landês e 4 km por pixel, isto é, 40 km por grau.

A escala foi definida como uma configuração operacional inicial. Para alterá-la, edite as constantes `PX_PER_DEG` e `KM_PER_PX` em `assets/js/app.js`, além dos valores equivalentes em `data/metadata.json`.

## Recursos

- Navegação por arraste, zoom por roda, toque e gesto de pinça.
- Pesquisa por cidade, província, Estado, região ou atividade econômica.
- 59 capitais continentais georreferenciadas sobre o mapa-base.
- Diretório das 62 divisões territoriais presentes na base de dados, incluindo ultramarinas.
- Dados de população, área, densidade, IDH, educação, infraestrutura, desemprego, municípios, freguesias, economia e composição setorial do PIB.
- Sefante destacado como marco zero.
- Grade, eixos, coordenadas em graus, minutos e segundos e conversor de coordenadas.
- Cálculo de rotas cartográficas e estimativas por modal.
- Medição livre entre dois pontos.
- Favoritos e marcadores pessoais salvos no navegador.
- Tema claro e escuro.
- URLs compartilháveis por lugar.
- Instalação como PWA e cache básico para uso posterior sem conexão.
- Interface adaptada a computador e celular.

## Publicação no GitHub Pages

1. Envie todos os arquivos desta pasta para a raiz do repositório.
2. No GitHub, abra **Settings > Pages**.
3. Em **Build and deployment**, escolha **Deploy from a branch**.
4. Selecione a branch principal e a pasta `/ (root)`.
5. Salve e aguarde a publicação.

Não abra o `index.html` diretamente por `file://`, porque os navegadores bloqueiam o carregamento dos arquivos JSON nesse modo. Para testar no computador, execute:

```bash
python -m http.server 8000
```

Depois acesse `http://localhost:8000`.

## Arquivos principais

- `index.html`: estrutura da interface.
- `assets/css/styles.css`: identidade visual e responsividade.
- `assets/js/app.js`: motor cartográfico e ferramentas.
- `data/provincias.json`: atlas provincial completo.
- `data/metadata.json`: metadados do país, mapa e coordenadas.
- `sw.js`: cache da aplicação.
- `manifest.webmanifest`: instalação como aplicativo web.

## Precisão cartográfica

Os marcadores foram posicionados sobre a imagem fornecida e constituem uma primeira georreferenciação do mapa raster. Como o arquivo original não possui geometrias vetoriais nem coordenadas oficiais, as posições devem ser revisadas futuramente caso seja criado um mapa SVG ou GeoJSON oficial. As províncias ultramarinas permanecem no diretório, mas não aparecem neste mapa continental.
