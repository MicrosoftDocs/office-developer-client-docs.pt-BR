---
title: Propriedade Recordset.Type (DAO)
TOCTitle: Type Property
ms:assetid: d841b088-50bf-16d9-33e0-2140050e1ac6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835080(v=office.15)
ms:contentKeyID: 48548030
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4a55af8aaa5cfb3d87e13125871a6ccbe1e7f2dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307550"
---
# <a name="recordsettype-property-dao"></a>Propriedade Recordset.Type (DAO)


**Aplica-se ao**: Access 2013, Office 2013

Define ou retorna um valor que indica o tipo operacional ou o tipo de dados de um objeto. **Integer** somente leitura.

## <a name="syntax"></a>Sintaxe

*expressão* .Type

*expression* Uma variável que representa um objeto **Recordset**.

## <a name="remarks"></a>Comentários

Para um objeto **Recordset**, as configurações e os valores de retorno possíveis são os seguintes:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
<th><p>Tipo de Recordset</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbOpenTable</strong></p></td>
<td><p>Tabela (somente em espaços de trabalho do Microsoft Access)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbOpenDynamic</strong></p></td>
<td><p>Dinâmico (somente em espaços de trabalho ODBCDirect)</p>
<p><strong>OBSERVAÇÃO</strong>: o Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use o ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbOpenDynaset</strong></p></td>
<td><p>Dynaset</p></td>
</tr>
<tr class="even">
<td><p><strong>dbOpenSnapshot</strong></p></td>
<td><p>Instantâneo</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbOpenForwardOnly</strong></p></td>
<td><p>Somente encaminhamento</p></td>
</tr>
</tbody>
</table>

