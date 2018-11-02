---
title: Propriedade Field.VisibleValue (DAO)
TOCTitle: VisibleValue Property
ms:assetid: e40fcb43-9a1d-69e7-1544-8f15ef21daf4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835776(v=office.15)
ms:contentKeyID: 48548332
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 461b8c43bf9000e5ecde3a3676cebf54be8e4166
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927568"
---
# <a name="fieldvisiblevalue-property-dao"></a><span data-ttu-id="8d44a-102">Propriedade Field.VisibleValue (DAO)</span><span class="sxs-lookup"><span data-stu-id="8d44a-102">Field.VisibleValue property (DAO)</span></span>


<span data-ttu-id="8d44a-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="8d44a-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="8d44a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8d44a-104">Syntax</span></span>

<span data-ttu-id="8d44a-105">*expressão* . VisibleValue</span><span class="sxs-lookup"><span data-stu-id="8d44a-105">*expression* .VisibleValue</span></span>

<span data-ttu-id="8d44a-106">*expressão* Uma variável que representa um objeto **Field** .</span><span class="sxs-lookup"><span data-stu-id="8d44a-106">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d44a-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="8d44a-107">Remarks</span></span>

<span data-ttu-id="8d44a-p101">Essa propriedade contém o valor do campo atualmente no banco de dados do servidor. Durante uma atualização em lotes otimista, pode ocorrer uma colisão na qual um segundo cliente modificou o mesmo campo e registro no intervalo entre a recuperação de dados e a tentativa de atualização do primeiro cliente. Quando isso acontecer, o valor definido pelo segundo cliente será acessível por meio desta propriedade.</span><span class="sxs-lookup"><span data-stu-id="8d44a-p101">This property contains the value of the field that is currently in the database on the server. During an optimistic batch update, a collision may occur where a second client modified the same field and record in between the time the first client retrieved the data and the first client's update attempt. When this happens, the value that the second client set will be accessible through this property.</span></span>

