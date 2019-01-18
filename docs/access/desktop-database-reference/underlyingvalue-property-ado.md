---
title: Propriedade UnderlyingValue (ADO)
TOCTitle: UnderlyingValue property (ADO)
ms:assetid: f84f4c1c-2bd4-a725-3575-ed063ead13c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250262(v=office.15)
ms:contentKeyID: 48548782
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6d1618a0cb310c1e564fe18289da6a2d35e91d0b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717290"
---
# <a name="underlyingvalue-property-ado"></a>Propriedade UnderlyingValue (ADO)


**Aplica-se a**: Access 2013, o Office 2013



Indica um valor atual do objeto [Field](field-object-ado.md) no banco de dados.

## <a name="return-value"></a>Valor de retorno

Retorna um valor **Variant** que indica o valor do **Field**.

## <a name="remarks"></a>Comentários

Utilize a propriedade **UnderlyingValue** para retornar o valor de campo atual do banco de dados. O valor de campo na propriedade **UnderlyingValue** é o valor visível para sua transação e pode ser o resultado de uma atualização recente efetuada por outra transação. Ele pode ser diferente da propriedade [OriginalValue](originalvalue-property-ado.md), que reflete o valor que foi retornado originalmente para o [Recordset](recordset-object-ado.md).

Isto é semelhante ao uso do método [Resync](resync-method-ado.md), mas a propriedade **UnderlyingValue** retorna somente o valor para um campo específico do registro atual. Esse é o mesmo valor que o método [Resync](resync-method-ado.md) utiliza para substituir a propriedade [Value](value-property-ado.md).

Quando você utiliza essa propriedade com a propriedade **OriginalValue**, é possível solucionar conflitos provenientes de atualizações em lote.

## <a name="record"></a>Registro

Nos objetos [Record](record-object-ado.md), esta propriedade estará vazia para os campos adicionados antes de o [Update](update-method-ado.md) ser chamado.

