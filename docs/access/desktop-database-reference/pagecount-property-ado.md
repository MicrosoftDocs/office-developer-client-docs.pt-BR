---
title: Propriedade PageCount (ADO)
TOCTitle: PageCount property (ADO)
ms:assetid: 9cd8bf5c-b1e7-a453-4629-9cba7e408f53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249712(v=office.15)
ms:contentKeyID: 48546609
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ef5179f44a2c7c153411ae33566f3806f1e93573
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867367"
---
# <a name="pagecount-property-ado"></a><span data-ttu-id="c4061-102">Propriedade PageCount (ADO)</span><span class="sxs-lookup"><span data-stu-id="c4061-102">PageCount property (ADO)</span></span>


<span data-ttu-id="c4061-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="c4061-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c4061-104">Indica a quantidade de páginas de dados que o objeto [Recordset](recordset-object-ado.md) contém.</span><span class="sxs-lookup"><span data-stu-id="c4061-104">Indicates how many pages of data the [Recordset](recordset-object-ado.md) object contains.</span></span>

## <a name="return-value"></a><span data-ttu-id="c4061-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c4061-105">Return value</span></span>

<span data-ttu-id="c4061-106">Retorna um valor **Long**, indicando a quantidade de páginas do **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="c4061-106">Returns a **Long** value that indicates the number of pages in the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4061-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="c4061-107">Remarks</span></span>

<span data-ttu-id="c4061-108">Utilize a propriedade **PageCount** para determinar a quantidade de páginas de dados contida no objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="c4061-108">Use the **PageCount** property to determine how many pages of data are in the **Recordset** object.</span></span> <span data-ttu-id="c4061-109">*Páginas* são grupos de registros cujo tamanho é igual a configuração da propriedade [PageSize](pagesize-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="c4061-109">*Pages* are groups of records whose size equals the [PageSize](pagesize-property-ado.md) property setting.</span></span> <span data-ttu-id="c4061-110">Mesmo que a última página esteja incompleta por conter menos registros que no valor **PageSize**, ela será considerada como uma página adicional no valor **PageCount**.</span><span class="sxs-lookup"><span data-stu-id="c4061-110">Even if the last page is incomplete because there are fewer records than the **PageSize** value, it counts as an additional page in the **PageCount** value.</span></span> <span data-ttu-id="c4061-111">Se o objeto **Recordset** não oferecer suporte a essa propriedade, o valor será -1, indicando que **PageCount** é indeterminável.</span><span class="sxs-lookup"><span data-stu-id="c4061-111">If the **Recordset** object does not support this property, the value will be -1 to indicate that the **PageCount** is indeterminable.</span></span>

<span data-ttu-id="c4061-112">Consulte as propriedades **PageSize** e [AbsolutePage](absolutepage-property-ado.md) para obter mais informações sobre a funcionalidade da página.</span><span class="sxs-lookup"><span data-stu-id="c4061-112">See the **PageSize** and [AbsolutePage](absolutepage-property-ado.md) properties for more on page functionality.</span></span>

