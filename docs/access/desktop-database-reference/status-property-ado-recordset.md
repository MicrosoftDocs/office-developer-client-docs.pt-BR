---
title: Propriedade Status (Recordset do ADO)
TOCTitle: Status property (ADO Recordset)
ms:assetid: bf3ccb36-c985-5fae-4f76-c48a0e20e6f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249930(v=office.15)
ms:contentKeyID: 48547482
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4017ff216c17479a69d6d07d0abe51b30fd5e680
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308516"
---
# <a name="status-property-ado-recordset"></a><span data-ttu-id="2ef2b-102">Propriedade Status (Recordset do ADO)</span><span class="sxs-lookup"><span data-stu-id="2ef2b-102">Status property (ADO Recordset)</span></span>


<span data-ttu-id="2ef2b-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2ef2b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2ef2b-104">Indica o status do registro atual com relação às atualizações em lote ou outras operações em massa.</span><span class="sxs-lookup"><span data-stu-id="2ef2b-104">Indicates the status of the current record with respect to batch updates or other bulk operations.</span></span>

## <a name="return-value"></a><span data-ttu-id="2ef2b-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2ef2b-105">Return value</span></span>

<span data-ttu-id="2ef2b-106">Retorna a soma de um ou mais valores [RecordStatusEnum](recordstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="2ef2b-106">Returns a sum of one or more [RecordStatusEnum](recordstatusenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ef2b-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ef2b-107">Remarks</span></span>

<span data-ttu-id="2ef2b-p101">Utilize a propriedade **Status** para verificar quais alterações estão pendentes para registros modificados durante a atualização em lote. Você também pode utilizar a propriedade **Status** para exibir o status dos registros que falharam durante as operações em massa; por exemplo, quando você chama os métodos [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) ou [CancelBatch](cancelbatch-method-ado.md) em um objeto [Recordset](recordset-object-ado.md) ou define a propriedade [Filter](filter-property-ado.md) em um objeto **Recordset** para uma matriz de indicadores. Com esta propriedade, você pode identificar como um registro específico falhou e solucionar o problema de forma adequada.</span><span class="sxs-lookup"><span data-stu-id="2ef2b-p101">Use the **Status** property to see what changes are pending for records modified during batch updating. You can also use the **Status** property to view the status of records that fail during bulk operations, such as when you call the [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), or [CancelBatch](cancelbatch-method-ado.md) methods on a [Recordset](recordset-object-ado.md) object, or set the [Filter](filter-property-ado.md) property on a **Recordset** object to an array of bookmarks. With this property, you can determine how a given record failed and resolve it accordingly.</span></span>

