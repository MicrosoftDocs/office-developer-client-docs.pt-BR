---
title: Conflitos com a leitura do nível de isolamento repetido
TOCTitle: Deadlocks With Read Repeatable Isolation Level
ms:assetid: 3d5f3293-33bb-cf6d-362a-278f9ec1bd3c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249165(v=office.15)
ms:contentKeyID: 48544342
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: de936da2772b809199d3890140683afd5ef01659
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462554"
---
# <a name="deadlocks-with-read-repeatable-isolation-level"></a><span data-ttu-id="2d37c-102">Conflitos com a leitura do nível de isolamento repetido</span><span class="sxs-lookup"><span data-stu-id="2d37c-102">Deadlocks With Read Repeatable Isolation Level</span></span>


<span data-ttu-id="2d37c-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d37c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2d37c-p101">Se um objeto de negócios personalizado usa um nível de isolamento de leitura repetida para acessar um SQL Server e o objeto de negócios for chamado simultaneamente por dois clientes que enviam uma consulta e são atualizados na mesma transação, é possível haver um conflito. O Serviço de dados remotos foi projetado para permitir que um dos processos expire para eliminar o conflito, mas a atualização falhará para aquele cliente.</span><span class="sxs-lookup"><span data-stu-id="2d37c-p101">If a custom business object uses an isolation level of read repeatable to access a SQL Server, and the business object is called simultaneously by two clients that send a query and update in the same transaction, a deadlock is possible. Remote Data Service is designed to allow one of the processes to time out to release the deadlock, but the update will fail for that client.</span></span>

<span data-ttu-id="2d37c-106">Use a propriedade dinâmica [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md)**Command Time Out** para modificar a duração do tempo limite.</span><span class="sxs-lookup"><span data-stu-id="2d37c-106">Use the [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md)**Command Time Out** dynamic property to modify the length of the timeout.</span></span>

