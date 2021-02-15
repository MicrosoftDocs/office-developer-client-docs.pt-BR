---
title: Método QueryDefs.Append (DAO)
TOCTitle: Append Method
ms:assetid: 9b62a26b-3b7c-6d26-7707-177b00a23178
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198041(v=office.15)
ms:contentKeyID: 48546570
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b4183a7b438d3f55d73eb63adb2d124da7eeecc1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300935"
---
# <a name="querydefsappend-method-dao"></a>Método QueryDefs.Append (DAO)

**Aplica-se ao:** Access 2013, Office 2013

Adiciona um novo **QueryDef** à coleção **QueryDefs**.

## <a name="syntax"></a>Sintaxe

*expressão* .Append(***Object***)

*expressão* Uma variável que representa **um objeto QueryDefs** .

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
<td><p><em>Object</em></p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>Object</strong></p></td>
<td><p>Uma variável de objeto que representa o campo sendo acrescentado à coleção.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

O objeto acrescentado torna-se um objeto persistente, armazenado em disco, até que seja excluído utilizando o método **Delete**.

A adição de um novo objeto ocorre imediatamente, mas você deve usar o método **Refresh** em qualquer outra coleção que possa ser afetada pelas alterações na estrutura do banco de dados.

Se o objeto que você está acrescentando não estiver completo (como quando você não acrescentou um objeto **Field** a uma coleção **Fields** de um objeto **Index** antes de ele ser acrescentado a uma coleção **Indexes**) ou se as propriedades definidas em um ou mais objetos subordinados estiverem incorretas, a utilização do método **Append** causará um erro. Por exemplo, se você não especificou um tipo de campo e tentou acrescentar o objeto **Field** a uma coleção **Fields** em um objeto **TableDef**, a utilização do método **Append** aciona um erro em tempo de execução.

