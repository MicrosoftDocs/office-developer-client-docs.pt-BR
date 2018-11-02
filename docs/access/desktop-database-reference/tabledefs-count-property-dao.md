---
title: Propriedade TableDefs.Count (DAO)
TOCTitle: Count Property
ms:assetid: 6e2cf3e5-524f-a643-b1dc-99a4b2bb2e63
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195561(v=office.15)
ms:contentKeyID: 48545508
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 88a38180973b83232c324d052db0548cb308740a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923767"
---
# <a name="tabledefscount-property-dao"></a><span data-ttu-id="23cf7-102">Propriedade TableDefs.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="23cf7-102">TableDefs.Count property (DAO)</span></span>


<span data-ttu-id="23cf7-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="23cf7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="23cf7-p101">Retorna o número de objetos na coleção especificada. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="23cf7-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="23cf7-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="23cf7-106">Syntax</span></span>

<span data-ttu-id="23cf7-107">*expressão* . Contagem</span><span class="sxs-lookup"><span data-stu-id="23cf7-107">*expression* .Count</span></span>

<span data-ttu-id="23cf7-108">*expressão* Uma variável que representa um objeto **TableDefs** .</span><span class="sxs-lookup"><span data-stu-id="23cf7-108">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="23cf7-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="23cf7-109">Remarks</span></span>

<span data-ttu-id="23cf7-p102">Como os membros de uma coleção começam com 0, você sempre deve codificar os loops começando com o membro 0 e terminando com o valor da propriedade **Count** menos 1. Para efetuar loop pelos membros de uma coleção sem verificar a propriedade **Count**, use o comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="23cf7-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="23cf7-p103">A definição da propriedade **Count** nunca será Null. Se o valor for 0, não haverá objetos na coleção.</span><span class="sxs-lookup"><span data-stu-id="23cf7-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

