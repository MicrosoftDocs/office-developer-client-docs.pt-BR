---
title: ResyncEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: ResyncEnum
ms:assetid: 3d38b77b-6afe-e6a0-1a05-7c7ffc19edef
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249164(v=office.15)
ms:contentKeyID: 48544337
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: d75ae42d5d3b63e1eea56153ef8e2dd2fb366a30
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870062"
---
# <a name="resyncenum"></a>ResyncEnum

**Aplica-se a**: Access 2013, o Office 2013

Especifica se os valores subjacentes são sobregravados por uma chamada para [Resync](resync-method-ado.md).

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
<td><p><strong>adResyncAllValues</strong></p></td>
<td><p>2</p></td>
<td><p>Padrão. Sobregrava dados e as atualizações pendentes são canceladas.</p></td>
</tr>
<tr class="even">
<td><p><strong>adResyncUnderlyingValues</strong></p></td>
<td><p>1</p></td>
<td><p>Não sobregrava os dados e as atualizações pendentes não são canceladas.</p></td>
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
<td><p>AdoEnums.Resync.ALLVALUES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Resync.UNDERLYINGVALUES</p></td>
</tr>
</tbody>
</table>

