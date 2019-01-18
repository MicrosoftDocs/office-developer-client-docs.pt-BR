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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717976"
---
# <a name="attributes-property-ado"></a><span data-ttu-id="e2eb9-102">Propriedade Attributes (ADO)</span><span class="sxs-lookup"><span data-stu-id="e2eb9-102">Attributes property (ADO)</span></span>


<span data-ttu-id="e2eb9-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="e2eb9-103">**Applies to**: Access 2013, Office 2013</span></span>


## <a name="attributes-property"></a><span data-ttu-id="e2eb9-104">Propriedade Attributes</span><span class="sxs-lookup"><span data-stu-id="e2eb9-104">Attributes Property</span></span>

<span data-ttu-id="e2eb9-105">Indica uma ou mais características de um objeto.</span><span class="sxs-lookup"><span data-stu-id="e2eb9-105">Indicates one or more characteristics of an object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="e2eb9-106">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="e2eb9-106">Settings and return values</span></span>

<span data-ttu-id="e2eb9-107">Define ou retorna um valor **Long**.</span><span class="sxs-lookup"><span data-stu-id="e2eb9-107">Sets or returns a **Long** value.</span></span>

<span data-ttu-id="e2eb9-p101">Em um objeto [Connection](connection-object-ado.md), a propriedade **Attributes** é leitura/gravação e seu valor pode ser a soma de um ou mais valores [XactAttributeEnum](xactattributeenum.md). O padrão é zero (0).</span><span class="sxs-lookup"><span data-stu-id="e2eb9-p101">For a [Connection](connection-object-ado.md) object, the **Attributes** property is read/write, and its value can be the sum of one or more [XactAttributeEnum](xactattributeenum.md) values. The default is zero (0).</span></span>

<span data-ttu-id="e2eb9-p102">Em um objeto [Parameter](parameter-object-ado.md), a propriedade **Attributes** é leitura/gravação e seu valor pode ser a soma de um ou mais valores [ParameterAttributesEnum](parameterattributesenum.md). O padrão é **adParamSigned**.</span><span class="sxs-lookup"><span data-stu-id="e2eb9-p102">For a [Parameter](parameter-object-ado.md) object, the **Attributes** property is read/write, and its value can be the sum of any one or more [ParameterAttributesEnum](parameterattributesenum.md) values. The default is **adParamSigned**.</span></span>

<span data-ttu-id="e2eb9-p103">Em um objeto [Field](field-object-ado.md), a propriedade **Attributes** pode ser a soma de um ou mais valores [FieldAttributeEnum](fieldattributeenum.md). Normalmente, ela é somente leitura. Contudo, para novos objetos **Field** que tenham sido acrescentados à coleção [Field](fields-collection-ado.md) de um [Record](record-object-ado.md), **Attributes** será leitura/gravação apenas depois que a propriedade [Value](value-property-ado.md) para o **Field** tiver sido especificada e o novo **Field** tiver sido adicionado com sucesso pelo provedor de dados chamando o método [Update](update-method-ado.md) da coleção **Fields**.</span><span class="sxs-lookup"><span data-stu-id="e2eb9-p103">For a [Field](field-object-ado.md) object, the **Attributes** property can be the sum of one or more [FieldAttributeEnum](fieldattributeenum.md) values. It is normally read-only, However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Attributes** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the new **Field** has been successfully added by the data provider by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="e2eb9-114">Em um objeto [Property](property-object-ado.md), a propriedade **Attributes** é somente leitura e seu valor pode ser a soma de um ou mais valores [PropertyAttributesEnum](propertyattributesenum.md).</span><span class="sxs-lookup"><span data-stu-id="e2eb9-114">For a [Property](property-object-ado.md) object, the **Attributes** property is read-only, and its value can be the sum of any one or more [PropertyAttributesEnum](propertyattributesenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2eb9-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2eb9-115">Remarks</span></span>

<span data-ttu-id="e2eb9-116">Use a propriedade **Attributes** para definir ou retornar características de objetos **Connection**, **Parameter**, [Field](field-object-ado.md) ou [Property](property-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="e2eb9-116">Use the **Attributes** property to set or return characteristics of **Connection** objects, **Parameter** objects, [Field](field-object-ado.md) objects, or [Property](property-object-ado.md) objects.</span></span>

<span data-ttu-id="e2eb9-p104">Quando vários atributos são definidos, é possível somar as constantes adequadas. A definição do valor de propriedade para uma soma, incluindo constantes incompatíveis, provocará um erro.</span><span class="sxs-lookup"><span data-stu-id="e2eb9-p104">When you set multiple attributes, you can sum the appropriate constants. If you set the property value to a sum including incompatible constants, an error occurs.</span></span>

<span data-ttu-id="e2eb9-119">**Uso de serviço de dados remotos** Essa propriedade não está disponível em um objeto de **Conexão** do cliente.</span><span class="sxs-lookup"><span data-stu-id="e2eb9-119">**Remote Data Service Usage**This property is not available on a client-side **Connection** object.</span></span>

