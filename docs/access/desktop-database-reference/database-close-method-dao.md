---
title: Método Database.Close (DAO)
TOCTitle: Close Method
ms:assetid: b777ee92-172a-3342-31fc-76e7361c47fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822418(v=office.15)
ms:contentKeyID: 48547296
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 190b47b59bd9781553912f91156c74a3fd09c2d5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295020"
---
# <a name="databaseclose-method-dao"></a><span data-ttu-id="56e89-102">Método Database.Close (DAO)</span><span class="sxs-lookup"><span data-stu-id="56e89-102">Database.Close method (DAO)</span></span>


<span data-ttu-id="56e89-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="56e89-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="56e89-104">Fecha um objeto **Database** aberto.</span><span class="sxs-lookup"><span data-stu-id="56e89-104">Closes an open **Database**.</span></span>

## <a name="syntax"></a><span data-ttu-id="56e89-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="56e89-105">Syntax</span></span>

<span data-ttu-id="56e89-106">*expressão* .Close</span><span class="sxs-lookup"><span data-stu-id="56e89-106">*expression* .Close</span></span>

<span data-ttu-id="56e89-107">*expressão* Uma variável que representa um objeto do **Banco de dados**.</span><span class="sxs-lookup"><span data-stu-id="56e89-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="56e89-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="56e89-108">Remarks</span></span>

<span data-ttu-id="56e89-109">Se o objeto **Database** já estiver fechado quando você usar **Close**, ocorrerá um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="56e89-109">If the **Database** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="56e89-110">Uma alternativa ao método **Fechar**, é definir o valor de uma variável de um objeto para **Nada** (Definir dbsTemp = Nada).</span><span class="sxs-lookup"><span data-stu-id="56e89-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

