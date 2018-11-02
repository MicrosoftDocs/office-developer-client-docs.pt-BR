---
title: Método Close (DAO)
TOCTitle: Close Method
ms:assetid: 9b1a77cb-da12-24d6-892f-a56be103d51d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198015(v=office.15)
ms:contentKeyID: 48546559
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b6f84b9580fbd6256069de57b2295cf3460edaf8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928975"
---
# <a name="connectionclose-method-dao"></a><span data-ttu-id="8ef53-102">Método Close (DAO)</span><span class="sxs-lookup"><span data-stu-id="8ef53-102">Connection.Close method (DAO)</span></span>


<span data-ttu-id="8ef53-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="8ef53-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8ef53-104">Fecha um objeto **Connection** aberto.</span><span class="sxs-lookup"><span data-stu-id="8ef53-104">Closes an open **Connection**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ef53-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8ef53-105">Syntax</span></span>

<span data-ttu-id="8ef53-106">*expressão* . Fechar</span><span class="sxs-lookup"><span data-stu-id="8ef53-106">*expression* .Close</span></span>

<span data-ttu-id="8ef53-107">*expressão* Uma variável que representa um objeto de **Conexão** .</span><span class="sxs-lookup"><span data-stu-id="8ef53-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ef53-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="8ef53-108">Remarks</span></span>

<span data-ttu-id="8ef53-109">Se o objeto **Recordset** já estiver fechado quando você usar **Close**, ocorrerá um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="8ef53-109">If the **Recordset** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="8ef53-p101">Se você tentar fechar um objeto **Connection** enquanto ele tiver objetos **Recordset** abertos, os objetos **Recordset** serão fechados e quaisquer atualizações ou edições pendentes serão canceladas. Da mesma maneira, se você tentar fechar um objeto **Workspace** enquanto ele tiver objetos **Connection** abertos, esses objetos **Connection** serão fechados, o que fechará seus objetos **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="8ef53-p101">If you try to close a **Connection** object while it has any open **Recordset** objects, the **Recordset** objects will be closed and any pending updates or edits will be canceled. Similarly, if you try to close a **Workspace** object while it has any open **Connection** objects, those **Connection** objects will be closed, which will close their **Recordset** objects.</span></span>

<span data-ttu-id="8ef53-112">Uma alternativa ao método **Close** é definir o valor de uma variável de objeto para **Nothing** (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="8ef53-112">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

