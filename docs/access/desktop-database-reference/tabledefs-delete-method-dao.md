---
title: Método TableDefs.Delete (DAO)
TOCTitle: Delete Method
ms:assetid: 130bb50d-17c3-b2ab-9360-0d91d0cee131
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845419(v=office.15)
ms:contentKeyID: 48543358
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2d511155f7a5fe1e6b83092e2065302bab99765b
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25999005"
---
# <a name="tabledefsdelete-method-dao"></a>Método TableDefs.Delete (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Exclui o objeto **TableDef** especificado da coleção **TableDefs**.

## <a name="syntax"></a>Sintaxe

*expressão* . Excluir (***nome***)

*expressão* Uma variável que representa um objeto **TableDefs** .

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
<td><p>O nome de TableDef a ser excluído.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

O método Delete é aceito somente quando o objeto **TableDef** é novo e não tiver sido acrescentado ao banco de dados, ou quando a propriedade **Updatable** de **TableDef** está definida como **True**.

