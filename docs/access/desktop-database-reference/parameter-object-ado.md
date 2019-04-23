---
title: Objeto Parameter (ADO)
TOCTitle: Parameter object (ADO)
ms:assetid: 7577598e-3d0c-30c6-5f24-1cfe98791798
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249481(v=office.15)
ms:contentKeyID: 48545676
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d6f3acd4af280f30706e35eb7ecda1dee11aa7d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288074"
---
# <a name="parameter-object-ado"></a>Objeto Parameter (ADO)


**Aplica-se ao:** Access 2013, Office 2013

Representa um parâmetro ou argumento associado ao objeto [Command](command-object-ado.md) com base em uma consulta parametrizada ou em um procedimento armazenado.

## <a name="remarks"></a>Comentários

Muitos provedores suportam comandos parametrizados. Esses são comandos no quais a ação deseja é definida uma vez, mas as variáveis (ou parâmetros) são usados para alterar alguns detalhes do comando. Por exemplo, uma instrução SQL SELECT poderia usar um parâmetro para definir os critérios de correspondência de uma cláusula WHERE e outro para definir o nome da coluna de uma cláusula SORT BY.

Os objetos **Parameter** representam os parâmetros associados à consultas parametrizadas ou aos argumentos de entrada/saída e os valores de retorno de procedimentos armazenados. Dependendo da funcionalidade do provedor, alguns métodos e algumas coleções e propriedades de um objeto **Parameter** podem não estar disponíveis.

Com as coleções, os métodos e as propriedades de um objeto **Parameter**, você pode fazer o seguinte:

  - Definir ou retornar o nome de um parâmetro com a propriedade [Name](name-property-ado.md).

  - Definir ou retornar o valor de um parâmetro com a propriedade [Value](value-property-ado.md). **Value** é a propriedade padrão do objeto **Parameter**.

  - Definir ou retornar as características do parâmetro com as propriedades [Attributes](attributes-property-ado.md), [Direction](direction-property-ado.md), [Precision](precision-property-ado.md), [NumericScale](numericscale-property-ado.md), [Size](size-property-ado.md) e [Type](type-property-ado.md).

  - Passar os dados binários longos ou os dados de caracteres para um parâmetro com o método [AppendChunk](appendchunk-method-ado.md).

  - Acessar os atributos específicos do provedor com a coleção [Properties](properties-collection-ado.md).

Se você souber os nomes e as propriedades dos parâmetros associados ao procedimento armazenado ou à consulta parametrizada que será chamada, use o método [CreateParameter](createparameter-method-ado.md) para criar objetos **Parameter** com as definições de propriedade adequadas e use o método [Append](append-method-ado.md) para adicioná-las à coleção [Parameters](parameters-collection-ado.md). Isso permite a definição e o retorno dos valores do parâmetro sem ter de chamar o método [Refresh](refresh-method-ado.md) na coleção **Parameters** para recuperar as informações do parâmetro a partir do provedor, uma operação de recursos potencialmente intensivos.

