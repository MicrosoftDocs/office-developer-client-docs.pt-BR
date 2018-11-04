---
title: Método UpdateBatch (ADO)
TOCTitle: UpdateBatch method (ADO)
ms:assetid: 69e72a65-b637-36fd-d09f-7f81050f71ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249416(v=office.15)
ms:contentKeyID: 48545420
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3ce946d3354f6bbf05ac3819efc5f96c436fa174
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950122"
---
# <a name="updatebatch-method-ado"></a><span data-ttu-id="35152-102">Método UpdateBatch (ADO)</span><span class="sxs-lookup"><span data-stu-id="35152-102">UpdateBatch method (ADO)</span></span>

<span data-ttu-id="35152-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="35152-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="35152-104">Grava todas as atualizações em lote pendentes no disco.</span><span class="sxs-lookup"><span data-stu-id="35152-104">Writes all pending batch updates to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="35152-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="35152-105">Syntax</span></span>

<span data-ttu-id="35152-106">*conjunto de registros*. UpdateBatch*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="35152-106">*recordset*.UpdateBatch*AffectRecords*</span></span>

## <a name="parameters"></a><span data-ttu-id="35152-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="35152-107">Parameters</span></span>

|<span data-ttu-id="35152-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="35152-108">Parameter</span></span>|<span data-ttu-id="35152-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="35152-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="35152-110">*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="35152-110">*AffectRecords*</span></span> |<span data-ttu-id="35152-p101">Opcional. Um valor [AffectEnum](affectenum.md) que indica quantos registros o método **UpdateBatch** afetará.</span><span class="sxs-lookup"><span data-stu-id="35152-p101">Optional. An [AffectEnum](affectenum.md) value that indicates how many records the **UpdateBatch** method will affect.</span></span>|

## <a name="remarks"></a><span data-ttu-id="35152-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="35152-113">Remarks</span></span>

<span data-ttu-id="35152-114">Utilize o método **UpdateBatch** ao modificar um objeto **Recordset** no modo de atualização em lote a fim de transmitir todas as alterações feitas em um objeto **Recordset** para o banco de dados base.</span><span class="sxs-lookup"><span data-stu-id="35152-114">Use the **UpdateBatch** method when modifying a **Recordset** object in batch update mode to transmit all changes made in a **Recordset** object to the underlying database.</span></span>

<span data-ttu-id="35152-p102">Se o objeto **Recordset** suportar atualização em lote, você poderá armazenar localmente em cache diversas alterações em um ou mais registros até chamar o método **UpdateBatch**. Se estiver editando o registro atual ou adicionando um novo registro ao chamar o método **UpdateBatch**, o ADO chamará automaticamente o método [Update](update-method-ado.md) para salvar quaisquer informações pendentes no registro atual antes de transmitir as alterações em lote ao provedor. Você deve utilizar a atualização em lote apenas com um conjunto de chaves ou um cursor estático.</span><span class="sxs-lookup"><span data-stu-id="35152-p102">If the **Recordset** object supports batch updating, you can cache multiple changes to one or more records locally until you call the **UpdateBatch** method. If you are editing the current record or adding a new record when you call the **UpdateBatch** method, ADO will automatically call the [Update](update-method-ado.md) method to save any pending changes to the current record before transmitting the batched changes to the provider. You should use batch updating with either a keyset or static cursor only.</span></span>

> [!NOTE]
> <span data-ttu-id="35152-118">[!OBSERVAçãO] A especificação de **adAffectGroup** como o valor para esse parâmetro resultará em um erro quando não existirem registros visíveis no **Recordset** atual (tal como um filtro ao qual nenhum registro corresponde).</span><span class="sxs-lookup"><span data-stu-id="35152-118">Specifying **adAffectGroup** as the value for this parameter will result in an error when there are no visible records in the current **Recordset** (such as a filter for which no records match).</span></span>

<span data-ttu-id="35152-p103">Se a tentativa de transmitir alterações falhar para algum ou todos os registros devido a um conflito com os dados base (por exemplo, um registro já foi excluído por outro usuário), o provedor retornará avisos para a coleção [Errors](errors-collection-ado.md) e ocorrerá um erro em tempo de execução. Utilize a propriedade [Filter](filter-property-ado.md) (**adFilterAffectedRecords**) e a propriedade [Status](status-property-ado-recordset.md) para localizar registros com conflitos.</span><span class="sxs-lookup"><span data-stu-id="35152-p103">If the attempt to transmit changes fails for any or all records because of a conflict with the underlying data (for example, a record has already been deleted by another user), the provider returns warnings to the [Errors](errors-collection-ado.md) collection and a run-time error occurs. Use the [Filter](filter-property-ado.md) property (**adFilterAffectedRecords**) and the [Status](status-property-ado-recordset.md) property to locate records with conflicts.</span></span>

<span data-ttu-id="35152-121">Para cancelar todas as atualizações em lote pendentes, utilize o método [CancelBatch](cancelbatch-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="35152-121">To cancel all pending batch updates, use the [CancelBatch](cancelbatch-method-ado.md) method.</span></span>

<span data-ttu-id="35152-122">Se as propriedades dinâmicas [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) e [Update Resync](update-resync-property-dynamic-ado.md)forem definidas e o **Recordset** for o resultado da execução de uma operação JOIN em várias tabelas, então a execução do método **UpdateBatch** será implicitamente seguida pelo método [Resync](resync-method-ado.md), dependendo das definições da propriedade **Update Resync**.</span><span class="sxs-lookup"><span data-stu-id="35152-122">If the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) and [Update Resync](update-resync-property-dynamic-ado.md) dynamic properties are set, and the **Recordset** is the result of executing a JOIN operation on multiple tables, then the execution of the **UpdateBatch** method is implicitly followed by the [Resync](resync-method-ado.md) method depending on the settings of the **Update Resync** property.</span></span>

<span data-ttu-id="35152-p104">A ordem na qual as atualizações individuais de um lote são executadas na fonte de dados não é necessariamente a mesma que a ordem na qual elas foram executadas no **Recordset** local. A ordem da atualização depende do provedor. Leve isso em consideração ao codificar atualizações que estão relacionadas entre si, tais como restrições de chave estrangeira ou uma inserção ou atualização.</span><span class="sxs-lookup"><span data-stu-id="35152-p104">The order in which the individual updates of a batch are performed on the data source is not necessarily the same as the order in which they were performed on the local **Recordset**. Update order is dependent upon the provider. Take this into account when coding updates that are related to one another, such as foreign key constraints on an insert or update.</span></span>

