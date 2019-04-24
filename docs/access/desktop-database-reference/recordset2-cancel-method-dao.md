---
title: Método Recordset2. Cancel (DAO)
TOCTitle: Cancel Method
ms:assetid: cae49f36-3aad-80d8-c15f-a7a584aa2e9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834366(v=office.15)
ms:contentKeyID: 48547703
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d203d1f1888539a4907da246e20ed711e61ee51f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307410"
---
# <a name="recordset2cancel-method-dao"></a><span data-ttu-id="b68d0-102">Método Recordset2. Cancel (DAO)</span><span class="sxs-lookup"><span data-stu-id="b68d0-102">Recordset2.Cancel method (DAO)</span></span>


<span data-ttu-id="b68d0-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b68d0-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="b68d0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b68d0-104">Syntax</span></span>

<span data-ttu-id="b68d0-105">*expressão* . Cancelar</span><span class="sxs-lookup"><span data-stu-id="b68d0-105">*expression* .Cancel</span></span>

<span data-ttu-id="b68d0-106">*expressão* Uma expressão que retorna um objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="b68d0-106">*expression* An expression that returns a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b68d0-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="b68d0-107">Remarks</span></span>

<span data-ttu-id="b68d0-108">Use o método **Cancel** para encerrar a execução de uma chamada de método **Execute** ou **OpenConnection** assíncrona (ou seja, o método foi invocado com a opção dbRunAsync).</span><span class="sxs-lookup"><span data-stu-id="b68d0-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="b68d0-109">**Cancel** retornará um erro em tempo de execução se dbRunAsync não tiver sido usado no método que você está tentando encerrar.</span><span class="sxs-lookup"><span data-stu-id="b68d0-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

