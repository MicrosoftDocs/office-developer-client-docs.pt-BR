---
title: Método Recordset2.MoveNext (DAO)
TOCTitle: MoveNext Method
ms:assetid: 0eeb917e-f76a-03ec-9e1e-aa8d501db031
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845265(v=office.15)
ms:contentKeyID: 48543254
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6f500578182aac74b608117ee4105a6b657057df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309552"
---
# <a name="recordset2movenext-method-dao"></a>Método Recordset2.MoveNext (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Move para o próximo registro em um objeto **Recordset** específico e o torna o registro atual. 

## <a name="syntax"></a>Sintaxe

*expressão* .MoveNext

*expressão* Uma variável que representa **um objeto Recordset2** .

## <a name="remarks"></a>Comentários

Use os métodos **Move** para mover de um registro para outro sem aplicar nenhuma condição.

Se você editar o registro atual, certifique-se de usar o método **Update** para salvar as alterações antes de mover para outro registro. Se você mover para outro registro sem realizar a atualização, as alterações serão perdidas sem nenhum aviso.

Quando você abre um **Recordset**, o primeiro registro é o atual, e a propriedade **BOF** é **False**. Se o **Recordset** não contiver nenhum registro, a propriedade **BOF** será **True**, e não haverá nenhum registro atual.

Se você usar o **MoveNext** quando o último registro for o atual, a propriedade **EOF** será **True**, e não haverá nenhum registro atual. Se você usar **MoveNext** novamente, ocorrerá um erro, e **EOF** permanece **True**.

Se o recordset se referir a um tipo de tabela **Recordset**(apenas espaços de trabalho do Microsoft Access), a movimentação seguirá o índice atual. Você pode definir o índice atual utilizando a propriedade **Index**. Se você não definir o índice atual, a ordem dos registros retornados será indefinida.

Você não pode usar os métodos **MoveFirst**, **MoveLast** e **MovePrevious** em um objeto **Recordset** do tipo somente encaminhamento.

Para mover a posição do registro atual em um número específico de registros do objeto **Recordset** para frente ou para trás, use o método **Move**.

