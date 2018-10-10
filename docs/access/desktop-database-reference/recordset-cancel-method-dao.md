---
title: Método Recordset.Cancel (DAO)
TOCTitle: Cancel Method
ms:assetid: 89acfbf1-b937-dc19-ada1-6f8f50489147
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197080(v=office.15)
ms:contentKeyID: 48546169
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1d7e77bd844385b9400449027312dacc02940e58
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462675"
---
# <a name="recordsetcancel-method-dao"></a><span data-ttu-id="df01a-102">Método Recordset.Cancel (DAO)</span><span class="sxs-lookup"><span data-stu-id="df01a-102">Recordset.Cancel Method (DAO)</span></span>


<span data-ttu-id="df01a-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="df01a-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="df01a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df01a-104">Syntax</span></span>

<span data-ttu-id="df01a-105">*expressão* . Cancelar</span><span class="sxs-lookup"><span data-stu-id="df01a-105">*expression* .Cancel</span></span>

<span data-ttu-id="df01a-106">*expressão* Uma variável que representa um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="df01a-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="df01a-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="df01a-107">Remarks</span></span>

<span data-ttu-id="df01a-108">Use o método **Cancel** para terminar a execução de uma chamada de método assíncrona **Execute** ou **OpenConnection** (ou seja, o método foi chamado com a opção dbRunAsync).</span><span class="sxs-lookup"><span data-stu-id="df01a-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="df01a-109">**Cancelar** retornará um erro em tempo de execução se dbRunAsync não foi usada no método que você está tentando finalizar.</span><span class="sxs-lookup"><span data-stu-id="df01a-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

