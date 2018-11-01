---
title: Propriedade ActiveCommand (ADO)
TOCTitle: ActiveCommand property (ADO)
ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15)
ms:contentKeyID: 48544459
ms.date: 10/17/2018
mtps_version: v=office.15
ms.openlocfilehash: 473a0b99310d2eb5e050ed50f1e331cb65174ae8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869558"
---
# <a name="activecommand-property-ado"></a><span data-ttu-id="53e17-102">Propriedade ActiveCommand (ADO)</span><span class="sxs-lookup"><span data-stu-id="53e17-102">ActiveCommand property (ADO)</span></span>

<span data-ttu-id="53e17-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="53e17-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="53e17-104">Indica o objeto [Command](command-object-ado.md) que criou o objeto [Recordset](recordset-object-ado.md) associado.</span><span class="sxs-lookup"><span data-stu-id="53e17-104">Indicates the [Command](command-object-ado.md) object that created the associated [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="53e17-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="53e17-105">Return value</span></span>

<span data-ttu-id="53e17-p101">Retorna um **Variant** contendo um objeto **Command**. O padrão é uma referência nula ao objeto.</span><span class="sxs-lookup"><span data-stu-id="53e17-p101">Returns a **Variant** that contains a **Command** object. Default is a null object reference.</span></span>

## <a name="remarks"></a><span data-ttu-id="53e17-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="53e17-108">Remarks</span></span>

<span data-ttu-id="53e17-109">A propriedade **ActiveCommand** é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="53e17-109">The **ActiveCommand** property is read-only.</span></span>

<span data-ttu-id="53e17-110">Se um objeto **Command** não foi usado para criar o **Recordset**atual, uma referência de objeto **nula** será retornada.</span><span class="sxs-lookup"><span data-stu-id="53e17-110">If a **Command** object was not used to create the current **Recordset**, a **Null** object reference is returned.</span></span>

<span data-ttu-id="53e17-111">Use essa propriedade para encontrar o objeto **Command** associado quando receber apenas o objeto **Recordset** resultante.</span><span class="sxs-lookup"><span data-stu-id="53e17-111">Use this property to find the associated **Command** object when you are given only the resulting **Recordset** object.</span></span>

