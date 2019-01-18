---
title: Ação da macro DefinirClassificadoPor
TOCTitle: SetOrderBy macro action
ms:assetid: 78f65ce9-b56f-f476-3bd6-f3307bc22a08
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196152(v=office.15)
ms:contentKeyID: 48545765
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm98639
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 86834cd8b6132e8939067c0e34037ca1b0ef8bad
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704417"
---
# <a name="setorderby-macro-action"></a>Ação da macro DefinirClassificadoPor


**Aplica-se a**: Access 2013, o Office 2013

Você pode usar a ação **DefinirClassificadoPor** para especificar como deseja classificar os registros em um formulário, relatório, tabela ou resultado da consulta.

## <a name="setting"></a>Configuração

A ação **DefinirClassificadoPor** tem os seguintes argumentos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento da ação</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Classificado Por</strong></p></td>
<td><p>Uma expressão de cadeia de caracteres que inclui o nome do(s) campo(s) no(s) qual(is) serão classificados os registros e as palavras-chave CRESC ou DECRESC opcionais.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nome do Controle</strong></p></td>
<td><p>Se for fornecido e um objeto ativo for um formulário ou um relatório, o nome do controle que corresponde ao subformulário ou ao subrelatório a ser filtrado. Se estiver em branco e o objeto ativo for um formulário ou um relatório, o formulário ou relatório pai será classificado.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Quando você executar essa ação de macro, a classificação será aplicada à tabela, ao formulário, ao relatório ou à folha de dados (resultado da pesquisa) que está ativa e que tem o foco.

O argumento Classificado Por é o nome do campo ou dos campos nos quais você deseja classificar registros. Quando você usa mais de um nome de campo, separe-os com vírgula (,). A propriedade **OrderBy** do objeto ativo é usada para salvar um valor de classificação e aplicá-lo posteriormente. Os valores de OrderBy são salvos com os objetos nos quais foram criados. Eles são carregados automaticamente quando o objeto é aberto, mas não são aplicados automaticamente.

Quando você define o argumento Classificado Por digitando um ou mais nomes de campo e executa a macro, os registros são classificados por padrão em ordem crescente.

Para classificar registros em ordem decrescente, digite DESC no final da expressão de argumento Classificado Por. Por exemplo, para classificar registros de cliente em ordem decrescente por nome de contato, defina o argumento OrderBy como "NomedoContato DESC". Para classificar nomes por Sobrenomes em ordem decrescente e Nomes em ordem crescente, defina o argumento Classificado Por como "Sobrenome DESC, Nome ASC".

