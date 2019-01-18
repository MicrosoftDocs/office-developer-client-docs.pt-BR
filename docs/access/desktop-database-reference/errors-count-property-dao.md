---
title: Propriedade Errors (DAO)
TOCTitle: Count Property
ms:assetid: ad135955-3b18-4f99-66d9-aff1492df13b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821719(v=office.15)
ms:contentKeyID: 48547028
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c2cbbed2c7061b225d969dbd7554191e8db4a28a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707252"
---
# <a name="errorscount-property-dao"></a><span data-ttu-id="46d12-102">Propriedade Errors (DAO)</span><span class="sxs-lookup"><span data-stu-id="46d12-102">Errors.Count property (DAO)</span></span>


<span data-ttu-id="46d12-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="46d12-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="46d12-p101">Retorna o número de objetos na coleção especificada. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="46d12-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="46d12-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46d12-106">Syntax</span></span>

<span data-ttu-id="46d12-107">*expressão* . Contagem</span><span class="sxs-lookup"><span data-stu-id="46d12-107">*expression* .Count</span></span>

<span data-ttu-id="46d12-108">*expressão* Uma variável que representa um objeto **Errors** .</span><span class="sxs-lookup"><span data-stu-id="46d12-108">*expression* A variable that represents an **Errors** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="46d12-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="46d12-109">Remarks</span></span>

<span data-ttu-id="46d12-p102">Como os membros de uma coleção começam com 0, você sempre deve codificar os loops começando com o membro 0 e terminando com o valor da propriedade **Count** menos 1. Para efetuar loop pelos membros de uma coleção sem verificar a propriedade **Count**, use o comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="46d12-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="46d12-p103">A definição da propriedade **Count** nunca será Null. Se o valor for 0, não haverá objetos na coleção.</span><span class="sxs-lookup"><span data-stu-id="46d12-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

