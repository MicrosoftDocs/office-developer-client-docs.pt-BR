---
title: Propriedade Type (ADO)
TOCTitle: Type property (ADO)
ms:assetid: 14d99172-2145-05ae-620b-459ba097f05c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248914(v=office.15)
ms:contentKeyID: 48543397
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 34a5d1cb1750dc9803c62202a06feccc2d464f9b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314011"
---
# <a name="type-property-ado"></a><span data-ttu-id="d0ae6-102">Propriedade Type (ADO)</span><span class="sxs-lookup"><span data-stu-id="d0ae6-102">Type property (ADO)</span></span>


<span data-ttu-id="d0ae6-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d0ae6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d0ae6-104">Indica o tipo operacional ou o tipo de dados de um objeto [Parameter](parameter-object-ado.md), [Field](field-object-ado.md) ou [Property](property-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d0ae6-104">Indicates the operational type or data type of a [Parameter](parameter-object-ado.md), [Field](field-object-ado.md), or [Property](property-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="d0ae6-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="d0ae6-105">Settings and return values</span></span>

<span data-ttu-id="d0ae6-106">Define ou retorna um valor [DataTypeEnum](datatypeenum.md).</span><span class="sxs-lookup"><span data-stu-id="d0ae6-106">Sets or returns a [DataTypeEnum](datatypeenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0ae6-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0ae6-107">Remarks</span></span>

<span data-ttu-id="d0ae6-p101">Para os objetos **Parameter**, a propriedade **Type** é leitura/gravação. Para novos objetos **Field** que foram acrescentados à coleção [Fields](fields-collection-ado.md) de um [Record](record-object-ado.md), **Type** é leitura/gravação somente depois que a propriedade [Value](value-property-ado.md) para o **Field** for especificada e o provedor de dados adicionar com êxito o novo **Field** chamando o método [Update](update-method-ado.md) da coleção **Fields**.</span><span class="sxs-lookup"><span data-stu-id="d0ae6-p101">For **Parameter** objects, the **Type** property is read/write. For new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Type** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="d0ae6-110">Para todos os outros objetos, a propriedade **Type** é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="d0ae6-110">For all other objects, the **Type** property is read-only.</span></span>

