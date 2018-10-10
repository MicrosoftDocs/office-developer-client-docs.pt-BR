---
title: Campo objeto - ActiveX Data Objects (ADO)
TOCTitle: Field Object (ADO)
ms:assetid: 1dbd535e-48ad-a5c8-a1b2-6776c1e3e19d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248968(v=office.15)
ms:contentKeyID: 48543600
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 240cb821ec861d33f22d157207cd62a566b4013a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25461989"
---
# <a name="field-object-ado"></a><span data-ttu-id="28bb6-102">Objeto Field (ADO)</span><span class="sxs-lookup"><span data-stu-id="28bb6-102">Field Object (ADO)</span></span>


<span data-ttu-id="28bb6-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="28bb6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="28bb6-104">Representa uma coluna de dados com um tipo de dados comuns.</span><span class="sxs-lookup"><span data-stu-id="28bb6-104">Represents a column of data with a common data type.</span></span>

## <a name="remarks"></a><span data-ttu-id="28bb6-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="28bb6-105">Remarks</span></span>

<span data-ttu-id="28bb6-p101">Cada objeto **Field** corresponde a uma coluna do [Recordset](recordset-object-ado.md). Use a propriedade [Value](value-property-ado.md) dos objetos **Field** para definir ou retornar dados do registro atual. Dependendo da funcionalidade apresentada pelo provedor, alguns métodos, algumas coleções e propriedades do objeto **Field** poderão não estar disponíveis.</span><span class="sxs-lookup"><span data-stu-id="28bb6-p101">Each **Field** object corresponds to a column in the [Recordset](recordset-object-ado.md). You use the [Value](value-property-ado.md) property of **Field** objects to set or return data for the current record. Depending on the functionality the provider exposes, some collections, methods, or properties of a **Field** object may not be available.</span></span>

<span data-ttu-id="28bb6-109">Com as coleções, os métodos e as propriedades de um objeto **Field**, você pode fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="28bb6-109">With the collections, methods, and properties of a **Field** object, you can do the following:</span></span>

  - <span data-ttu-id="28bb6-110">Retornar o nome de um campo com a propriedade [Name](name-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="28bb6-110">Return the name of a field with the [Name](name-property-ado.md) property.</span></span>

  - <span data-ttu-id="28bb6-p102">Exibir ou alterar os dados do campo com a propriedade **Value**. **Value** é a propriedade padrão do objeto **Field**.</span><span class="sxs-lookup"><span data-stu-id="28bb6-p102">View or change the data in the field with the **Value** property. **Value** is the default property of the **Field** object.</span></span>

  - <span data-ttu-id="28bb6-113">Retornar as características básicas de um campo com as propriedades [Type](type-property-ado.md), [Precision](precision-property-ado.md) e [NumericScale](numericscale-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="28bb6-113">Return the basic characteristics of a field with the [Type](type-property-ado.md), [Precision](precision-property-ado.md), and [NumericScale](numericscale-property-ado.md) properties.</span></span>

  - <span data-ttu-id="28bb6-114">Retornar o tamanho declarado de um campo com a propriedade [DefinedSize](definedsize-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="28bb6-114">Return the declared size of a field with the [DefinedSize](definedsize-property-ado.md) property.</span></span>

  - <span data-ttu-id="28bb6-115">Retornar o tamanho real dos dados em um determinado campo com a propriedade [ActualSize](actualsize-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="28bb6-115">Return the actual size of the data in a given field with the [ActualSize](actualsize-property-ado.md) property.</span></span>

  - <span data-ttu-id="28bb6-116">Determinar quais tipos de funcionalidade serão suportados para um determinado campo com a propriedade [Attributes](attributes-property-ado.md) e a coleção [Properties](properties-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="28bb6-116">Determine what types of functionality are supported for a given field with the [Attributes](attributes-property-ado.md) property and [Properties](properties-collection-ado.md) collection.</span></span>

  - <span data-ttu-id="28bb6-117">Manipular os valores dos campos contendo dados binários longos ou caracteres longos com os métodos [AppendChunk](appendchunk-method-ado.md) e [GetChunk](getchunk-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="28bb6-117">Manipulate the values of fields containing long binary or long character data with the [AppendChunk](appendchunk-method-ado.md) and [GetChunk](getchunk-method-ado.md) methods.</span></span>

  - <span data-ttu-id="28bb6-118">Se o provedor suportar as atualizações, resolver as discrepâncias nos valores do campo durante a atualização das propriedades [OriginalValue](originalvalue-property-ado.md) e [UnderlyingValue](underlyingvalue-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="28bb6-118">If the provider supports batch updates, resolve discrepancies in field values during batch updating with the [OriginalValue](originalvalue-property-ado.md) and [UnderlyingValue](underlyingvalue-property-ado.md) properties.</span></span>

<span data-ttu-id="28bb6-p103">Todas as propriedades de metadados (**Name**, **Type**, **DefinedSize**, **Precision** e **NumericScale**) estarão disponíveis antes da abertura do **Recordset** do objeto **Field**. A definição de todas essas propriedades nesse momento é útil para construir formulários dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="28bb6-p103">All of the metadata properties (**Name**, **Type**, **DefinedSize**, **Precision**, and **NumericScale**) are available before opening the **Field** object's **Recordset**. Setting them at that time is useful for dynamically constructing forms.</span></span>

