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
# <a name="property-object-ado"></a><span data-ttu-id="7f5bd-102">Objeto Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="7f5bd-102">Property Object (ADO)</span></span>


<span data-ttu-id="7f5bd-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7f5bd-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7f5bd-104">Representa uma característica dinâmica de um objeto ADO definido pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="7f5bd-104">Represents a dynamic characteristic of an ADO object that is defined by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f5bd-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f5bd-105">Remarks</span></span>

<span data-ttu-id="7f5bd-106">Os objetos ADO têm dois tipos de propriedades: internas e dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="7f5bd-106">ADO objects have two types of properties: built-in and dynamic.</span></span>

<span data-ttu-id="7f5bd-107">As propriedades internas são aquelas propriedades implementadas no ADO e estão disponíveis para qualquer novo objeto, usando a sintaxe imediatamente.</span><span class="sxs-lookup"><span data-stu-id="7f5bd-107">Built-in properties are those properties implemented in ADO and immediately available to any new object, using the syntax.</span></span> <span data-ttu-id="7f5bd-108">Essas propriedades não aparecem como objetos **Property** na coleção [Properties](properties-collection-ado.md), por isso, embora você possa alterar seus valores, não será possível modificar suas características.</span><span class="sxs-lookup"><span data-stu-id="7f5bd-108">They do not appear as **Property** objects in an object's [Properties](properties-collection-ado.md) collection, so although you can change their values, you cannot modify their characteristics.</span></span>

<span data-ttu-id="7f5bd-109">As propriedades dinâmicas são definidas pelo provedor de dados subjacentes e aparecem na coleção **Properties** referente ao objeto ADO adequado.</span><span class="sxs-lookup"><span data-stu-id="7f5bd-109">Dynamic properties are defined by the underlying data provider, and appear in the **Properties** collection for the appropriate ADO object.</span></span> <span data-ttu-id="7f5bd-110">Por exemplo, uma propriedade específica do provedor pode indicar se um objeto [Recordset](recordset-object-ado.md) oferece suporte a transações ou à atualização.</span><span class="sxs-lookup"><span data-stu-id="7f5bd-110">For example, a property specific to the provider may indicate if a [Recordset](recordset-object-ado.md) object supports transactions or updating.</span></span> <span data-ttu-id="7f5bd-111">Essas propriedades adicionais serão exibidas como objetos **Property** na coleção **Properties** do objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="7f5bd-111">These additional properties will appear as **Property** objects in that **Recordset** object's **Properties** collection.</span></span> <span data-ttu-id="7f5bd-112">Propriedades dinâmicas podem ser referenciadas somente através da coleção, usando o MyObject.Properties(0) ou ou MyObject.Properties("Name") sintaxe.</span><span class="sxs-lookup"><span data-stu-id="7f5bd-112">Dynamic properties can be referenced only through the collection, using the MyObject.Properties(0) or or MyObject.Properties("Name") syntax.</span></span>

<span data-ttu-id="7f5bd-113">Não é possível excluir nenhum tipo de propriedade.</span><span class="sxs-lookup"><span data-stu-id="7f5bd-113">You cannot delete either kind of property.</span></span>

<span data-ttu-id="7f5bd-114">Um objeto **Property** dinâmico tem quatro propriedades internas próprias:</span><span class="sxs-lookup"><span data-stu-id="7f5bd-114">A dynamic **Property** object has four built-in properties of its own:</span></span>

  - <span data-ttu-id="7f5bd-115">A propriedade [Name](name-property-ado.md) é uma cadeia de caracteres que identifica a propriedade.</span><span class="sxs-lookup"><span data-stu-id="7f5bd-115">The [Name](name-property-ado.md) property is a string that identifies the property.</span></span>

  - <span data-ttu-id="7f5bd-116">A propriedade [Type](type-property-ado.md) é um número inteiro que especifica o tipo de dados da propriedade.</span><span class="sxs-lookup"><span data-stu-id="7f5bd-116">The [Type](type-property-ado.md) property is an integer that specifies the property data type.</span></span>

  - <span data-ttu-id="7f5bd-p103">A propriedade [Value](value-property-ado.md) é uma variante que contém a definição da propriedade. **Value** é a propriedade padrão de um objeto **Property**.</span><span class="sxs-lookup"><span data-stu-id="7f5bd-p103">The [Value](value-property-ado.md) property is a variant that contains the property setting. **Value** is the default property for a **Property** object.</span></span>

  - <span data-ttu-id="7f5bd-119">A propriedade [Attributes](attributes-property-ado.md) é um valor completo que indica as características de uma propriedade específica para o provedor.</span><span class="sxs-lookup"><span data-stu-id="7f5bd-119">The [Attributes](attributes-property-ado.md) property is a long value that indicates characteristics of the property specific to the provider.</span></span>

