---
title: PreprocessMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PreprocessMessage
api_type:
- COM
ms.assetid: dda50325-74b3-445e-986e-115f6536561f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 878c3aaf22a6cf8a08c8234df41b671088c435c7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584986"
---
# <a name="preprocessmessage"></a><span data-ttu-id="e4338-103">PreprocessMessage</span><span class="sxs-lookup"><span data-stu-id="e4338-103">PreprocessMessage</span></span>

  
  
<span data-ttu-id="e4338-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4338-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4338-105">Define uma função que pré-processa o conteúdo da mensagem ou o formato de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="e4338-105">Defines a function that preprocesses message contents or the format of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e4338-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="e4338-106">Header file:</span></span>  <br/> |<span data-ttu-id="e4338-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="e4338-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="e4338-108">Função definido implementada por:</span><span class="sxs-lookup"><span data-stu-id="e4338-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="e4338-109">Provedores de transporte</span><span class="sxs-lookup"><span data-stu-id="e4338-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="e4338-110">Função definido chamada pelo:</span><span class="sxs-lookup"><span data-stu-id="e4338-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="e4338-111">Spooler MAPI</span><span class="sxs-lookup"><span data-stu-id="e4338-111">MAPI spooler</span></span>  <br/> |
   
```cpp
HRESULT PreprocessMessage(
  LPVOID lpvSession,
  LPMESSAGE lpMessage,
  LPADRBOOK lpAdrBook,
  LPMAPIFOLDER lpFolder,
  LPALLOCATEBUFFER AllocateBuffer,
  LPALLOCATEMORE AllocateMore,
  LPFREEBUFFER FreeBuffer,
  ULONG FAR * lpcOutbound,
  LPMESSAGE FAR * FAR * lpppMessage,
  LPADRLIST FAR * lppRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="e4338-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4338-112">Parameters</span></span>

 <span data-ttu-id="e4338-113">_lpvSession_</span><span class="sxs-lookup"><span data-stu-id="e4338-113">_lpvSession_</span></span>
  
> <span data-ttu-id="e4338-114">[in] Ponteiro para a sessão a ser usado.</span><span class="sxs-lookup"><span data-stu-id="e4338-114">[in] Pointer to the session to be used.</span></span> 
    
 <span data-ttu-id="e4338-115">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="e4338-115">_lpMessage_</span></span>
  
> <span data-ttu-id="e4338-116">[in] Ponteiro para a mensagem para ser processado.</span><span class="sxs-lookup"><span data-stu-id="e4338-116">[in] Pointer to the message to be preprocessed.</span></span> 
    
 <span data-ttu-id="e4338-117">_lpAdrBook_</span><span class="sxs-lookup"><span data-stu-id="e4338-117">_lpAdrBook_</span></span>
  
> <span data-ttu-id="e4338-118">[in] Ponteiro para o catálogo de endereços do qual o usuário deve selecionar destinatários da mensagem.</span><span class="sxs-lookup"><span data-stu-id="e4338-118">[in] Pointer to the address book from which the user should select recipients for the message.</span></span> 
    
 <span data-ttu-id="e4338-119">_lpFolder_</span><span class="sxs-lookup"><span data-stu-id="e4338-119">_lpFolder_</span></span>
  
> <span data-ttu-id="e4338-120">[além, out] Ponteiro para uma pasta.</span><span class="sxs-lookup"><span data-stu-id="e4338-120">[in, out] Pointer to a folder.</span></span> <span data-ttu-id="e4338-121">Na entrada, o parâmetro _lpFolder_ aponta para a pasta que contém mensagens para ser processado.</span><span class="sxs-lookup"><span data-stu-id="e4338-121">On input, the  _lpFolder_ parameter points to the folder that contains messages to be preprocessed.</span></span> <span data-ttu-id="e4338-122">Na saída, _lpFolder_ aponta para a pasta onde as mensagens pré-processado tiverem sido colocadas.</span><span class="sxs-lookup"><span data-stu-id="e4338-122">On output,  _lpFolder_ points to the folder where preprocessed messages have been placed.</span></span> 
    
 <span data-ttu-id="e4338-123">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="e4338-123">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="e4338-124">[in] Ponteiro para a função de [MAPIAllocateBuffer](mapiallocatebuffer.md) , para ser usado para alocar memória.</span><span class="sxs-lookup"><span data-stu-id="e4338-124">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="e4338-125">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="e4338-125">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="e4338-126">[in] Ponteiro para a função de [MAPIAllocateMore](mapiallocatemore.md) , para ser usado para alocar memória adicional onde necessário.</span><span class="sxs-lookup"><span data-stu-id="e4338-126">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory where required.</span></span> 
    
 <span data-ttu-id="e4338-127">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="e4338-127">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="e4338-128">[in] Ponteiro para a função [MAPIFreeBuffer](mapifreebuffer.md) , que será usada para liberar memória.</span><span class="sxs-lookup"><span data-stu-id="e4338-128">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="e4338-129">_lpcOutbound_</span><span class="sxs-lookup"><span data-stu-id="e4338-129">_lpcOutbound_</span></span>
  
> <span data-ttu-id="e4338-130">[out] Ponteiro para o número de mensagens na matriz apontado pelo parâmetro _lpppMessage_ .</span><span class="sxs-lookup"><span data-stu-id="e4338-130">[out] Pointer to the number of messages in the array pointed to by the  _lpppMessage_ parameter.</span></span> 
    
 <span data-ttu-id="e4338-131">_lpppMessage_</span><span class="sxs-lookup"><span data-stu-id="e4338-131">_lpppMessage_</span></span>
  
> <span data-ttu-id="e4338-132">[out] Ponteiro para um ponteiro para uma matriz de ponteiros para preprocessada ou caso contrário gerada mensagens.</span><span class="sxs-lookup"><span data-stu-id="e4338-132">[out] Pointer to a pointer to an array of pointers to preprocessed or otherwise generated messages.</span></span> 
    
 <span data-ttu-id="e4338-133">_lppRecipList_</span><span class="sxs-lookup"><span data-stu-id="e4338-133">_lppRecipList_</span></span>
  
> <span data-ttu-id="e4338-134">[out] Ponteiro para uma estrutura [ADRLIST](adrlist.md) retornado opcional, listando os destinatários pré-processador detectado para o qual a mensagem é entregue.</span><span class="sxs-lookup"><span data-stu-id="e4338-134">[out] Pointer to an optional returned [ADRLIST](adrlist.md) structure, listing preprocessor-detected recipients for which the message is undeliverable.</span></span> <span data-ttu-id="e4338-135">Para obter mais informações sobre o conteúdo desta lista, consulte o método [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) .</span><span class="sxs-lookup"><span data-stu-id="e4338-135">For more information about the contents of this list, see the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e4338-136">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e4338-136">Return value</span></span>

<span data-ttu-id="e4338-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="e4338-137">S_OK</span></span>
  
> <span data-ttu-id="e4338-138">Conteúdo da mensagem foram pré-processados com êxito.</span><span class="sxs-lookup"><span data-stu-id="e4338-138">Message contents were successfully preprocessed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e4338-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4338-139">Remarks</span></span>

<span data-ttu-id="e4338-140">Um pré-processador de mensagem do provedor de transporte pode representar um indicador de progresso durante a mensagem pré-processamento.</span><span class="sxs-lookup"><span data-stu-id="e4338-140">A transport-provider message preprocessor can present a progress indicator during message preprocessing.</span></span> <span data-ttu-id="e4338-141">No entanto, ele nunca deve apresentar uma caixa de diálogo exigir interação do usuário durante a mensagem pré-processamento.</span><span class="sxs-lookup"><span data-stu-id="e4338-141">However, it should never present a dialog box requiring user interaction during message preprocessing.</span></span> 
  
<span data-ttu-id="e4338-142">Quando um pré-processador adiciona grandes quantidades de dados a uma mensagem de saída, certos procedimentos devem ser seguidos.</span><span class="sxs-lookup"><span data-stu-id="e4338-142">When a preprocessor adds large amounts of data to an outbound message, certain procedures should be followed.</span></span> <span data-ttu-id="e4338-143">Esse tipo de mensagem pode ser armazenado em um armazenamento de mensagens baseado em servidor, causando o pré-processador acessar um repositório remoto, um procedimento demorado.</span><span class="sxs-lookup"><span data-stu-id="e4338-143">This type of message can be stored in a server-based message store, causing the preprocessor to access a remote store, a time-consuming procedure.</span></span> <span data-ttu-id="e4338-144">Para evitar a fazer isso, o pré-processador deve ter uma opção que ativa para armazenar dados que utiliza uma grande quantidade de espaço em um repositório de mensagens local e para fornecer uma referência para esse repositório local na mensagem.</span><span class="sxs-lookup"><span data-stu-id="e4338-144">To avoid having to do so, the preprocessor should have an option that enables it to store data that takes a large amount of space in a local message store and to provide a reference to that local store in the message.</span></span> 
  
<span data-ttu-id="e4338-145">O pré-processador não deve liberar qualquer um dos objetos originalmente passados para a função de **PreprocessMessage** com base.</span><span class="sxs-lookup"><span data-stu-id="e4338-145">The preprocessor should not release any of the objects originally passed to the **PreprocessMessage** based function.</span></span> 
  
<span data-ttu-id="e4338-146">Antes do MAPI spooler pode chamar uma função de **PreprocessMessage** , o provedor de transporte deve ter registrado a função em uma chamada ao método [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) .</span><span class="sxs-lookup"><span data-stu-id="e4338-146">Before the MAPI spooler can call a **PreprocessMessage** function, the transport provider must have registered the function in a call to the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method.</span></span> <span data-ttu-id="e4338-147">Depois de chamar uma função **PreprocessMessage** , o spooler não pode continuar enviando uma mensagem até que a função retornará.</span><span class="sxs-lookup"><span data-stu-id="e4338-147">After calling a **PreprocessMessage** function, the spooler cannot continue submitting a message until the function returns.</span></span> 
  
<span data-ttu-id="e4338-148">O MAPI spooler possui a tarefa de envio de mensagens.</span><span class="sxs-lookup"><span data-stu-id="e4338-148">The MAPI spooler owns the task of submitting messages.</span></span> <span data-ttu-id="e4338-149">Isso significa que a mensagem original nunca é colocada em uma matriz de ponteiros de mensagem e que uma chamada para os métodos **SubmitMessage** nunca é necessária.</span><span class="sxs-lookup"><span data-stu-id="e4338-149">This means the original message is never placed in an array of message pointers and that a call to the **SubmitMessage** methods is never required.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e4338-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4338-150">See also</span></span>



[<span data-ttu-id="e4338-151">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e4338-151">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="e4338-152">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="e4338-152">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="e4338-153">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e4338-153">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

