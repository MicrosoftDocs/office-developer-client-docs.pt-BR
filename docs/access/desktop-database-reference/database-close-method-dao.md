---
title: Método Database.Close (DAO)
TOCTitle: Close Method
ms:assetid: b777ee92-172a-3342-31fc-76e7361c47fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822418(v=office.15)
ms:contentKeyID: 48547296
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 92b4075f09bb34eca465f49d30a9ba8777b3e583
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869649"
---
# <a name="databaseclose-method-dao"></a><span data-ttu-id="7a072-102">Método Database.Close (DAO)</span><span class="sxs-lookup"><span data-stu-id="7a072-102">Database.Close Method (DAO)</span></span>


<span data-ttu-id="7a072-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="7a072-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7a072-104">Fecha um objeto **Database** aberto.</span><span class="sxs-lookup"><span data-stu-id="7a072-104">Closes an open **Database**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a072-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7a072-105">Syntax</span></span>

<span data-ttu-id="7a072-106">*expressão* . Fechar</span><span class="sxs-lookup"><span data-stu-id="7a072-106">*expression* .Close</span></span>

<span data-ttu-id="7a072-107">*expressão* Uma variável que representa um objeto de **banco de dados** .</span><span class="sxs-lookup"><span data-stu-id="7a072-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a072-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a072-108">Remarks</span></span>

<span data-ttu-id="7a072-109">Se o objeto **Database** já estiver fechado quando você usar **Close**, ocorrerá um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="7a072-109">If the **Database** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="7a072-110">Uma alternativa ao método **Close** é definir o valor de uma variável de objeto para **Nothing** (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="7a072-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

