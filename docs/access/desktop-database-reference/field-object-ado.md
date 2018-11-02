---
title: Campo objeto - ActiveX Data Objects (ADO)
TOCTitle: Field object (ADO)
ms:assetid: 1dbd535e-48ad-a5c8-a1b2-6776c1e3e19d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248968(v=office.15)
ms:contentKeyID: 48543600
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d131f2634551c9c2538a87cdc8f15cfa6cc96430
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924866"
---
# <a name="field-object-ado"></a>Objeto Field (ADO)


**Aplica-se a**: Access 2013, o Office 2013

Representa uma coluna de dados com um tipo de dados comuns.

## <a name="remarks"></a>Comentários

Cada objeto **Field** corresponde a uma coluna do [Recordset](recordset-object-ado.md). Use a propriedade [Value](value-property-ado.md) dos objetos **Field** para definir ou retornar dados do registro atual. Dependendo da funcionalidade apresentada pelo provedor, alguns métodos, algumas coleções e propriedades do objeto **Field** poderão não estar disponíveis.

Com as coleções, os métodos e as propriedades de um objeto **Field**, você pode fazer o seguinte:

  - Retornar o nome de um campo com a propriedade [Name](name-property-ado.md).

  - Exibir ou alterar os dados do campo com a propriedade **Value**. **Value** é a propriedade padrão do objeto **Field**.

  - Retornar as características básicas de um campo com as propriedades [Type](type-property-ado.md), [Precision](precision-property-ado.md) e [NumericScale](numericscale-property-ado.md).

  - Retornar o tamanho declarado de um campo com a propriedade [DefinedSize](definedsize-property-ado.md).

  - Retornar o tamanho real dos dados em um determinado campo com a propriedade [ActualSize](actualsize-property-ado.md).

  - Determinar quais tipos de funcionalidade serão suportados para um determinado campo com a propriedade [Attributes](attributes-property-ado.md) e a coleção [Properties](properties-collection-ado.md).

  - Manipular os valores dos campos contendo dados binários longos ou caracteres longos com os métodos [AppendChunk](appendchunk-method-ado.md) e [GetChunk](getchunk-method-ado.md).

  - Se o provedor suportar as atualizações, resolver as discrepâncias nos valores do campo durante a atualização das propriedades [OriginalValue](originalvalue-property-ado.md) e [UnderlyingValue](underlyingvalue-property-ado.md).

Todas as propriedades de metadados (**Name**, **Type**, **DefinedSize**, **Precision** e **NumericScale**) estarão disponíveis antes da abertura do **Recordset** do objeto **Field**. A definição de todas essas propriedades nesse momento é útil para construir formulários dinamicamente.

