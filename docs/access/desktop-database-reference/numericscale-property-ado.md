---
title: Propriedade NumericScale (ADO)
TOCTitle: NumericScale property (ADO)
ms:assetid: 51b232d2-5bfd-521c-f4e9-65655ecc7c70
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249263(v=office.15)
ms:contentKeyID: 48544824
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1bcb0c1a38108fbd02551df2a3296abe4d9a3791
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288550"
---
# <a name="numericscale-property-ado"></a>Propriedade NumericScale (ADO)


**Aplica-se ao:** Access 2013, Office 2013

Indica a escala de valores numéricos em um objeto [Parameter](parameter-object-ado.md) ou [Field](field-object-ado.md).

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **Byte** que indica o número de casas decimais para as quais os valores numéricos serão resolvidos.

## <a name="remarks"></a>Comentários

Use a propriedade **NumericScale** para determinar quantos dígitos à direita da vírgula decimal serão usados para representar valores de um objeto numérico **Parameter** ou **Field**.

Em objetos **Parameter**, a propriedade **NumericScale** é leitura/gravação.

Em um objeto **Field**, **NumericScale** normalmente é somente leitura. No entanto, para novos objetos **Field** que foram acrescentados à coleção [Fields](fields-collection-ado.md) de um [Record](record-object-ado.md), **NumericScale** será leitura/gravação apenas depois que a propriedade [Value](value-property-ado.md) para o **Field** for especificada e o provedor de dados tiver adicionado com sucesso o novo **Field** chamando o método [Update](update-method-ado.md) da coleção **Fields**.

