---
title: Método Resync (ADO)
TOCTitle: Resync Method (ADO)
ms:assetid: f594a200-56e6-fcf5-9b0a-900c56377f24
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250251(v=office.15)
ms:contentKeyID: 48548717
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d8e4a863449d8aea5d95002a6183978d9ca953a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884496"
---
# <a name="resync-method-ado"></a><span data-ttu-id="09140-102">Método Resync (ADO)</span><span class="sxs-lookup"><span data-stu-id="09140-102">Resync Method (ADO)</span></span>


<span data-ttu-id="09140-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="09140-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="09140-104">Atualiza os dados no objeto [Recordset](recordset-object-ado.md) atual, ou a coleção [Fields](fields-collection-ado.md) de um objeto [Record](record-object-ado.md), a partir do banco de dados subjacente.</span><span class="sxs-lookup"><span data-stu-id="09140-104">Refreshes the data in the current [Recordset](recordset-object-ado.md) object, or [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md) object, from the underlying database.</span></span>

## <a name="syntax"></a><span data-ttu-id="09140-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09140-105">Syntax</span></span>

<span data-ttu-id="09140-106">*Conjunto de registros*. Resync*AffectRecords*, *ResyncValues*</span><span class="sxs-lookup"><span data-stu-id="09140-106">*Recordset*.Resync*AffectRecords*, *ResyncValues*</span></span>

<span data-ttu-id="09140-107">*Registro*.</span><span class="sxs-lookup"><span data-stu-id="09140-107">*Record*.</span></span> <span data-ttu-id="09140-108">*Campos*. Resync*ResyncValues*</span><span class="sxs-lookup"><span data-stu-id="09140-108">*Fields*.Resync*ResyncValues*</span></span>

## <a name="parameters"></a><span data-ttu-id="09140-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09140-109">Parameters</span></span>

  - <span data-ttu-id="09140-110">*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="09140-110">*AffectRecords*</span></span>

  - <span data-ttu-id="09140-p102">Opcional. Um valor [AffectEnum](affectenum.md) que determina a quantidade de registros que serão afetados pelo método **Resync**. O valor padrão é **adAffectAll**. Esse valor não está disponível com o método **Resync** da coleção **Fields** de um objeto **Record**.</span><span class="sxs-lookup"><span data-stu-id="09140-p102">Optional. An [AffectEnum](affectenum.md) value that determines how many records the **Resync** method will affect. The default value is **adAffectAll**. This value is not available with the **Resync** method of the **Fields** collection of a **Record** object.</span></span>

  - <span data-ttu-id="09140-115">*ResyncValues*</span><span class="sxs-lookup"><span data-stu-id="09140-115">*ResyncValues*</span></span>

  - <span data-ttu-id="09140-p103">Opcional. Um valor [ResyncEnum](resyncenum.md) que especifica se os valores subjacentes serão substituídos. O valor padrão é **adResyncAllValues**.</span><span class="sxs-lookup"><span data-stu-id="09140-p103">Optional. A [ResyncEnum](resyncenum.md) value that specifies whether underlying values are overwritten. The default value is **adResyncAllValues**.</span></span>

## <a name="remarks"></a><span data-ttu-id="09140-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="09140-119">Remarks</span></span>

<span data-ttu-id="09140-120">**Objeto Recordset**</span><span class="sxs-lookup"><span data-stu-id="09140-120">**Recordset**</span></span>

<span data-ttu-id="09140-p104">Use o método **Resync** para sincronizar novamente os registros do **Recordset** atual com o banco de dados subjacente. Esse procedimento será útil se você estiver usando um cursor estático ou somente de encaminhamento e desejar ver as alterações no banco de dados subjacente.</span><span class="sxs-lookup"><span data-stu-id="09140-p104">Use the **Resync** method to resynchronize records in the current **Recordset** with the underlying database. This is useful if you are using either a static or forward-only cursor, but you want to see any changes in the underlying database.</span></span>

<span data-ttu-id="09140-123">Se você definir a propriedade [CursorLocation](cursorlocation-property-ado.md) como **adUseClient**, **Resync** somente estará disponível para os objetos **Recordset** que não sejam somente leitura.</span><span class="sxs-lookup"><span data-stu-id="09140-123">If you set the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**, **Resync** is only available for non-read-only **Recordset** objects.</span></span>

<span data-ttu-id="09140-p105">Diferente do método [Requery](requery-method-ado.md), o método **Resync** não reexecuta o comando subjacente do objeto **Recordset**. Os novos registros no banco de dados subjacente não estarão visíveis.</span><span class="sxs-lookup"><span data-stu-id="09140-p105">Unlike the [Requery](requery-method-ado.md) method, the **Resync** method does not re-execute the **Recordset** object's underlying command. New records in the underlying database will not be visible.</span></span>

<span data-ttu-id="09140-p106">Se a tentativa de nova sincronização falhar devido a um conflito com os dados subjacentes (por exemplo, por causa da exclusão de um registro por outro usuário), o provedor retornará avisos à coleção [Errors](errors-collection-ado.md) e ocorrerá um erro em tempo de execução. Use a propriedade [Filter](filter-property-ado.md) (**adFilterConflictingRecords**) e a propriedade [Status](status-property-ado-recordset.md) para localizar registros com conflitos.</span><span class="sxs-lookup"><span data-stu-id="09140-p106">If the attempt to resynchronize fails because of a conflict with the underlying data (for example, a record has been deleted by another user), the provider returns warnings to the [Errors](errors-collection-ado.md) collection and a run-time error occurs. Use the [Filter](filter-property-ado.md) property (**adFilterConflictingRecords**) and the [Status](status-property-ado-recordset.md) property to locate records with conflicts.</span></span>

<span data-ttu-id="09140-128">Se as propriedades dinâmicas [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) e [Resync Command](resync-command-property-dynamic-ado.md) forem definidas e **Recordset** resultar da execução de uma operação JOIN em várias tabelas, o método **Resync** executará o comando fornecido na propriedade **Resync Command** somente na tabela nomeada na propriedade **Unique Table**.</span><span class="sxs-lookup"><span data-stu-id="09140-128">If the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) and [Resync Command](resync-command-property-dynamic-ado.md) dynamic properties are set, and the **Recordset** is the result of executing a JOIN operation on multiple tables, then the **Resync** method will execute the command given in the **Resync Command** property only on the table named in the **Unique Table** property.</span></span>

<span data-ttu-id="09140-129">**Coleção Fields**</span><span class="sxs-lookup"><span data-stu-id="09140-129">**Fields**</span></span>

<span data-ttu-id="09140-p107">Use o método **Resync** para sincronizar novamente os valores da coleção **Fields** de um objeto **Record** com a fonte de dados subjacente. A propriedade [Count](count-property-ado.md) não é afetada por esse método.</span><span class="sxs-lookup"><span data-stu-id="09140-p107">Use the **Resync** method to resynchronize the values of the **Fields** collection of a **Record** object with the underlying data source. The [Count](count-property-ado.md) property is not affected by this method.</span></span>

<span data-ttu-id="09140-132">Se *ResyncValues* for definido como **adResyncAllValues** (o valor padrão), as propriedades de [OriginalValue](originalvalue-property-ado.md) de objetos [Field](field-object-ado.md) na coleção, [valor](value-property-ado.md)e [UnderlyingValue](underlyingvalue-property-ado.md)são sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="09140-132">If *ResyncValues* is set to **adResyncAllValues** (the default value), then the [UnderlyingValue](underlyingvalue-property-ado.md), [Value](value-property-ado.md), and [OriginalValue](originalvalue-property-ado.md) properties of [Field](field-object-ado.md) objects in the collection are synchronized.</span></span> <span data-ttu-id="09140-133">Se *ResyncValues* for definido como **adResyncUnderlyingValues**, apenas a propriedade **UnderlyingValue** é sincronizada.</span><span class="sxs-lookup"><span data-stu-id="09140-133">If *ResyncValues* is set to **adResyncUnderlyingValues**, only the **UnderlyingValue** property is synchronized.</span></span>

<span data-ttu-id="09140-p109">O valor da propriedade **Status** para cada objeto **Field** no momento da chamada também afeta o comportamento de **Resync**. **Resync** não terá efeito para os objetos **Field** com valor **adFieldPendingUnknown** ou **adFieldPendingInsert** para **Status**. Para o valor **adFieldPendingChange** ou **adFieldPendingDelete** de **Status**, **Resync** sincronizará os valores de dados dos campos ainda existentes na fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="09140-p109">The value of the **Status** property for each **Field** object at the time of the call also affects the behavior of **Resync**. For **Field** objects with **Status** values of **adFieldPendingUnknown** or **adFieldPendingInsert**, **Resync** has no effect. For **Status** values of **adFieldPendingChange** or **adFieldPendingDelete**, **Resync** synchronizes data values for fields that still exist at the data source.</span></span>

<span data-ttu-id="09140-p110">**Resync** não modificará os valores de **Status** dos objetos **Field**, a menos que ocorra um erro no momento em que ele for chamado. Por exemplo, se o campo não existir mais, o provedor retornará um valor de **Status** apropriado para o objeto **Field**, por exemplo, **adFieldDoesNotExist**. Os valores de **Status** retornados poderão ser combinados logicamente dentro do valor da propriedade \*\*Status \*\*\*\*\*\*.</span><span class="sxs-lookup"><span data-stu-id="09140-p110">**Resync** will not modify **Status** values of **Field** objects unless an error occurs when **Resync** is called. For example, if the field no longer exists, the provider will return an appropriate **Status** value for the **Field** object, such as **adFieldDoesNotExist**. Returned **Status** values may be logically combined within the value of the **Status** property.</span></span>

