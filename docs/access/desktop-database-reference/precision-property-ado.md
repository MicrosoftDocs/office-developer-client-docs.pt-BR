---
title: Propriedade Precision (ADO)
TOCTitle: Precision property (ADO)
ms:assetid: c9d54d78-d5a5-caf8-d635-259d1fcc0595
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249983(v=office.15)
ms:contentKeyID: 48547685
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: db2000c2db48215df42b5cd81fb35be0f0c4be9b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869957"
---
# <a name="precision-property-ado"></a>Propriedade Precision (ADO)


**Aplica-se a**: Access 2013, o Office 2013

Indica o grau de precisão de valores numéricos em um objeto [Parameter](parameter-object-ado.md) ou de objetos [Field](field-object-ado.md) numéricos.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **Byte** que indica o número máximo de dígitos utilizado para representar os valores.

## <a name="remarks"></a>Comentários

Utilize a propriedade **Precision** para determinar o número máximo de dígitos utilizado para representar os valores de um objeto numérico **Parameter** ou **Field**.

O valor é leitura/gravação em um objeto **Parameter**.

Para um objeto **Field**, a propriedade **Precision** normalmente é somente leitura. Entretanto, para novos objetos **Field** que tenham sido acrescentados à coleção [Fields](fields-collection-ado.md) de um [Record](record-object-ado.md), **Precision** será leitura/gravação somente depois que a propriedade [Value](value-property-ado.md) de **Field** tiver sido especificada e o provedor de dados tiver adicionado com êxito o novo **Field** por meio da chamada do método [Update](update-method-ado.md) da coleção **Fields**.

