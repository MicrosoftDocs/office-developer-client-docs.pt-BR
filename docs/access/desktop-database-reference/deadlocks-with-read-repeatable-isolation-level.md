---
title: Deadlocks com nível de isolamento repetido de leitura
TOCTitle: Deadlocks with read repeatable isolation level
ms:assetid: 3d5f3293-33bb-cf6d-362a-278f9ec1bd3c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249165(v=office.15)
ms:contentKeyID: 48544342
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5c3e38f6054e6548dfc14d30ce6ec89dcb2e4b01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294173"
---
# <a name="deadlocks-with-read-repeatable-isolation-level"></a><span data-ttu-id="f7dfc-102">Deadlocks com nível de isolamento repetido de leitura</span><span class="sxs-lookup"><span data-stu-id="f7dfc-102">Deadlocks with read repeatable isolation level</span></span>


<span data-ttu-id="f7dfc-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f7dfc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f7dfc-p101">Se um objeto de negócios personalizado usa um nível de isolamento de leitura repetida para acessar um SQL Server e o objeto de negócios for chamado simultaneamente por dois clientes que enviam uma consulta e são atualizados na mesma transação, é possível haver um conflito. O Serviço de dados remotos foi projetado para permitir que um dos processos expire para eliminar o conflito, mas a atualização falhará para aquele cliente.</span><span class="sxs-lookup"><span data-stu-id="f7dfc-p101">If a custom business object uses an isolation level of read repeatable to access a SQL Server, and the business object is called simultaneously by two clients that send a query and update in the same transaction, a deadlock is possible. Remote Data Service is designed to allow one of the processes to time out to release the deadlock, but the update will fail for that client.</span></span>

<span data-ttu-id="f7dfc-106">Use a propriedade dinâmica Time **Out** do Comando do Serviço de [Cursor](microsoft-cursor-service-for-ole-db-ado-service-component.md)para modificar a duração do tempo final.</span><span class="sxs-lookup"><span data-stu-id="f7dfc-106">Use the [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md)**Command Time Out** dynamic property to modify the length of the timeout.</span></span>

