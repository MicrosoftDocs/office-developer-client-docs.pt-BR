---
title: Método TableDefs.Delete (DAO)
TOCTitle: Delete Method
ms:assetid: 130bb50d-17c3-b2ab-9360-0d91d0cee131
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845419(v=office.15)
ms:contentKeyID: 48543358
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 63f543fd86e309372e0432c3e45513cd9d3942ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313990"
---
# <a name="tabledefsdelete-method-dao"></a>Método TableDefs.Delete (DAO)

**Aplica-se ao:** Access 2013, Office 2013

Exclui o objeto **TableDef** especificado da coleção **TableDefs**.

## <a name="syntax"></a>Sintaxe

*expressão* . Delete(***Name***)

*expressão* Uma variável que representa **um objeto TableDefs** .

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
<th><p>Necessária/opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>String</strong></p></td>
<td><p>O nome de TableDef a ser excluído.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

O método Delete é aceito somente quando o objeto **TableDef** é novo e não foi acrescentado ao banco de dados, ou quando a propriedade **Updatable** de **TableDef** está definida como **True**.

