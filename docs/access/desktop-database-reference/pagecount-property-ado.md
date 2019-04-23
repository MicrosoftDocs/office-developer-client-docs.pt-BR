---
title: Propriedade PageCount (ADO)
TOCTitle: PageCount property (ADO)
ms:assetid: 9cd8bf5c-b1e7-a453-4629-9cba7e408f53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249712(v=office.15)
ms:contentKeyID: 48546609
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b37ccc0c9a61e00b3c2e8f5eb3367831e5ddea43
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288116"
---
# <a name="pagecount-property-ado"></a><span data-ttu-id="5e005-102">Propriedade PageCount (ADO)</span><span class="sxs-lookup"><span data-stu-id="5e005-102">PageCount property (ADO)</span></span>


<span data-ttu-id="5e005-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5e005-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5e005-104">Indica a quantidade de páginas de dados que o objeto [Recordset](recordset-object-ado.md) contém.</span><span class="sxs-lookup"><span data-stu-id="5e005-104">Indicates how many pages of data the [Recordset](recordset-object-ado.md) object contains.</span></span>

## <a name="return-value"></a><span data-ttu-id="5e005-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5e005-105">Return value</span></span>

<span data-ttu-id="5e005-106">Retorna um valor **Long**, indicando a quantidade de páginas do **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="5e005-106">Returns a **Long** value that indicates the number of pages in the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e005-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e005-107">Remarks</span></span>

<span data-ttu-id="5e005-p101">Utilize a propriedade **PageCount** para determinar a quantidade de páginas de dados contida no objeto **Recordset**. \*As páginas \* são grupos de registros cujo tamanho se iguala ao da definição da propriedade [PageSize](pagesize-property-ado.md). Mesmo que a última página esteja incompleta por conter menos registros que no valor **PageSize**, ela será considerada como uma página adicional no valor **PageCount**. Se o objeto **Recordset** não oferecer suporte a essa propriedade, o valor será -1, indicando que **PageCount** é indeterminável.</span><span class="sxs-lookup"><span data-stu-id="5e005-p101">Use the **PageCount** property to determine how many pages of data are in the **Recordset** object. *Pages* are groups of records whose size equals the [PageSize](pagesize-property-ado.md) property setting. Even if the last page is incomplete because there are fewer records than the **PageSize** value, it counts as an additional page in the **PageCount** value. If the **Recordset** object does not support this property, the value will be -1 to indicate that the **PageCount** is indeterminable.</span></span>

<span data-ttu-id="5e005-112">Consulte as propriedades **PageSize** e [AbsolutePage](absolutepage-property-ado.md) para obter mais informações sobre a funcionalidade da página.</span><span class="sxs-lookup"><span data-stu-id="5e005-112">See the **PageSize** and [AbsolutePage](absolutepage-property-ado.md) properties for more on page functionality.</span></span>

