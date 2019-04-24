---
title: Propriedade Recordsets. Count (DAO)
TOCTitle: Count Property
ms:assetid: 4362aa16-c8e9-e517-887e-c4532bd1eef9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192940(v=office.15)
ms:contentKeyID: 48544500
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a81c1ede8a3afb95e39b2c33fb8112119faf8bd8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309287"
---
# <a name="recordsetscount-property-dao"></a><span data-ttu-id="c9d16-102">Propriedade Recordsets. Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="c9d16-102">Recordsets.Count property (DAO)</span></span>


<span data-ttu-id="c9d16-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c9d16-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c9d16-104">Retorna o número de objetos da coleção especificada.</span><span class="sxs-lookup"><span data-stu-id="c9d16-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="c9d16-105">**Integer** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="c9d16-105">Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9d16-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9d16-106">Syntax</span></span>

<span data-ttu-id="c9d16-107">*expressão* . Desconto</span><span class="sxs-lookup"><span data-stu-id="c9d16-107">*expression* .Count</span></span>

<span data-ttu-id="c9d16-108">*expressão* Uma variável que representa um \*\*\*\* objeto Recordsets.</span><span class="sxs-lookup"><span data-stu-id="c9d16-108">*expression* A variable that represents a **Recordsets** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9d16-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9d16-109">Remarks</span></span>

<span data-ttu-id="c9d16-p102">Como os membros de uma coleção começam com 0, você sempre deve codificar os loops começando com o membro 0 e terminando com o valor da propriedade **Count** menos 1. Se você deseja fazer um loop nos membros de uma coleção sem verificar a propriedade **Count**, use o comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="c9d16-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="c9d16-p103">A definição da propriedade **Count** nunca será Null. Se o valor for 0, não existirão objetos na coleção.</span><span class="sxs-lookup"><span data-stu-id="c9d16-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

