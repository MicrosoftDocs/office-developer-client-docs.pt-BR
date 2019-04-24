---
title: Propriedade Attributes (ADO)
TOCTitle: Attributes property (ADO)
ms:assetid: 4cc1f036-606e-7d4b-d270-af374e9d99fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249242(v=office.15)
ms:contentKeyID: 48544716
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231117
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 6495c70f64930e1b335c603f13e720ad581203a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296980"
---
# <a name="attributes-property-ado"></a>Propriedade Attributes (ADO)


**Aplica-se ao:** Access 2013, Office 2013


## <a name="attributes-property"></a>Propriedade Attributes

Indica uma ou mais características de um objeto.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **Long**.

Em um objeto [Connection](connection-object-ado.md), a propriedade **Attributes** é leitura/gravação e seu valor pode ser a soma de um ou mais valores [XactAttributeEnum](xactattributeenum.md). O padrão é zero (0).

Em um objeto [Parameter](parameter-object-ado.md), a propriedade **Attributes** é leitura/gravação e seu valor pode ser a soma de um ou mais valores [ParameterAttributesEnum](parameterattributesenum.md). O padrão é **adParamSigned**.

Em um objeto [Field](field-object-ado.md), a propriedade **Attributes** pode ser a soma de um ou mais valores [FieldAttributeEnum](fieldattributeenum.md). Normalmente, ela é somente leitura. Contudo, para novos objetos **Field** que tenham sido acrescentados à coleção [Field](fields-collection-ado.md) de um [Record](record-object-ado.md), **Attributes** será leitura/gravação apenas depois que a propriedade [Value](value-property-ado.md) para o **Field** tiver sido especificada e o novo **Field** tiver sido adicionado com sucesso pelo provedor de dados chamando o método [Update](update-method-ado.md) da coleção **Fields**.

Em um objeto [Property](property-object-ado.md), a propriedade **Attributes** é somente leitura e seu valor pode ser a soma de um ou mais valores [PropertyAttributesEnum](propertyattributesenum.md).

## <a name="remarks"></a>Comentários

Use a propriedade **Attributes** para definir ou retornar características de objetos **Connection**, **Parameter**, [Field](field-object-ado.md) ou [Property](property-object-ado.md).

Quando vários atributos são definidos, é possível somar as constantes adequadas. A definição do valor de propriedade para uma soma, incluindo constantes incompatíveis, provocará um erro.

**Uso do Remote Data Service** Esta propriedade não está disponível em um objeto **Connection** do lado do cliente.

