---
title: Propriedade Relations.Count (DAO)
TOCTitle: Count Property
ms:assetid: 7cb3885f-6896-8402-8b18-12769473f051
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196377(v=office.15)
ms:contentKeyID: 48545843
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dd9cc00d2dc33263d6226783770fdae5207137f5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699559"
---
# <a name="relationscount-property-dao"></a><span data-ttu-id="a93ad-102">Propriedade Relations.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="a93ad-102">Relations.Count property (DAO)</span></span>


<span data-ttu-id="a93ad-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="a93ad-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a93ad-p101">Retorna o número de objetos na coleção especificada. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="a93ad-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a93ad-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a93ad-106">Syntax</span></span>

<span data-ttu-id="a93ad-107">*expressão* . Contagem</span><span class="sxs-lookup"><span data-stu-id="a93ad-107">*expression* .Count</span></span>

<span data-ttu-id="a93ad-108">*expressão* Uma variável que representa um objeto **Relations** .</span><span class="sxs-lookup"><span data-stu-id="a93ad-108">*expression* A variable that represents a **Relations** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a93ad-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="a93ad-109">Remarks</span></span>

<span data-ttu-id="a93ad-p102">Como os membros de uma coleção começam com 0, você sempre deve codificar os loops começando com o membro 0 e terminando com o valor da propriedade **Count** menos 1. Para efetuar loop pelos membros de uma coleção sem verificar a propriedade **Count**, use o comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="a93ad-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="a93ad-p103">A definição da propriedade **Count** nunca será Null. Se o valor for 0, não haverá objetos na coleção.</span><span class="sxs-lookup"><span data-stu-id="a93ad-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

