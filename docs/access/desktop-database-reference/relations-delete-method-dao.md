---
title: Método Relations.Delete (DAO)
TOCTitle: Delete Method
ms:assetid: e95408d2-9dde-44e7-875e-8f2d4b837cf6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836064(v=office.15)
ms:contentKeyID: 48548438
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7c7a42098bcc64a58f8a004c0f1d5a35fd4f34b7
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998921"
---
# <a name="relationsdelete-method-dao"></a>Método Relations.Delete (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Exclui o objeto **Relation** especificado da coleção **Relations**.

## <a name="syntax"></a>Sintaxe

*expressão* . Excluir (***nome***)

*expressão* Uma variável que representa um objeto **Relations** .

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
<td><p><strong>Cadeia de caracteres</strong></p></td>
<td><p>O nome da relação a ser excluída.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

O método **Delete** é aceito somente quando o objeto **Relation** é um objeto novo e não acrescentado.

