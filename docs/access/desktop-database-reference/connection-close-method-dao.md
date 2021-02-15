---
title: Método Connection.Close (DAO)
TOCTitle: Close Method
ms:assetid: 9b1a77cb-da12-24d6-892f-a56be103d51d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198015(v=office.15)
ms:contentKeyID: 48546559
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bf99abf97a2eb1b88e7056a36c160eb774959719
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295958"
---
# <a name="connectionclose-method-dao"></a><span data-ttu-id="6bbf3-102">Método Connection.Close (DAO)</span><span class="sxs-lookup"><span data-stu-id="6bbf3-102">Connection.Close method (DAO)</span></span>


<span data-ttu-id="6bbf3-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6bbf3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6bbf3-104">Fecha um objeto **Connection** aberto.</span><span class="sxs-lookup"><span data-stu-id="6bbf3-104">Closes an open **Connection**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bbf3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6bbf3-105">Syntax</span></span>

<span data-ttu-id="6bbf3-106">*expressão* .Close</span><span class="sxs-lookup"><span data-stu-id="6bbf3-106">*expression* .Close</span></span>

<span data-ttu-id="6bbf3-107">*expressão* Uma variável que representa um objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="6bbf3-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bbf3-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="6bbf3-108">Remarks</span></span>

<span data-ttu-id="6bbf3-109">Se o objeto **Recordset** já estiver fechado quando você usar **Close**, ocorrerá um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="6bbf3-109">If the **Recordset** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="6bbf3-p101">Se você tentar fechar um objeto **Connection** enquanto ele tiver objetos **Recordset** abertos, os objetos **Recordset** serão fechados e quaisquer atualizações ou edições pendentes serão canceladas. Da mesma maneira, se você tentar fechar um objeto **Workspace** enquanto ele tiver objetos **Connection** abertos, esses objetos **Connection** serão fechados, o que fechará seus objetos **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="6bbf3-p101">If you try to close a **Connection** object while it has any open **Recordset** objects, the **Recordset** objects will be closed and any pending updates or edits will be canceled. Similarly, if you try to close a **Workspace** object while it has any open **Connection** objects, those **Connection** objects will be closed, which will close their **Recordset** objects.</span></span>

<span data-ttu-id="6bbf3-112">Uma alternativa ao método **Fechar**, é definir o valor de uma variável de um objeto para **Nada** (Definir dbsTemp = Nada).</span><span class="sxs-lookup"><span data-stu-id="6bbf3-112">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

