---
title: Propriedade Recordset.StillExecuting (DAO)
TOCTitle: StillExecuting Property
ms:assetid: 0e53c98f-17ac-3569-d780-540a6932013e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845245(v=office.15)
ms:contentKeyID: 48543245
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4c7a245da39f3509022fb0bc4103da88ecbd302a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884370"
---
# <a name="recordsetstillexecuting-property-dao"></a><span data-ttu-id="fcd1d-102">Propriedade Recordset.StillExecuting (DAO)</span><span class="sxs-lookup"><span data-stu-id="fcd1d-102">Recordset.StillExecuting Property (DAO)</span></span>


<span data-ttu-id="fcd1d-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="fcd1d-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="fcd1d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fcd1d-104">Syntax</span></span>

<span data-ttu-id="fcd1d-105">*expressão* . StillExecuting</span><span class="sxs-lookup"><span data-stu-id="fcd1d-105">*expression* .StillExecuting</span></span>

<span data-ttu-id="fcd1d-106">*expressão* Uma variável que representa um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="fcd1d-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcd1d-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="fcd1d-107">Remarks</span></span>

<span data-ttu-id="fcd1d-p101">Use a propriedade **StillExecuting** para determinar se o método **Execute** ou **OpenConnection** chamado mais recentemente de forma assíncrona (ou seja, um método executado com a opção **dbRunAsync**) foi concluído. Enquanto a propriedade **StillExecuting** for **True**, qualquer objeto retornado não poderá ser acessado.</span><span class="sxs-lookup"><span data-stu-id="fcd1d-p101">Use the **StillExecuting** property to determine if the most recently called asynchronous **Execute** or **OpenConnection** method (that is, a method executed with the **dbRunAsync** option) is complete. While the **StillExecuting** property is **True**, any returned object cannot be accessed.</span></span>

<span data-ttu-id="fcd1d-p102">Assim que a propriedade **StillExecuting** retornar **False**, depois que a chamada **OpenConnection** retornar o objeto **Connection** associado, o objeto poderá ser mencionado. Contanto que **StillExecuting** permaneça **True**, o objeto poderá não ser mencionado, a não ser para ler a propriedade **StillExecuting**.</span><span class="sxs-lookup"><span data-stu-id="fcd1d-p102">Once the **StillExecuting** property returns **False**, following the **OpenConnection** call that returns the associated **Connection** object, the object can be referenced. So long as **StillExecuting** remains **True**, the object may not be referenced, other than to read the **StillExecuting** property.</span></span>

<span data-ttu-id="fcd1d-112">Use o método **[Cancel](connection-cancel-method-dao.md)** para concluir a execução de uma tarefa em andamento.</span><span class="sxs-lookup"><span data-stu-id="fcd1d-112">Use the **[Cancel](connection-cancel-method-dao.md)** method to terminate execution of a task in progress.</span></span>

