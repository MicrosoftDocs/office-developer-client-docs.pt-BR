---
title: Propriedade Optimize -- Dinâmica (ADO)
TOCTitle: Optimize Property--Dynamic (ADO)
ms:assetid: 2253b052-2d8a-f6f0-f8b8-f56e79d243de
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249001(v=office.15)
ms:contentKeyID: 48543705
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 62af17d9590b2fad39d61639a32de536f0438193
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883229"
---
# <a name="optimize-property--dynamic-ado"></a><span data-ttu-id="080eb-102">Propriedade Optimize -- Dinâmica (ADO)</span><span class="sxs-lookup"><span data-stu-id="080eb-102">Optimize Property--Dynamic (ADO)</span></span>


<span data-ttu-id="080eb-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="080eb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="080eb-104">Especifica se um índice deve ser criado em um campo</span><span class="sxs-lookup"><span data-stu-id="080eb-104">Specifies whether an index should be created on a field.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="080eb-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="080eb-105">Settings and return values</span></span>

<span data-ttu-id="080eb-106">Define ou retorna um valor **Boolean** que indica se um índice deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="080eb-106">Sets or returns a **Boolean** value that indicates whether an index should be created.</span></span>

## <a name="remarks"></a><span data-ttu-id="080eb-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="080eb-107">Remarks</span></span>

<span data-ttu-id="080eb-p101">Um índice pode melhorar o desempenho das operações que localizam ou classificam valores em um [Recordset](recordset-object-ado.md). O índice é interno para o ADO  você não pode acessar explicitamente ou usá-lo em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="080eb-p101">An index can improve the performance of operations that find or sort values in a [Recordset](recordset-object-ado.md). The index is internal to ADO — you cannot explicitly access or use it in your application.</span></span>

<span data-ttu-id="080eb-p102">Para criar um índice em um campo, defina a propriedade **Optimize** como **True**. Para excluir o índice, defina essa propriedade como **False**.</span><span class="sxs-lookup"><span data-stu-id="080eb-p102">To create an index on a field, set the **Optimize** property to **True**. To delete the index, set this property to **False**.</span></span>

<span data-ttu-id="080eb-112">**Optimize** é uma propriedade dinâmica acrescentada à coleção [Properties](field-object-ado.md) do objeto [Field](properties-collection-ado.md) quando a propriedade [CursorLocation](cursorlocation-property-ado.md) estiver definida como **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="080eb-112">**Optimize** is a dynamic property appended to the [Field](field-object-ado.md) object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

<span data-ttu-id="080eb-113">**Usage**</span><span class="sxs-lookup"><span data-stu-id="080eb-113">**Usage**</span></span>

```vb
    Dim rs As New Recordset
    Dim fld As Field
    rs.CursorLocation = adUseClient      'Enable index creation
    rs.Fields.Append "Field1", adChar, 35, adFldIsNullable
    rs.Open
    Set fld = rs.Fields(0)
    fld.Properties("Optimize") = True    'Create an index
    fld.Properties("Optimize") = False   'Delete an index
```
