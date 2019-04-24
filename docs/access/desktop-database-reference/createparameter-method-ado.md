---
title: Método createParameter (ADO)
TOCTitle: CreateParameter method (ADO)
ms:assetid: cf080a0b-75d2-dcdf-2715-10af147358e9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250026(v=office.15)
ms:contentKeyID: 48547799
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231042
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: fa060811f60379e720e06be9f94e9403477c7869
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295384"
---
# <a name="createparameter-method-ado"></a><span data-ttu-id="727ae-102">Método createParameter (ADO)</span><span class="sxs-lookup"><span data-stu-id="727ae-102">CreateParameter method (ADO)</span></span>

<span data-ttu-id="727ae-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="727ae-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="727ae-104">Cria um novo objeto [Parameter](parameter-object-ado.md) com as propriedades especificadas.</span><span class="sxs-lookup"><span data-stu-id="727ae-104">Creates a new [Parameter](parameter-object-ado.md) object with the specified properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="727ae-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="727ae-105">Syntax</span></span>

<span data-ttu-id="727ae-106">**Definir** *parâmetro*  =  *comando*. CreateParameter (*nome*, *tipo*, *direção*, *tamanho*, *valor*)</span><span class="sxs-lookup"><span data-stu-id="727ae-106">**Set** *parameter* = *command*.CreateParameter (*Name*, *Type*, *Direction*, *Size*, *Value*)</span></span>

## <a name="return-value"></a><span data-ttu-id="727ae-107">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="727ae-107">Return value</span></span>

<span data-ttu-id="727ae-108">Retorna um objeto **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="727ae-108">Returns a **Parameter** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="727ae-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="727ae-109">Parameters</span></span>

|<span data-ttu-id="727ae-110">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="727ae-110">Parameter</span></span>|<span data-ttu-id="727ae-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="727ae-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="727ae-112">*Name*</span><span class="sxs-lookup"><span data-stu-id="727ae-112">*Name*</span></span> |<span data-ttu-id="727ae-p101">Opcional. Um valor **String** que contém o nome do objeto **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="727ae-p101">Optional. A **String** value that contains the name of the **Parameter** object.</span></span>|
|<span data-ttu-id="727ae-115">*Type*</span><span class="sxs-lookup"><span data-stu-id="727ae-115">*Type*</span></span> |<span data-ttu-id="727ae-p102">Opcional. Um valor [DataTypeEnum](datatypeenum.md) que especifica o tipo de dados do objeto **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="727ae-p102">Optional. A [DataTypeEnum](datatypeenum.md) value that specifies the data type of the **Parameter** object.</span></span>|
|<span data-ttu-id="727ae-118">*Direction*</span><span class="sxs-lookup"><span data-stu-id="727ae-118">*Direction*</span></span> |<span data-ttu-id="727ae-p103">Opcional. Um valor [ParameterDirectionEnum](parameterdirectionenum.md) que especifica o tipo do objeto **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="727ae-p103">Optional. A [ParameterDirectionEnum](parameterdirectionenum.md) value that specifies the type of **Parameter** object.</span></span>|
|<span data-ttu-id="727ae-121">*Size*</span><span class="sxs-lookup"><span data-stu-id="727ae-121">*Size*</span></span> |<span data-ttu-id="727ae-p104">Opcional. Um valor **Long** que especifica o comprimento máximo do valor do parâmetro em caracteres ou bytes.</span><span class="sxs-lookup"><span data-stu-id="727ae-p104">Optional. A **Long** value that specifies the maximum length for the parameter value in characters or bytes.</span></span>|
|<span data-ttu-id="727ae-124">*Value*</span><span class="sxs-lookup"><span data-stu-id="727ae-124">*Value*</span></span> |<span data-ttu-id="727ae-p105">Opcional. Uma **Variant** que especifica o valor do objeto **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="727ae-p105">Optional. A **Variant** that specifies the value for the **Parameter** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="727ae-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="727ae-127">Remarks</span></span>

<span data-ttu-id="727ae-p106">Utilize o método **CreateParameter** para criar um novo objeto **Parameter** com um nome, tipo, direção, tamanho e valor especificados. Quaisquer valores passados nos argumentos são gravados nas propriedades correspondentes de **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="727ae-p106">Use the **CreateParameter** method to create a new **Parameter** object with a specified name, type, direction, size, and value. Any values you pass in the arguments are written to the corresponding **Parameter** properties.</span></span>

<span data-ttu-id="727ae-p107">Esse método não acrescenta automaticamente o objeto **Parameter** na coleção **Parameters** de um objeto [Command](command-object-ado.md). Isso permite definir propriedades adicionais cujos valores o ADO validará quando você acrescentar o objeto **Parameter** na coleção.</span><span class="sxs-lookup"><span data-stu-id="727ae-p107">This method does not automatically append the **Parameter** object to the **Parameters** collection of a [Command](command-object-ado.md) object. This lets you set additional properties whose values ADO will validate when you append the **Parameter** object to the collection.</span></span>

<span data-ttu-id="727ae-132">Se você especificar um tipo de dados de comprimento variável no argumento *Type*, deverá passar um argumento *Size* ou definir a propriedade [Size](size-property-ado.md) do objeto **Parameter** antes de acrescentá-lo na coleção **Parameters**; caso contrário, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="727ae-132">If you specify a variable-length data type in the *Type* argument, you must either pass a *Size* argument or set the [Size](size-property-ado.md) property of the **Parameter** object before appending it to the **Parameters** collection; otherwise, an error occurs.</span></span>

<span data-ttu-id="727ae-133">Se você especificar um tipo de dados numérico (**adNumeric** ou **adDecimal**) no argumento *Type*, também deverá definir as propriedades [NumericScale](numericscale-property-ado.md) e [Precision](precision-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="727ae-133">If you specify a numeric data type (**adNumeric** or **adDecimal**) in the *Type* argument, then you must also set the [NumericScale](numericscale-property-ado.md) and [Precision](precision-property-ado.md) properties.</span></span>

