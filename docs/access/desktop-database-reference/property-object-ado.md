---
title: Objeto Property (ADO)
TOCTitle: Property object (ADO)
ms:assetid: eec318fd-f5ed-d9ef-9830-848439a8914d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250210(v=office.15)
ms:contentKeyID: 48548567
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 262f4873359508a985b27f3d4ea70a5fcbfd620f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302916"
---
# <a name="property-object-ado"></a>Objeto Property (ADO)


**Aplica-se ao:** Access 2013, Office 2013

Representa uma característica dinâmica de um objeto ADO definido pelo provedor.

## <a name="remarks"></a>Comentários

Os objetos ADO têm dois tipos de propriedades: internas e dinâmicas.

Propriedades internas são aquelas implementadas no ADO e disponibilizadas imediatamente para qualquer objeto novo, usando a sintaxe. Essas propriedades não aparecem como objetos **Property** na coleção [Properties](properties-collection-ado.md), por isso, embora você possa alterar seus valores, não será possível modificar suas características.

As propriedades dinâmicas são definidas pelo provedor de dados subjacentes e aparecem na coleção **Properties** referente ao objeto ADO adequado. Por exemplo, uma propriedade específica do provedor pode indicar se um objeto [Recordset](recordset-object-ado.md) oferece suporte a transações ou à atualização. Essas propriedades adicionais serão exibidas como objetos **Property** na coleção **Properties** do objeto **Recordset**. As propriedades dinâmicas podem ser referenciadas somente através da coleção, usando a sintaxe MyObject. Properties (0) ou MyObject. Properties ("Name").

Não é possível excluir nenhum tipo de propriedade.

Um objeto **Property** dinâmico tem quatro propriedades internas próprias:

  - A propriedade [Name](name-property-ado.md) é uma sequência de caracteres que identifica a propriedade.

  - A propriedade [Type](type-property-ado.md) é um inteiro que especifica o tipo de dados da propriedade.

  - A propriedade [Value](value-property-ado.md) é uma variante que contém a definição da propriedade. **Value** é a propriedade padrão de um objeto **Property**.

  - A propriedade [Attributes](attributes-property-ado.md) é um valor completo que indica as características de uma propriedade específica para o provedor.

