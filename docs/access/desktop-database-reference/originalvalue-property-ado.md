---
title: Propriedade OriginalValue (ADO)
TOCTitle: OriginalValue property (ADO)
ms:assetid: 02ffc728-4692-d439-e2a6-2f02cca53a71
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248798(v=office.15)
ms:contentKeyID: 48542974
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0724320e1aaa1e7bfd3ceab8cf54afd5921c7425
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288179"
---
# <a name="originalvalue-property-ado"></a>Propriedade OriginalValue (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Indica o valor de um [Field](field-object-ado.md) que existia no registro antes de as alterações serem efetuadas.

## <a name="return-value"></a>Valor de retorno

Retorna um valor **Variant** que representa o valor de um campo antes de qualquer alteração.

## <a name="remarks"></a>Comentários

Utilize a propriedade **OriginalValue** para retornar o valor do campo original de um campo a partir do registro atual.

No modo de atualização imediata *(no* qual o provedor grava alterações na fonte de dados subjacente depois que você chama o método [Update),](update-method-ado.md) a propriedade **OriginalValue** retorna o valor do campo que existia antes de quaisquer alterações (ou seja, desde a última chamada do método **Update).** Esse é o mesmo valor que o método [CancelUpdate](cancelupdate-method-ado.md) utiliza para substituir a propriedade [Value](value-property-ado.md).

No *modo de atualização em lote* (no qual o provedor armazena em cache várias alterações e as grava na fonte de dados base somente quando você chama o método [UpdateBatch](updatebatch-method-ado.md)), a propriedade **OriginalValue** retorna o valor do campo que existia antes das alterações (isto é, desde a última chamada do método **UpdateBatch**). Esse é o mesmo valor que o método [CancelBatch](cancelbatch-method-ado.md) utiliza para substituir a propriedade **Value**. Quando você utiliza essa propriedade com a propriedade [UnderlyingValue](underlyingvalue-property-ado.md), é possível solucionar conflitos provenientes da atualizações em lote.

## <a name="record"></a>Registro

Para os objetos [Record](record-object-ado.md), a propriedade **OriginalValue** estará em branco nos campos adicionados antes da chamada do [ Update](update-method-ado.md).

