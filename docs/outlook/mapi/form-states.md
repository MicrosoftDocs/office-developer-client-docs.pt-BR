---
title: Estados de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dfc9fbf1-90d4-4756-92d9-032ac56a9c50
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 195a82bfcc163ee01d2d42c71e79a8f5c9c620e5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564630"
---
# <a name="form-states"></a><span data-ttu-id="22350-103">Estados de formulário</span><span class="sxs-lookup"><span data-stu-id="22350-103">Form states</span></span>

<span data-ttu-id="22350-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22350-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22350-105">Objetos de formulário podem estar em um dos cinco estados distintos, dependendo do que métodos tiverem sido chamados neles e se ocorreu algum erro na execução desses métodos.</span><span class="sxs-lookup"><span data-stu-id="22350-105">Form objects can be in one of five distinct states, depending on what methods have been called in them and whether any errors have occurred in performing those methods.</span></span> <span data-ttu-id="22350-106">Os estados são descritos nos tópicos a seguir:</span><span class="sxs-lookup"><span data-stu-id="22350-106">The states are described in the following topics:</span></span>
  
- [<span data-ttu-id="22350-107">Estado Uninitialized</span><span class="sxs-lookup"><span data-stu-id="22350-107">Uninitialized State</span></span>](uninitialized-state.md)
    
- [<span data-ttu-id="22350-108">Estado Normal</span><span class="sxs-lookup"><span data-stu-id="22350-108">Normal State</span></span>](normal-state.md)
    
- [<span data-ttu-id="22350-109">Estado NoScribble</span><span class="sxs-lookup"><span data-stu-id="22350-109">NoScribble State</span></span>](noscribble-state.md)
    
- [<span data-ttu-id="22350-110">Estado HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="22350-110">HandsOffAfterSave State</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="22350-111">Estado HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="22350-111">HandsOffFromNormal State</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="22350-112">Os estados estão relacionadas principalmente até o status dos dados no objeto form.</span><span class="sxs-lookup"><span data-stu-id="22350-112">The states primarily relate to the status of the data in the form object.</span></span> <span data-ttu-id="22350-113">Os diferentes estados refletem se os dados precisam ser salvo, se o objeto de formulário deve permitir modificações aos dados, e que o ponto no processo de salvar os dados que o formulário está nesse.</span><span class="sxs-lookup"><span data-stu-id="22350-113">The different states reflect whether the data needs to be saved, whether the form object should allow modifications to the data, and what point in the process of saving the data the form is in.</span></span> <span data-ttu-id="22350-114">Sendo assim, o formulário Estados e transições entre elas têm mais a ver com a implementação do seu servidor de formulário do [IPersistMessage: IUnknown](ipersistmessageiunknown.md) métodos que qualquer outra de interface.</span><span class="sxs-lookup"><span data-stu-id="22350-114">As such, the form states and transitions between them have more to do with your form server's implementation of [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interface methods than any other.</span></span> <span data-ttu-id="22350-115">É muito útil para implementação adequada das interfaces de formulário de MAPI que seu servidor do formulário deve implementar o conhecimento desses estados.</span><span class="sxs-lookup"><span data-stu-id="22350-115">Knowledge of these states is very useful for proper implementation of the MAPI form interfaces that your form server must implement.</span></span> 
  
<span data-ttu-id="22350-116">Os tópicos desta seção descrevem os diversos estados, juntamente com as ações permitidas que causam transições para outros estados.</span><span class="sxs-lookup"><span data-stu-id="22350-116">The topics in this section describe the various states, along with the allowed actions that cause transitions to other states.</span></span> <span data-ttu-id="22350-117">Qualquer transições não listadas nos tópicos não são permitidas.</span><span class="sxs-lookup"><span data-stu-id="22350-117">Any transitions not listed in the topics are not allowed.</span></span> <span data-ttu-id="22350-118">Se os objetos de formulário fizer não autorizadas transições entre estados, elas não serão se comportam das maneiras que os clientes de mensagens esperam e podem causar comportamento imprevisível do objeto de cliente ou formulário.</span><span class="sxs-lookup"><span data-stu-id="22350-118">If your form objects make disallowed transitions between states, they will not behave in the ways that messaging clients expect and could cause unpredictable client or form object behavior.</span></span>
  
> [!NOTE]
> <span data-ttu-id="22350-119">Algumas transições de estado dependem de informações nos estados anteriores.</span><span class="sxs-lookup"><span data-stu-id="22350-119">Some state transitions depend on information from previous states.</span></span> <span data-ttu-id="22350-120">Seu servidor de formulário provavelmente terá de implementar um sinalizador em seus objetos de formulário para indicar se os valores das propriedades da mensagem foram alterados para facilitar posteriores alterações de estado.</span><span class="sxs-lookup"><span data-stu-id="22350-120">Your form server will most likely have to implement a flag in its form objects to indicate whether the values of the message's properties have been changed to facilitate later state changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="22350-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="22350-121">See also</span></span>

- [<span data-ttu-id="22350-122">Desenvolver servidores de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="22350-122">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

