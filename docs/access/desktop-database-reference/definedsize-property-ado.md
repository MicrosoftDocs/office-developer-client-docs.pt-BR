---
title: Propriedade DefinedSize (ADO)
TOCTitle: DefinedSize property (ADO)
ms:assetid: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15)
ms:contentKeyID: 48546257
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0a0e67cfdbe60ebf2c49cb3e726311d2fa61bd3e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868851"
---
# <a name="definedsize-property-ado"></a><span data-ttu-id="dd581-102">Propriedade DefinedSize (ADO)</span><span class="sxs-lookup"><span data-stu-id="dd581-102">DefinedSize property (ADO)</span></span>


<span data-ttu-id="dd581-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="dd581-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dd581-104">Indica a capacidade de dados de um objeto [Field](field-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="dd581-104">Indicates the data capacity of a [Field](field-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="dd581-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="dd581-105">Return value</span></span>

<span data-ttu-id="dd581-106">Retorna um valor **Long** que reflete o tamanho definido de um campo como um número de bytes.</span><span class="sxs-lookup"><span data-stu-id="dd581-106">Returns a **Long** value that reflects the defined size of a field as a number of bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd581-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="dd581-107">Remarks</span></span>

<span data-ttu-id="dd581-108">Use a propriedade **DefinedSize** para determinar a capacidade de dados de um objeto **Field**.</span><span class="sxs-lookup"><span data-stu-id="dd581-108">Use the **DefinedSize** property to determine the data capacity of a **Field** object.</span></span>

<span data-ttu-id="dd581-p101">As propriedades **DefinedSize** e [ActualSize](actualsize-property-ado.md) são diferentes. Por exemplo, considere um objeto **Field** com um tipo declarado de **adVarChar** e um valor de propriedade **DefinedSize** de 50, contendo um único caractere. O valor da propriedade **ActualSize** retornado será a extensão em bytes deste único caractere.</span><span class="sxs-lookup"><span data-stu-id="dd581-p101">The **DefinedSize** and [ActualSize](actualsize-property-ado.md) properties are different. For example, consider a **Field** object with a declared type of **adVarChar** and a **DefinedSize** property value of 50, containing a single character. The **ActualSize** property value it returns is the length in bytes of the single character.</span></span>

