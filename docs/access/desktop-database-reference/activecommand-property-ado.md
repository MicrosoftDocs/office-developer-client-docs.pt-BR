---
title: Propriedade ActiveCommand (ADO)
TOCTitle: ActiveCommand Property (ADO)
ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15)
ms:contentKeyID: 48544459
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f01ae4c821d8beb6c8de84c7ed671a373d7372c9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464838"
---
# <a name="activecommand-property-ado"></a><span data-ttu-id="b853a-102">Propriedade ActiveCommand (ADO)</span><span class="sxs-lookup"><span data-stu-id="b853a-102">ActiveCommand Property (ADO)</span></span>


<span data-ttu-id="b853a-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b853a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b853a-104">Indica o objeto [Command](command-object-ado.md) que criou o objeto [Recordset](recordset-object-ado.md) associado.</span><span class="sxs-lookup"><span data-stu-id="b853a-104">Indicates the [Command](command-object-ado.md) object that created the associated [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="b853a-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b853a-105">Return Value</span></span>

<span data-ttu-id="b853a-p101">Retorna um **Variant** contendo um objeto **Command**. O padrão é uma referência nula ao objeto.</span><span class="sxs-lookup"><span data-stu-id="b853a-p101">Returns a **Variant** that contains a **Command** object. Default is a null object reference.</span></span>

## <a name="remarks"></a><span data-ttu-id="b853a-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="b853a-108">Remarks</span></span>

<span data-ttu-id="b853a-109">A propriedade **ActiveCommand** é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="b853a-109">The **ActiveCommand** property is read-only.</span></span>

<span data-ttu-id="b853a-110">Se um objeto **Command** não tiver sido usado para criar o **Recordset** atual, então uma referência de objeto **Nula** será retornada.</span><span class="sxs-lookup"><span data-stu-id="b853a-110">If a **Command** object was not used to create the current **Recordset**, then a **Null** object reference is returned.</span></span>

<span data-ttu-id="b853a-111">Use essa propriedade para encontrar o objeto **Command** associado quando receber apenas o objeto **Recordset** resultante.</span><span class="sxs-lookup"><span data-stu-id="b853a-111">Use this property to find the associated **Command** object when you are given only the resulting **Recordset** object.</span></span>

