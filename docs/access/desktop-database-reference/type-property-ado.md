---
title: Propriedade Type (ADO)
TOCTitle: Type property (ADO)
ms:assetid: 14d99172-2145-05ae-620b-459ba097f05c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248914(v=office.15)
ms:contentKeyID: 48543397
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 34a5d1cb1750dc9803c62202a06feccc2d464f9b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698250"
---
# <a name="type-property-ado"></a>Propriedade Type (ADO)


**Aplica-se a**: Access 2013, o Office 2013

Indica o tipo operacional ou o tipo de dados de um objeto [Parameter](parameter-object-ado.md), [Field](field-object-ado.md) ou [Property](property-object-ado.md).

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor [DataTypeEnum](datatypeenum.md).

## <a name="remarks"></a>Comentários

Para os objetos **Parameter**, a propriedade **Type** é leitura/gravação. Para novos objetos **Field** que foram acrescentados à coleção [Fields](fields-collection-ado.md) de um [Record](record-object-ado.md), **Type** é leitura/gravação somente depois que a propriedade [Value](value-property-ado.md) para o **Field** for especificada e o provedor de dados adicionar com êxito o novo **Field** chamando o método [Update](update-method-ado.md) da coleção **Fields**.

Para todos os outros objetos, a propriedade **Type** é somente leitura.

