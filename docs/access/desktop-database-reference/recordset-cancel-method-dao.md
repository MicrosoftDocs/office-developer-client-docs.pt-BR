---
title: Método Recordset.Cancel (DAO)
TOCTitle: Cancel Method
ms:assetid: 89acfbf1-b937-dc19-ada1-6f8f50489147
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197080(v=office.15)
ms:contentKeyID: 48546169
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 102511575770ceb38cf682d5e627fb7e64faa1ff
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716709"
---
# <a name="recordsetcancel-method-dao"></a><span data-ttu-id="d3e9d-102">Método Recordset.Cancel (DAO)</span><span class="sxs-lookup"><span data-stu-id="d3e9d-102">Recordset.Cancel method (DAO)</span></span>


<span data-ttu-id="d3e9d-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="d3e9d-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="d3e9d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d3e9d-104">Syntax</span></span>

<span data-ttu-id="d3e9d-105">*expressão* . Cancelar</span><span class="sxs-lookup"><span data-stu-id="d3e9d-105">*expression* .Cancel</span></span>

<span data-ttu-id="d3e9d-106">*expressão* Uma variável que representa um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="d3e9d-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3e9d-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3e9d-107">Remarks</span></span>

<span data-ttu-id="d3e9d-108">Use o método **Cancel** para terminar a execução de uma chamada de método assíncrona **Execute** ou **OpenConnection** (ou seja, o método foi chamado com a opção dbRunAsync).</span><span class="sxs-lookup"><span data-stu-id="d3e9d-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="d3e9d-109">**Cancelar** retornará um erro em tempo de execução se dbRunAsync não foi usada no método que você está tentando finalizar.</span><span class="sxs-lookup"><span data-stu-id="d3e9d-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

