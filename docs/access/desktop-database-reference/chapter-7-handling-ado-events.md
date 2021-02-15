---
title: 'Capítulo 7: Manipulação de eventos do ADO'
TOCTitle: 'Chapter 7: Handling ADO events'
ms:assetid: 22924fe2-d00d-8a0c-52f5-2dc6039537ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249004(v=office.15)
ms:contentKeyID: 48543709
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e7357cc60a3bddbf96c2abae39fecfb7107025e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296399"
---
# <a name="chapter-7-handling-ado-events"></a><span data-ttu-id="e3241-102">Capítulo 7: Manipulação de eventos do ADO</span><span class="sxs-lookup"><span data-stu-id="e3241-102">Chapter 7: Handling ADO events</span></span>

<span data-ttu-id="e3241-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e3241-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e3241-p101">O modelo de evento ADO oferece suporte a determinadas operações ADO síncronas e assíncronas que emitem *eventos*, ou notificações, antes de a operação começar ou depois de ela ser concluída. Um evento geralmente é uma chamada a uma rotina do manipulador de eventos que você define no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e3241-p101">The ADO event model supports certain synchronous and asynchronous ADO operations that issue *events*, or notifications, before the operation starts or after it completes. An event is actually a call to an event-handler routine that you define in your application.</span></span>

<span data-ttu-id="e3241-p102">Se você fornecer funções ou procedimentos do manipulador para o grupo de eventos que ocorrem antes de a operação começar, poderá examinar ou modificar os parâmetros transmitidos para a operação. Uma vez que ainda não foi executada, você poderá cancelar a operação ou permitir que ela seja concluída.</span><span class="sxs-lookup"><span data-stu-id="e3241-p102">If you provide handler functions or procedures for the group of events that occur before the operation starts, you can examine or modify the parameters that were passed to the operation. Because it has not been executed yet, you can either cancel the operation or allow it to complete.</span></span>

<span data-ttu-id="e3241-p103">O grupo de eventos que ocorrem depois de uma operação concluir são especificamente importantes se você usar o ADO de maneira assíncrona. Por exemplo, um aplicativo que inicia uma operação [Recordset.Open](open-method-ado-recordset.md) assíncrona é notificado por um evento de conclusão de execução quando a operação for concluída.</span><span class="sxs-lookup"><span data-stu-id="e3241-p103">The group of events that occur after an operation completes are especially important if you use ADO asynchronously. For example, an application that starts an asynchronous [Recordset.Open](open-method-ado-recordset.md) operation is notified by an execution complete event when the operation concludes.</span></span>

<span data-ttu-id="e3241-110">O uso do modelo de eventos ADO adiciona uma sobrecarga no aplicativo, mas oferece muito mais flexibilidade do que os outros métodos de lidar com operações assíncronas, como o monitoramento da propriedade [State](state-property-ado.md) de um objeto com um loop.</span><span class="sxs-lookup"><span data-stu-id="e3241-110">Using the ADO event model adds some overhead to your application but provides far more flexibility than other methods of dealing with asynchronous operations, such as monitoring the [State](state-property-ado.md) property of an object with a loop.</span></span>

<span data-ttu-id="e3241-111">Este capítulo aborda os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="e3241-111">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="e3241-112">Resumo do manipulador de eventos do ADO</span><span class="sxs-lookup"><span data-stu-id="e3241-112">ADO event handler summary</span></span>](ado-event-handler-summary.md)
- [<span data-ttu-id="e3241-113">Tipos de eventos</span><span class="sxs-lookup"><span data-stu-id="e3241-113">Types of events</span></span>](types-of-events.md)
- [<span data-ttu-id="e3241-114">Parâmetros de eventos</span><span class="sxs-lookup"><span data-stu-id="e3241-114">Event parameters</span></span>](event-parameters.md)
- [<span data-ttu-id="e3241-115">Como os manipuladores de eventos funcionam juntos</span><span class="sxs-lookup"><span data-stu-id="e3241-115">How event handlers work together</span></span>](how-event-handlers-work-together.md)
- [<span data-ttu-id="e3241-116">Instaciação de eventos do ADO por idioma (ADO)</span><span class="sxs-lookup"><span data-stu-id="e3241-116">ADO event instantiation by language (ADO)</span></span>](ado-event-instantiation-by-language-ado.md)
