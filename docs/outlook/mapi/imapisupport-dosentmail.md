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
ms.openlocfilehash: 8289b8dd2e0ab3c760e77a37b821d2fe74e4abe9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423948"
---
# <a name="imapisupportdosentmail"></a><span data-ttu-id="ca689-103">IMAPISupport::DoSentMail</span><span class="sxs-lookup"><span data-stu-id="ca689-103">IMAPISupport::DoSentMail</span></span>

  
  
<span data-ttu-id="ca689-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca689-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca689-105">Processa uma mensagem enviada.</span><span class="sxs-lookup"><span data-stu-id="ca689-105">Processes a sent message.</span></span>
  
```cpp
HRESULT DoSentMail(
  ULONG ulFlags,
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a><span data-ttu-id="ca689-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca689-106">Parameters</span></span>

 <span data-ttu-id="ca689-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ca689-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ca689-108">no Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ca689-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="ca689-109">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="ca689-109">_lpMessage_</span></span>
  
> <span data-ttu-id="ca689-110">no Um ponteiro para a mensagem aberta para a qual uma mensagem deve ser gerada na pasta designada para reter itens enviados.</span><span class="sxs-lookup"><span data-stu-id="ca689-110">[in] A pointer to the open message for which a message should be generated in the folder designated to hold sent items.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ca689-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ca689-111">Return value</span></span>

<span data-ttu-id="ca689-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="ca689-112">S_OK</span></span> 
  
> <span data-ttu-id="ca689-113">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="ca689-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ca689-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca689-114">Remarks</span></span>

<span data-ttu-id="ca689-115">O método **IMAPISupport::D osentmail** é implementado para objetos de suporte do provedor de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ca689-115">The **IMAPISupport::DoSentMail** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="ca689-116">Os provedores de repositório de mensagens chamam **DoSentMail** de sua implementação do método [IMsgStore:: FinishedMsg](imsgstore-finishedmsg.md) , que é chamado pelo spooler MAPI quando o processamento de uma mensagem é concluído.</span><span class="sxs-lookup"><span data-stu-id="ca689-116">Message store providers call **DoSentMail** from their implementation of the [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method, which is called by the MAPI spooler when it has finished processing a message.</span></span> <span data-ttu-id="ca689-117">**FinishedMsg** desbloqueia a mensagem, garante que a contagem de referência da mensagem seja 1 e chama o **DoSentMail**.</span><span class="sxs-lookup"><span data-stu-id="ca689-117">**FinishedMsg** unlocks the message, ensures that the message's reference count is 1, and calls **DoSentMail**.</span></span>
  
 <span data-ttu-id="ca689-118">O **DoSentMail** executa as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="ca689-118">**DoSentMail** performs the following tasks:</span></span> 
  
- <span data-ttu-id="ca689-119">Verifica a mensagem da propriedade **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) para determinar se a mensagem deve ser excluída após o envio.</span><span class="sxs-lookup"><span data-stu-id="ca689-119">Checks the message for the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property to determine whether the message should be deleted after sending.</span></span>
    
- <span data-ttu-id="ca689-120">Determina o local da pasta Itens enviados.</span><span class="sxs-lookup"><span data-stu-id="ca689-120">Determines the location of the Sent Items folder.</span></span>
    
- <span data-ttu-id="ca689-121">Inicia o processamento de interceptador de mensagens para qualquer gancho definido na pasta Itens enviados.</span><span class="sxs-lookup"><span data-stu-id="ca689-121">Initiates message hook processing for any hooks set on the Sent Items folder.</span></span>
    
- <span data-ttu-id="ca689-122">Move a mensagem para a pasta Itens enviados, a pasta itens excluídos ou para outra pasta.</span><span class="sxs-lookup"><span data-stu-id="ca689-122">Moves the message to the Sent Items folder, Deleted Items folder, or to another folder.</span></span>
    
- <span data-ttu-id="ca689-123">Libera a mensagem.</span><span class="sxs-lookup"><span data-stu-id="ca689-123">Releases the message.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ca689-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca689-124">See also</span></span>



[<span data-ttu-id="ca689-125">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="ca689-125">IMsgStore::FinishedMsg</span></span>](imsgstore-finishedmsg.md)
  
[<span data-ttu-id="ca689-126">Propriedade canônica PidTagDeleteAfterSubmit</span><span class="sxs-lookup"><span data-stu-id="ca689-126">PidTagDeleteAfterSubmit Canonical Property</span></span>](pidtagdeleteaftersubmit-canonical-property.md)
  
[<span data-ttu-id="ca689-127">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ca689-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

