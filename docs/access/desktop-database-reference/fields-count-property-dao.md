---
title: Propriedade Fields.Count (DAO)
TOCTitle: Count Property
ms:assetid: 574de1db-2640-159b-7756-28c37acc9f83
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194261(v=office.15)
ms:contentKeyID: 48544969
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2f788b726f5be7cdfd7531d4522b6c653744d1c8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886743"
---
# <a name="fieldscount-property-dao"></a><span data-ttu-id="e8d6f-102">Propriedade Fields.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="e8d6f-102">Fields.Count Property (DAO)</span></span>


<span data-ttu-id="e8d6f-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="e8d6f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e8d6f-p101">Retorna o número de objetos da coleção especificada. **Integer** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-p101">Returns the number of objects in the specified collection. Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8d6f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e8d6f-106">Syntax</span></span>

<span data-ttu-id="e8d6f-107">*expressão* . Contagem</span><span class="sxs-lookup"><span data-stu-id="e8d6f-107">*expression* .Count</span></span>

<span data-ttu-id="e8d6f-108">*expressão* Uma variável que representa um objeto **Fields** .</span><span class="sxs-lookup"><span data-stu-id="e8d6f-108">*expression* A variable that represents a **Fields** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8d6f-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8d6f-109">Remarks</span></span>

<span data-ttu-id="e8d6f-p102">Como os membros de uma coleção começam com 0, você sempre deve codificar os loops começando com o membro 0 e terminando com o valor da propriedade **Count** menos 1. Para efetuar loop pelos membros de uma coleção sem verificar a propriedade **Count**, use o comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="e8d6f-p103">A definição da propriedade **Count** nunca será Null. Se o valor for 0, não haverá objetos na coleção.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

