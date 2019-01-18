---
title: Método Workspaces.Append (DAO)
TOCTitle: Append Method
ms:assetid: 195c26a6-a1d1-40a8-7e7e-13cd632008b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845644(v=office.15)
ms:contentKeyID: 48543498
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 11d721d58301d2adb33b2e381d88d7245531ff06
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718879"
---
# <a name="workspacesappend-method-dao"></a>Método Workspaces.Append (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Adiciona um novo objeto **Workspace** à coleção **Workspaces**.

## <a name="syntax"></a>Sintaxe

*expressão* . Acrescentar (***objeto***)

*expressão* Uma variável que representa um objeto **Workspaces** .

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

Se o objeto que você está acrescentando não estiver completo (como quando você não acrescentou um objeto **Field** a uma coleção **Fields** de um objeto **Index** antes de ele ser acrescentado a uma coleção **Indexes**) ou se as propriedades definidas em um ou mais objetos subordinados estiverem incorretas, a utilização do método **Append** causará um erro. Por exemplo, se você ainda não tiver especificado um tipo de campo e, então, tenta acrescentar o objeto **Field** à coleção **Fields** em um objeto **TableDef** , usar o método **Append** dispara um erro em tempo de execução.

