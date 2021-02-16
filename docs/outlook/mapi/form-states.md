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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429163"
---
# <a name="form-states"></a><span data-ttu-id="7060b-103">Estados de formulários</span><span class="sxs-lookup"><span data-stu-id="7060b-103">Form states</span></span>

<span data-ttu-id="7060b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7060b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7060b-105">Os objetos de formulário podem estar em um dos cinco estados distintos, dependendo de quais métodos foram chamados neles e se algum erro ocorreu ao executar esses métodos.</span><span class="sxs-lookup"><span data-stu-id="7060b-105">Form objects can be in one of five distinct states, depending on what methods have been called in them and whether any errors have occurred in performing those methods.</span></span> <span data-ttu-id="7060b-106">Os estados são descritos nos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="7060b-106">The states are described in the following topics:</span></span>
  
- [<span data-ttu-id="7060b-107">Estado não reinicializado</span><span class="sxs-lookup"><span data-stu-id="7060b-107">Uninitialized State</span></span>](uninitialized-state.md)
    
- [<span data-ttu-id="7060b-108">Estado Normal</span><span class="sxs-lookup"><span data-stu-id="7060b-108">Normal State</span></span>](normal-state.md)
    
- [<span data-ttu-id="7060b-109">Estado NoScribble</span><span class="sxs-lookup"><span data-stu-id="7060b-109">NoScribble State</span></span>](noscribble-state.md)
    
- [<span data-ttu-id="7060b-110">Estado HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="7060b-110">HandsOffAfterSave State</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="7060b-111">Estado HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="7060b-111">HandsOffFromNormal State</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="7060b-112">Os estados se relacionam principalmente com o status dos dados no objeto form.</span><span class="sxs-lookup"><span data-stu-id="7060b-112">The states primarily relate to the status of the data in the form object.</span></span> <span data-ttu-id="7060b-113">Os diferentes estados refletem se os dados precisam ser salvos, se o objeto de formulário deve permitir modificações nos dados e em que ponto no processo de salvar os dados em que o formulário está.</span><span class="sxs-lookup"><span data-stu-id="7060b-113">The different states reflect whether the data needs to be saved, whether the form object should allow modifications to the data, and what point in the process of saving the data the form is in.</span></span> <span data-ttu-id="7060b-114">Dessa forma, os estados do formulário e as transições entre eles têm mais a ver com a implementação de [IPersistMessage :](ipersistmessageiunknown.md) métodos de interface IUnknown do que com qualquer outro servidor de formulário.</span><span class="sxs-lookup"><span data-stu-id="7060b-114">As such, the form states and transitions between them have more to do with your form server's implementation of [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interface methods than any other.</span></span> <span data-ttu-id="7060b-115">O conhecimento desses estados é muito útil para a implementação adequada das interfaces de formulário MAPI que seu servidor de formulário deve implementar.</span><span class="sxs-lookup"><span data-stu-id="7060b-115">Knowledge of these states is very useful for proper implementation of the MAPI form interfaces that your form server must implement.</span></span> 
  
<span data-ttu-id="7060b-116">Os tópicos desta seção descrevem os vários estados, juntamente com as ações permitidas que causam transições para outros estados.</span><span class="sxs-lookup"><span data-stu-id="7060b-116">The topics in this section describe the various states, along with the allowed actions that cause transitions to other states.</span></span> <span data-ttu-id="7060b-117">As transições não listadas nos tópicos não são permitidas.</span><span class="sxs-lookup"><span data-stu-id="7060b-117">Any transitions not listed in the topics are not allowed.</span></span> <span data-ttu-id="7060b-118">Se seus objetos de formulário fizerem transições não permitidos entre os estados, eles não se comportarão da maneira que os clientes de mensagens esperam e podem causar um comportamento imprevisível de objeto de cliente ou formulário.</span><span class="sxs-lookup"><span data-stu-id="7060b-118">If your form objects make disallowed transitions between states, they will not behave in the ways that messaging clients expect and could cause unpredictable client or form object behavior.</span></span>
  
> [!NOTE]
> <span data-ttu-id="7060b-119">Algumas transições de estado dependem de informações de estados anteriores.</span><span class="sxs-lookup"><span data-stu-id="7060b-119">Some state transitions depend on information from previous states.</span></span> <span data-ttu-id="7060b-120">Seu servidor de formulário provavelmente terá que implementar um sinalizador em seus objetos de formulário para indicar se os valores das propriedades da mensagem foram alterados para facilitar alterações de estado posteriores.</span><span class="sxs-lookup"><span data-stu-id="7060b-120">Your form server will most likely have to implement a flag in its form objects to indicate whether the values of the message's properties have been changed to facilitate later state changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7060b-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="7060b-121">See also</span></span>

- [<span data-ttu-id="7060b-122">Desenvolvendo servidores de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="7060b-122">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

