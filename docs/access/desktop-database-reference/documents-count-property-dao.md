---
title: Propriedade Documents.Count (DAO)
TOCTitle: Count Property
ms:assetid: 3fc0b1e6-f7be-cd43-711f-5cf5763fe7f6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192858(v=office.15)
ms:contentKeyID: 48544407
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053325
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: dd9cc563ecc885fca4fa0ef5829d82aa2f8bfef6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293739"
---
# <a name="documentscount-property-dao"></a><span data-ttu-id="31fe7-102">Propriedade Documents.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="31fe7-102">Documents.Count property (DAO)</span></span>


<span data-ttu-id="31fe7-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="31fe7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="31fe7-104">Retorna o número de objetos na coleção especificada.</span><span class="sxs-lookup"><span data-stu-id="31fe7-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="31fe7-105">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="31fe7-105">Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="31fe7-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31fe7-106">Syntax</span></span>

<span data-ttu-id="31fe7-107">*expressão* . Count</span><span class="sxs-lookup"><span data-stu-id="31fe7-107">*expression* .Count</span></span>

<span data-ttu-id="31fe7-108">*expressão* Uma variável que representa um **objeto Documents** .</span><span class="sxs-lookup"><span data-stu-id="31fe7-108">*expression* A variable that represents a **Documents** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="31fe7-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="31fe7-109">Remarks</span></span>

<span data-ttu-id="31fe7-p102">Como os membros de uma coleção começam com 0, você sempre deve codificar os loops começando com o membro 0 e terminando com o valor da propriedade **Count** menos 1. Se você deseja fazer um loop nos membros de uma coleção sem verificar a propriedade **Count**, use o comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="31fe7-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="31fe7-p103">A definição da propriedade **Count** nunca será Null. Se o valor for 0, não existirão objetos na coleção.</span><span class="sxs-lookup"><span data-stu-id="31fe7-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

