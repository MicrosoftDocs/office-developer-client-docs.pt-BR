---
title: Propriedade Status (Recordset do ADO)
TOCTitle: Status Property (ADO Recordset)
ms:assetid: bf3ccb36-c985-5fae-4f76-c48a0e20e6f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249930(v=office.15)
ms:contentKeyID: 48547482
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1979ad721a01ef72c08da1531a8826ec320915e5
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604614"
---
# <a name="status-property-ado-recordset"></a><span data-ttu-id="8bbda-102">Propriedade Status (Recordset do ADO)</span><span class="sxs-lookup"><span data-stu-id="8bbda-102">Status Property (ADO Recordset)</span></span>


<span data-ttu-id="8bbda-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8bbda-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8bbda-104">Indica o status do registro atual com relação às atualizações em lote ou outras operações em massa.</span><span class="sxs-lookup"><span data-stu-id="8bbda-104">Indicates the status of the current record with respect to batch updates or other bulk operations.</span></span>

<span data-ttu-id="8bbda-105"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="8bbda-105"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="8bbda-106">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="8bbda-106">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="8bbda-107">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="8bbda-107">Return value</span></span>
>>>>>>> <span data-ttu-id="8bbda-108">mestre</span><span class="sxs-lookup"><span data-stu-id="8bbda-108">master</span></span>

<span data-ttu-id="8bbda-109">Retorna a soma de um ou mais valores [RecordStatusEnum](recordstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="8bbda-109">Returns a sum of one or more [RecordStatusEnum](recordstatusenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bbda-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="8bbda-110">Remarks</span></span>

<span data-ttu-id="8bbda-p101">Utilize a propriedade **Status** para verificar quais alterações estão pendentes para registros modificados durante a atualização em lote. Você também pode utilizar a propriedade **Status** para exibir o status dos registros que falharam durante as operações em massa; por exemplo, quando você chama os métodos [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) ou [CancelBatch](cancelbatch-method-ado.md) em um objeto [Recordset](recordset-object-ado.md) ou define a propriedade [Filter](filter-property-ado.md) em um objeto **Recordset** para uma matriz de indicadores. Com esta propriedade, você pode identificar como um registro específico falhou e solucionar o problema de forma adequada.</span><span class="sxs-lookup"><span data-stu-id="8bbda-p101">Use the **Status** property to see what changes are pending for records modified during batch updating. You can also use the **Status** property to view the status of records that fail during bulk operations, such as when you call the [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), or [CancelBatch](cancelbatch-method-ado.md) methods on a [Recordset](recordset-object-ado.md) object, or set the [Filter](filter-property-ado.md) property on a **Recordset** object to an array of bookmarks. With this property, you can determine how a given record failed and resolve it accordingly.</span></span>

