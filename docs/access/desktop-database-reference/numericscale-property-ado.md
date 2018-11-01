---
title: Propriedade NumericScale (ADO)
TOCTitle: NumericScale property (ADO)
ms:assetid: 51b232d2-5bfd-521c-f4e9-65655ecc7c70
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249263(v=office.15)
ms:contentKeyID: 48544824
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eb2c799fd7c9d1cc74c6081c10f7a8d356e79faf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876012"
---
# <a name="numericscale-property-ado"></a>Propriedade NumericScale (ADO)


**Aplica-se a**: Access 2013, o Office 2013

Indica a escala de valores numéricos em um objeto [Parameter](parameter-object-ado.md) ou [Field](field-object-ado.md).

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **Byte** que indica o número de casas decimais para as quais os valores numéricos serão resolvidos.

## <a name="remarks"></a>Comentários

Use a propriedade **NumericScale** para determinar quantos dígitos à direita da vírgula decimal serão usados para representar valores de um objeto numérico **Parameter** ou **Field**.

Em objetos **Parameter**, a propriedade **NumericScale** é leitura/gravação.

Em um objeto **Field**, **NumericScale** normalmente é somente leitura. No entanto, para novos objetos **Field** que foram acrescentados à coleção [Fields](fields-collection-ado.md) de um [Record](record-object-ado.md), **NumericScale** será leitura/gravação apenas depois que a propriedade [Value](value-property-ado.md) para o **Field** for especificada e o provedor de dados tiver adicionado com sucesso o novo **Field** chamando o método [Update](update-method-ado.md) da coleção **Fields**.

