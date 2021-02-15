---
title: Método Indexes.Append (DAO)
TOCTitle: Append Method
ms:assetid: 60dce80f-505b-e988-3ac1-8ecaae3d3d09
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194835(v=office.15)
ms:contentKeyID: 48545191
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bcebcf2f7fbce59c6050100f1763923a6025526e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291648"
---
# <a name="indexesappend-method-dao"></a>Método Indexes.Append (DAO)

**Aplica-se ao:** Access 2013, Office 2013

Adiciona um novo **Index** à coleção **Indexes**.

## <a name="syntax"></a>Sintaxe

*expressão* .Append(***Object***)

*expressão* Uma variável que representa um **objeto Indexes** .

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
<td><p>Uma variável objeto que representa o item que está sendo acrescentado à coleção.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

O objeto acrescentado torna-se um objeto persistente, armazenado em disco, até que seja excluído utilizando o método **Delete**.

A adição de um novo objeto ocorre imediatamente, mas você deve usar o método **Refresh** em qualquer outra coleção que possa ser afetada pelas alterações na estrutura do banco de dados.

Se o objeto que você está acrescentando não estiver completo (como quando você não acrescentou um objeto **Field** a uma coleção **Fields** de um objeto **Index** antes de ele ser acrescentado a uma coleção **Indexes**) ou se as propriedades definidas em um ou mais objetos subordinados estiverem incorretas, a utilização do método **Append** causará um erro. Por exemplo, se você não especificou um tipo de campo e tentou acrescentar o objeto **Field** a uma coleção **Fields** em um objeto **TableDef**, a utilização do método **Append** aciona um erro em tempo de execução.

