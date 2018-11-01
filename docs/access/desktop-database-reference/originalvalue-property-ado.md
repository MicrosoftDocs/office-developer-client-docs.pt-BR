---
title: Propriedade OriginalValue (ADO)
TOCTitle: OriginalValue property (ADO)
ms:assetid: 02ffc728-4692-d439-e2a6-2f02cca53a71
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248798(v=office.15)
ms:contentKeyID: 48542974
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 872e7c88e5ea4e79d6bff4aa590e72743feb3893
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884909"
---
# <a name="originalvalue-property-ado"></a><span data-ttu-id="dd548-102">Propriedade OriginalValue (ADO)</span><span class="sxs-lookup"><span data-stu-id="dd548-102">OriginalValue property (ADO)</span></span>

<span data-ttu-id="dd548-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="dd548-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dd548-104">Indica o valor de um [Field](field-object-ado.md) que existia no registro antes de as alterações serem efetuadas.</span><span class="sxs-lookup"><span data-stu-id="dd548-104">Indicates the value of a [Field](field-object-ado.md) that existed in the record before any changes were made.</span></span>

## <a name="return-value"></a><span data-ttu-id="dd548-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="dd548-105">Return value</span></span>

<span data-ttu-id="dd548-106">Retorna um valor **Variant** que representa o valor de um campo antes de qualquer alteração.</span><span class="sxs-lookup"><span data-stu-id="dd548-106">Returns a **Variant** value that represents the value of a field prior to any change.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd548-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="dd548-107">Remarks</span></span>

<span data-ttu-id="dd548-108">Utilize a propriedade **OriginalValue** para retornar o valor do campo original de um campo a partir do registro atual.</span><span class="sxs-lookup"><span data-stu-id="dd548-108">Use the **OriginalValue** property to return the original field value for a field from the current record.</span></span>

<span data-ttu-id="dd548-109">No *modo de atualização imediata* (no qual o provedor grava as alterações à fonte de dados subjacente depois de chamar o método [Update](update-method-ado.md) ), a propriedade **OriginalValue** retorna o valor do campo que se encontrava antes que quaisquer alterações (ou seja, desde que o última chamada de método de **atualização** ).</span><span class="sxs-lookup"><span data-stu-id="dd548-109">In *immediate update mode* (in which the provider writes changes to the underlying data source after you call the [Update](update-method-ado.md) method), the **OriginalValue** property returns the field value that existed prior to any changes (that is, since the last **Update** method call).</span></span> <span data-ttu-id="dd548-110">Esse é o mesmo valor que o método [CancelUpdate](cancelupdate-method-ado.md) utiliza para substituir a propriedade [Value](value-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="dd548-110">This is the same value that the [CancelUpdate](cancelupdate-method-ado.md) method uses to replace the [Value](value-property-ado.md) property.</span></span>

<span data-ttu-id="dd548-111">No *modo de atualização em lotes* (no qual o provedor caches várias alterações e grava-los à fonte de dados subjacente somente quando você chamar o método [UpdateBatch](updatebatch-method-ado.md) ), a propriedade **OriginalValue** retorna o valor do campo que se encontrava antes de qualquer um altera (ou seja, desde o último método **UpdateBatch** é chamada).</span><span class="sxs-lookup"><span data-stu-id="dd548-111">In *batch update mode* (in which the provider caches multiple changes and writes them to the underlying data source only when you call the [UpdateBatch](updatebatch-method-ado.md) method), the **OriginalValue** property returns the field value that existed prior to any changes (that is, since the last **UpdateBatch** method call).</span></span> <span data-ttu-id="dd548-112">Esse é o mesmo valor que o método [CancelBatch](cancelbatch-method-ado.md) utiliza para substituir a propriedade **Value**.</span><span class="sxs-lookup"><span data-stu-id="dd548-112">This is the same value that the [CancelBatch](cancelbatch-method-ado.md) method uses to replace the **Value** property.</span></span> <span data-ttu-id="dd548-113">Quando você utiliza essa propriedade com a propriedade [UnderlyingValue](underlyingvalue-property-ado.md), é possível solucionar conflitos provenientes da atualizações em lote.</span><span class="sxs-lookup"><span data-stu-id="dd548-113">When you use this property with the [UnderlyingValue](underlyingvalue-property-ado.md) property, you can resolve conflicts that arise from batch updates.</span></span>

## <a name="record"></a><span data-ttu-id="dd548-114">Registro</span><span class="sxs-lookup"><span data-stu-id="dd548-114">Record</span></span>

<span data-ttu-id="dd548-115">Para os objetos [Record](record-object-ado.md), a propriedade **OriginalValue** estará em branco nos campos adicionados antes da chamada do [ Update ](update-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="dd548-115">For [Record](record-object-ado.md) objects, the **OriginalValue** property will be empty for fields added before [Update](update-method-ado.md) is called.</span></span>

