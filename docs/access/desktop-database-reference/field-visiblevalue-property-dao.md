---
title: Propriedade Field.VisibleValue (DAO)
TOCTitle: VisibleValue Property
ms:assetid: e40fcb43-9a1d-69e7-1544-8f15ef21daf4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835776(v=office.15)
ms:contentKeyID: 48548332
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1b3e1b6ec6cd34112f0ba1d84101390bbd400f82
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292913"
---
# <a name="fieldvisiblevalue-property-dao"></a><span data-ttu-id="4a711-102">Propriedade Field.VisibleValue (DAO)</span><span class="sxs-lookup"><span data-stu-id="4a711-102">Field.VisibleValue property (DAO)</span></span>


<span data-ttu-id="4a711-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4a711-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="4a711-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4a711-104">Syntax</span></span>

<span data-ttu-id="4a711-105">*expressão* . VisibleValue</span><span class="sxs-lookup"><span data-stu-id="4a711-105">*expression* .VisibleValue</span></span>

<span data-ttu-id="4a711-106">*expressão* Uma variável que representa um objeto de **Campo**.</span><span class="sxs-lookup"><span data-stu-id="4a711-106">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a711-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a711-107">Remarks</span></span>

<span data-ttu-id="4a711-p101">Essa propriedade contém o valor do campo atualmente no banco de dados do servidor. Durante uma atualização em lotes otimista, pode ocorrer uma colisão na qual um segundo cliente modificou o mesmo campo e registro no intervalo entre a recuperação de dados e a tentativa de atualização do primeiro cliente. Quando isso acontecer, o valor definido pelo segundo cliente será acessível por meio desta propriedade.</span><span class="sxs-lookup"><span data-stu-id="4a711-p101">This property contains the value of the field that is currently in the database on the server. During an optimistic batch update, a collision may occur where a second client modified the same field and record in between the time the first client retrieved the data and the first client's update attempt. When this happens, the value that the second client set will be accessible through this property.</span></span>

