ï»¿# PêÂ­lulas de Ouro ê¢â¬â IA em projetos prêÂ¡ticos

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


Curso em portuguêÂªs no formato INEMA v2: **4 trilhas, 12 mêÂ³dulos, 72 têÂ³picos e 12 prêÂ¡ticas**. Inclui exemplos, exercêÂ­cios com conferêÂªncia, dois projetos de conclusêÂ£o, progresso de leitura, dêÂºvidas, grifos, anotaêÂ§êÂµes e exportaêÂ§êÂ£o da jornada.

[Abrir o curso](https://inematds.github.io/pilulasdeouro/) êÂ· [Materiais do aluno](https://inematds.github.io/pilulasdeouro/materiais/) êÂ· [Plano de projetos](PLANO-PROJETOS.md)

## Estudar

Comece pelos fundamentos ou escolha uma trilha no êÂ­ndice. Marque os têÂ³picos lidos e selecione trechos para grifar/anotar. O progresso fica no navegador: use **Minha jornada ê¢â â Exportar** para guardar uma cêÂ³pia ou mudar de dispositivo. Sem JavaScript, o conteêÂºdo permanece disponêÂ­vel para leitura.

A estimativa de sete horas inclui as prêÂ¡ticas; adapte o ritmo êÂ  sua experiêÂªncia. Os exemplos usam dados fictêÂ­cios. As ferramentas externas podem exigir instalaêÂ§êÂ£o ou conta prêÂ³pria.

## Editar e executar

Requer Python 3. O conteêÂºdo editorial estêÂ¡ em `conteudo/curso.json`; as pêÂ¡ginas sêÂ£o geradas, sem dependêÂªncias de build externas.

```bash
python3 scripts/gerar_curso.py
python3 scripts/verificar_curso.py
python3 -m http.server 8766
```

Abra `http://localhost:8766`. Edite textos no JSON, estrutura no gerador e apresentaêÂ§êÂ£o/interaêÂ§êÂµes em `assets/`. Regere as pêÂ¡ginas antes de commitar.

- `curso/`: êÂ­ndices das quatro trilhas e mêÂ³dulos completos.
- `materiais/`: fichas prêÂ¡ticas, CSV fictêÂ­cio e curso em Markdown.
- `assets/`: fontes locais, estilos e aprendizagem.
- `PLANO-PROJETOS.md`: portfêÂ³lio de 12 projetos propostos; implementaêÂ§êÂµes futuras.
- `PRODUCT.md` e `DESIGN.md`: decisêÂµes de produto e interface.

## PublicaêÂ§êÂ£o e privacidade

GitHub Pages publica a raiz da branch `main` deste repositêÂ³rio. O curso e seus materiais editoriais ficam versionados aqui. Materiais privados de preparaêÂ§êÂ£o em `down/`, mêÂ­dias, transcriêÂ§êÂµes e ferramentas de coleta sêÂ£o excluêÂ­dos pelo `.gitignore` e nêÂ£o fazem parte da publicaêÂ§êÂ£o.

A licenêÂ§a da fonte Inter acompanha os arquivos em `assets/inter-LICENSE.txt`.

<!-- inema-backlink:v1 -->
## Mais no INEMA.CLUB

- [Ficha completa deste curso](https://www.inema.club/cursos/275-pilulas-de-ouro-ia-em-projetos-praticos/)
- [Guia: como aprender inteligêÂªncia artificial](https://www.inema.club/aprender-inteligencia-artificial/)
- [Todos os cursos](https://www.inema.club/cursos/)
<!-- /inema-backlink:v1 -->

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>