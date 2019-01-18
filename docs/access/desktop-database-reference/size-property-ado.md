---
title: Propriedade Size (ADO)
TOCTitle: Size property (ADO)
ms:assetid: 24596b5c-b1cc-e97e-68b6-8ff53baf150b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249017(v=office.15)
ms:contentKeyID: 48543753
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2a1bed3454d081b9d5de3a01e9b326130b40baa4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711606"
---
# <a name="size-property-ado"></a>Propriedade Size (ADO)


**Aplica-se a**: Access 2013, o Office 2013

Indica o tamanho máximo, em bytes ou caracteres, de um objeto [Parameter](parameter-object-ado.md).

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **Long** que indica o tamanho máximo em bytes ou caracteres de um valor em um objeto **Parameter**.

## <a name="remarks"></a>Comentários

Utilize a propriedade **Size** para determinar o tamanho máximo dos valores gravados em ou lidos a partir da propriedade [Value](value-property-ado.md) de um objeto **Parameter**.

Se você especificar um tipo de dados de tamanho variável para um objeto **Parameter** (por exemplo, qualquer tipo **String**, como **adVarChar**), será preciso definir a propriedade **Size** do objeto antes de acrescentá-lo à coleção [Parameters](parameters-collection-ado.md); caso contrário, ocorrerá um erro.

Se você já tiver acrescentado o objeto **Parameter** à coleção **Parameters** de um objeto [Command](command-object-ado.md) e você alterar seu tipo para um tipo de dados de tamanho variável, será preciso definir a propriedade **Size** do objeto **Parameter** antes de executar o objeto **Command**; caso contrário, ocorrerá um erro.

Se você utilizar o método [Refresh](refresh-method-ado.md) para obter as informações de parâmetro a partir de um provedor e ele retornar um ou mais objetos **Parameter** de tipo de dados de tamanho variável, o ADO poderá alocar memória para os parâmetros com base em seu potencial máximo de tamanho, o que poderia causar um erro durante a execução. Para evitar um erro, você deve definir explicitamente a propriedade **Size** para esses parâmetros antes de executar o comando.

A propriedade **Size** é leitura/gravação.

