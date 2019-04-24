---
title: Método Properties. Append (DAO)
TOCTitle: Append Method
ms:assetid: 47f1e24f-975c-3fdc-5c3c-8c91f2920c81
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193232(v=office.15)
ms:contentKeyID: 48544609
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 528809495ebefd15a8895b15a9d51f84e6892980
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301306"
---
# <a name="propertiesappend-method-dao"></a>Método Properties. Append (DAO)

**Aplica-se ao:** Access 2013, Office 2013

Adiciona um novo **Property** à coleção **Properties**.

## <a name="syntax"></a>Sintaxe

*expressão* . Append (***objeto***)

*expressão* Uma variável que representa um objeto **Properties** .

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
<td><p><strong>Objeto</strong></p></td>
<td><p>Uma variável de objeto que representa o campo sendo acrescentado à coleção.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

O objeto acrescentado torna-se um objeto persistente, armazenado em disco, até que seja excluído utilizando o método **Delete**.

A adição de um novo objeto ocorre imediatamente, mas você deve usar o método **Refresh** em qualquer outra coleção que possa ser afetada pelas alterações na estrutura do banco de dados.

Se o objeto que você está acrescentando não estiver completo (como quando você não acrescentou um objeto **Field** a uma coleção **Fields** de um objeto **Index** antes de ele ser acrescentado a uma coleção **Indexes**) ou se as propriedades definidas em um ou mais objetos subordinados estiverem incorretas, a utilização do método **Append** causará um erro. Por exemplo, se você não tiver especificado um tipo de campo e tentar acrescentar o objeto **Field** à coleção **Fields** em um objeto **TableDef** , o uso do método **Append** disparará um erro em tempo de execução.

