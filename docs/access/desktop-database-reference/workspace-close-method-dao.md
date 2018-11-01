---
title: Método Workspace.Close (DAO)
TOCTitle: Close Method
ms:assetid: 9b3d28f9-5cde-0dd9-8a4a-d2efaec5fe5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198027(v=office.15)
ms:contentKeyID: 48546565
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 38f1a7a525a2cf57a98ee3fa015ce29b368aab9b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884125"
---
# <a name="workspaceclose-method-dao"></a><span data-ttu-id="ba0bc-102">Método Workspace.Close (DAO)</span><span class="sxs-lookup"><span data-stu-id="ba0bc-102">Workspace.Close Method (DAO)</span></span>


<span data-ttu-id="ba0bc-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="ba0bc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ba0bc-104">Fecha um **Workspace** aberto.</span><span class="sxs-lookup"><span data-stu-id="ba0bc-104">Closes an open **Workspace**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba0bc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba0bc-105">Syntax</span></span>

<span data-ttu-id="ba0bc-106">*expressão* . Fechar</span><span class="sxs-lookup"><span data-stu-id="ba0bc-106">*expression* .Close</span></span>

<span data-ttu-id="ba0bc-107">*expressão* Uma variável que representa um objeto **Workspace** .</span><span class="sxs-lookup"><span data-stu-id="ba0bc-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba0bc-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba0bc-108">Remarks</span></span>

<span data-ttu-id="ba0bc-109">Se o objeto **Workspace** já estiver fechado quando você usar **Close**, ocorrerá um erro de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="ba0bc-109">If the **Workspace** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="ba0bc-110">Uma alternativa ao método **Close** é definir o valor de uma variável de objeto para **Nothing** (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="ba0bc-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

