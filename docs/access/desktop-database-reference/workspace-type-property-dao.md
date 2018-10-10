---
title: Propriedade Workspace.Type (DAO)
TOCTitle: Type Property
ms:assetid: 89e59280-d2cd-b6a2-16c5-9f14f42fdd99
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197086(v=office.15)
ms:contentKeyID: 48546177
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d062adbde4e9d7053e61342b7433939d4fbffcb8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462617"
---
# <a name="workspacetype-property-dao"></a>Propriedade Workspace.Type (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Define ou retorna um valor que indica o tipo operacional ou o tipo de dados de um objeto. **Integer** somente leitura.

## <a name="syntax"></a>Sintaxe

*expressão* . Tipo

*expressão* Uma variável que representa um objeto **Workspace** .

## <a name="remarks"></a>Comentários

Para um objeto **Workspace**, as configurações e valores de retorno possíveis são os seguintes:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Tipo de Workspace</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbUseJet</strong></p></td>
<td><p>O <strong>Workspace </strong> está conectado ao mecanismo de banco de dados do Microsoft Access.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbUseODBC</strong></p></td>
<td><p>O <strong>Workspace</strong> está conectado a uma fontes de dados ODBC.</p></td>
</tr>
</tbody>
</table>
