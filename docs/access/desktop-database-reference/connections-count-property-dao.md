---
title: Propriedade Connections.Count (DAO)
TOCTitle: Count Property
ms:assetid: 9b2f0aaa-785a-7fe7-15c3-aea37fdacd12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198023(v=office.15)
ms:contentKeyID: 48546563
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 572fed8afa9eb0f40a2b4938a31e866824147c83
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924461"
---
# <a name="connectionscount-property-dao"></a><span data-ttu-id="393ec-102">Propriedade Connections.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="393ec-102">Connections.Count property (DAO)</span></span>


<span data-ttu-id="393ec-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="393ec-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="393ec-104">Retorna o número de objetos **[Connection](connection-object-dao.md)** na coleção **[Connections](connections-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="393ec-104">Returns the number of **[Connection](connection-object-dao.md)** objects in the **[Connections](connections-collection-dao.md)** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="393ec-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="393ec-105">Syntax</span></span>

<span data-ttu-id="393ec-106">*expressão* . Contagem</span><span class="sxs-lookup"><span data-stu-id="393ec-106">*expression* .Count</span></span>

<span data-ttu-id="393ec-107">*expressão* Uma variável que representa um objeto **Connections** .</span><span class="sxs-lookup"><span data-stu-id="393ec-107">*expression* A variable that represents a **Connections** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="393ec-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="393ec-108">Remarks</span></span>

<span data-ttu-id="393ec-p101">Como os membros de uma coleção começam com 0, você sempre deve codificar os loops começando com o membro 0 e terminando com o valor da propriedade **Count** menos 1. Para efetuar loop pelos membros de uma coleção sem verificar a propriedade **Count**, use o comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="393ec-p101">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="393ec-p102">A definição da propriedade **Count** nunca será Null. Se o valor for 0, não haverá objetos na coleção.</span><span class="sxs-lookup"><span data-stu-id="393ec-p102">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

