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
ms.openlocfilehash: 2d3fbf8f7a725f121579066001715fb0bc6beba0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430928"
---
# <a name="deferring-processing"></a><span data-ttu-id="b95cd-103">Adiar o processamento</span><span class="sxs-lookup"><span data-stu-id="b95cd-103">Deferring Processing</span></span>

  
  
<span data-ttu-id="b95cd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b95cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b95cd-105">Passe o sinalizador MAPI_DEFERRED_ERRORS para chamadas de método o máximo possível.</span><span class="sxs-lookup"><span data-stu-id="b95cd-105">Pass the MAPI_DEFERRED_ERRORS flag to method calls as much as possible.</span></span> <span data-ttu-id="b95cd-106">Muitas das chamadas de método MAPI foram otimizadas para aceitar esse sinalizador, fazendo com que o provedor adie a tarefa solicitada até que várias tarefas possam ser executadas ao mesmo tempo ou você pode não esperar mais pelos resultados.</span><span class="sxs-lookup"><span data-stu-id="b95cd-106">Many of the MAPI method calls have been optimized to accept this flag, causing the provider to either postpone the requested task until multiple tasks can be performed at once or you can wait no longer for the results.</span></span>
  
<span data-ttu-id="b95cd-107">Por exemplo, se você passar MAPI_DEFERRED_ERRORS para [IMsgStore:: OpenEntry](imsgstore-openentry.md) para abrir uma pasta, a abertura da pasta e uma possível chamada remota poderão ser adiadas até que você faça outra chamada, como uma chamada para a GetHierarchyTable da pasta \*\*\*\* ou \*\* \*\*Métodos GetProps.</span><span class="sxs-lookup"><span data-stu-id="b95cd-107">For example, if you pass MAPI_DEFERRED_ERRORS to [IMsgStore::OpenEntry](imsgstore-openentry.md) to open a folder, the opening of the folder and a possible remote call can be postponed until you make another call such as a call to the folder's **GetHierarchyTable** or **GetProps** methods.</span></span> <span data-ttu-id="b95cd-108">O \*\*\*\* GetHierarchyTable e o GetProps exigem o retorno de dados do provedor de serviços, uma tarefa que deve ser executada imediatamente. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="b95cd-108">Both **GetHierarchyTable** and **GetProps** require the return of data from the service provider, a task that must be performed immediately.</span></span> 
  
<span data-ttu-id="b95cd-109">Outra maneira de adiar o processamento é simplesmente não fazer uma chamada.</span><span class="sxs-lookup"><span data-stu-id="b95cd-109">Another way to defer processing is simply not to make a call.</span></span> <span data-ttu-id="b95cd-110">Ao ter conhecimento do usuário e quando o usuário pode perceber um dreno nos recursos ou tempo de processamento, você pode determinar quando faz sentido fazer chamadas.</span><span class="sxs-lookup"><span data-stu-id="b95cd-110">By being aware of the user and when the user can perceive a drain on resources or processing time, you can determine when it makes sense to make calls.</span></span> <span data-ttu-id="b95cd-111">Há uma oportunidade de melhorar o desempenho fazendo chamadas em um momento em que o usuário não irá notar ou não fazendo isso.</span><span class="sxs-lookup"><span data-stu-id="b95cd-111">There is an opportunity to improve performance by making calls either at a time when the user will not notice or by not making them at all.</span></span>
  
<span data-ttu-id="b95cd-112">Por exemplo, considere a situação em que você está recebendo mais de uma notificação por segundo de um repositório de mensagens que está movendo um grande número de mensagens.</span><span class="sxs-lookup"><span data-stu-id="b95cd-112">For example, consider the situation when you are receiving more than one notification per second from a message store that is moving a great number of messages.</span></span> <span data-ttu-id="b95cd-113">Um indicador de progresso é exibido para indicar a porcentagem da conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="b95cd-113">A progress indicator is displayed to indicate the percentage of the operation's completion.</span></span> <span data-ttu-id="b95cd-114">Normalmente, os usuários não perceberão que essa operação será lenta até que alguns segundos tenham passado.</span><span class="sxs-lookup"><span data-stu-id="b95cd-114">Users typically will not perceive this operation to be slow until a few seconds have passed.</span></span> <span data-ttu-id="b95cd-115">Portanto, se você estiver atualizando o indicador de progresso, não faça nenhuma alteração até pelo menos quatro segundos após o início da operação de movimentação.</span><span class="sxs-lookup"><span data-stu-id="b95cd-115">Therefore, if you are updating the progress indicator, do not make any changes until at least four seconds after the initiation of the move operation.</span></span> <span data-ttu-id="b95cd-116">Isso poupará tempo nos casos comuns quando a operação for rápida e informará os usuários em tempo hábil quando a operação for lenta.</span><span class="sxs-lookup"><span data-stu-id="b95cd-116">This will save time in the common cases when the operation is fast and inform users in a timely manner when the operation is slow.</span></span>
  

