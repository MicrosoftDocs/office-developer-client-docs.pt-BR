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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316524"
---
# <a name="imapisupportexpandrecips"></a><span data-ttu-id="4c606-103">IMAPISupport::ExpandRecips</span><span class="sxs-lookup"><span data-stu-id="4c606-103">IMAPISupport::ExpandRecips</span></span>

  
  
<span data-ttu-id="4c606-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c606-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c606-105">Conclui a lista de destinatários de uma mensagem, expandindo listas de distribuição específicas.</span><span class="sxs-lookup"><span data-stu-id="4c606-105">Completes a message's recipient list, expanding particular distribution lists.</span></span>
  
```cpp
HRESULT ExpandRecips(
  LPMESSAGE lpMessage,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="4c606-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c606-106">Parameters</span></span>

 <span data-ttu-id="4c606-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="4c606-107">_lpMessage_</span></span>
  
> <span data-ttu-id="4c606-108">no Um ponteiro para a mensagem que tem a lista de destinatários a ser processada.</span><span class="sxs-lookup"><span data-stu-id="4c606-108">[in] A pointer to the message that has the recipient list to be processed.</span></span>
    
 <span data-ttu-id="4c606-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="4c606-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="4c606-110">bota Um ponteiro para uma bitmask de sinalizadores que controla o tipo de processamento que ocorre.</span><span class="sxs-lookup"><span data-stu-id="4c606-110">[out] A pointer to a bitmask of flags that controls the type of processing that occurs.</span></span> <span data-ttu-id="4c606-111">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="4c606-111">The following flags can be set:</span></span>
    
<span data-ttu-id="4c606-112">NEEDS_PREPROCESSING</span><span class="sxs-lookup"><span data-stu-id="4c606-112">NEEDS_PREPROCESSING</span></span> 
  
> <span data-ttu-id="4c606-113">A mensagem precisa ser preprocessada antes de ser enviada.</span><span class="sxs-lookup"><span data-stu-id="4c606-113">The message needs to be preprocessed before it is sent.</span></span>
    
<span data-ttu-id="4c606-114">NEEDS_SPOOLER</span><span class="sxs-lookup"><span data-stu-id="4c606-114">NEEDS_SPOOLER</span></span> 
  
> <span data-ttu-id="4c606-115">O spooler MAPI (em vez do provedor de transporte ao qual o chamador está rigidamente acoplado) deve enviar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="4c606-115">The MAPI spooler (rather than the transport provider to which the caller is tightly coupled) must send the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4c606-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4c606-116">Return value</span></span>

<span data-ttu-id="4c606-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="4c606-117">S_OK</span></span> 
  
> <span data-ttu-id="4c606-118">A lista de destinatários da mensagem foi processada com êxito.</span><span class="sxs-lookup"><span data-stu-id="4c606-118">The message's recipient list was successfully processed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4c606-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c606-119">Remarks</span></span>

<span data-ttu-id="4c606-120">O método **IMAPISupport:: ExpandRecips** é implementado para objetos de suporte do provedor de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="4c606-120">The **IMAPISupport::ExpandRecips** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="4c606-121">Os provedores de repositório de mensagens chamam o **ExpandRecips** para solicitar MAPI para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="4c606-121">Message store providers call **ExpandRecips** to prompt MAPI to perform the following tasks:</span></span> 
  
- <span data-ttu-id="4c606-122">Expanda determinadas listas de distribuição pessoais para seus destinatários do componente.</span><span class="sxs-lookup"><span data-stu-id="4c606-122">Expand certain personal distribution lists to their component recipients.</span></span>
    
- <span data-ttu-id="4c606-123">Substitua todos os nomes para exibição que foram alterados com os nomes originais.</span><span class="sxs-lookup"><span data-stu-id="4c606-123">Replace all display names that have been changed with the original names.</span></span>
    
- <span data-ttu-id="4c606-124">Marque as entradas duplicadas.</span><span class="sxs-lookup"><span data-stu-id="4c606-124">Mark any duplicate entries.</span></span>
    
- <span data-ttu-id="4c606-125">Resolva todos os endereços únicos.</span><span class="sxs-lookup"><span data-stu-id="4c606-125">Resolve all one-off addresses.</span></span> 
    
- <span data-ttu-id="4c606-126">Verifique se a mensagem precisa de pré-processamento e, em caso afirmativo, defina o sinalizador apontado por _lpulFlags_ para NEEDS_PREPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="4c606-126">Check whether the message needs preprocessing and, if it does, set the flag pointed to by  _lpulFlags_ to NEEDS_PREPROCESSING.</span></span> 
    
 <span data-ttu-id="4c606-127">**ExpandRecips** expande qualquer lista de distribuição que tenha o tipo de endereço de mensagem de MAPIPDL.</span><span class="sxs-lookup"><span data-stu-id="4c606-127">**ExpandRecips** expands any distribution lists that have the messaging address type of MAPIPDL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4c606-128">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="4c606-128">Notes to callers</span></span>

<span data-ttu-id="4c606-129">Sempre chame **ExpandRecips** como parte do seu processamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="4c606-129">Always call **ExpandRecips** as part of your message processing.</span></span> <span data-ttu-id="4c606-130">Faça uma chamada para **ExpandRecips** uma das primeiras chamadas em sua implementação do método [IMessage: SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="4c606-130">Make a call to **ExpandRecips** one of the first calls in your [IMessage::SubmitMessage](imessage-submitmessage.md) method implementation.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4c606-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c606-131">See also</span></span>



[<span data-ttu-id="4c606-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="4c606-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="4c606-133">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="4c606-133">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

