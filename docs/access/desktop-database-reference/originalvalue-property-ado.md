---
title: Propriedade OriginalValue (ADO)
TOCTitle: OriginalValue property (ADO)
ms:assetid: 02ffc728-4692-d439-e2a6-2f02cca53a71
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248798(v=office.15)
ms:contentKeyID: 48542974
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0724320e1aaa1e7bfd3ceab8cf54afd5921c7425
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288179"
---
# <a name="originalvalue-property-ado"></a><span data-ttu-id="53cdb-102">Propriedade OriginalValue (ADO)</span><span class="sxs-lookup"><span data-stu-id="53cdb-102">OriginalValue property (ADO)</span></span>

<span data-ttu-id="53cdb-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="53cdb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="53cdb-104">Indica o valor de um [Field](field-object-ado.md) que existia no registro antes de as alterações serem efetuadas.</span><span class="sxs-lookup"><span data-stu-id="53cdb-104">Indicates the value of a [Field](field-object-ado.md) that existed in the record before any changes were made.</span></span>

## <a name="return-value"></a><span data-ttu-id="53cdb-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="53cdb-105">Return value</span></span>

<span data-ttu-id="53cdb-106">Retorna um valor **Variant** que representa o valor de um campo antes de qualquer alteração.</span><span class="sxs-lookup"><span data-stu-id="53cdb-106">Returns a **Variant** value that represents the value of a field prior to any change.</span></span>

## <a name="remarks"></a><span data-ttu-id="53cdb-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="53cdb-107">Remarks</span></span>

<span data-ttu-id="53cdb-108">Utilize a propriedade **OriginalValue** para retornar o valor do campo original de um campo a partir do registro atual.</span><span class="sxs-lookup"><span data-stu-id="53cdb-108">Use the **OriginalValue** property to return the original field value for a field from the current record.</span></span>

<span data-ttu-id="53cdb-109">No *modo de atualização imediata* (no qual o provedor grava alterações na fonte de dados subjacente após chamar o método [Update](update-method-ado.md) ), a propriedade **OriginalValue** retorna o valor do campo que existia antes de qualquer alteração (isto é, como o chamada do método da última **atualização** ).</span><span class="sxs-lookup"><span data-stu-id="53cdb-109">In *immediate update mode* (in which the provider writes changes to the underlying data source after you call the [Update](update-method-ado.md) method), the **OriginalValue** property returns the field value that existed prior to any changes (that is, since the last **Update** method call).</span></span> <span data-ttu-id="53cdb-110">Esse é o mesmo valor que o método [CancelUpdate](cancelupdate-method-ado.md) utiliza para substituir a propriedade [Value](value-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="53cdb-110">This is the same value that the [CancelUpdate](cancelupdate-method-ado.md) method uses to replace the [Value](value-property-ado.md) property.</span></span>

<span data-ttu-id="53cdb-p102">No *modo de atualização em lote* (no qual o provedor armazena em cache várias alterações e as grava na fonte de dados base somente quando você chama o método [UpdateBatch](updatebatch-method-ado.md)), a propriedade **OriginalValue** retorna o valor do campo que existia antes das alterações (isto é, desde a última chamada do método **UpdateBatch**). Esse é o mesmo valor que o método [CancelBatch](cancelbatch-method-ado.md) utiliza para substituir a propriedade **Value**. Quando você utiliza essa propriedade com a propriedade [UnderlyingValue](underlyingvalue-property-ado.md), é possível solucionar conflitos provenientes da atualizações em lote.</span><span class="sxs-lookup"><span data-stu-id="53cdb-p102">In *batch update mode* (in which the provider caches multiple changes and writes them to the underlying data source only when you call the [UpdateBatch](updatebatch-method-ado.md) method), the **OriginalValue** property returns the field value that existed prior to any changes (that is, since the last **UpdateBatch** method call). This is the same value that the [CancelBatch](cancelbatch-method-ado.md) method uses to replace the **Value** property. When you use this property with the [UnderlyingValue](underlyingvalue-property-ado.md) property, you can resolve conflicts that arise from batch updates.</span></span>

## <a name="record"></a><span data-ttu-id="53cdb-114">Registro</span><span class="sxs-lookup"><span data-stu-id="53cdb-114">Record</span></span>

<span data-ttu-id="53cdb-115">Para os objetos [Record](record-object-ado.md), a propriedade **OriginalValue** estará em branco nos campos adicionados antes da chamada do [ Update](update-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="53cdb-115">For [Record](record-object-ado.md) objects, the **OriginalValue** property will be empty for fields added before [Update](update-method-ado.md) is called.</span></span>

