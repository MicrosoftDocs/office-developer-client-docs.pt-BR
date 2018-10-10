---
title: Propriedade Parameters.Count (DAO)
TOCTitle: Count Property
ms:assetid: bc8c814b-da55-22b7-431f-a0f7e6cac994
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822720(v=office.15)
ms:contentKeyID: 48547415
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 318fc1c5f93edc032aaf83a4f557e496e747743b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463690"
---
# <a name="parameterscount-property-dao"></a><span data-ttu-id="fb89f-102">Propriedade Parameters.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="fb89f-102">Parameters.Count Property (DAO)</span></span>


<span data-ttu-id="fb89f-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fb89f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fb89f-p101">Retorna o número de objetos na coleção especificada. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="fb89f-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb89f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb89f-106">Syntax</span></span>

<span data-ttu-id="fb89f-107">*expressão* . Contagem</span><span class="sxs-lookup"><span data-stu-id="fb89f-107">*expression* .Count</span></span>

<span data-ttu-id="fb89f-108">*expressão* Uma variável que representa um objeto **Parameters** .</span><span class="sxs-lookup"><span data-stu-id="fb89f-108">*expression* A variable that represents a **Parameters** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb89f-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb89f-109">Remarks</span></span>

<span data-ttu-id="fb89f-p102">Como os membros de uma coleção começam com 0, você sempre deve codificar os loops começando com o membro 0 e terminando com o valor da propriedade **Count** menos 1. Para efetuar loop pelos membros de uma coleção sem verificar a propriedade **Count**, use o comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="fb89f-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="fb89f-p103">A definição da propriedade **Count** nunca será Null. Se o valor for 0, não haverá objetos na coleção.</span><span class="sxs-lookup"><span data-stu-id="fb89f-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

