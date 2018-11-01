---
title: Método Recordset.Cancel (DAO)
TOCTitle: Cancel Method
ms:assetid: 89acfbf1-b937-dc19-ada1-6f8f50489147
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197080(v=office.15)
ms:contentKeyID: 48546169
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cde31424f409f3b3d152189e3964bc3447cfd53c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871483"
---
# <a name="recordsetcancel-method-dao"></a><span data-ttu-id="9fe2b-102">Método Recordset.Cancel (DAO)</span><span class="sxs-lookup"><span data-stu-id="9fe2b-102">Recordset.Cancel Method (DAO)</span></span>


<span data-ttu-id="9fe2b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="9fe2b-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="9fe2b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9fe2b-104">Syntax</span></span>

<span data-ttu-id="9fe2b-105">*expressão* . Cancelar</span><span class="sxs-lookup"><span data-stu-id="9fe2b-105">*expression* .Cancel</span></span>

<span data-ttu-id="9fe2b-106">*expressão* Uma variável que representa um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="9fe2b-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fe2b-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="9fe2b-107">Remarks</span></span>

<span data-ttu-id="9fe2b-108">Use o método **Cancel** para terminar a execução de uma chamada de método assíncrona **Execute** ou **OpenConnection** (ou seja, o método foi chamado com a opção dbRunAsync).</span><span class="sxs-lookup"><span data-stu-id="9fe2b-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="9fe2b-109">**Cancelar** retornará um erro em tempo de execução se dbRunAsync não foi usada no método que você está tentando finalizar.</span><span class="sxs-lookup"><span data-stu-id="9fe2b-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

