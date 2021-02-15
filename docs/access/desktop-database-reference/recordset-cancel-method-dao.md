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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300809"
---
# <a name="recordsetcancel-method-dao"></a><span data-ttu-id="eae19-102">Método Recordset.Cancel (DAO)</span><span class="sxs-lookup"><span data-stu-id="eae19-102">Recordset.Cancel method (DAO)</span></span>


<span data-ttu-id="eae19-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="eae19-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="eae19-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eae19-104">Syntax</span></span>

<span data-ttu-id="eae19-105">*expressão* . Cancelar</span><span class="sxs-lookup"><span data-stu-id="eae19-105">*expression* .Cancel</span></span>

<span data-ttu-id="eae19-106">*expression* Uma variável que representa um objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="eae19-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="eae19-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="eae19-107">Remarks</span></span>

<span data-ttu-id="eae19-108">Use o **método Cancel** para encerrar a execução de uma chamada de método **Execute** ou **OpenConnection** assíncrona (ou seja, o método foi invocado com a opção dbRunAsync).</span><span class="sxs-lookup"><span data-stu-id="eae19-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="eae19-109">**O** cancelamento retornará um erro em tempo de executar se dbRunAsync não tiver sido usado no método que você está tentando encerrar.</span><span class="sxs-lookup"><span data-stu-id="eae19-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

