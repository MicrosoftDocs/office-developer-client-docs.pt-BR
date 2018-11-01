---
title: Método QueryDef.Cancel (DAO)
TOCTitle: Cancel Method
ms:assetid: 91e61012-c01c-4c24-185c-bdadb7f33a58
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197642(v=office.15)
ms:contentKeyID: 48546364
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1055470
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 8e121457f7084b4d13e89c43a30a7632a3cd7377
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873975"
---
# <a name="querydefcancel-method-dao"></a><span data-ttu-id="f5caf-102">Método QueryDef.Cancel (DAO)</span><span class="sxs-lookup"><span data-stu-id="f5caf-102">QueryDef.Cancel Method (DAO)</span></span>


<span data-ttu-id="f5caf-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="f5caf-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="f5caf-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5caf-104">Syntax</span></span>

<span data-ttu-id="f5caf-105">*expressão* . Cancelar</span><span class="sxs-lookup"><span data-stu-id="f5caf-105">*expression* .Cancel</span></span>

<span data-ttu-id="f5caf-106">*expressão* Uma variável que representa um objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="f5caf-106">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5caf-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5caf-107">Remarks</span></span>

<span data-ttu-id="f5caf-108">Use o método **Cancel** para terminar a execução de uma chamada de método assíncrona **Execute** ou **OpenConnection** (ou seja, o método foi chamado com a opção dbRunAsync).</span><span class="sxs-lookup"><span data-stu-id="f5caf-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="f5caf-109">**Cancelar** retornará um erro em tempo de execução se dbRunAsync não foi usada no método que você está tentando finalizar.</span><span class="sxs-lookup"><span data-stu-id="f5caf-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

