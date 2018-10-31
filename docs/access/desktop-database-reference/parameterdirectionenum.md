---
title: ParameterDirectionEnum
TOCTitle: ParameterDirectionEnum
ms:assetid: 73a97522-010e-d8f4-1a30-15df2469cad4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249473(v=office.15)
ms:contentKeyID: 48545643
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2ae3f65b42032e9a5d8f905516de080a9c575e5b
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863625"
---
# <a name="parameterdirectionenum"></a>ParameterDirectionEnum


**Aplica-se a**: Access 2013 | Office 2013

Especifica se [Parameter](parameter-object-ado.md) representa um parâmetro de entrada, de saída, ou ambos, ou o valor de retorno de um procedimento armazenado.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
<th><p>Valor</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adParamInput</strong></p></td>
<td><p>1</p></td>
<td><p>Padrão. Indica que o parâmetro representa um parâmetro de entrada.</p></td>
</tr>
<tr class="even">
<td><p><strong>adParamInputOutput</strong></p></td>
<td><p>3</p></td>
<td><p>Indica que o parâmetro representa um parâmetro de entrada e de saída.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adParamOutput</strong></p></td>
<td><p>2</p></td>
<td><p>Indica que o parâmetro representa um parâmetro de saída.</p></td>
</tr>
<tr class="even">
<td><p><strong>adParamReturnValue</strong></p></td>
<td><p>4</p></td>
<td><p>Indica que o parâmetro representa um valor de retorno.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adParamUnknown</strong></p></td>
<td><p>0</p></td>
<td><p>Indica que a direção do parâmetro é desconhecida.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente ADO/WFC

Pacote: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.ParameterDirection.INPUT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ParameterDirection.INPUTOUTPUT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ParameterDirection.OUTPUT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ParameterDirection.RETURNVALUE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ParameterDirection.UNKNOWN</p></td>
</tr>
</tbody>
</table>

