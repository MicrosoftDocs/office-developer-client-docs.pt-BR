---
title: Propriedade Indexes.Count (DAO)
TOCTitle: Count Property
ms:assetid: 195ede10-f91e-50c6-6af4-b318c476b9ea
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845647(v=office.15)
ms:contentKeyID: 48543499
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cffbf14e73e97113194eb25b8e0d5799d3578086
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718025"
---
# <a name="indexescount-property-dao"></a><span data-ttu-id="95b48-102">Propriedade Indexes.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="95b48-102">Indexes.Count property (DAO)</span></span>


<span data-ttu-id="95b48-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="95b48-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="95b48-p101">Retorna o número de objetos na coleção especificada. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="95b48-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="95b48-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="95b48-106">Syntax</span></span>

<span data-ttu-id="95b48-107">*expressão* . Contagem</span><span class="sxs-lookup"><span data-stu-id="95b48-107">*expression* .Count</span></span>

<span data-ttu-id="95b48-108">*expressão* Uma variável que representa um objeto **Indexes** .</span><span class="sxs-lookup"><span data-stu-id="95b48-108">*expression* A variable that represents an **Indexes** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="95b48-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="95b48-109">Remarks</span></span>

<span data-ttu-id="95b48-p102">Como os membros de uma coleção começam com 0, você sempre deve codificar os loops começando com o membro 0 e terminando com o valor da propriedade **Count** menos 1. Para efetuar loop pelos membros de uma coleção sem verificar a propriedade **Count**, use o comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="95b48-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="95b48-p103">A definição da propriedade **Count** nunca será Null. Se o valor for 0, não haverá objetos na coleção.</span><span class="sxs-lookup"><span data-stu-id="95b48-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

