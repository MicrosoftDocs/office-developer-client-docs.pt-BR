---
title: Adicionando vários campos
TOCTitle: Adding Multiple Fields
ms:assetid: 81b2f9de-4805-4494-9990-09ffda1b2068
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249560(v=office.15)
ms:contentKeyID: 48545961
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b9bca4035917f4376ccf69201d79894a0273ceb9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464001"
---
# <a name="adding-multiple-fields"></a><span data-ttu-id="42ec1-102">Adicionando vários campos</span><span class="sxs-lookup"><span data-stu-id="42ec1-102">Adding Multiple Fields</span></span>


<span data-ttu-id="42ec1-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="42ec1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="42ec1-104">Às vezes, pode ser mais eficiente passar uma matriz de campos e seus valores correspondentes para o método **AddNew**, em vez de definir **Value** várias vezes para cada novo campo.</span><span class="sxs-lookup"><span data-stu-id="42ec1-104">Occasionally, it might be more efficient to pass in an array of fields and their corresponding values to the **AddNew** method, rather than setting **Value** multiple times for each new field.</span></span> <span data-ttu-id="42ec1-105">Se *FieldList* é uma matriz, os *valores* também deve ser uma matriz com o mesmo número de membros; Caso contrário, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="42ec1-105">If *FieldList* is an array, *Values* must also be an array with the same number of members; otherwise, an error occurs.</span></span> <span data-ttu-id="42ec1-106">A ordem dos nomes de campo deve corresponder à ordem dos valores de campo em cada matriz.</span><span class="sxs-lookup"><span data-stu-id="42ec1-106">The order of field names must match the order of field values in each array.</span></span> <span data-ttu-id="42ec1-107">O código a seguir passa uma matriz de campos e uma matriz de valores para o método **AddNew**.</span><span class="sxs-lookup"><span data-stu-id="42ec1-107">The following code passes an array of fields and an array of values to the **AddNew** method.</span></span>

```vb 
 
'BeginAddNew2 
 Dim avarFldNames As Variant 
 Dim avarFldValues As Variant 
 
 avarFldNames = Array("CompanyName", "Phone") 
 avarFldValues = Array("Sample Shipper 2", "(931) 555-6334") 
 
 If objRs1.Supports(adAddNew) Then 
 objRs1.AddNew avarFldNames, avarFldValues 
 End If 
 
 'Re-establish a Connection and update 
 Set objRs1.ActiveConnection = GetNewConnection 
 objRs1.UpdateBatch 
'EndAddNew2 
```

