---
title: Propriedade Indexes. Count (DAO)
TOCTitle: Count Property
ms:assetid: 195ede10-f91e-50c6-6af4-b318c476b9ea
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845647(v=office.15)
ms:contentKeyID: 48543499
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cffbf14e73e97113194eb25b8e0d5799d3578086
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291542"
---
# <a name="indexescount-property-dao"></a><span data-ttu-id="7238d-102">Propriedade Indexes. Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="7238d-102">Indexes.Count property (DAO)</span></span>


<span data-ttu-id="7238d-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7238d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7238d-104">Retorna o número de objetos na coleção especificada.</span><span class="sxs-lookup"><span data-stu-id="7238d-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="7238d-105">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="7238d-105">Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7238d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7238d-106">Syntax</span></span>

<span data-ttu-id="7238d-107">*expressão* . Desconto</span><span class="sxs-lookup"><span data-stu-id="7238d-107">*expression* .Count</span></span>

<span data-ttu-id="7238d-108">*expressão* Uma variável que representa um \*\*\*\* objeto indexes.</span><span class="sxs-lookup"><span data-stu-id="7238d-108">*expression* A variable that represents an **Indexes** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7238d-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="7238d-109">Remarks</span></span>

<span data-ttu-id="7238d-p102">Como os membros de uma coleção começam com 0, você sempre deve codificar os loops começando com o membro 0 e terminando com o valor da propriedade **Count** menos 1. Se você deseja fazer um loop nos membros de uma coleção sem verificar a propriedade **Count**, use o comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="7238d-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="7238d-p103">A definição da propriedade **Count** nunca será Null. Se o valor for 0, não existirão objetos na coleção.</span><span class="sxs-lookup"><span data-stu-id="7238d-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

