---
title: Número de deadlocks com o nível de isolamento repetido leitura
TOCTitle: Deadlocks with read repeatable isolation level
ms:assetid: 3d5f3293-33bb-cf6d-362a-278f9ec1bd3c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249165(v=office.15)
ms:contentKeyID: 48544342
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5c3e38f6054e6548dfc14d30ce6ec89dcb2e4b01
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703773"
---
# <a name="deadlocks-with-read-repeatable-isolation-level"></a><span data-ttu-id="92b7b-102">Número de deadlocks com o nível de isolamento repetido leitura</span><span class="sxs-lookup"><span data-stu-id="92b7b-102">Deadlocks with read repeatable isolation level</span></span>


<span data-ttu-id="92b7b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="92b7b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="92b7b-p101">Se um objeto de negócios personalizado usa um nível de isolamento de leitura repetida para acessar um SQL Server e o objeto de negócios for chamado simultaneamente por dois clientes que enviam uma consulta e são atualizados na mesma transação, é possível haver um conflito. O Serviço de dados remotos foi projetado para permitir que um dos processos expire para eliminar o conflito, mas a atualização falhará para aquele cliente.</span><span class="sxs-lookup"><span data-stu-id="92b7b-p101">If a custom business object uses an isolation level of read repeatable to access a SQL Server, and the business object is called simultaneously by two clients that send a query and update in the same transaction, a deadlock is possible. Remote Data Service is designed to allow one of the processes to time out to release the deadlock, but the update will fail for that client.</span></span>

<span data-ttu-id="92b7b-106">Use a propriedade dinâmica [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md)**Command Time Out** para modificar a duração do tempo limite.</span><span class="sxs-lookup"><span data-stu-id="92b7b-106">Use the [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md)**Command Time Out** dynamic property to modify the length of the timeout.</span></span>

