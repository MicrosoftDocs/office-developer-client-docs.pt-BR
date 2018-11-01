---
title: Propriedade OriginalValue (ADO)
TOCTitle: OriginalValue property (ADO)
ms:assetid: 02ffc728-4692-d439-e2a6-2f02cca53a71
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248798(v=office.15)
ms:contentKeyID: 48542974
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 872e7c88e5ea4e79d6bff4aa590e72743feb3893
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884909"
---
# <a name="originalvalue-property-ado"></a>Propriedade OriginalValue (ADO)

**Aplica-se a**: Access 2013, o Office 2013

Indica o valor de um [Field](field-object-ado.md) que existia no registro antes de as alterações serem efetuadas.

## <a name="return-value"></a>Valor de retorno

Retorna um valor **Variant** que representa o valor de um campo antes de qualquer alteração.

## <a name="remarks"></a>Comentários

Utilize a propriedade **OriginalValue** para retornar o valor do campo original de um campo a partir do registro atual.

No *modo de atualização imediata* (no qual o provedor grava as alterações à fonte de dados subjacente depois de chamar o método [Update](update-method-ado.md) ), a propriedade **OriginalValue** retorna o valor do campo que se encontrava antes que quaisquer alterações (ou seja, desde que o última chamada de método de **atualização** ). Esse é o mesmo valor que o método [CancelUpdate](cancelupdate-method-ado.md) utiliza para substituir a propriedade [Value](value-property-ado.md).

No *modo de atualização em lotes* (no qual o provedor caches várias alterações e grava-los à fonte de dados subjacente somente quando você chamar o método [UpdateBatch](updatebatch-method-ado.md) ), a propriedade **OriginalValue** retorna o valor do campo que se encontrava antes de qualquer um altera (ou seja, desde o último método **UpdateBatch** é chamada). Esse é o mesmo valor que o método [CancelBatch](cancelbatch-method-ado.md) utiliza para substituir a propriedade **Value**. Quando você utiliza essa propriedade com a propriedade [UnderlyingValue](underlyingvalue-property-ado.md), é possível solucionar conflitos provenientes da atualizações em lote.

## <a name="record"></a>Registro

Para os objetos [Record](record-object-ado.md), a propriedade **OriginalValue** estará em branco nos campos adicionados antes da chamada do [ Update ](update-method-ado.md).

