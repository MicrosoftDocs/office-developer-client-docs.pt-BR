---
title: Propriedade Optimize -- Dinâmica (ADO)
TOCTitle: Optimize Property--Dynamic (ADO)
ms:assetid: 2253b052-2d8a-f6f0-f8b8-f56e79d243de
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249001(v=office.15)
ms:contentKeyID: 48543705
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7276e642e15137bdcfcb939330a3642d96e9a5a2
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605174"
---
# <a name="optimize-property--dynamic-ado"></a><span data-ttu-id="18fc5-102">Propriedade Optimize -- Dinâmica (ADO)</span><span class="sxs-lookup"><span data-stu-id="18fc5-102">Optimize Property--Dynamic (ADO)</span></span>


<span data-ttu-id="18fc5-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="18fc5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="18fc5-104">Especifica se um índice deve ser criado em um campo</span><span class="sxs-lookup"><span data-stu-id="18fc5-104">Specifies whether an index should be created on a field.</span></span>

<span data-ttu-id="18fc5-105"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="18fc5-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="18fc5-106">Configurações e valor de retorno</span><span class="sxs-lookup"><span data-stu-id="18fc5-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="18fc5-107">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="18fc5-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="18fc5-108">mestre</span><span class="sxs-lookup"><span data-stu-id="18fc5-108">master</span></span>

<span data-ttu-id="18fc5-109">Define ou retorna um valor **Boolean** que indica se um índice deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="18fc5-109">Sets or returns a **Boolean** value that indicates whether an index should be created.</span></span>

## <a name="remarks"></a><span data-ttu-id="18fc5-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="18fc5-110">Remarks</span></span>

<span data-ttu-id="18fc5-p101">Um índice pode melhorar o desempenho das operações que localizam ou classificam valores em um [Recordset](recordset-object-ado.md). O índice é interno para o ADO  você não pode acessar explicitamente ou usá-lo em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="18fc5-p101">An index can improve the performance of operations that find or sort values in a [Recordset](recordset-object-ado.md). The index is internal to ADO — you cannot explicitly access or use it in your application.</span></span>

<span data-ttu-id="18fc5-p102">Para criar um índice em um campo, defina a propriedade **Optimize** como **True**. Para excluir o índice, defina essa propriedade como **False**.</span><span class="sxs-lookup"><span data-stu-id="18fc5-p102">To create an index on a field, set the **Optimize** property to **True**. To delete the index, set this property to **False**.</span></span>

<span data-ttu-id="18fc5-115">**Optimize** é uma propriedade dinâmica acrescentada à coleção [Properties](field-object-ado.md) do objeto [Field](properties-collection-ado.md) quando a propriedade [CursorLocation](cursorlocation-property-ado.md) estiver definida como **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="18fc5-115">**Optimize** is a dynamic property appended to the [Field](field-object-ado.md) object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

<span data-ttu-id="18fc5-116">**Usage**</span><span class="sxs-lookup"><span data-stu-id="18fc5-116">**Usage**</span></span>

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
