# PÃ­lulas de Ouro â€” IA em projetos prÃ¡ticos

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


Curso em portuguÃªs no formato INEMA v2: **4 trilhas, 12 mÃ³dulos, 72 tÃ³picos e 12 prÃ¡ticas**. Inclui exemplos, exercÃ­cios com conferÃªncia, dois projetos de conclusÃ£o, progresso de leitura, dÃºvidas, grifos, anotaÃ§Ãµes e exportaÃ§Ã£o da jornada.

[Abrir o curso](https://inematds.github.io/pilulasdeouro/) Â· [Materiais do aluno](https://inematds.github.io/pilulasdeouro/materiais/) Â· [Plano de projetos](PLANO-PROJETOS.md)

## Estudar

Comece pelos fundamentos ou escolha uma trilha no Ã­ndice. Marque os tÃ³picos lidos e selecione trechos para grifar/anotar. O progresso fica no navegador: use **Minha jornada â†’ Exportar** para guardar uma cÃ³pia ou mudar de dispositivo. Sem JavaScript, o conteÃºdo permanece disponÃ­vel para leitura.

A estimativa de sete horas inclui as prÃ¡ticas; adapte o ritmo Ã  sua experiÃªncia. Os exemplos usam dados fictÃ­cios. As ferramentas externas podem exigir instalaÃ§Ã£o ou conta prÃ³pria.

## Editar e executar

Requer Python 3. O conteÃºdo editorial estÃ¡ em `conteudo/curso.json`; as pÃ¡ginas sÃ£o geradas, sem dependÃªncias de build externas.

```bash
python3 scripts/gerar_curso.py
python3 scripts/verificar_curso.py
python3 -m http.server 8766
```

Abra `http://localhost:8766`. Edite textos no JSON, estrutura no gerador e apresentaÃ§Ã£o/interaÃ§Ãµes em `assets/`. Regere as pÃ¡ginas antes de commitar.

- `curso/`: Ã­ndices das quatro trilhas e mÃ³dulos completos.
- `materiais/`: fichas prÃ¡ticas, CSV fictÃ­cio e curso em Markdown.
- `assets/`: fontes locais, estilos e aprendizagem.
- `PLANO-PROJETOS.md`: portfÃ³lio de 12 projetos propostos; implementaÃ§Ãµes futuras.
- `PRODUCT.md` e `DESIGN.md`: decisÃµes de produto e interface.

## PublicaÃ§Ã£o e privacidade

GitHub Pages publica a raiz da branch `main` deste repositÃ³rio. O curso e seus materiais editoriais ficam versionados aqui. Materiais privados de preparaÃ§Ã£o em `down/`, mÃ­dias, transcriÃ§Ãµes e ferramentas de coleta sÃ£o excluÃ­dos pelo `.gitignore` e nÃ£o fazem parte da publicaÃ§Ã£o.

A licenÃ§a da fonte Inter acompanha os arquivos em `assets/inter-LICENSE.txt`.

<!-- inema-backlink:v1 -->
## Mais no INEMA.CLUB

- [Ficha completa deste curso](https://www.inema.club/cursos/275-pilulas-de-ouro-ia-em-projetos-praticos/)
- [Guia: como aprender inteligÃªncia artificial](https://www.inema.club/aprender-inteligencia-artificial/)
- [Todos os cursos](https://www.inema.club/cursos/)
<!-- /inema-backlink:v1 -->

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>