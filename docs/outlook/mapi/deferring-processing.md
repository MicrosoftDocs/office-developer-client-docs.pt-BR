---
title: Adiar o processamento
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a791b95f-56ad-493a-9ba5-fb4c7dd80e89
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2c4577a35315c9df0055e97de26dd0baf1a2b489
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580583"
---
# <a name="deferring-processing"></a><span data-ttu-id="feda0-103">Adiar o processamento</span><span class="sxs-lookup"><span data-stu-id="feda0-103">Deferring Processing</span></span>

  
  
<span data-ttu-id="feda0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="feda0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="feda0-105">Passe o sinalizador MAPI_DEFERRED_ERRORS às chamadas do método tanto quanto possível.</span><span class="sxs-lookup"><span data-stu-id="feda0-105">Pass the MAPI_DEFERRED_ERRORS flag to method calls as much as possible.</span></span> <span data-ttu-id="feda0-106">Muitas das chamadas MAPI método foram otimizadas para aceitar esse sinalizador, fazendo com que o provedor ou adiar a tarefa solicitada até várias tarefas podem ser executadas simultaneamente ou você pode esperar que não são mais os resultados.</span><span class="sxs-lookup"><span data-stu-id="feda0-106">Many of the MAPI method calls have been optimized to accept this flag, causing the provider to either postpone the requested task until multiple tasks can be performed at once or you can wait no longer for the results.</span></span>
  
<span data-ttu-id="feda0-107">Por exemplo, se você passar MAPI_DEFERRED_ERRORS para [IMsgStore::OpenEntry](imsgstore-openentry.md) para abrir uma pasta, a abertura da pasta e uma chamada remota possível possa ser adiada até você fazer outra chamada como uma chamada para **GetHierarchyTable** da pasta ou o \*\* GetProps\*\* métodos.</span><span class="sxs-lookup"><span data-stu-id="feda0-107">For example, if you pass MAPI_DEFERRED_ERRORS to [IMsgStore::OpenEntry](imsgstore-openentry.md) to open a folder, the opening of the folder and a possible remote call can be postponed until you make another call such as a call to the folder's **GetHierarchyTable** or **GetProps** methods.</span></span> <span data-ttu-id="feda0-108">**GetHierarchyTable** e o **GetProps** exigem o retorno de dados do provedor do serviço, uma tarefa que deve ser executado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="feda0-108">Both **GetHierarchyTable** and **GetProps** require the return of data from the service provider, a task that must be performed immediately.</span></span> 
  
<span data-ttu-id="feda0-109">Outra maneira para adiar o processamento é simplesmente não para fazer uma chamada.</span><span class="sxs-lookup"><span data-stu-id="feda0-109">Another way to defer processing is simply not to make a call.</span></span> <span data-ttu-id="feda0-110">Ao ser ciente do usuário e o usuário pode percebem diminui o tempo de processamento ou recursos, você pode determinar quando fizer sentido para fazer chamadas.</span><span class="sxs-lookup"><span data-stu-id="feda0-110">By being aware of the user and when the user can perceive a drain on resources or processing time, you can determine when it makes sense to make calls.</span></span> <span data-ttu-id="feda0-111">Não há uma oportunidade para melhorar o desempenho fazendo chamadas a cada vez quando o usuário não notarão ou por não torná-los.</span><span class="sxs-lookup"><span data-stu-id="feda0-111">There is an opportunity to improve performance by making calls either at a time when the user will not notice or by not making them at all.</span></span>
  
<span data-ttu-id="feda0-112">Por exemplo, considere a situação quando você está recebendo mais de uma notificação por segundo de um repositório de mensagem que está se movendo um grande número de mensagens.</span><span class="sxs-lookup"><span data-stu-id="feda0-112">For example, consider the situation when you are receiving more than one notification per second from a message store that is moving a great number of messages.</span></span> <span data-ttu-id="feda0-113">Um indicador de progresso é exibido para indicar a porcentagem de conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="feda0-113">A progress indicator is displayed to indicate the percentage of the operation's completion.</span></span> <span data-ttu-id="feda0-114">Os usuários geralmente não serão percebam esta operação para ser lenta enquanto alguns segundos passados.</span><span class="sxs-lookup"><span data-stu-id="feda0-114">Users typically will not perceive this operation to be slow until a few seconds have passed.</span></span> <span data-ttu-id="feda0-115">Portanto, se você estiver atualizando o indicador de progresso, não faça qualquer alteração até pelo menos quatro segundos após o início da operação de movimentação.</span><span class="sxs-lookup"><span data-stu-id="feda0-115">Therefore, if you are updating the progress indicator, do not make any changes until at least four seconds after the initiation of the move operation.</span></span> <span data-ttu-id="feda0-116">Isso irá economizar tempo nos casos comuns quando a operação é fast e informar os usuários de modo oportuno quando a operação está lenta.</span><span class="sxs-lookup"><span data-stu-id="feda0-116">This will save time in the common cases when the operation is fast and inform users in a timely manner when the operation is slow.</span></span>
  

