---
title: 'Capítulo 7: Controlando eventos ADO'
TOCTitle: 'Chapter 7: Handling ADO Events'
ms:assetid: 22924fe2-d00d-8a0c-52f5-2dc6039537ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249004(v=office.15)
ms:contentKeyID: 48543709
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4d85532c93c6d175b90f957d7831b71a460ba5b6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464629"
---
# <a name="chapter-7-handling-ado-events"></a><span data-ttu-id="685fa-102">Capítulo 7: Controlando eventos ADO</span><span class="sxs-lookup"><span data-stu-id="685fa-102">Chapter 7: Handling ADO Events</span></span>


<span data-ttu-id="685fa-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="685fa-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="685fa-p101">O modelo de evento ADO oferece suporte a determinadas operações ADO síncronas e assíncronas que emitem *eventos*, ou notificações, antes de a operação começar ou depois de ela ser concluída. Um evento geralmente é uma chamada a uma rotina do manipulador de eventos que você define no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="685fa-p101">The ADO event model supports certain synchronous and asynchronous ADO operations that issue *events*, or notifications, before the operation starts or after it completes. An event is actually a call to an event-handler routine that you define in your application.</span></span>

<span data-ttu-id="685fa-p102">Se você fornecer funções ou procedimentos do manipulador para o grupo de eventos que ocorrem antes de a operação começar, poderá examinar ou modificar os parâmetros transmitidos para a operação. Uma vez que ainda não foi executada, você poderá cancelar a operação ou permitir que ela seja concluída.</span><span class="sxs-lookup"><span data-stu-id="685fa-p102">If you provide handler functions or procedures for the group of events that occur before the operation starts, you can examine or modify the parameters that were passed to the operation. Because it has not been executed yet, you can either cancel the operation or allow it to complete.</span></span>

<span data-ttu-id="685fa-p103">O grupo de eventos que ocorrem depois de uma operação concluir são especificamente importantes se você usar o ADO de maneira assíncrona. Por exemplo, um aplicativo que inicia uma operação [Recordset.Open](open-method-ado-recordset.md) assíncrona é notificado por um evento de conclusão de execução quando a operação for concluída.</span><span class="sxs-lookup"><span data-stu-id="685fa-p103">The group of events that occur after an operation completes are especially important if you use ADO asynchronously. For example, an application that starts an asynchronous [Recordset.Open](open-method-ado-recordset.md) operation is notified by an execution complete event when the operation concludes.</span></span>

<span data-ttu-id="685fa-110">O uso do modelo de eventos ADO adiciona uma sobrecarga no aplicativo, mas oferece muito mais flexibilidade do que os outros métodos de lidar com operações assíncronas, como o monitoramento da propriedade [State](state-property-ado.md) de um objeto com um loop.</span><span class="sxs-lookup"><span data-stu-id="685fa-110">Using the ADO event model adds some overhead to your application but provides far more flexibility than other methods of dealing with asynchronous operations, such as monitoring the [State](state-property-ado.md) property of an object with a loop.</span></span>

