---
title: ADCPROP_ASYNCTHREADPRIORITY_ENUM
TOCTitle: ADCPROP_ASYNCTHREADPRIORITY_ENUM
ms:assetid: b15006dd-22d5-fcf3-8196-9e24ea9d55a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249844(v=office.15)
ms:contentKeyID: 48547143
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 53e51f2386658ee975ec8847f7e5550ac22bbd8e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700273"
---
# <a name="adcpropasyncthreadpriorityenum"></a>ADCPROP\_ASYNCTHREADPRIORITY\_ENUM

**Aplica-se a**: Access 2013, o Office 2013

Para um objeto do [Recordset](recordset-object-ado.md) RDS, especifica a prioridade de execução do encadeamento assíncrono que recupera os dados.

Use essas constantes com o **Recordset** da propriedade dinâmica "**Prioridade de Encadeamento em Segundo Plano**" , que referenciada no Índice de Propriedades Dinâmicas ADO e documentada no [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md).

<br/>

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
<td><p><strong>adPriorityAboveNormal</strong></p></td>
<td><p>4</p></td>
<td><p>Define a prioridade entre normal e mais alta.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPriorityBelowNormal</strong></p></td>
<td><p>2</p></td>
<td><p>Define a prioridade entre mais baixa e normal.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPriorityHighest</strong></p></td>
<td><p>5</p></td>
<td><p>Define a prioridade para o valor mais alto possível.</p></td>
</tr>
<tr class="even">
<td><p><strong>AdPriorityLowest</strong></p></td>
<td><p>1</p></td>
<td><p>Define a prioridade para o valor mais baixo possível.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPriorityNormal</strong></p></td>
<td><p>3</p></td>
<td><p>Define a prioridade como normal.</p></td>
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
<td><p>AdoEnums.AdcPropAsyncThreadPriority.ABOVENORMAL</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.AdcPropAsyncThreadPriority.BELOWNORMAL</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.AdcPropAsyncThreadPriority.HIGHEST</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.AdcPropAsyncThreadPriority.LOWEST</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.AdcPropAsyncThreadPriority.NORMAL</p></td>
</tr>
</tbody>
</table>

