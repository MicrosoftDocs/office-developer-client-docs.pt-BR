---
title: Método Indexes.Delete (DAO)
TOCTitle: Delete Method
ms:assetid: 8d3c3221-3b2e-15ba-32ff-f2dfc592d82c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197351(v=office.15)
ms:contentKeyID: 48546252
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6ab52f353b7a3e636f64ff2ad6ad5354d62bed48
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703542"
---
# <a name="indexesdelete-method-dao"></a>Método Indexes.Delete (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Exclui o **Index** especificado da coleção **Indexes**.

## <a name="syntax"></a>Sintaxe

*expressão* . Excluir (***nome***)

*expressão* Uma variável que representa um objeto **Indexes** .

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
<td><p><em>Name</em></p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>String</strong></p></td>
<td><p>O nome do índice a ser excluído.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

O método **Delete** é suportado somente quando o objeto **Index** for novo e não tiver sido acrescentado ao banco de dados.

