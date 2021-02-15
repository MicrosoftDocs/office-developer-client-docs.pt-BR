---
title: Enumeração UpdateCriteriaEnum (DAO)
TOCTitle: UpdateCriteriaEnum Enumeration
ms:assetid: 1f83a0c6-bdc8-9c3e-380b-524f611f6476
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845853(v=office.15)
ms:contentKeyID: 48543644
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e27eb1bdfb9b393df76af8bdf54bc7f05fd82c2e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306367"
---
# <a name="updatecriteriaenum-enumeration-dao"></a>Enumeração UpdateCriteriaEnum (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Usada com o método **UpdateOptions** para especificar como uma atualização em lotes é construída.

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
<td><p>dbCriteriaAllCols</p></td>
<td><p>4 </p></td>
<td><p>Usa a(s) coluna(s) chave e todas as colunas da cláusula where.</p></td>
</tr>
<tr class="even">
<td><p>dbCriteriaDeleteInsert</p></td>
<td><p>16 </p></td>
<td><p>Usa um par de instruções DELETE e INSERT para cada linha modificada.</p></td>
</tr>
<tr class="odd">
<td><p>dbCriteriaKey</p></td>
<td><p>1 </p></td>
<td><p>Use apenas a(s) coluna(s) chave na cláusula where.</p></td>
</tr>
<tr class="even">
<td><p>dbCriteriaModValues</p></td>
<td><p>2 </p></td>
<td><p>Usa a(s) coluna(s) chave e todas as colunas atualizadas na cláusula where.</p></td>
</tr>
<tr class="odd">
<td><p>dbCriteriaTimestamp</p></td>
<td><p>8 </p></td>
<td><p>Usa apenas a coluna de carimbo de data/hora, se estiver disponível (gerará um erro em tempo de execução se nenhuma coluna de carimbo de data/hora estiver no conjunto de resultados).</p></td>
</tr>
<tr class="even">
<td><p>dbCriteriaUpdate</p></td>
<td><p>32</p></td>
<td><p>Usa uma instrução UPDATE para cada linha modificada.</p></td>
</tr>
</tbody>
</table>

