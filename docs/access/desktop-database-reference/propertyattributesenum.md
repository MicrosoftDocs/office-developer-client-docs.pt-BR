---
title: PropertyAttributesEnum
TOCTitle: PropertyAttributesEnum
ms:assetid: cbe93f65-a3ee-4741-1ac7-1c98ac53cdde
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250012(v=office.15)
ms:contentKeyID: 48547726
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2567d07ad33670fcd68be4513d7a409ffdcd599c
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864043"
---
# <a name="propertyattributesenum"></a>PropertyAttributesEnum


**Aplica-se a**: Access 2013 | Office 2013

Especifica os atributos de um objeto [Property](property-object-ado.md).

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
<td><p><strong>adPropNotSupported</strong></p></td>
<td><p>0</p></td>
<td><p>Indica que o provedor não oferece suporte para a propriedade.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPropRequired</strong></p></td>
<td><p>1</p></td>
<td><p>Indica que o usuário deve especificar um valor para essa propriedade antes de a fonte de dados ser inicializada.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPropOptional</strong></p></td>
<td><p>2</p></td>
<td><p>Indica que o usuário não precisa especificar um valor para essa propriedade antes de a fonte de dados ser inicializada.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPropRead</strong></p></td>
<td><p>512</p></td>
<td><p>Indica que o usuário pode ler a propriedade.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPropWrite</strong></p></td>
<td><p>1024</p></td>
<td><p>Indica que o usuário pode definir a propriedade.</p></td>
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
<td><p>AdoEnums.PropertyAttributes.NOTSUPPORTED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.PropertyAttributes.REQUIRED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.PropertyAttributes.OPTIONAL</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.PropertyAttributes.READ</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.PropertyAttributes.WRITE</p></td>
</tr>
</tbody>
</table>

