---
title: Método CancelUpdate (RDS)
TOCTitle: CancelUpdate method (RDS)
ms:assetid: 373a3feb-125d-915a-fd56-d4b04b20db54
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249130(v=office.15)
ms:contentKeyID: 48544188
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b0c02a9ca72add763e1d3ccf62d5ede8adaecc6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296665"
---
# <a name="cancelupdate-method-rds"></a><span data-ttu-id="174f7-102">Método CancelUpdate (RDS)</span><span class="sxs-lookup"><span data-stu-id="174f7-102">CancelUpdate method (RDS)</span></span>

<span data-ttu-id="174f7-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="174f7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="174f7-104">Cancela quaisquer alterações feitas na linha atual ou nova de um objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="174f7-104">Cancels any changes made to the current or new row of a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="174f7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="174f7-105">Syntax</span></span>

<span data-ttu-id="174f7-106">*DataControl*. CancelUpdate</span><span class="sxs-lookup"><span data-stu-id="174f7-106">*DataControl*.CancelUpdate</span></span>

## <a name="parameters"></a><span data-ttu-id="174f7-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="174f7-107">Parameters</span></span>

|<span data-ttu-id="174f7-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="174f7-108">Parameter</span></span>|<span data-ttu-id="174f7-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="174f7-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="174f7-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="174f7-110">*DataControl*</span></span> |<span data-ttu-id="174f7-111">Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="174f7-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="174f7-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="174f7-112">Remarks</span></span>

<span data-ttu-id="174f7-p101">O Cursor Service for OLE DB mantém uma cópia dos valores originais e um cache de alterações. Ao chamar **CancelUpdate**, o cache de alterações é redefinido para vazio e quaisquer controles de ligação são atualizados com os dados originais.</span><span class="sxs-lookup"><span data-stu-id="174f7-p101">The Cursor Service for OLE DB keeps both a copy of the original values and a cache of changes. When you call **CancelUpdate**, the cache of changes is reset to empty, and any bound controls are refreshed with the original data.</span></span>

