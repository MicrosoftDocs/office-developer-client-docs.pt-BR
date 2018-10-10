---
title: Método CancelUpdate (RDS)
TOCTitle: CancelUpdate Method (RDS)
ms:assetid: 373a3feb-125d-915a-fd56-d4b04b20db54
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249130(v=office.15)
ms:contentKeyID: 48544188
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ea646f2412ec078f3a45334ec2b1cdbe449285b6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463233"
---
# <a name="cancelupdate-method-rds"></a><span data-ttu-id="d59d9-102">Método CancelUpdate (RDS)</span><span class="sxs-lookup"><span data-stu-id="d59d9-102">CancelUpdate Method (RDS)</span></span>


<span data-ttu-id="d59d9-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d59d9-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="d59d9-104">Cancela quaisquer alterações feitas na linha atual ou nova de um objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d59d9-104">Cancels any changes made to the current or new row of a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d59d9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d59d9-105">Syntax</span></span>

<span data-ttu-id="d59d9-106">*DataControl*. CancelUpdate</span><span class="sxs-lookup"><span data-stu-id="d59d9-106">*DataControl*.CancelUpdate</span></span>

## <a name="parameters"></a><span data-ttu-id="d59d9-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d59d9-107">Parameters</span></span>

  - <span data-ttu-id="d59d9-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="d59d9-108">*DataControl*</span></span>

  - <span data-ttu-id="d59d9-109">Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="d59d9-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d59d9-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="d59d9-110">Remarks</span></span>

<span data-ttu-id="d59d9-p101">O Cursor Service for OLE DB mantém uma cópia dos valores originais e um cache de alterações. Ao chamar **CancelUpdate**, o cache de alterações é redefinido para vazio e quaisquer controles de ligação são atualizados com os dados originais.</span><span class="sxs-lookup"><span data-stu-id="d59d9-p101">The Cursor Service for OLE DB keeps both a copy of the original values and a cache of changes. When you call **CancelUpdate**, the cache of changes is reset to empty, and any bound controls are refreshed with the original data.</span></span>

