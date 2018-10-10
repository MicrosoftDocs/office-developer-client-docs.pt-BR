---
title: Propriedade Containers.Count (DAO)
TOCTitle: Count Property
ms:assetid: 3b0bf865-a4d5-82bb-c1a9-9957f110db4c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192657(v=office.15)
ms:contentKeyID: 48544276
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 233066d9860547c2410f6e480563b51f77ad5766
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463129"
---
# <a name="containerscount-property-dao"></a><span data-ttu-id="8d601-102">Propriedade Containers.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="8d601-102">Containers.Count Property (DAO)</span></span>


<span data-ttu-id="8d601-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8d601-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8d601-104">Retorna o número de objetos **[Connection](connection-object-dao.md)** na coleção **[Connections](connections-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="8d601-104">Returns the number of **[Connection](connection-object-dao.md)** objects in the **[Connections](connections-collection-dao.md)** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d601-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8d601-105">Syntax</span></span>

<span data-ttu-id="8d601-106">*expressão* . Contagem</span><span class="sxs-lookup"><span data-stu-id="8d601-106">*expression* .Count</span></span>

<span data-ttu-id="8d601-107">*expressão* Uma variável que representa um objeto **Connections** .</span><span class="sxs-lookup"><span data-stu-id="8d601-107">*expression* A variable that represents a **Connections** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d601-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="8d601-108">Remarks</span></span>

<span data-ttu-id="8d601-p101">Como os membros de uma coleção começam com 0, você sempre deve codificar os loops começando com o membro 0 e terminando com o valor da propriedade **Count** menos 1. Para efetuar loop pelos membros de uma coleção sem verificar a propriedade **Count**, use o comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="8d601-p101">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="8d601-p102">A definição da propriedade **Count** nunca será Null. Se o valor for 0, não haverá objetos na coleção.</span><span class="sxs-lookup"><span data-stu-id="8d601-p102">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

