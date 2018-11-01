---
title: Propriedade Workspaces.Count (DAO)
TOCTitle: Count Property
ms:assetid: bc7c5a11-13d3-27bd-1be4-5d069e888ac2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822719(v=office.15)
ms:contentKeyID: 48547414
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0632556d7e62b426f462e17d732db323513afcec
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888248"
---
# <a name="workspacescount-property-dao"></a><span data-ttu-id="34542-102">Propriedade Workspaces.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="34542-102">Workspaces.Count Property (DAO)</span></span>


<span data-ttu-id="34542-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="34542-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="34542-p101">Retorna o número de objetos na coleção especificada. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="34542-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="34542-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="34542-106">Syntax</span></span>

<span data-ttu-id="34542-107">*expressão* . Contagem</span><span class="sxs-lookup"><span data-stu-id="34542-107">*expression* .Count</span></span>

<span data-ttu-id="34542-108">*expressão* Uma variável que representa um objeto **Workspaces** .</span><span class="sxs-lookup"><span data-stu-id="34542-108">*expression* A variable that represents a **Workspaces** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="34542-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="34542-109">Remarks</span></span>

<span data-ttu-id="34542-p102">Como os membros de uma coleção começam com 0, você sempre deve codificar os loops começando com o membro 0 e terminando com o valor da propriedade **Count** menos 1. Para efetuar loop pelos membros de uma coleção sem verificar a propriedade **Count**, use o comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="34542-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="34542-p103">A definição da propriedade **Count** nunca será Null. Se o valor for 0, não haverá objetos na coleção.</span><span class="sxs-lookup"><span data-stu-id="34542-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

