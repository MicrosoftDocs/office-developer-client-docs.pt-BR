---
title: Enumeração LockTypeEnum (DAO)
TOCTitle: LockTypeEnum Enumeration
ms:assetid: d40f984c-b37f-72f7-7b05-752f106b6029
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834802(v=office.15)
ms:contentKeyID: 48547925
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 82a09db7baff93ba7fd51de593bc4d1dfff41dc1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463511"
---
# <a name="locktypeenum-enumeration-dao"></a>Enumeração LockTypeEnum (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Especifica o tipo de bloqueio de registro usado ao abrir um conjunto de registros.

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
<td><p>dbOptimistic</p></td>
<td><p>3</p></td>
<td><p>Concorrência otimista baseada no código de registros antigos e novos, para determinar se foram feitas alterações desde que o registro foi acessado pela última vez.</p></td>
</tr>
<tr class="even">
<td><p>dbOptimisticBatch</p></td>
<td><p>5</p></td>
<td><p>Ativa atualizações otimistas em lotes (somente espaços de trabalho de ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p>dbOptimisticValue</p></td>
<td><p>1</p></td>
<td><p>Concorrência otimista baseada nos valores dos registros. O cursor compara os valores de dados de registros antigos e novos, para determinar se foram feitas alterações desde que o registro foi acessado pela última vez (somente espaços de trabalho de ODBCDirect).</p>

> [!NOTE]
> <P>[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</P>


</td>
</tr>
<tr class="even">
<td><p>dbPessimistic</p></td>
<td><p>2</p></td>
<td><p>Concorrência pessimista. O cursor usa o nível mais baixo de bloqueio, suficiente para garantir que o registro possa ser atualizado.</p></td>
</tr>
</tbody>
</table>

