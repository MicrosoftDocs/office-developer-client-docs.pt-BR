---
title: Método CreateParameter (ADO)
TOCTitle: CreateParameter Method (ADO)
ms:assetid: cf080a0b-75d2-dcdf-2715-10af147358e9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250026(v=office.15)
ms:contentKeyID: 48547799
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231042
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d851b60500ae3847afb47c574fba83e8399e45d3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868557"
---
# <a name="createparameter-method-ado"></a><span data-ttu-id="ce1de-102">Método CreateParameter (ADO)</span><span class="sxs-lookup"><span data-stu-id="ce1de-102">CreateParameter Method (ADO)</span></span>


<span data-ttu-id="ce1de-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="ce1de-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="ce1de-104">Cria um novo objeto [Parameter](parameter-object-ado.md) com as propriedades especificadas.</span><span class="sxs-lookup"><span data-stu-id="ce1de-104">Creates a new [Parameter](parameter-object-ado.md) object with the specified properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce1de-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ce1de-105">Syntax</span></span>

<span data-ttu-id="ce1de-106">**Definir** *parâmetro*  =  *comando*. CreateParameter (*nome*, *tipo*, *direção*, *tamanho*, *valor*)</span><span class="sxs-lookup"><span data-stu-id="ce1de-106">**Set** *parameter* = *command*.CreateParameter (*Name*, *Type*, *Direction*, *Size*, *Value*)</span></span>

## <a name="return-value"></a><span data-ttu-id="ce1de-107">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ce1de-107">Return value</span></span>

<span data-ttu-id="ce1de-108">Retorna um objeto **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="ce1de-108">Returns a **Parameter** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="ce1de-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce1de-109">Parameters</span></span>

  - <span data-ttu-id="ce1de-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="ce1de-110">*Name*</span></span>

  - <span data-ttu-id="ce1de-p101">Opcional. Um valor **String** que contém o nome do objeto **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="ce1de-p101">Optional. A **String** value that contains the name of the **Parameter** object.</span></span>

  - <span data-ttu-id="ce1de-113">*Type*</span><span class="sxs-lookup"><span data-stu-id="ce1de-113">*Type*</span></span>

  - <span data-ttu-id="ce1de-p102">Opcional. Um valor [DataTypeEnum](datatypeenum.md) que especifica o tipo de dados do objeto **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="ce1de-p102">Optional. A [DataTypeEnum](datatypeenum.md) value that specifies the data type of the **Parameter** object.</span></span>

  - <span data-ttu-id="ce1de-116">*Direction*</span><span class="sxs-lookup"><span data-stu-id="ce1de-116">*Direction*</span></span>

  - <span data-ttu-id="ce1de-p103">Opcional. Um valor [ParameterDirectionEnum](parameterdirectionenum.md) que especifica o tipo do objeto **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="ce1de-p103">Optional. A [ParameterDirectionEnum](parameterdirectionenum.md) value that specifies the type of **Parameter** object.</span></span>

  - <span data-ttu-id="ce1de-119">*Size*</span><span class="sxs-lookup"><span data-stu-id="ce1de-119">*Size*</span></span>

  - <span data-ttu-id="ce1de-p104">Opcional. Um valor **Long** que especifica o comprimento máximo do valor do parâmetro em caracteres ou bytes.</span><span class="sxs-lookup"><span data-stu-id="ce1de-p104">Optional. A **Long** value that specifies the maximum length for the parameter value in characters or bytes.</span></span>

  - <span data-ttu-id="ce1de-122">*Value*</span><span class="sxs-lookup"><span data-stu-id="ce1de-122">*Value*</span></span>

  - <span data-ttu-id="ce1de-p105">Opcional. Uma **Variant** que especifica o valor do objeto **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="ce1de-p105">Optional. A **Variant** that specifies the value for the **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce1de-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="ce1de-125">Remarks</span></span>

<span data-ttu-id="ce1de-p106">Utilize o método **CreateParameter** para criar um novo objeto **Parameter** com um nome, tipo, direção, tamanho e valor especificados. Quaisquer valores passados nos argumentos são gravados nas propriedades correspondentes de **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="ce1de-p106">Use the **CreateParameter** method to create a new **Parameter** object with a specified name, type, direction, size, and value. Any values you pass in the arguments are written to the corresponding **Parameter** properties.</span></span>

<span data-ttu-id="ce1de-p107">Esse método não acrescenta automaticamente o objeto **Parameter** na coleção **Parameters** de um objeto [Command](command-object-ado.md). Isso permite definir propriedades adicionais cujos valores o ADO validará quando você acrescentar o objeto **Parameter** na coleção.</span><span class="sxs-lookup"><span data-stu-id="ce1de-p107">This method does not automatically append the **Parameter** object to the **Parameters** collection of a [Command](command-object-ado.md) object. This lets you set additional properties whose values ADO will validate when you append the **Parameter** object to the collection.</span></span>

<span data-ttu-id="ce1de-130">Se você especificar um tipo de dados de comprimento variável no argumento de *tipo* , você deve passar um argumento de *tamanho* ou definir a propriedade [Size](size-property-ado.md) do objeto **Parameter** antes de acrescentá-lo à coleção **Parameters** ; Caso contrário, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="ce1de-130">If you specify a variable-length data type in the *Type* argument, you must either pass a *Size* argument or set the [Size](size-property-ado.md) property of the **Parameter** object before appending it to the **Parameters** collection; otherwise, an error occurs.</span></span>

<span data-ttu-id="ce1de-131">Se você especificar um tipo de dados numérico (**adNumeric** ou **adDecimal**) no argumento *Type*, também deverá definir as propriedades [NumericScale](numericscale-property-ado.md) e [Precision](precision-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ce1de-131">If you specify a numeric data type (**adNumeric** or **adDecimal**) in the *Type* argument, then you must also set the [NumericScale](numericscale-property-ado.md) and [Precision](precision-property-ado.md) properties.</span></span>

