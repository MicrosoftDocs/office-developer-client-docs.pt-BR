---
title: PersistFormatEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: PersistFormatEnum
ms:assetid: 5aa99a63-d422-0812-5aba-19305a3ad405
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249313(v=office.15)
ms:contentKeyID: 48545050
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e3254d60c6daa032857227b1f16f9a9c085164dc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463185"
---
# <a name="persistformatenum"></a>PersistFormatEnum


**Aplica-se a**: Access 2013 | Office 2013

Especifica o formato no qual se deve salvar um [Recorset](recordset-object-ado.md).

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
<td><p><strong>adPersistADTG</strong></p></td>
<td><p>0</p></td>
<td><p>Indica o formato Microsoft Advanced Data TableGram (ADTG).</p></td>
</tr>
<tr class="even">
<td><p><strong>adPersistADO</strong></p></td>
<td><p>1</p></td>
<td><p>Indica que será usado o formato Extensible Markup Language (XML) do próprio ADO. Este valor é igual a adPersistXML e é incluído para compatibilidade reversa.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPersistXML</strong></p></td>
<td><p>1</p></td>
<td><p>Indica o formato Extensible Markup Language (XML).</p></td>
</tr>
<tr class="even">
<td><p><strong>adPersistProviderSpecific</strong></p></td>
<td><p>2</p></td>
<td><p>Indica que o provedor manterá o <strong>Recorset</strong> usando seu próprio formato.</p></td>
</tr>
</tbody>
</table>


**ADO/WFC Equivalente**

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
<td><p>AdoEnums.PersistFormat.ADTG</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.PersistFormat.XML</p></td>
</tr>
</tbody>
</table>

