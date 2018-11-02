---
title: Propriedade QueryDefs.Count (DAO)
TOCTitle: Count Property
ms:assetid: 8caa01c5-692f-95e4-4b11-6e6c591f5872
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197340(v=office.15)
ms:contentKeyID: 48546240
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f5efc7479f69d379f406a9a7cda5d4c522df6325
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930893"
---
# <a name="querydefscount-property-dao"></a><span data-ttu-id="2a9d5-102">Propriedade QueryDefs.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="2a9d5-102">QueryDefs.Count property (DAO)</span></span>


<span data-ttu-id="2a9d5-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="2a9d5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2a9d5-p101">Retorna o número de objetos na coleção especificada. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="2a9d5-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a9d5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2a9d5-106">Syntax</span></span>

<span data-ttu-id="2a9d5-107">*expressão* . Contagem</span><span class="sxs-lookup"><span data-stu-id="2a9d5-107">*expression* .Count</span></span>

<span data-ttu-id="2a9d5-108">*expressão* Uma variável que representa um objeto **QueryDefs** .</span><span class="sxs-lookup"><span data-stu-id="2a9d5-108">*expression* A variable that represents a **QueryDefs** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a9d5-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a9d5-109">Remarks</span></span>

<span data-ttu-id="2a9d5-p102">Como os membros de uma coleção começam com 0, você sempre deve codificar os loops começando com o membro 0 e terminando com o valor da propriedade **Count** menos 1. Para efetuar loop pelos membros de uma coleção sem verificar a propriedade **Count**, use o comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="2a9d5-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="2a9d5-p103">A definição da propriedade **Count** nunca será Null. Se o valor for 0, não haverá objetos na coleção.</span><span class="sxs-lookup"><span data-stu-id="2a9d5-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

