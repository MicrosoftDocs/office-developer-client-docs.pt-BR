---
title: Método indexes. Delete (DAO)
TOCTitle: Delete Method
ms:assetid: 8d3c3221-3b2e-15ba-32ff-f2dfc592d82c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197351(v=office.15)
ms:contentKeyID: 48546252
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6ab52f353b7a3e636f64ff2ad6ad5354d62bed48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291549"
---
# <a name="indexesdelete-method-dao"></a>Método indexes. Delete (DAO)

**Aplica-se ao:** Access 2013, Office 2013

Exclui o **Index** especificado da coleção **Indexes**.

## <a name="syntax"></a>Sintaxe

*expressão* . Excluir (***nome***)

*expressão* Uma variável que representa um **** objeto indexes.

## <a name="parameters"></a>Parâmetros

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Obrigatório/opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Nome</em></p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>String</strong></p></td>
<td><p>O nome do índice a ser excluído.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

O método **Delete** tem suporte apenas quando o objeto **Index** for novo e não tiver sido acrescentado ao banco de dados.

