---
title: Método Workspace. Close (DAO)
TOCTitle: Close Method
ms:assetid: 9b3d28f9-5cde-0dd9-8a4a-d2efaec5fe5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198027(v=office.15)
ms:contentKeyID: 48546565
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0049fb335c869a050a2c20d5740c487413c76786
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305954"
---
# <a name="workspaceclose-method-dao"></a><span data-ttu-id="c46c4-102">Método Workspace. Close (DAO)</span><span class="sxs-lookup"><span data-stu-id="c46c4-102">Workspace.Close method (DAO)</span></span>


<span data-ttu-id="c46c4-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c46c4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c46c4-104">Fecha um **Workspace** aberto.</span><span class="sxs-lookup"><span data-stu-id="c46c4-104">Closes an open **Workspace**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c46c4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c46c4-105">Syntax</span></span>

<span data-ttu-id="c46c4-106">*expressão* . Fechado</span><span class="sxs-lookup"><span data-stu-id="c46c4-106">*expression* .Close</span></span>

<span data-ttu-id="c46c4-107">*expressão* Uma variável que representa um objeto **Workspace** .</span><span class="sxs-lookup"><span data-stu-id="c46c4-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c46c4-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="c46c4-108">Remarks</span></span>

<span data-ttu-id="c46c4-109">Se o objeto **Workspace** já estiver fechado quando você usar **Close**, ocorrerá um erro de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="c46c4-109">If the **Workspace** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="c46c4-110">Uma alternativa para o método **Close** é definir o valor de uma variável de objeto como **Nothing** (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="c46c4-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

