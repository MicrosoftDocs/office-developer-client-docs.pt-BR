---
title: Propriedade paraMeters. Count (DAO)
TOCTitle: Count Property
ms:assetid: bc8c814b-da55-22b7-431f-a0f7e6cac994
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822720(v=office.15)
ms:contentKeyID: 48547415
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 536e058a0485479cabd1cc2a0aae09f2396bfbcc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287871"
---
# <a name="parameterscount-property-dao"></a><span data-ttu-id="57194-102">Propriedade paraMeters. Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="57194-102">Parameters.Count property (DAO)</span></span>


<span data-ttu-id="57194-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="57194-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="57194-104">Retorna o número de objetos na coleção especificada.</span><span class="sxs-lookup"><span data-stu-id="57194-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="57194-105">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="57194-105">Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="57194-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="57194-106">Syntax</span></span>

<span data-ttu-id="57194-107">*expressão* . Desconto</span><span class="sxs-lookup"><span data-stu-id="57194-107">*expression* .Count</span></span>

<span data-ttu-id="57194-108">*expressão* Uma variável que representa um \*\*\*\* objeto Parameters.</span><span class="sxs-lookup"><span data-stu-id="57194-108">*expression* A variable that represents a **Parameters** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="57194-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="57194-109">Remarks</span></span>

<span data-ttu-id="57194-p102">Como os membros de uma coleção começam com 0, você sempre deve codificar os loops começando com o membro 0 e terminando com o valor da propriedade **Count** menos 1. Se você deseja fazer um loop nos membros de uma coleção sem verificar a propriedade **Count**, use o comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="57194-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="57194-p103">A definição da propriedade **Count** nunca será Null. Se o valor for 0, não existirão objetos na coleção.</span><span class="sxs-lookup"><span data-stu-id="57194-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

