---
title: Propriedade Recordset2.StillExecuting (DAO)
TOCTitle: StillExecuting Property
ms:assetid: f051c350-0451-44fe-0e47-b152bae4b481
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836546(v=office.15)
ms:contentKeyID: 48548601
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa94622374990ce48c857e9ad45c3531975bb9a8
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705670"
---
# <a name="recordset2stillexecuting-property-dao"></a><span data-ttu-id="a918d-102">Propriedade Recordset2.StillExecuting (DAO)</span><span class="sxs-lookup"><span data-stu-id="a918d-102">Recordset2.StillExecuting property (DAO)</span></span>


<span data-ttu-id="a918d-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="a918d-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="a918d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a918d-104">Syntax</span></span>

<span data-ttu-id="a918d-105">*expressão* . StillExecuting</span><span class="sxs-lookup"><span data-stu-id="a918d-105">*expression* .StillExecuting</span></span>

<span data-ttu-id="a918d-106">*expressão* Uma variável que representa um objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="a918d-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a918d-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="a918d-107">Remarks</span></span>

<span data-ttu-id="a918d-p101">Use a propriedade **StillExecuting** para determinar se o método **Execute** ou **OpenConnection** chamado mais recentemente de forma assíncrona (ou seja, um método executado com a opção **dbRunAsync**) foi concluído. Enquanto a propriedade **StillExecuting** for **True**, qualquer objeto retornado não poderá ser acessado.</span><span class="sxs-lookup"><span data-stu-id="a918d-p101">Use the **StillExecuting** property to determine if the most recently called asynchronous **Execute** or **OpenConnection** method (that is, a method executed with the **dbRunAsync** option) is complete. While the **StillExecuting** property is **True**, any returned object cannot be accessed.</span></span>

<span data-ttu-id="a918d-p102">Assim que a propriedade **StillExecuting** retornar **False**, depois que a chamada **OpenConnection** retornar o objeto **Connection** associado, o objeto poderá ser mencionado. Contanto que **StillExecuting** permaneça **True**, o objeto poderá não ser mencionado, a não ser para ler a propriedade **StillExecuting**.</span><span class="sxs-lookup"><span data-stu-id="a918d-p102">Once the **StillExecuting** property returns **False**, following the **OpenConnection** call that returns the associated **Connection** object, the object can be referenced. So long as **StillExecuting** remains **True**, the object may not be referenced, other than to read the **StillExecuting** property.</span></span>

<span data-ttu-id="a918d-112">Use o método **[Cancel](connection-cancel-method-dao.md)** para concluir a execução de uma tarefa em andamento.</span><span class="sxs-lookup"><span data-stu-id="a918d-112">Use the **[Cancel](connection-cancel-method-dao.md)** method to terminate execution of a task in progress.</span></span>

