---
title: Propriedade Type (ADO)
TOCTitle: Type Property (ADO)
ms:assetid: 14d99172-2145-05ae-620b-459ba097f05c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248914(v=office.15)
ms:contentKeyID: 48543397
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2ac119b9582634e619455870c8a2e115f5e8dafa
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462871"
---
# <a name="type-property-ado"></a>Propriedade Type (ADO)


**Aplica-se a**: Access 2013 | Office 2013

Indica o tipo operacional ou o tipo de dados de um objeto [Parameter](parameter-object-ado.md), [Field](field-object-ado.md) ou [Property](property-object-ado.md).

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor [DataTypeEnum](datatypeenum.md).

## <a name="remarks"></a>Comentários

Para os objetos **Parameter**, a propriedade **Type** é leitura/gravação. Para novos objetos **Field** que foram acrescentados à coleção [Fields](fields-collection-ado.md) de um [Record](record-object-ado.md), **Type** é leitura/gravação somente depois que a propriedade [Value](value-property-ado.md) para o **Field** for especificada e o provedor de dados adicionar com êxito o novo **Field** chamando o método [Update](update-method-ado.md) da coleção **Fields**.

Para todos os outros objetos, a propriedade **Type** é somente leitura.

