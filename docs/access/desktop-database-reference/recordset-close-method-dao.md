---
title: Método Recordset.Close (DAO)
TOCTitle: Close Method
ms:assetid: e76a81c6-ca0d-e310-c1dc-cbc5d6f6248b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836011(v=office.15)
ms:contentKeyID: 48548404
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1d19cc340079c94d2e5c6bf271fdee20d9a5c017
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464651"
---
# <a name="recordsetclose-method-dao"></a><span data-ttu-id="f4f4c-102">Método Recordset.Close (DAO)</span><span class="sxs-lookup"><span data-stu-id="f4f4c-102">Recordset.Close Method (DAO)</span></span>


<span data-ttu-id="f4f4c-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f4f4c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f4f4c-104">Fecha um **Recordset** aberto.</span><span class="sxs-lookup"><span data-stu-id="f4f4c-104">Closes an open **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4f4c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f4f4c-105">Syntax</span></span>

<span data-ttu-id="f4f4c-106">*expressão* . Fechar</span><span class="sxs-lookup"><span data-stu-id="f4f4c-106">*expression* .Close</span></span>

<span data-ttu-id="f4f4c-107">*expressão* Uma variável que representa um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="f4f4c-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4f4c-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4f4c-108">Remarks</span></span>

<span data-ttu-id="f4f4c-109">Se o objeto **Recordset** já estiver fechado quando você usar **Close**, ocorrerá um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="f4f4c-109">If the **Recordset** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="f4f4c-p101">Se você tentar fechar um objeto **Connection** enquanto ele tiver objetos **Recordset** abertos, os objetos **Recordset** serão fechados e quaisquer atualizações ou edições pendentes serão canceladas. Da mesma maneira, se você tentar fechar um objeto **Workspace** enquanto ele tiver objetos **Connection** abertos, esses objetos **Connection** serão fechados, o que fechará seus objetos **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f4f4c-p101">If you try to close a **Connection** object while it has any open **Recordset** objects, the **Recordset** objects will be closed and any pending updates or edits will be canceled. Similarly, if you try to close a **Workspace** object while it has any open **Connection** objects, those **Connection** objects will be closed, which will close their **Recordset** objects.</span></span>

<span data-ttu-id="f4f4c-112">Uma alternativa ao método **Close** é definir o valor de uma variável de objeto para **Nothing** (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="f4f4c-112">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

