---
title: Propriedade Workspace. Type (DAO)
TOCTitle: Type Property
ms:assetid: 89e59280-d2cd-b6a2-16c5-9f14f42fdd99
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197086(v=office.15)
ms:contentKeyID: 48546177
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e698963d60809e8d88c4ff87532fb7b74cff275c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311302"
---
# <a name="workspacetype-property-dao"></a>Propriedade Workspace. Type (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Define ou retorna um valor que indica o tipo operacional ou o tipo de dados de um objeto. **Integer** somente leitura.

## <a name="syntax"></a>Sintaxe

*expressão* . Escreva

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
<th><p>Constant</p></th>
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

