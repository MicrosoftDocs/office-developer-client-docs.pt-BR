---
title: Método Workspace.Close (DAO)
TOCTitle: Close Method
ms:assetid: 9b3d28f9-5cde-0dd9-8a4a-d2efaec5fe5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198027(v=office.15)
ms:contentKeyID: 48546565
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 63b935fa178eb4c55ce11724ec3fd5f62d056779
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919847"
---
# <a name="workspaceclose-method-dao"></a><span data-ttu-id="16f10-102">Método Workspace.Close (DAO)</span><span class="sxs-lookup"><span data-stu-id="16f10-102">Workspace.Close method (DAO)</span></span>


<span data-ttu-id="16f10-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="16f10-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="16f10-104">Fecha um **Workspace** aberto.</span><span class="sxs-lookup"><span data-stu-id="16f10-104">Closes an open **Workspace**.</span></span>

## <a name="syntax"></a><span data-ttu-id="16f10-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16f10-105">Syntax</span></span>

<span data-ttu-id="16f10-106">*expressão* . Fechar</span><span class="sxs-lookup"><span data-stu-id="16f10-106">*expression* .Close</span></span>

<span data-ttu-id="16f10-107">*expressão* Uma variável que representa um objeto **Workspace** .</span><span class="sxs-lookup"><span data-stu-id="16f10-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="16f10-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="16f10-108">Remarks</span></span>

<span data-ttu-id="16f10-109">Se o objeto **Workspace** já estiver fechado quando você usar **Close**, ocorrerá um erro de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="16f10-109">If the **Workspace** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="16f10-110">Uma alternativa ao método **Close** é definir o valor de uma variável de objeto para **Nothing** (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="16f10-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

