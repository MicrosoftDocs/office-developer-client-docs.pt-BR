---
title: Método Database.Close (DAO)
TOCTitle: Close Method
ms:assetid: b777ee92-172a-3342-31fc-76e7361c47fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822418(v=office.15)
ms:contentKeyID: 48547296
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c97786db2e909074f1a1e0d81e4af03d34301602
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920680"
---
# <a name="databaseclose-method-dao"></a><span data-ttu-id="7ec82-102">Método Database.Close (DAO)</span><span class="sxs-lookup"><span data-stu-id="7ec82-102">Database.Close method (DAO)</span></span>


<span data-ttu-id="7ec82-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="7ec82-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7ec82-104">Fecha um objeto **Database** aberto.</span><span class="sxs-lookup"><span data-stu-id="7ec82-104">Closes an open **Database**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ec82-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ec82-105">Syntax</span></span>

<span data-ttu-id="7ec82-106">*expressão* . Fechar</span><span class="sxs-lookup"><span data-stu-id="7ec82-106">*expression* .Close</span></span>

<span data-ttu-id="7ec82-107">*expressão* Uma variável que representa um objeto de **banco de dados** .</span><span class="sxs-lookup"><span data-stu-id="7ec82-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ec82-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ec82-108">Remarks</span></span>

<span data-ttu-id="7ec82-109">Se o objeto **Database** já estiver fechado quando você usar **Close**, ocorrerá um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="7ec82-109">If the **Database** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="7ec82-110">Uma alternativa ao método **Close** é definir o valor de uma variável de objeto para **Nothing** (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="7ec82-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

