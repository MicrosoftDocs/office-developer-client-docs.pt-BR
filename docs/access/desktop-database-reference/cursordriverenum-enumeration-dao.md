---
title: Enumeração CursorDriverEnum (DAO)
TOCTitle: CursorDriverEnum Enumeration
ms:assetid: d0312ece-c30a-7d61-d5f3-75edf0d0afc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834707(v=office.15)
ms:contentKeyID: 48547832
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bcce8eefad7fcad7dee7e46274ffc45125dc36c9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464322"
---
# <a name="cursordriverenum-enumeration-dao"></a>Enumeração CursorDriverEnum (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Especifica o tipo de driver de cursor.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Valor</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>dbUseClientBatchCursor</p></td>
<td><p>3</p></td>
<td><p>Sempre utiliza a Biblioteca de Cursores do FoxPro. Esta opção é necessária para executar atualizações em lotes.</p></td>
</tr>
<tr class="even">
<td><p>dbUseDefaultCursor</p></td>
<td><p>-1</p></td>
<td><p>(Padrão) Utiliza cursores do servidor se este oferecer suporte; caso contrário, usa a Biblioteca de Cursores ODBC.</p></td>
</tr>
<tr class="odd">
<td><p>dbUseNoCursor</p></td>
<td><p>4</p></td>
<td><p>Abre todos os cursores (ou seja, objetos <strong>Recordset</strong> ) como tipo somente de encaminhamento, como somente leitura, com um tamanho de conjunto de linhas de 1. Também conhecido como &quot;consultas sem cursor.&quot;</p></td>
</tr>
<tr class="even">
<td><p>dbUseODBCCursor</p></td>
<td><p>1</p></td>
<td><p>Sempre utiliza a Biblioteca de Cursores ODBC. Esta opção fornece melhor desempenho para pequenos conjuntos de resultados, mas se degrada rapidamente em conjuntos de resultados maiores.</p></td>
</tr>
<tr class="odd">
<td><p>dbUseServerCursor</p></td>
<td><p>2</p></td>
<td><p>Sempre utiliza cursores do servidor. Para a maioria das grandes operações esta opção oferece melhor desempenho, mas pode gerar mais tráfego na rede.</p></td>
</tr>
</tbody>
</table>

