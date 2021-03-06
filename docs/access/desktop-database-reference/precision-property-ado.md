---
title: Propriedade Precision (ADO)
TOCTitle: Precision property (ADO)
ms:assetid: c9d54d78-d5a5-caf8-d635-259d1fcc0595
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249983(v=office.15)
ms:contentKeyID: 48547685
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 662e5e9287da1ccfb81c727f5d5e5dfedce2969b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287472"
---
# <a name="precision-property-ado"></a>Propriedade Precision (ADO)


**Aplica-se ao:** Access 2013, Office 2013

Indica o grau de precisão de valores numéricos em um objeto [Parameter](parameter-object-ado.md) ou de objetos [Field](field-object-ado.md) numéricos.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **Byte** que indica o número máximo de dígitos utilizado para representar os valores.

## <a name="remarks"></a>Comentários

Utilize a propriedade **Precision** para determinar o número máximo de dígitos utilizado para representar os valores de um objeto numérico **Parameter** ou **Field**.

O valor é leitura/gravação em um objeto **Parameter**.

Para um objeto **Field**, a propriedade **Precision** normalmente é somente leitura. Entretanto, para novos objetos **Field** que tenham sido acrescentados à coleção [Fields](fields-collection-ado.md) de um [Record](record-object-ado.md), **Precision** será leitura/gravação somente depois que a propriedade [Value](value-property-ado.md) de **Field** tiver sido especificada e o provedor de dados tiver adicionado com êxito o novo **Field** por meio da chamada do método [Update](update-method-ado.md) da coleção **Fields**.

