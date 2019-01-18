---
title: Propriedade Status (Field do ADO)
TOCTitle: Status property (ADO Field)
ms:assetid: 7a7b45e8-2934-2e8e-77fa-a4f38272548d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249507(v=office.15)
ms:contentKeyID: 48545795
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9c5f9d73a1081bb27c88541ac99307165222ab65
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712236"
---
# <a name="status-property-ado-field"></a><span data-ttu-id="1b63f-102">Propriedade Status (Field do ADO)</span><span class="sxs-lookup"><span data-stu-id="1b63f-102">Status property (ADO Field)</span></span>


<span data-ttu-id="1b63f-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="1b63f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1b63f-104">Indica o status de um objeto [Field](field-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="1b63f-104">Indicates the status of a [Field](field-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="1b63f-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1b63f-105">Return value</span></span>

<span data-ttu-id="1b63f-p101">Retorna um valor [FieldStatusEnum](fieldstatusenum.md). O valor padrão é **adFieldOK**.</span><span class="sxs-lookup"><span data-stu-id="1b63f-p101">Returns a [FieldStatusEnum](fieldstatusenum.md) value. The default value is **adFieldOK**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b63f-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="1b63f-108">Remarks</span></span>

<span data-ttu-id="1b63f-109">Essa propriedade sempre retorna **adFieldOK** para os campos de um objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="1b63f-109">This property always returns **adFieldOK** for fields of a [Recordset](recordset-object-ado.md) object.</span></span>

<span data-ttu-id="1b63f-p102">Adições e exclusões executadas nas coleções [Fields](fields-collection-ado.md) do objeto [Record](record-object-ado.md) são armazenadas em cache até que o método [Update](update-method-ado.md) seja chamado. A propriedade **Status** permite que você identifique quais campos foram adicionados ou excluídos com êxito.</span><span class="sxs-lookup"><span data-stu-id="1b63f-p102">Additions and deletions to the [Fields](fields-collection-ado.md) collections of the [Record](record-object-ado.md) object are cached until the [Update](update-method-ado.md) method is called. The **Status** property enables you to determine which fields have been successfully added or deleted.</span></span>

<span data-ttu-id="1b63f-112">Para melhorar o desempenho, as alterações de esquema são armazenadas em cache até que o método **Update** seja chamado e, em seguida, são efetuadas em uma atualização em lote otimista.</span><span class="sxs-lookup"><span data-stu-id="1b63f-112">To enhance performance, schema changes are cached until **Update** is called, and then the changes are made in a batch optimistic update.</span></span> <span data-ttu-id="1b63f-113">Se o método **Update** não for chamado, o servidor não será atualizado.</span><span class="sxs-lookup"><span data-stu-id="1b63f-113">If the **Update** method is not called, the server is not updated.</span></span> <span data-ttu-id="1b63f-114">Se as atualizações falharem, um erro será retornado e a propriedade **Status** indicará os valores combinados da operação e o código de status do erro.</span><span class="sxs-lookup"><span data-stu-id="1b63f-114">If any updates fail then an error is returned and the **Status** property indicates the combined values of the operation and error status code.</span></span> <span data-ttu-id="1b63f-115">Por exemplo, **adFieldPendingInsert** **OU** **adFieldPermissionDenied**.</span><span class="sxs-lookup"><span data-stu-id="1b63f-115">For example, **adFieldPendingInsert** **OR** **adFieldPermissionDenied**.</span></span> <span data-ttu-id="1b63f-116">A propriedade **Status** de cada **Field** pode ser usada para determinar o motivo pelo qual o **Field** não foi adicionado, modificado ou excluído.</span><span class="sxs-lookup"><span data-stu-id="1b63f-116">The **Status** property for each **Field** can be used to determine why the **Field** was not added, modified, or deleted.</span></span> <span data-ttu-id="1b63f-117">**Status** apenas de forma significativa é exposta no **registro**. Coleção **Fields** e não o **Recordset**. Coleção **Fields** .</span><span class="sxs-lookup"><span data-stu-id="1b63f-117">**Status** is only meaningfully exposed on the **Record**.**Fields** collection and not the **Recordset**.**Fields** collection.</span></span>

<span data-ttu-id="1b63f-p104">Podem surgir dois problemas durante a adição, modificação ou exclusão de um **Field**. Se o usuário excluir um **Field**, ele será marcado para exclusão da coleção **Fields**. Se o **Update** subsequente retornar um erro porque o usuário tentou excluir um **Field** para o qual não tinha permissão, o **Field** terá o status de **adFieldPermissionDenied** **OU** **adFieldPendingDelete**. A chamada do método [CancelUpdate](cancelupdate-method-ado.md) restaura os valores originais e define **Status** como **adFieldOK**. Da mesma forma, o método **Update** pode retornar um erro porque um novo **Field** foi adicionado com um valor inválido. Neste caso, o novo **Field** estará na coleção **Fields** e terá o status **adFieldPendingInsert** e, talvez, **adFieldCantCreate**. Você pode inserir um valor válido para o novo **Field** e chamar **Update** novamente. Em vez disso, a chamada de **Resync** repete a consulta ao provedor.</span><span class="sxs-lookup"><span data-stu-id="1b63f-p104">Two problems can arise when adding, modifying, or deleting a **Field**. If the user deletes a **Field**, it is marked for deletion from the **Fields** collection. If the subsequent **Update** returns an error because the user tried to delete a **Field** for which they do not have permission, the **Field** will have a status of **adFieldPermissionDenied** **OR** **adFieldPendingDelete**. Calling the [CancelUpdate](cancelupdate-method-ado.md) method restores original values and sets the **Status** to **adFieldOK**. Similarly, the **Update** method may return an error because a new **Field** was added and given an inappropriate value. In that case the new **Field** will be in the **Fields** collection and have a status of **adFieldPendingInsert** and perhaps **adFieldCantCreate**. You can supply an appropriate value for the new **Field** and call **Update** again. Note that calling **Resync** instead requeries the provider.</span></span>

