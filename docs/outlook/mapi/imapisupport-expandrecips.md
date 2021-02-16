---
title: IMAPISupportExpandRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ExpandRecips
api_type:
- COM
ms.assetid: 78edd549-d557-489a-85f5-adfb5c44a7d4
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 105219fe430cd8746c3aa6cf5cd90629d5f72080
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411243"
---
# <a name="imapisupportexpandrecips"></a><span data-ttu-id="a831a-103">IMAPISupport::ExpandRecips</span><span class="sxs-lookup"><span data-stu-id="a831a-103">IMAPISupport::ExpandRecips</span></span>

  
  
<span data-ttu-id="a831a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a831a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a831a-105">Conclui a lista de destinatários de uma mensagem, expandindo listas de distribuição específicas.</span><span class="sxs-lookup"><span data-stu-id="a831a-105">Completes a message's recipient list, expanding particular distribution lists.</span></span>
  
```cpp
HRESULT ExpandRecips(
  LPMESSAGE lpMessage,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a831a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a831a-106">Parameters</span></span>

 <span data-ttu-id="a831a-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="a831a-107">_lpMessage_</span></span>
  
> <span data-ttu-id="a831a-108">[in] Um ponteiro para a mensagem que tem a lista de destinatários a ser processada.</span><span class="sxs-lookup"><span data-stu-id="a831a-108">[in] A pointer to the message that has the recipient list to be processed.</span></span>
    
 <span data-ttu-id="a831a-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="a831a-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="a831a-110">[out] Um ponteiro para uma máscara de bits de sinalizadores que controla o tipo de processamento que ocorre.</span><span class="sxs-lookup"><span data-stu-id="a831a-110">[out] A pointer to a bitmask of flags that controls the type of processing that occurs.</span></span> <span data-ttu-id="a831a-111">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="a831a-111">The following flags can be set:</span></span>
    
<span data-ttu-id="a831a-112">NEEDS_PREPROCESSING</span><span class="sxs-lookup"><span data-stu-id="a831a-112">NEEDS_PREPROCESSING</span></span> 
  
> <span data-ttu-id="a831a-113">A mensagem precisa ser pré-processada antes de ser enviada.</span><span class="sxs-lookup"><span data-stu-id="a831a-113">The message needs to be preprocessed before it is sent.</span></span>
    
<span data-ttu-id="a831a-114">NEEDS_SPOOLER</span><span class="sxs-lookup"><span data-stu-id="a831a-114">NEEDS_SPOOLER</span></span> 
  
> <span data-ttu-id="a831a-115">O spooler MAPI (em vez do provedor de transporte ao qual o chamador está fortemente próximo) deve enviar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="a831a-115">The MAPI spooler (rather than the transport provider to which the caller is tightly coupled) must send the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a831a-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a831a-116">Return value</span></span>

<span data-ttu-id="a831a-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="a831a-117">S_OK</span></span> 
  
> <span data-ttu-id="a831a-118">A lista de destinatários da mensagem foi processada com êxito.</span><span class="sxs-lookup"><span data-stu-id="a831a-118">The message's recipient list was successfully processed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a831a-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="a831a-119">Remarks</span></span>

<span data-ttu-id="a831a-120">O **método IMAPISupport::ExpandRecips** é implementado para objetos de suporte do provedor de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a831a-120">The **IMAPISupport::ExpandRecips** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="a831a-121">Os provedores de armazenamento de mensagens **chamam ExpandRecips** para solicitar que o MAPI execute as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="a831a-121">Message store providers call **ExpandRecips** to prompt MAPI to perform the following tasks:</span></span> 
  
- <span data-ttu-id="a831a-122">Expanda determinadas listas de distribuição pessoais para seus destinatários de componentes.</span><span class="sxs-lookup"><span data-stu-id="a831a-122">Expand certain personal distribution lists to their component recipients.</span></span>
    
- <span data-ttu-id="a831a-123">Substitua todos os nomes de exibição que foram alterados com os nomes originais.</span><span class="sxs-lookup"><span data-stu-id="a831a-123">Replace all display names that have been changed with the original names.</span></span>
    
- <span data-ttu-id="a831a-124">Marque qualquer entrada duplicada.</span><span class="sxs-lookup"><span data-stu-id="a831a-124">Mark any duplicate entries.</span></span>
    
- <span data-ttu-id="a831a-125">Resolver todos os endereços one-off.</span><span class="sxs-lookup"><span data-stu-id="a831a-125">Resolve all one-off addresses.</span></span> 
    
- <span data-ttu-id="a831a-126">Verifique se a mensagem precisa de pré-processamento e, se precisar, defina o sinalizador apontado por  _lpulFlags_ como NEEDS_PREPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="a831a-126">Check whether the message needs preprocessing and, if it does, set the flag pointed to by  _lpulFlags_ to NEEDS_PREPROCESSING.</span></span> 
    
 <span data-ttu-id="a831a-127">**ExpandRecips** expande todas as listas de distribuição que tenham o tipo de endereço de mensagens de MAPIPDL.</span><span class="sxs-lookup"><span data-stu-id="a831a-127">**ExpandRecips** expands any distribution lists that have the messaging address type of MAPIPDL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a831a-128">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="a831a-128">Notes to callers</span></span>

<span data-ttu-id="a831a-129">Sempre chame **ExpandRecips** como parte do processamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a831a-129">Always call **ExpandRecips** as part of your message processing.</span></span> <span data-ttu-id="a831a-130">Faça uma chamada para **ExpandRecips** uma das primeiras chamadas na implementação do método [IMessage::SubmitMessage.](imessage-submitmessage.md)</span><span class="sxs-lookup"><span data-stu-id="a831a-130">Make a call to **ExpandRecips** one of the first calls in your [IMessage::SubmitMessage](imessage-submitmessage.md) method implementation.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a831a-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="a831a-131">See also</span></span>



[<span data-ttu-id="a831a-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="a831a-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="a831a-133">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a831a-133">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

