---
title: IMAPISupportDoSentMail
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoSentMail
api_type:
- COM
ms.assetid: 4bb65c2a-9926-42da-9161-47836e8de40a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 82490dbe597ebd3f7198aa7e0c904a10202ecd77
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568207"
---
# <a name="imapisupportdosentmail"></a><span data-ttu-id="f08d8-103">IMAPISupport::DoSentMail</span><span class="sxs-lookup"><span data-stu-id="f08d8-103">IMAPISupport::DoSentMail</span></span>

  
  
<span data-ttu-id="f08d8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f08d8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f08d8-105">Processa uma mensagem enviada.</span><span class="sxs-lookup"><span data-stu-id="f08d8-105">Processes a sent message.</span></span>
  
```cpp
HRESULT DoSentMail(
  ULONG ulFlags,
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a><span data-ttu-id="f08d8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f08d8-106">Parameters</span></span>

 <span data-ttu-id="f08d8-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f08d8-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f08d8-108">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f08d8-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="f08d8-109">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="f08d8-109">_lpMessage_</span></span>
  
> <span data-ttu-id="f08d8-110">[in] Um ponteiro para a mensagem de aberta para o qual uma mensagem deve ser gerada na pasta designada para armazenar itens enviados.</span><span class="sxs-lookup"><span data-stu-id="f08d8-110">[in] A pointer to the open message for which a message should be generated in the folder designated to hold sent items.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f08d8-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f08d8-111">Return value</span></span>

<span data-ttu-id="f08d8-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="f08d8-112">S_OK</span></span> 
  
> <span data-ttu-id="f08d8-113">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="f08d8-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f08d8-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f08d8-114">Remarks</span></span>

<span data-ttu-id="f08d8-115">O método **IMAPISupport::DoSentMail** é implementado para objetos de suporte do provedor de repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="f08d8-115">The **IMAPISupport::DoSentMail** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="f08d8-116">Provedores de armazenamento de mensagem chamarem **DoSentMail** da sua implementação do método [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) , que é chamado pelo spooler MAPI quando ele tiver terminado de processamento de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="f08d8-116">Message store providers call **DoSentMail** from their implementation of the [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method, which is called by the MAPI spooler when it has finished processing a message.</span></span> <span data-ttu-id="f08d8-117">**FinishedMsg** desbloqueia a mensagem, garante que a contagem de referência da mensagem é 1 e chama **DoSentMail**.</span><span class="sxs-lookup"><span data-stu-id="f08d8-117">**FinishedMsg** unlocks the message, ensures that the message's reference count is 1, and calls **DoSentMail**.</span></span>
  
 <span data-ttu-id="f08d8-118">**DoSentMail** executa as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="f08d8-118">**DoSentMail** performs the following tasks:</span></span> 
  
- <span data-ttu-id="f08d8-119">Verifica a mensagem para a propriedade **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) determinar se a mensagem deve ser excluída após o envio.</span><span class="sxs-lookup"><span data-stu-id="f08d8-119">Checks the message for the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property to determine whether the message should be deleted after sending.</span></span>
    
- <span data-ttu-id="f08d8-120">Determina o local da pasta Itens enviados.</span><span class="sxs-lookup"><span data-stu-id="f08d8-120">Determines the location of the Sent Items folder.</span></span>
    
- <span data-ttu-id="f08d8-121">Inicia o processamento para qualquer ganchos definidas na pasta Itens enviados do gancho de mensagem.</span><span class="sxs-lookup"><span data-stu-id="f08d8-121">Initiates message hook processing for any hooks set on the Sent Items folder.</span></span>
    
- <span data-ttu-id="f08d8-122">Move a mensagem para a pasta Itens enviados, itens excluídos ou para outra pasta.</span><span class="sxs-lookup"><span data-stu-id="f08d8-122">Moves the message to the Sent Items folder, Deleted Items folder, or to another folder.</span></span>
    
- <span data-ttu-id="f08d8-123">Libera a mensagem.</span><span class="sxs-lookup"><span data-stu-id="f08d8-123">Releases the message.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f08d8-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="f08d8-124">See also</span></span>



[<span data-ttu-id="f08d8-125">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="f08d8-125">IMsgStore::FinishedMsg</span></span>](imsgstore-finishedmsg.md)
  
[<span data-ttu-id="f08d8-126">Propriedade canônico de PidTagDeleteAfterSubmit</span><span class="sxs-lookup"><span data-stu-id="f08d8-126">PidTagDeleteAfterSubmit Canonical Property</span></span>](pidtagdeleteaftersubmit-canonical-property.md)
  
[<span data-ttu-id="f08d8-127">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f08d8-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

