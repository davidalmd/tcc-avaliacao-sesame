# Avaliando o Merge Semi-Estruturado: um estudo comparativo de corretude e desempenho da ferramenta SESAME

> **Status:** 🎓 Trabalho de Conclusão de Curso (TCC) em andamento.

Este repositório armazena o código-fonte (em LaTeX) do documento do Trabalho de Conclusão de Curso do curso de Bacharelado em Engenharia de Software do IFPE - Campus Belo Jardim.

---

## 🔗 Ecossistema do Projeto

Este trabalho é composto por múltiplos componentes distribuídos nos seguintes repositórios:

1.  **[Pré-Projeto (Concluído)](https://github.com/davidalmd/pre-projeto-tcc-avaliacao-sesame)**
    * Contém o documento de planejamento, a revisão bibliográfica e a metodologia proposta para este TCC.

2.  **Este Repositório (`tcc-avaliacao-sesame`)**
    * Contém o documento final do TCC, que descreve a execução dos experimentos e a análise dos resultados.
      
3.  **[Framework de Avaliação Incrementado](https://github.com/davidalmd/AST-Merging-Evaluation-TCC)**
    * Repositório pessoal onde a implementação prática e as contribuições de código para a avaliação da ferramenta SESAME são realizadas.
      
4.  **[Framework de Avaliação Original](https://github.com/benedikt-schesch/AST-Merging-Evaluation)**
    * Repositório principal onde encontra-se a ferramenta de avaliação oficial e original utilizada nesse trabalho de conclusão de curso.

---

## 📖 Sobre o Projeto

O objetivo deste trabalho é avaliar empiricamente a ferramenta de merge semi-estruturado SESAME, que utiliza separadores sintáticos específicos da linguagem para aprimorar a resolução de conflitos. A ferramenta é integrada a um robusto framework de avaliação comparativa e executada em milhares de cenários de merge extraídos de projetos de código aberto. A eficácia de cada merge é verificada pela execução de suítes de teste automatizadas, permitindo uma análise de desempenho e corretude frente a outras ferramentas do estado da arte.

Segue abaixo o **Resumo** deste trabalho:

A integração de modificações concorrentes é um desafio crítico no desenvolvimento colaborativo de software. Enquanto ferramentas de merge não estruturadas (textuais) frequentemente geram conflitos espúrios, abordagens estruturadas, apesar de mais precisas, podem introduzir erros semânticos silenciosos e possuem alto custo computacional. Neste contexto, a ferramenta SESAME propõe uma abordagem semi-estruturada inovadora, utilizando separadores sintáticos para inferir a estrutura do código de forma leve. Este trabalho apresenta uma avaliação empírica do SESAME através de uma replicação diferenciada do estudo de Schesch et al. (2024). Adotando um protocolo experimental rigoroso, avaliou-se a ferramenta não apenas pela contagem de conflitos, mas pela corretude semântica verificada através da execução de suítes de testes automatizados em um vasto conjunto de projetos Java. O desempenho do SESAME foi contrastado com ferramentas do estado da arte (Git Merge, Spork e IntelliMerge) utilizando um dataset robusto com mais de 5.000 cenários de merge, com métricas de Corretude, Tempo de Execução e Redução de Esforço (Effort Reduction). Os resultados revelam que, embora ferramentas puramente estruturadas maximizem a resolução de conflitos, elas introduzem taxas elevadas de erros (11% no Spork) e impõem latência proibitiva. Em contraste, o SESAME consolidou-se como um sweet spot: manteve a segurança próxima ao padrão textual (apenas 3% de erro) com um tempo de execução uma ordem de grandeza inferior às ferramentas estruturadas, validando-se como uma alternativa pragmática e eficiente para esteiras de Integração Contínua.

**Palavras-chave:** Merge Semi-Estruturado, Ferramentas de Merge, Conflitos de Merge, Avaliação de Desempenho, Corretude de Software.

---

## 📁 Estrutura do Repositório

O documento está organizado da seguinte forma:

-   `main.tex`: Arquivo LaTeX principal do TCC.
-   `bibliografia.bib`: Base de dados das referências bibliográficas.
-   `ArtigoIFPE.sty`: Arquivo de estilo customizado para o template do IFPE.
-   `latexmkrc`: Arquivo de configuração para a compilação automatizada.
-   `/Imagens/`: Diretório contendo as imagens, gráficos e figuras.
-   `/biblatex-abnt-34/`: Estilos para a formatação da bibliografia no padrão ABNT.
-   `.gitignore`: Arquivo para ignorar arquivos gerados pela compilação.

---

## ⚙️ Como Compilar o Documento

### Pré-requisitos
1.  Distribuição LaTeX completa (ex: [MiKTeX](https://miktex.org/) ou [TeX Live](https://www.tug.org/texlive/)).
2.  [Visual Studio Code](https://code.visualstudio.com/) com a extensão [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop).

### Passos para Compilação
1.  Clone este repositório.
2.  Abra a pasta do projeto no VS Code.
3.  Abra o arquivo `main.tex`.
4.  Compile o projeto (`Ctrl+Alt+B`), garantindo que o compilador **`xelatex`** seja utilizado.

O arquivo `main.pdf` será gerado na raiz do projeto.

---

**Autor:** David Lucas Alves de Almeida (`dlaa@discente.ifpe.edu.br` | `david.almeida2707@gmail.com`)  
**Orientador:** Prof. Dr. Guilherme José de Carvalho Cavalcanti
