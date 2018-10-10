---
title: Propriedade Errors (DAO)
TOCTitle: Count Property
ms:assetid: ad135955-3b18-4f99-66d9-aff1492df13b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821719(v=office.15)
ms:contentKeyID: 48547028
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7b554b88153e79dfc1909bd55d95a3c3e48a855e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465040"
---
# <a name="errorscount-property-dao"></a><span data-ttu-id="f49dd-102">Propriedade Errors (DAO)</span><span class="sxs-lookup"><span data-stu-id="f49dd-102">Errors.Count Property (DAO)</span></span>


<span data-ttu-id="f49dd-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f49dd-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f49dd-p101">Retorna o número de objetos na coleção especificada. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="f49dd-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f49dd-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f49dd-106">Syntax</span></span>

<span data-ttu-id="f49dd-107">*expressão* . Contagem</span><span class="sxs-lookup"><span data-stu-id="f49dd-107">*expression* .Count</span></span>

<span data-ttu-id="f49dd-108">*expressão* Uma variável que representa um objeto **Errors** .</span><span class="sxs-lookup"><span data-stu-id="f49dd-108">*expression* A variable that represents an **Errors** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f49dd-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="f49dd-109">Remarks</span></span>

<span data-ttu-id="f49dd-p102">Como os membros de uma coleção começam com 0, você sempre deve codificar os loops começando com o membro 0 e terminando com o valor da propriedade **Count** menos 1. Para efetuar loop pelos membros de uma coleção sem verificar a propriedade **Count**, use o comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="f49dd-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="f49dd-p103">A definição da propriedade **Count** nunca será Null. Se o valor for 0, não haverá objetos na coleção.</span><span class="sxs-lookup"><span data-stu-id="f49dd-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

