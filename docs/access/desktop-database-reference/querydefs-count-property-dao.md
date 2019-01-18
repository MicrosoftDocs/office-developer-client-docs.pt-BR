---
title: Propriedade QueryDefs.Count (DAO)
TOCTitle: Count Property
ms:assetid: 8caa01c5-692f-95e4-4b11-6e6c591f5872
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197340(v=office.15)
ms:contentKeyID: 48546240
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95624c82ee9ab322eec5455759cf4ec2e9708dba
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707427"
---
# <a name="querydefscount-property-dao"></a><span data-ttu-id="00cdf-102">Propriedade QueryDefs.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="00cdf-102">QueryDefs.Count property (DAO)</span></span>


<span data-ttu-id="00cdf-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="00cdf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="00cdf-p101">Retorna o número de objetos na coleção especificada. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="00cdf-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="00cdf-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="00cdf-106">Syntax</span></span>

<span data-ttu-id="00cdf-107">*expressão* . Contagem</span><span class="sxs-lookup"><span data-stu-id="00cdf-107">*expression* .Count</span></span>

<span data-ttu-id="00cdf-108">*expressão* Uma variável que representa um objeto **QueryDefs** .</span><span class="sxs-lookup"><span data-stu-id="00cdf-108">*expression* A variable that represents a **QueryDefs** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="00cdf-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="00cdf-109">Remarks</span></span>

<span data-ttu-id="00cdf-p102">Como os membros de uma coleção começam com 0, você sempre deve codificar os loops começando com o membro 0 e terminando com o valor da propriedade **Count** menos 1. Para efetuar loop pelos membros de uma coleção sem verificar a propriedade **Count**, use o comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="00cdf-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="00cdf-p103">A definição da propriedade **Count** nunca será Null. Se o valor for 0, não haverá objetos na coleção.</span><span class="sxs-lookup"><span data-stu-id="00cdf-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

