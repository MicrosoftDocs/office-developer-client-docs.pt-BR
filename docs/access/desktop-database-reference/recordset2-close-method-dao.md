---
title: Método Recordset2.Close (DAO)
TOCTitle: Close Method
ms:assetid: ef816969-9857-37cf-9562-d5c80d2815ea
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836412(v=office.15)
ms:contentKeyID: 48548584
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 62bd5f60ed48e863a5190a19e546d292156f8dac
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888332"
---
# <a name="recordset2close-method-dao"></a><span data-ttu-id="dd140-102">Método Recordset2.Close (DAO)</span><span class="sxs-lookup"><span data-stu-id="dd140-102">Recordset2.Close Method (DAO)</span></span>


<span data-ttu-id="dd140-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="dd140-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dd140-104">Fecha um **Recordset** aberto.</span><span class="sxs-lookup"><span data-stu-id="dd140-104">Closes an open **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd140-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dd140-105">Syntax</span></span>

<span data-ttu-id="dd140-106">*expressão* . Fechar</span><span class="sxs-lookup"><span data-stu-id="dd140-106">*expression* .Close</span></span>

<span data-ttu-id="dd140-107">*expressão* Uma variável que representa um objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="dd140-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd140-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="dd140-108">Remarks</span></span>

<span data-ttu-id="dd140-109">Se o objeto **Recordset** já estiver fechado quando você usar **Close**, ocorrerá um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="dd140-109">If the **Recordset** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="dd140-p101">Se você tentar fechar um objeto **Connection** enquanto ele tiver objetos **Recordset** abertos, os objetos **Recordset** serão fechados e quaisquer atualizações ou edições pendentes serão canceladas. Da mesma maneira, se você tentar fechar um objeto **Workspace** enquanto ele tiver objetos **Connection** abertos, esses objetos **Connection** serão fechados, o que fechará seus objetos **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="dd140-p101">If you try to close a **Connection** object while it has any open **Recordset** objects, the **Recordset** objects will be closed and any pending updates or edits will be canceled. Similarly, if you try to close a **Workspace** object while it has any open **Connection** objects, those **Connection** objects will be closed, which will close their **Recordset** objects.</span></span>

<span data-ttu-id="dd140-112">Uma alternativa ao método **Close** é definir o valor de uma variável de objeto para **Nothing** (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="dd140-112">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

