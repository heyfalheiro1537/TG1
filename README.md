# Template Thesis ITA

Template LaTeX para Trabalhos Acadêmicos do Instituto Tecnológico de Aeronáutica (ITA)  
Adaptado para Overleaf | Conforme ABNT NBR 6023:2018

## Quick Start

1. Configure o tipo de documento no `tese.tex`
2. Preencha suas informações pessoais 
3. Edite os capítulos nas respectivas pastas
4. Compile com pdfLaTeX

## Tipos de Documento

**Principais:**
- `[tg]` / `[tgfem]` - Trabalho de Graduação
- `[msc]` / `[mscfem]` - Dissertação de Mestrado  
- `[dsc]` / `[dscfem]` - Tese de Doutorado
- `[quali]` / `[qualifem]` - Exame de Qualificação
- `[report]` - Relatório de Seminário de Tese

**Opções adicionais:**
- `[eng]` - Documento em inglês
- `[dv]` - Versão preliminar com data no rodapé

**Exemplo:** `\documentclass[dsc, eng, dv]{ita}`

## Estrutura do Projeto

```
template-thesis-ita/
├── tese.tex                    # Arquivo principal
├── ita.cls                     # Classe do documento
├── PreTextuais/                # Resumo, abstract, listas
├── Cap1/, Cap2/, Cap3/...      # Capítulos
├── References/referencias.bib   # Bibliografia
├── ApeA/, AneA/               # Apêndices e anexos (opcionais)
└── Figures/                   # Figuras gerais
```

## Configuração Principal

No arquivo `tese.tex`, configure:

```latex
% Tipo de documento
\documentclass[report]{ita}

% Informações pessoais
\course{Aeronautical Infrastructure Engineering}
\area{Air Transport and Airports}
\author{Name}{LastName}
\title{Title of the Research/Thesis}

% Orientador
\advisor{Prof.~Dr.}{Name}{ITA}

% Para relatórios, configure também:
\newcommand{\student}{Student Name}
\newcommand{\degr}{Master's Degree Candidate}
\newcommand{\advisors}{Prof. Dr. Name}
\newcommand{\semreg}{2nd}
```

## Características Especiais

### Capítulos Condicionais
- **Updates** e **Schedule**: Aparecem automaticamente em documentos `[report]`
- Outros capítulos seguem estrutura padrão de tese/dissertação

### Suporte Bilíngue
- Detecção automática do idioma
- Títulos e formatação adaptados (PT/EN)
- Configuração de referências bibliográficas

### Elementos Opcionais
- Apêndices e anexos podem ser comentados se não utilizados
- Listas de abreviaturas e símbolos em `PreTextuais/`
- Glossário disponível (comentado por padrão)

## Compilação

**Overleaf:** Configure para pdfLaTeX e compile  
**Local:** 
```bash
pdflatex tese.tex
bibtex tese
pdflatex tese.tex  
pdflatex tese.tex
```

## Dicas Importantes

1. **Figuras:** Coloque em pastas específicas dos capítulos
2. **Referências:** Use formato BibTeX em `References/referencias.bib`
3. **Idioma:** Para trabalhos em inglês, use `[eng]` e preencha dados em inglês
4. **Banca:** Configure membros da banca no `tese.tex`
5. **Palavras-chave:** Defina com `\kwcip{}` para a ficha catalográfica

## Pacotes Principais

- `longtable`, `booktabs` - Tabelas
- `subcaption`, `graphicx` - Figuras
- `amsmath`, `amssymb` - Matemática
- `hyperref` - Links clicáveis
- `mathptmx` - Times New Roman

## Problemas Comuns

**Referências não aparecem:** Execute bibtex após primeira compilação  
**Erro de compilação:** Rode BUILD OUTPUT novamente após alterar classe do documento  
**Caracteres especiais:** Certifique-se que arquivos estão em UTF-8

## Links Úteis

- [Template no Overleaf](https://pt.overleaf.com/latex/templates/thesis-template-aeronautics-institute-of-technology-ita/yhfrqqydpygk)
- [Repositório GitHub](https://github.com/AlejandroRios/Template_Thesis_ITA)
- Biblioteca ITA: www.bibl.ita.br

---
**Última atualização:** Agosto 2025  
**Compatível com:** TeX Live 2020+, Overleaf