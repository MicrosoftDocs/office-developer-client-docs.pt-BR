---
title: Método Recordset2.Cancel (DAO)
TOCTitle: Cancel Method
ms:assetid: cae49f36-3aad-80d8-c15f-a7a584aa2e9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834366(v=office.15)
ms:contentKeyID: 48547703
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5df46c36ff28bae1e48dfc8dc77443f707fc3e0a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877531"
---
# <a name="recordset2cancel-method-dao"></a><span data-ttu-id="017ef-102">Método Recordset2.Cancel (DAO)</span><span class="sxs-lookup"><span data-stu-id="017ef-102">Recordset2.Cancel Method (DAO)</span></span>


<span data-ttu-id="017ef-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="017ef-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="017ef-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="017ef-104">Syntax</span></span>

<span data-ttu-id="017ef-105">*expressão* . Cancelar</span><span class="sxs-lookup"><span data-stu-id="017ef-105">*expression* .Cancel</span></span>

<span data-ttu-id="017ef-106">*expressão* Uma expressão que retorna um objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="017ef-106">*expression* An expression that returns a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="017ef-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="017ef-107">Remarks</span></span>

<span data-ttu-id="017ef-108">Use o método **Cancel** para terminar a execução de uma chamada de método assíncrona **Execute** ou **OpenConnection** (ou seja, o método foi chamado com a opção dbRunAsync).</span><span class="sxs-lookup"><span data-stu-id="017ef-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="017ef-109">**Cancelar** retornará um erro em tempo de execução se dbRunAsync não foi usada no método que você está tentando finalizar.</span><span class="sxs-lookup"><span data-stu-id="017ef-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

