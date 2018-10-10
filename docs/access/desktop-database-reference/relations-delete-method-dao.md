---
title: Método Relations.Delete (DAO)
TOCTitle: Delete Method
ms:assetid: e95408d2-9dde-44e7-875e-8f2d4b837cf6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836064(v=office.15)
ms:contentKeyID: 48548438
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6b228c21931131023d58efc91d0087ad76ca3b61
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462910"
---
# <a name="relationsdelete-method-dao"></a>Método Relations.Delete (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Exclui o objeto **Relation** especificado da coleção **Relations**.

## <a name="syntax"></a>Sintaxe

*expressão* . Excluir (***nome***)

*expressão* Uma variável que representa um objeto **Relations** .

### <a name="parameters"></a>Parâmetros

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
<th><p>Obrigatório/Opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Name</p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>String</strong></p></td>
<td><p>O nome da relação a ser excluída.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

O método **Delete** é aceito somente quando o objeto **Relation** é um objeto novo e não acrescentado.

