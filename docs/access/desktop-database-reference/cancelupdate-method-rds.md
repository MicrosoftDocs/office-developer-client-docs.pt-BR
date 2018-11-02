---
title: Método CancelUpdate (RDS)
TOCTitle: CancelUpdate method (RDS)
ms:assetid: 373a3feb-125d-915a-fd56-d4b04b20db54
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249130(v=office.15)
ms:contentKeyID: 48544188
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d6a6427574cd04d8196153618c5960cb38da2b04
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924733"
---
# <a name="cancelupdate-method-rds"></a><span data-ttu-id="266f4-102">Método CancelUpdate (RDS)</span><span class="sxs-lookup"><span data-stu-id="266f4-102">CancelUpdate method (RDS)</span></span>


<span data-ttu-id="266f4-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="266f4-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="266f4-104">Cancela quaisquer alterações feitas na linha atual ou nova de um objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="266f4-104">Cancels any changes made to the current or new row of a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="266f4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="266f4-105">Syntax</span></span>

<span data-ttu-id="266f4-106">*DataControl*. CancelUpdate</span><span class="sxs-lookup"><span data-stu-id="266f4-106">*DataControl*.CancelUpdate</span></span>

## <a name="parameters"></a><span data-ttu-id="266f4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="266f4-107">Parameters</span></span>

  - <span data-ttu-id="266f4-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="266f4-108">*DataControl*</span></span>

  - <span data-ttu-id="266f4-109">Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="266f4-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="266f4-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="266f4-110">Remarks</span></span>

<span data-ttu-id="266f4-p101">O Cursor Service for OLE DB mantém uma cópia dos valores originais e um cache de alterações. Ao chamar **CancelUpdate**, o cache de alterações é redefinido para vazio e quaisquer controles de ligação são atualizados com os dados originais.</span><span class="sxs-lookup"><span data-stu-id="266f4-p101">The Cursor Service for OLE DB keeps both a copy of the original values and a cache of changes. When you call **CancelUpdate**, the cache of changes is reset to empty, and any bound controls are refreshed with the original data.</span></span>

