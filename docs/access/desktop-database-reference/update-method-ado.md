---
title: Método Update (ADO)
TOCTitle: Update method (ADO)
ms:assetid: fc88cab6-c379-bb4f-530c-da08107924e0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250294(v=office.15)
ms:contentKeyID: 48548893
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c0a62618eef0a829db84de050aa07c2c645636e5
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929430"
---
# <a name="update-method-ado"></a><span data-ttu-id="27e85-102">Método Update (ADO)</span><span class="sxs-lookup"><span data-stu-id="27e85-102">Update method (ADO)</span></span>


<span data-ttu-id="27e85-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="27e85-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="27e85-104">Salva quaisquer alterações feitas na linha atual de um objeto [Recordset](recordset-object-ado.md) ou na coleção [Fields](fields-collection-ado.md) de um objeto [Record](record-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="27e85-104">Saves any changes you make to the current row of a [Recordset](recordset-object-ado.md) object, or the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="27e85-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="27e85-105">Syntax</span></span>

<span data-ttu-id="27e85-106">*conjunto de registros*. Atualizar*campos*, *valores*</span><span class="sxs-lookup"><span data-stu-id="27e85-106">*recordset*.Update*Fields*, *Values*</span></span>

<span data-ttu-id="27e85-107">*registro*.</span><span class="sxs-lookup"><span data-stu-id="27e85-107">*record*.</span></span> <span data-ttu-id="27e85-108">*Campos*. Atualização</span><span class="sxs-lookup"><span data-stu-id="27e85-108">*Fields*.Update</span></span>

## <a name="parameters"></a><span data-ttu-id="27e85-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="27e85-109">Parameters</span></span>

  - <span data-ttu-id="27e85-110">*Fields*</span><span class="sxs-lookup"><span data-stu-id="27e85-110">*Fields*</span></span>

  - <span data-ttu-id="27e85-p102">Opcional. Uma **Variant** que representa um único nome, ou uma matriz **Variant** que representa nomes ou posições ordinais do campo ou campos que deseja modificar.</span><span class="sxs-lookup"><span data-stu-id="27e85-p102">Optional. A **Variant** that represents a single name, or a **Variant** array that represents names or ordinal positions of the field or fields you wish to modify.</span></span>

  - <span data-ttu-id="27e85-113">*Values*</span><span class="sxs-lookup"><span data-stu-id="27e85-113">*Values*</span></span>

  - <span data-ttu-id="27e85-p103">Opcional. Uma **Variant** que representa um único valor, ou uma matriz **Variant** que representa valores para o campo ou campos no novo registro.</span><span class="sxs-lookup"><span data-stu-id="27e85-p103">Optional. A **Variant** that represents a single value, or a **Variant** array that represents values for the field or fields in the new record.</span></span>

## <a name="remarks"></a><span data-ttu-id="27e85-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="27e85-116">Remarks</span></span>

<span data-ttu-id="27e85-117">**Recordset**</span><span class="sxs-lookup"><span data-stu-id="27e85-117">**Recordset**</span></span>

<span data-ttu-id="27e85-p104">Utilize o método **Update** para salvar quaisquer alterações feitas no registro atual de um objeto **Recordset** desde a chamada ao método [AddNew](addnew-method-ado.md) ou desde a alteração de quaisquer valores de campo em um registro existente. O objeto **Recordset** deve suportar atualizações.</span><span class="sxs-lookup"><span data-stu-id="27e85-p104">Use the **Update** method to save any changes you make to the current record of a **Recordset** object since calling the [AddNew](addnew-method-ado.md) method or since changing any field values in an existing record. The **Recordset** object must support updates.</span></span>

<span data-ttu-id="27e85-120">Para definir valores de campos, execute um dos seguintes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="27e85-120">To set field values, do one of the following:</span></span>

  - <span data-ttu-id="27e85-121">Atribua valores à propriedade [Value](field-object-ado.md) de um objeto [Field](value-property-ado.md) e chame o método **Update**.</span><span class="sxs-lookup"><span data-stu-id="27e85-121">Assign values to a [Field](field-object-ado.md) object's [Value](value-property-ado.md) property and call the **Update** method.</span></span>

  - <span data-ttu-id="27e85-122">Passe o nome de um campo e um valor como argumentos com a chamada a **Update**.</span><span class="sxs-lookup"><span data-stu-id="27e85-122">Pass a field name and a value as arguments with the **Update** call.</span></span>

  - <span data-ttu-id="27e85-123">Passe uma matriz de nomes de campo e uma matriz de valores com a chamada a **Update**.</span><span class="sxs-lookup"><span data-stu-id="27e85-123">Pass an array of field names and an array of values with the **Update** call.</span></span>

<span data-ttu-id="27e85-p105">Ao utilizar matrizes de campos e valores, deve haver um número igual de elementos em ambas as matrizes. Além disso, a ordem dos nomes de campo deve corresponder à ordem dos valores de campo. Se o número e a ordem dos campos e valores não corresponder, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="27e85-p105">When you use arrays of fields and values, there must be an equal number of elements in both arrays. Also, the order of field names must match the order of field values. If the number and order of fields and values do not match, an error occurs.</span></span>

<span data-ttu-id="27e85-p106">Se o objeto **Recordset** suportar atualização em lote, você poderá armazenar localmente em cache diversas alterações em um ou mais registros até chamar o método [UpdateBatch](updatebatch-method-ado.md). Se estiver editando o registro atual ou adicionando um novo registro ao chamar o método **UpdateBatch**, o ADO chamará automaticamente o método **Update** para salvar quaisquer alterações pendentes no registro atual antes de transmitir as alterações em lote ao provedor.</span><span class="sxs-lookup"><span data-stu-id="27e85-p106">If the **Recordset** object supports batch updating, you can cache multiple changes to one or more records locally until you call the [UpdateBatch](updatebatch-method-ado.md) method. If you are editing the current record or adding a new record when you call the **UpdateBatch** method, ADO will automatically call the **Update** method to save any pending changes to the current record before transmitting the batched changes to the provider.</span></span>

<span data-ttu-id="27e85-p107">Se você mover do registro que está adicionando ou editando antes de chamar o método **Update**, o ADO chamará **Update** automaticamente para salvar as alterações. Você deve chamar o método [CancelUpdate](cancelupdate-method-ado.md) se deseja cancelar quaisquer alterações feitas no registro atual ou descartar um registro recém-adicionado.</span><span class="sxs-lookup"><span data-stu-id="27e85-p107">If you move from the record you are adding or editing before calling the **Update** method, ADO will automatically call **Update** to save the changes. You must call the [CancelUpdate](cancelupdate-method-ado.md) method if you want to cancel any changes made to the current record or discard a newly added record.</span></span>

<span data-ttu-id="27e85-131">O registro atual permanece atual depois da chamada ao método **Update**.</span><span class="sxs-lookup"><span data-stu-id="27e85-131">The current record remains current after you call the **Update** method.</span></span>

<span data-ttu-id="27e85-132">**Record**</span><span class="sxs-lookup"><span data-stu-id="27e85-132">**Record**</span></span>

<span data-ttu-id="27e85-133">O método **Update** finaliza adições, exclusões e atualizações de campos na coleção [Fields](fields-collection-ado.md) de um objeto **Record**.</span><span class="sxs-lookup"><span data-stu-id="27e85-133">The **Update** method finalizes additions, deletions, and updates to fields in the [Fields](fields-collection-ado.md) collection of a **Record** object.</span></span>

<span data-ttu-id="27e85-p108">Por exemplo, campos excluídos com o método **Delete** são marcados para exclusão imediatamente, mas permanecem na coleção. O método **Update** deve ser chamado para realmente excluir esses campos da coleção do provedor.</span><span class="sxs-lookup"><span data-stu-id="27e85-p108">For example, fields deleted with the **Delete** method are marked for deletion immediately but remain in the collection. The **Update** method must be called to actually delete these fields from the provider's collection.</span></span>

