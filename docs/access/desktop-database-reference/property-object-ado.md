---
title: Objeto Property (ADO)
TOCTitle: Property Object (ADO)
ms:assetid: eec318fd-f5ed-d9ef-9830-848439a8914d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250210(v=office.15)
ms:contentKeyID: 48548567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5b3cb4d5caedb6e73bf0819639c1feac12b9d3a8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462379"
---
# <a name="property-object-ado"></a>Objeto Property (ADO)


**Aplica-se a**: Access 2013 | Office 2013

Representa uma característica dinâmica de um objeto ADO definido pelo provedor.

## <a name="remarks"></a>Comentários

Os objetos ADO têm dois tipos de propriedades: internas e dinâmicas.

As propriedades internas são aquelas propriedades implementadas no ADO e estão disponíveis para qualquer novo objeto, usando a sintaxe imediatamente. Essas propriedades não aparecem como objetos **Property** na coleção [Properties](properties-collection-ado.md), por isso, embora você possa alterar seus valores, não será possível modificar suas características.

As propriedades dinâmicas são definidas pelo provedor de dados subjacentes e aparecem na coleção **Properties** referente ao objeto ADO adequado. Por exemplo, uma propriedade específica do provedor pode indicar se um objeto [Recordset](recordset-object-ado.md) oferece suporte a transações ou à atualização. Essas propriedades adicionais serão exibidas como objetos **Property** na coleção **Properties** do objeto **Recordset**. Propriedades dinâmicas podem ser referenciadas somente através da coleção, usando o MyObject.Properties(0) ou ou MyObject.Properties("Name") sintaxe.

Não é possível excluir nenhum tipo de propriedade.

Um objeto **Property** dinâmico tem quatro propriedades internas próprias:

  - A propriedade [Name](name-property-ado.md) é uma cadeia de caracteres que identifica a propriedade.

  - A propriedade [Type](type-property-ado.md) é um número inteiro que especifica o tipo de dados da propriedade.

  - A propriedade [Value](value-property-ado.md) é uma variante que contém a definição da propriedade. **Value** é a propriedade padrão de um objeto **Property**.

  - A propriedade [Attributes](attributes-property-ado.md) é um valor completo que indica as características de uma propriedade específica para o provedor.

