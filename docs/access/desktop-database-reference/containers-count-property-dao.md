---
title: Propriedade Containers.Count (DAO)
TOCTitle: Count Property
ms:assetid: 3b0bf865-a4d5-82bb-c1a9-9957f110db4c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192657(v=office.15)
ms:contentKeyID: 48544276
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 49ec4181d64f26d7a1a5d54ed58bfef6c1206bda
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873408"
---
# <a name="containerscount-property-dao"></a><span data-ttu-id="6f9c2-102">Propriedade Containers.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="6f9c2-102">Containers.Count Property (DAO)</span></span>


<span data-ttu-id="6f9c2-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="6f9c2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6f9c2-104">Retorna o número de objetos **[Connection](connection-object-dao.md)** na coleção **[Connections](connections-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="6f9c2-104">Returns the number of **[Connection](connection-object-dao.md)** objects in the **[Connections](connections-collection-dao.md)** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f9c2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6f9c2-105">Syntax</span></span>

<span data-ttu-id="6f9c2-106">*expressão* . Contagem</span><span class="sxs-lookup"><span data-stu-id="6f9c2-106">*expression* .Count</span></span>

<span data-ttu-id="6f9c2-107">*expressão* Uma variável que representa um objeto **Connections** .</span><span class="sxs-lookup"><span data-stu-id="6f9c2-107">*expression* A variable that represents a **Connections** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f9c2-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f9c2-108">Remarks</span></span>

<span data-ttu-id="6f9c2-p101">Como os membros de uma coleção começam com 0, você sempre deve codificar os loops começando com o membro 0 e terminando com o valor da propriedade **Count** menos 1. Para efetuar loop pelos membros de uma coleção sem verificar a propriedade **Count**, use o comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="6f9c2-p101">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="6f9c2-p102">A definição da propriedade **Count** nunca será Null. Se o valor for 0, não haverá objetos na coleção.</span><span class="sxs-lookup"><span data-stu-id="6f9c2-p102">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

