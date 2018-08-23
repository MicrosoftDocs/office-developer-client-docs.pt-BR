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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 379fdc47f35fb183dd0bf551e421422abb106c0e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591006"
---
# <a name="imapisupportexpandrecips"></a><span data-ttu-id="cf039-103">IMAPISupport::ExpandRecips</span><span class="sxs-lookup"><span data-stu-id="cf039-103">IMAPISupport::ExpandRecips</span></span>

  
  
<span data-ttu-id="cf039-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf039-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf039-105">Conclui a lista de destinatários da mensagem, expandindo listas de distribuição particular.</span><span class="sxs-lookup"><span data-stu-id="cf039-105">Completes a message's recipient list, expanding particular distribution lists.</span></span>
  
```cpp
HRESULT ExpandRecips(
  LPMESSAGE lpMessage,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="cf039-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cf039-106">Parameters</span></span>

 <span data-ttu-id="cf039-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="cf039-107">_lpMessage_</span></span>
  
> <span data-ttu-id="cf039-108">[in] Um ponteiro para a mensagem que tem a lista de destinatários a serem processados.</span><span class="sxs-lookup"><span data-stu-id="cf039-108">[in] A pointer to the message that has the recipient list to be processed.</span></span>
    
 <span data-ttu-id="cf039-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="cf039-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="cf039-110">[out] Um ponteiro para uma bitmask dos sinalizadores que controla o tipo de processamento ocorre.</span><span class="sxs-lookup"><span data-stu-id="cf039-110">[out] A pointer to a bitmask of flags that controls the type of processing that occurs.</span></span> <span data-ttu-id="cf039-111">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="cf039-111">The following flags can be set:</span></span>
    
<span data-ttu-id="cf039-112">NEEDS_PREPROCESSING</span><span class="sxs-lookup"><span data-stu-id="cf039-112">NEEDS_PREPROCESSING</span></span> 
  
> <span data-ttu-id="cf039-113">A mensagem precisa ser processado antes de serem enviada.</span><span class="sxs-lookup"><span data-stu-id="cf039-113">The message needs to be preprocessed before it is sent.</span></span>
    
<span data-ttu-id="cf039-114">NEEDS_SPOOLER</span><span class="sxs-lookup"><span data-stu-id="cf039-114">NEEDS_SPOOLER</span></span> 
  
> <span data-ttu-id="cf039-115">O MAPI spooler (ao invés do provedor de transporte para o qual o chamador está intimamente ligado) deve enviar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="cf039-115">The MAPI spooler (rather than the transport provider to which the caller is tightly coupled) must send the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cf039-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="cf039-116">Return value</span></span>

<span data-ttu-id="cf039-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="cf039-117">S_OK</span></span> 
  
> <span data-ttu-id="cf039-118">Lista de destinatários da mensagem foi processada com êxito.</span><span class="sxs-lookup"><span data-stu-id="cf039-118">The message's recipient list was successfully processed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cf039-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf039-119">Remarks</span></span>

<span data-ttu-id="cf039-120">O método **IMAPISupport::ExpandRecips** é implementado para objetos de suporte do provedor de repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="cf039-120">The **IMAPISupport::ExpandRecips** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="cf039-121">Provedores de armazenamento de mensagem chamarem **ExpandRecips** para solicitar que o MAPI para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="cf039-121">Message store providers call **ExpandRecips** to prompt MAPI to perform the following tasks:</span></span> 
  
- <span data-ttu-id="cf039-122">Expanda certas listas de distribuição pessoal aos destinatários componente.</span><span class="sxs-lookup"><span data-stu-id="cf039-122">Expand certain personal distribution lists to their component recipients.</span></span>
    
- <span data-ttu-id="cf039-123">Substitua todos os nomes para exibição que foram alterados os nomes originais.</span><span class="sxs-lookup"><span data-stu-id="cf039-123">Replace all display names that have been changed with the original names.</span></span>
    
- <span data-ttu-id="cf039-124">Marca quaisquer entradas duplicadas.</span><span class="sxs-lookup"><span data-stu-id="cf039-124">Mark any duplicate entries.</span></span>
    
- <span data-ttu-id="cf039-125">Resolva todos os endereços únicos.</span><span class="sxs-lookup"><span data-stu-id="cf039-125">Resolve all one-off addresses.</span></span> 
    
- <span data-ttu-id="cf039-126">Verifique se a mensagem precisa pré-processamento e, se contiver, defina o sinalizador apontado pela _lpulFlags_ para NEEDS_PREPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="cf039-126">Check whether the message needs preprocessing and, if it does, set the flag pointed to by  _lpulFlags_ to NEEDS_PREPROCESSING.</span></span> 
    
 <span data-ttu-id="cf039-127">**ExpandRecips** expande quaisquer listas de distribuição que tenham o tipo de endereço de mensagens de MAPIPDL.</span><span class="sxs-lookup"><span data-stu-id="cf039-127">**ExpandRecips** expands any distribution lists that have the messaging address type of MAPIPDL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="cf039-128">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="cf039-128">Notes to callers</span></span>

<span data-ttu-id="cf039-129">Sempre chame **ExpandRecips** como parte do seu processamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="cf039-129">Always call **ExpandRecips** as part of your message processing.</span></span> <span data-ttu-id="cf039-130">Fazer uma chamada para **ExpandRecips** uma das chamadas primeira na sua implementação do método [IMessage::SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="cf039-130">Make a call to **ExpandRecips** one of the first calls in your [IMessage::SubmitMessage](imessage-submitmessage.md) method implementation.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cf039-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf039-131">See also</span></span>



[<span data-ttu-id="cf039-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="cf039-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="cf039-133">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="cf039-133">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

