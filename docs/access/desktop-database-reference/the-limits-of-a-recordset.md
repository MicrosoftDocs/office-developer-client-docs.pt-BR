---
title: Os limites de um Recordset
TOCTitle: The Limits of a Recordset
ms:assetid: 51e27c95-e0c3-7fdc-ac11-891553620376
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249266(v=office.15)
ms:contentKeyID: 48544833
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d0da48080b64e43cc39b9567275e1a8755a8881
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314108"
---
# <a name="limits-of-a-recordset"></a>Limites de um conjunto de registros


**Aplica-se ao:** Access 2013, Office 2013

Use as propriedades **BOF** e **EOF** para determinar se um objeto **Recordset** contém registros ou se você ultrapassou os limites de um objeto **Recordset** ao se mover de um registro para outro. Pense nas propriedades **BOF** e **EOF** como registros "fantasmas" que são posicionados no início e no final de cada **Recordset**. Desenvolver o **Recordset** a partir de [Examinando dados](chapter-3-examining-data.md) daria a seguinte aparência ao objeto:

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ProductID</p></th>
<th><p>ProductName</p></th>
<th><p>UnitPrice</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>BOF</p></td>
<td><p><br />
</p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p>7 </p></td>
<td><p>Pêras secas orgânicas do Tio Bob</p></td>
<td><p>30.0000</p></td>
</tr>
<tr class="odd">
<td><p>14 </p></td>
<td><p>Tofu</p></td>
<td><p>23.2500</p></td>
</tr>
<tr class="even">
<td><p>28</p></td>
<td><p>Chucrute Rssle</p></td>
<td><p>45.6000</p></td>
</tr>
<tr class="odd">
<td><p>51</p></td>
<td><p>Maçãs secas Manjimup</p></td>
<td><p>53.0000</p></td>
</tr>
<tr class="even">
<td><p>74</p></td>
<td><p>Tofu longa vida</p></td>
<td><p>10.0000</p></td>
</tr>
<tr class="odd">
<td><p>EOF</p></td>
<td><p><br />
</p></td>
<td><p><br />
</p></td>
</tr>
</tbody>
</table>


A propriedade **BOF** retornará **True** (-1) se a posição do registro atual estiver antes do primeiro registro e **False** (0) se a posição do registro atual estiver no ou depois do primeiro registro.

A propriedade **EOF** retornará **True** se a posição do registro atual estiver depois do último registro e **Falso** se a posição atual do registro estiver no ou antes do último registro.

Se a propriedade **BOF** ou **EOF** for **True**, não haverá registro atual, conforme mostrado no código a seguir:

```vb 
 
If oRs.BOF And oRs.EOF Then 
 ' Command returned no records. 
End If 
```

Se você abrir um objeto **Recordset** que não contenha registros, as propriedades **BOF** e **EOF** serão definidas como **True** e o valor da configuração da propriedade **RecordCount** do objeto **Recordset** dependerá do tipo de cursor. -1 será retornado para cursores dinâmicos (**CursorType**  =  **adOpenDynamic**) e 0 será retornado para outros cursores.

Ao abrir um objeto **Recordset** que contenha pelo menos um registro, o primeiro registro será o registro atual e as propriedades **BOF** e **EOF** serão **False**.

Se você excluir o último registro do objeto **Recordset**, o cursor será deixado em estado indeterminado. As propriedades **BOF** e **EOF** podem permanecer como **False** até que seja feita uma tentativa de reposicionamento do registro atual, de acordo com o provedor.

