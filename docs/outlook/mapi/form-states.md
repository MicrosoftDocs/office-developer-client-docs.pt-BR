---
title: Estados de formulários
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dfc9fbf1-90d4-4756-92d9-032ac56a9c50
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 61d20ff7010151a82c53cafc69270e6925796a5c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327514"
---
# <a name="form-states"></a><span data-ttu-id="06a31-103">Estados de formulários</span><span class="sxs-lookup"><span data-stu-id="06a31-103">Form states</span></span>

<span data-ttu-id="06a31-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06a31-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06a31-105">Os objetos Form podem estar em um dos cinco Estados distintos, dependendo de quais métodos foram chamados neles e se algum erro ocorreu na execução desses métodos.</span><span class="sxs-lookup"><span data-stu-id="06a31-105">Form objects can be in one of five distinct states, depending on what methods have been called in them and whether any errors have occurred in performing those methods.</span></span> <span data-ttu-id="06a31-106">Os Estados são descritos nos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="06a31-106">The states are described in the following topics:</span></span>
  
- [<span data-ttu-id="06a31-107">Estado não inicializado</span><span class="sxs-lookup"><span data-stu-id="06a31-107">Uninitialized State</span></span>](uninitialized-state.md)
    
- [<span data-ttu-id="06a31-108">Estado normal</span><span class="sxs-lookup"><span data-stu-id="06a31-108">Normal State</span></span>](normal-state.md)
    
- [<span data-ttu-id="06a31-109">Estado noRabisco</span><span class="sxs-lookup"><span data-stu-id="06a31-109">NoScribble State</span></span>](noscribble-state.md)
    
- [<span data-ttu-id="06a31-110">Estado HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="06a31-110">HandsOffAfterSave State</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="06a31-111">Estado HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="06a31-111">HandsOffFromNormal State</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="06a31-112">Os Estados se relacionam principalmente com o status dos dados no objeto Form.</span><span class="sxs-lookup"><span data-stu-id="06a31-112">The states primarily relate to the status of the data in the form object.</span></span> <span data-ttu-id="06a31-113">Os diferentes Estados refletem se os dados precisam ser salvos, se o objeto Form deve permitir modificações nos dados e o ponto no processo de salvar os dados em que o formulário está.</span><span class="sxs-lookup"><span data-stu-id="06a31-113">The different states reflect whether the data needs to be saved, whether the form object should allow modifications to the data, and what point in the process of saving the data the form is in.</span></span> <span data-ttu-id="06a31-114">Assim, os Estados e as transições de formulário entre eles têm mais a fazer com a implementação do seu servidor de formulário de métodos de interface [IPersistMessage: IUnknown](ipersistmessageiunknown.md) do que outros.</span><span class="sxs-lookup"><span data-stu-id="06a31-114">As such, the form states and transitions between them have more to do with your form server's implementation of [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interface methods than any other.</span></span> <span data-ttu-id="06a31-115">O conhecimento desses Estados é muito útil para a implementação adequada das interfaces de formulário MAPI que seu servidor de formulários deve implementar.</span><span class="sxs-lookup"><span data-stu-id="06a31-115">Knowledge of these states is very useful for proper implementation of the MAPI form interfaces that your form server must implement.</span></span> 
  
<span data-ttu-id="06a31-116">Os tópicos desta seção descrevem os vários Estados, juntamente com as ações permitidas que causam transições para outros Estados.</span><span class="sxs-lookup"><span data-stu-id="06a31-116">The topics in this section describe the various states, along with the allowed actions that cause transitions to other states.</span></span> <span data-ttu-id="06a31-117">As transições não listadas nos tópicos não são permitidas.</span><span class="sxs-lookup"><span data-stu-id="06a31-117">Any transitions not listed in the topics are not allowed.</span></span> <span data-ttu-id="06a31-118">Se os objetos de formulário fizerem transições não permitidas entre Estados, elas não se comportarão de maneiras que os clientes de mensagens esperam e possam causar comportamento de cliente ou de formulário imprevisível.</span><span class="sxs-lookup"><span data-stu-id="06a31-118">If your form objects make disallowed transitions between states, they will not behave in the ways that messaging clients expect and could cause unpredictable client or form object behavior.</span></span>
  
> [!NOTE]
> <span data-ttu-id="06a31-119">Algumas transições de estado dependem das informações de Estados anteriores.</span><span class="sxs-lookup"><span data-stu-id="06a31-119">Some state transitions depend on information from previous states.</span></span> <span data-ttu-id="06a31-120">O servidor de formulário provavelmente terá que implementar um sinalizador em seus objetos Form para indicar se os valores das propriedades da mensagem foram alterados para facilitar as alterações de estado posteriores.</span><span class="sxs-lookup"><span data-stu-id="06a31-120">Your form server will most likely have to implement a flag in its form objects to indicate whether the values of the message's properties have been changed to facilitate later state changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="06a31-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="06a31-121">See also</span></span>

- [<span data-ttu-id="06a31-122">Desenvolver servidores de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="06a31-122">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

