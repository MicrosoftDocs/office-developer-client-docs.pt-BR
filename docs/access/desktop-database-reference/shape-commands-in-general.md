---
title: Comandos shape em geral
TOCTitle: Shape Commands in General
ms:assetid: ad555aa7-bc64-b495-a98d-e927061a5809
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249814(v=office.15)
ms:contentKeyID: 48547039
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5cf2dc58ee3fa9205b9657366d8706b64b0aa58a
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861026"
---
# <a name="shape-commands-in-general"></a>Comandos de forma em geral


**Aplica-se a**: Access 2013 | Office 2013

O data shaping define as colunas de um **Recordset** com formato, as relações entre as entidades representadas pelas colunas e o modo de preenchimento de **Recordset** com dados.

Um **Recordset** com formato pode consistir nos seguintes tipos de colunas.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Tipo de coluna</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>data</p></td>
<td><p>Campos de um <strong>Recordset</strong> retornados por um comando de consulta para um provedor de dados, uma tabela ou um <strong>Recordset</strong> com formato anterior.</p></td>
</tr>
<tr class="even">
<td><p>chapter</p></td>
<td><p>Uma referência a outro <strong>Recordset</strong>, denominado <em>capítulo</em>. As colunas de capítulo permitem definir uma relação <em>parent-child</em> em que <em>parent</em> representa o <strong>Recordset</strong> contendo a coluna de capítulo, e <em>child</em> é o <strong>Recordset</strong> representado pelo capítulo.</p></td>
</tr>
<tr class="odd">
<td><p>aggregate</p></td>
<td><p>O valor da coluna é derivado executando uma <em>função de agregação</em> em todas as linhas ou em uma coluna de todas as linhas de um <strong>Recordset</strong> filho. (Consulte Funções agregadas no tópico <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Funções agregadas, a função CALC e a palavra-chave NEW</a>.)</p></td>
</tr>
<tr class="even">
<td><p>calculated expression</p></td>
<td><p>O valor da coluna é derivado do cálculo de uma expressão do Visual Basic for Application nas colunas na mesma linha do <strong>Recordset</strong>. A expressão é o argumento para a função CALC. (Consulte Expressão calculada no tópico <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Funções agregadas, a função CALC e a palavra-chave NEW</a> e em <a href="visual-basic-for-applications-functions.md">Funções do Visual Basic for Applications</a>.)</p></td>
</tr>
<tr class="odd">
<td><p>new</p></td>
<td><p>Campos fabricados vazios, que podem ser preenchidos posteriormente com dados. A coluna é definida com a palavra-chave NEW. (Consulte Palavra-chave NEW no tópico <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Funções agregadas, a função CALC e a palavra-chave NEW</a>.)</p></td>
</tr>
</tbody>
</table>


Um comando shape pode conter uma cláusula especificando um comando de consulta para um provedor de dados subjacente que retornará um objeto **Recordset**. A sintaxe da consulta depende dos requisitos desse provedor. Em geral, será usada a linguagem SQL, embora o ADO não exija nenhuma linguagem de consulta específica.

É possível usar uma cláusula SQL JOIN para relacionar duas tabelas; entretanto, um **Recordset** hierárquico pode representar as informações com mais eficiência. Cada linha de um **Recordset** criada por um JOIN repete as informações de uma das tabelas de forma redundante. Um **Recordset** hierárquico possui apenas um **Recordset** pai para cada um dos diversos objetos **Recordset** filho.

<<<<<<< Comandos Shape com os diretores podem ser emitidos por objetos **Recordset** ou definindo a propriedade [CommandText](commandtext-property-ado.md) do objeto [Command](command-object-ado.md) e, em seguida, chamando o método [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) .
=== Comandos shape podem ser emitidos por objetos **Recordset** ou definindo a propriedade [CommandText](commandtext-property-ado.md) do objeto [Command](command-object-ado.md) e, em seguida, chamando o método [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) .
>>>>>>> mestre

Comandos Shape podem ser aninhados. Ou seja, o *parent-command* *filho-command* próprio poderá ou um outro comando shape.

O provedor de forma sempre retorna um cursor do cliente, mesmo quando o usuário especifica o local de cursor **adUseServer**.

Para obter informações sobre como navegar em um **Recordset** hierárquico, consulte [Acessando linhas em um conjunto de registros hierárquico](accessing-rows-in-a-hierarchical-recordset.md).

Para obter informações precisas sobre comandos shape sintaticamente corretos, consulte [Gramática formal de shape](formal-shape-grammar.md).

## <a name="see-also"></a>Confira também

- [Emitindo comandos para o provedor de dados adjacente](issuing-commands-to-the-underlying-data-provider.md)

