---
title: Propriedade Databases.Count (DAO)
TOCTitle: Count Property
ms:assetid: 7c542b17-9806-e00e-8cbd-58d6d17e98c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196364(v=office.15)
ms:contentKeyID: 48545831
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cd8908492721315202c5bdf26109753c88905a07
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720125"
---
# <a name="databasescount-property-dao"></a><span data-ttu-id="25dac-102">Propriedade Databases.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="25dac-102">Databases.Count property (DAO)</span></span>


<span data-ttu-id="25dac-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="25dac-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="25dac-p101">Retorna o número de objetos na coleção especificada. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="25dac-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="25dac-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25dac-106">Syntax</span></span>

<span data-ttu-id="25dac-107">*expressão* . Contagem</span><span class="sxs-lookup"><span data-stu-id="25dac-107">*expression* .Count</span></span>

<span data-ttu-id="25dac-108">*expressão* Uma variável que representa um objeto de **bancos de dados** .</span><span class="sxs-lookup"><span data-stu-id="25dac-108">*expression* A variable that represents a **Databases** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="25dac-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="25dac-109">Remarks</span></span>

<span data-ttu-id="25dac-p102">Como os membros de uma coleção começam com 0, você sempre deve codificar os loops começando com o membro 0 e terminando com o valor da propriedade **Count** menos 1. Para efetuar loop pelos membros de uma coleção sem verificar a propriedade **Count**, use o comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="25dac-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="25dac-p103">A definição da propriedade **Count** nunca será Null. Se o valor for 0, não haverá objetos na coleção.</span><span class="sxs-lookup"><span data-stu-id="25dac-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

