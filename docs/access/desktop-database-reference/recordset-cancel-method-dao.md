---
title: Método Recordset.Cancel (DAO)
TOCTitle: Cancel Method
ms:assetid: 89acfbf1-b937-dc19-ada1-6f8f50489147
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197080(v=office.15)
ms:contentKeyID: 48546169
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 81b08472b46ab3a3d35d184e2f8b7be8673f7d1f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927257"
---
# <a name="recordsetcancel-method-dao"></a><span data-ttu-id="eca4a-102">Método Recordset.Cancel (DAO)</span><span class="sxs-lookup"><span data-stu-id="eca4a-102">Recordset.Cancel method (DAO)</span></span>


<span data-ttu-id="eca4a-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="eca4a-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="eca4a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eca4a-104">Syntax</span></span>

<span data-ttu-id="eca4a-105">*expressão* . Cancelar</span><span class="sxs-lookup"><span data-stu-id="eca4a-105">*expression* .Cancel</span></span>

<span data-ttu-id="eca4a-106">*expressão* Uma variável que representa um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="eca4a-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="eca4a-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="eca4a-107">Remarks</span></span>

<span data-ttu-id="eca4a-108">Use o método **Cancel** para terminar a execução de uma chamada de método assíncrona **Execute** ou **OpenConnection** (ou seja, o método foi chamado com a opção dbRunAsync).</span><span class="sxs-lookup"><span data-stu-id="eca4a-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="eca4a-109">**Cancelar** retornará um erro em tempo de execução se dbRunAsync não foi usada no método que você está tentando finalizar.</span><span class="sxs-lookup"><span data-stu-id="eca4a-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

