# Sistema de Coordenadas Landesas de Sefante

## 1. Origem

O ponto fundamental do sistema é a cidade de **Sefante**, capital da província de Erena. No mapa raster fornecido, o marco foi fixado em:

- X: 838 pixels
- Y: 637 pixels
- Latitude landesa: 0°
- Longitude landesa: 0°

## 2. Orientação

- O norte possui latitude positiva.
- O sul possui latitude negativa.
- O leste possui longitude positiva.
- O oeste possui longitude negativa.

## 3. Conversão

O atlas utiliza a convenção operacional de 10 pixels por grau landês:

```text
longitude = (X − 838) ÷ 10
latitude  = (637 − Y) ÷ 10
```

A conversão inversa é:

```text
X = 838 + longitude × 10
Y = 637 − latitude × 10
```

## 4. Escala de distância

A primeira versão adota 4 km cartográficos por pixel, equivalentes a 40 km por grau landês. A distância direta entre dois pontos é calculada no plano do mapa:

```text
distância = √((X₂ − X₁)² + (Y₂ − Y₁)²) × 4 km
```

Essa escala é operacional e pode ser recalibrada posteriormente, sobretudo quando houver uma definição oficial da projeção, da extensão continental e das geometrias vetoriais do Império.

## 5. Precisão

O mapa-base é uma imagem raster sem metadados geográficos. Os marcadores das capitais foram posicionados visualmente sobre os símbolos existentes no arquivo. Assim, o sistema já é coerente e funcional para navegação, buscas, rotas e referências internas, mas ainda não constitui um levantamento geodésico definitivo.
