---
title: Propriedade Size (ADO)
TOCTitle: Size property (ADO)
ms:assetid: 24596b5c-b1cc-e97e-68b6-8ff53baf150b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249017(v=office.15)
ms:contentKeyID: 48543753
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 03434b0227c5110ac3a1f36512aaaebd5c23c97a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876404"
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

