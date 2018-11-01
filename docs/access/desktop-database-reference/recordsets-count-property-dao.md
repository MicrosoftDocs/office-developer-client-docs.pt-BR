---
title: Propriedade Recordsets.Count (DAO)
TOCTitle: Count Property
ms:assetid: 4362aa16-c8e9-e517-887e-c4532bd1eef9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192940(v=office.15)
ms:contentKeyID: 48544500
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3a5697dcb6dbf3eb306ac94041127ee3e5992467
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881661"
---
# <a name="recordsetscount-property-dao"></a><span data-ttu-id="5dda7-102">Propriedade Recordsets.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="5dda7-102">Recordsets.Count Property (DAO)</span></span>


<span data-ttu-id="5dda7-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="5dda7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5dda7-p101">Retorna o número de objetos da coleção especificada. **Integer** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="5dda7-p101">Returns the number of objects in the specified collection. Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dda7-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5dda7-106">Syntax</span></span>

<span data-ttu-id="5dda7-107">*expressão* . Contagem</span><span class="sxs-lookup"><span data-stu-id="5dda7-107">*expression* .Count</span></span>

<span data-ttu-id="5dda7-108">*expressão* Uma variável que representa um objeto **Recordsets** .</span><span class="sxs-lookup"><span data-stu-id="5dda7-108">*expression* A variable that represents a **Recordsets** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5dda7-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="5dda7-109">Remarks</span></span>

<span data-ttu-id="5dda7-p102">Como os membros de uma coleção começam com 0, você sempre deve codificar os loops começando com o membro 0 e terminando com o valor da propriedade **Count** menos 1. Para efetuar loop pelos membros de uma coleção sem verificar a propriedade **Count**, use o comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="5dda7-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="5dda7-p103">A definição da propriedade **Count** nunca será Null. Se o valor for 0, não haverá objetos na coleção.</span><span class="sxs-lookup"><span data-stu-id="5dda7-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

