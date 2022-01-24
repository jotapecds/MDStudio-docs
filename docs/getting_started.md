---
title: Getting Started
nav_order: 2
---

# Getting Started
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Modelagem de Dados

### Definição do modelo

#### Arquivo PMD

Os arquivos no formato **pmd** definem a base de dados, tendo informações referentes aos modelos em formato de classes com seus respectivos parâmetros. O atributo padrão é definido no pmd como PARM.  As classes podem ser definidas por MERGE_CLASS, sendo esta estática, enquanto as definidas por DEFINE_CLASS são classes dinâmicas. As definidas pelo MERGE_CLASS utilizam-se de duas ou mais classes na sua construção. Na figura 1 temos um exemplo da construção de um pmd.

Os parâmetros podem ser dos tipos: 

- DIMENSION: Representa a dimensão.
- DATE:  Representa o formato data.
- INTEGER: Representa um parâmetro definido por números inteiros.
- STRING: Representa um parâmetro definido por texto/caracteres.
- REAL: Representa um parâmetro definido por números reais.
- REFERENCE: Parâmetro que faz referência a outra classe já definida no mesmo PMD. 

Os parâmetros com o termo **@id** são utilizados como **identificadores**. Para todos os tipos é possível criar um vetor, contendo um número variado de dados deste mesmo tipo. Estes vetores podem ser indexados (**INDEX**) utilizando outros parâmetros.

`Figure 1. Exemplo de estruturação de um arquivo pmd. No lado esquerdo temos um exemplo de definição de uma classe. Na direita, temos um exemplo de um parâmetro que faz referência a um parâmetro de outra classe.`

<div style="text-align:center">
    <img src="../img/Picture1.png"/>
    <img src="../img/Picture2.png"/>
</div>

Quando o parâmetro possui o termo **DIM()** após a definição do seu tipo, é indicado a construção de colunas para esse parâmetro. O número de colunas irá seguir o tamanho do parâmetro utilizado dentro dos parênteses, geralmente sendo utilizado o parâmetro definido na mesma classe do tipo **DIMENSION**.    

### Arquivo PMK

Os arquivos **pmk** são arquivos necessários para ser possível registrar e escrever o pmd documento com os dados alterados. Esta funcionalidade do PSRClasses gera automaticamente todos os formatos de arquivos necessários para representar as estruturas de dados contidas no(s) arquivo(s) pmd(s). Considerando a mesma classe do exemplo anterior, temos o exemplo de arquivo pmk.

`Figure 2 Exemplo de criação de um arquivo pmk a partir de um arquivo pmd.`

<div style="text-align:center">
    <img src="../img/Picture3.png"/>
</div>

A criação de um arquivo pmk a partir do pmd é realizada de forma automática, sendo necessária apenas realizar alguns comandos no shell do Windows. 

<div style="text-align:center">
    <img src="../img/Picture4.png"/>
</div>

# Definição do layout das coleções na interface 

## Layout inicial do caso