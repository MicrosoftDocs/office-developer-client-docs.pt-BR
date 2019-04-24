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
ms.openlocfilehash: a3982520cb1c745874a938962ece075a294b6257
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351377"
---
# <a name="preprocessmessage"></a><span data-ttu-id="a29a0-103">PreprocessMessage</span><span class="sxs-lookup"><span data-stu-id="a29a0-103">PreprocessMessage</span></span>

  
  
<span data-ttu-id="a29a0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a29a0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a29a0-105">Define uma função que pré-processamento o conteúdo da mensagem ou o formato de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="a29a0-105">Defines a function that preprocesses message contents or the format of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a29a0-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="a29a0-106">Header file:</span></span>  <br/> |<span data-ttu-id="a29a0-107">Mapispi. h</span><span class="sxs-lookup"><span data-stu-id="a29a0-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="a29a0-108">Função definida implementada por:</span><span class="sxs-lookup"><span data-stu-id="a29a0-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="a29a0-109">Provedores de transporte</span><span class="sxs-lookup"><span data-stu-id="a29a0-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="a29a0-110">Função definida chamada por:</span><span class="sxs-lookup"><span data-stu-id="a29a0-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="a29a0-111">Spooler MAPI</span><span class="sxs-lookup"><span data-stu-id="a29a0-111">MAPI spooler</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="a29a0-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a29a0-112">Parameters</span></span>

 <span data-ttu-id="a29a0-113">_lpvSession_</span><span class="sxs-lookup"><span data-stu-id="a29a0-113">_lpvSession_</span></span>
  
> <span data-ttu-id="a29a0-114">no Ponteiro para a sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="a29a0-114">[in] Pointer to the session to be used.</span></span> 
    
 <span data-ttu-id="a29a0-115">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="a29a0-115">_lpMessage_</span></span>
  
> <span data-ttu-id="a29a0-116">no Ponteiro para a mensagem a ser preprocessada.</span><span class="sxs-lookup"><span data-stu-id="a29a0-116">[in] Pointer to the message to be preprocessed.</span></span> 
    
 <span data-ttu-id="a29a0-117">_lpAdrBook_</span><span class="sxs-lookup"><span data-stu-id="a29a0-117">_lpAdrBook_</span></span>
  
> <span data-ttu-id="a29a0-118">no Ponteiro para o catálogo de endereços do qual o usuário deve selecionar destinatários para a mensagem.</span><span class="sxs-lookup"><span data-stu-id="a29a0-118">[in] Pointer to the address book from which the user should select recipients for the message.</span></span> 
    
 <span data-ttu-id="a29a0-119">_lpFolder_</span><span class="sxs-lookup"><span data-stu-id="a29a0-119">_lpFolder_</span></span>
  
> <span data-ttu-id="a29a0-120">[in, out] Ponteiro para uma pasta.</span><span class="sxs-lookup"><span data-stu-id="a29a0-120">[in, out] Pointer to a folder.</span></span> <span data-ttu-id="a29a0-121">Na entrada, o parâmetro _lpFolder_ aponta para a pasta que contém as mensagens a serem processadas.</span><span class="sxs-lookup"><span data-stu-id="a29a0-121">On input, the  _lpFolder_ parameter points to the folder that contains messages to be preprocessed.</span></span> <span data-ttu-id="a29a0-122">Na saída, _lpFolder_ aponta para a pasta onde as mensagens pré processadas foram colocadas.</span><span class="sxs-lookup"><span data-stu-id="a29a0-122">On output,  _lpFolder_ points to the folder where preprocessed messages have been placed.</span></span> 
    
 <span data-ttu-id="a29a0-123">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="a29a0-123">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="a29a0-124">no Ponteiro para a função [MAPIAllocateBuffer](mapiallocatebuffer.md) , a ser usado para alocar memória.</span><span class="sxs-lookup"><span data-stu-id="a29a0-124">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="a29a0-125">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="a29a0-125">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="a29a0-126">no Ponteiro para a função [MAPIAllocateMore](mapiallocatemore.md) , a ser usado para alocar memória adicional onde for necessário.</span><span class="sxs-lookup"><span data-stu-id="a29a0-126">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory where required.</span></span> 
    
 <span data-ttu-id="a29a0-127">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="a29a0-127">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="a29a0-128">no Ponteiro para a função [MAPIFreeBuffer](mapifreebuffer.md) , a ser usado para liberar memória.</span><span class="sxs-lookup"><span data-stu-id="a29a0-128">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="a29a0-129">_lpcOutbound_</span><span class="sxs-lookup"><span data-stu-id="a29a0-129">_lpcOutbound_</span></span>
  
> <span data-ttu-id="a29a0-130">bota Ponteiro para o número de mensagens na matriz apontadas pelo parâmetro _lpppMessage_ .</span><span class="sxs-lookup"><span data-stu-id="a29a0-130">[out] Pointer to the number of messages in the array pointed to by the  _lpppMessage_ parameter.</span></span> 
    
 <span data-ttu-id="a29a0-131">_lpppMessage_</span><span class="sxs-lookup"><span data-stu-id="a29a0-131">_lpppMessage_</span></span>
  
> <span data-ttu-id="a29a0-132">bota Ponteiro para um ponteiro para uma matriz de ponteiros para mensagens preprocessadas ou de outra forma geradas.</span><span class="sxs-lookup"><span data-stu-id="a29a0-132">[out] Pointer to a pointer to an array of pointers to preprocessed or otherwise generated messages.</span></span> 
    
 <span data-ttu-id="a29a0-133">_lppRecipList_</span><span class="sxs-lookup"><span data-stu-id="a29a0-133">_lppRecipList_</span></span>
  
> <span data-ttu-id="a29a0-134">bota Ponteiro para uma estrutura [das ADRLIST](adrlist.md) retornada opcional, listando destinatários detectados pelo pré-processador para o qual a mensagem não é entregue.</span><span class="sxs-lookup"><span data-stu-id="a29a0-134">[out] Pointer to an optional returned [ADRLIST](adrlist.md) structure, listing preprocessor-detected recipients for which the message is undeliverable.</span></span> <span data-ttu-id="a29a0-135">Para obter mais informações sobre o conteúdo dessa lista, consulte o método [IMAPISupport:: StatusRecips](imapisupport-statusrecips.md) .</span><span class="sxs-lookup"><span data-stu-id="a29a0-135">For more information about the contents of this list, see the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a29a0-136">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a29a0-136">Return value</span></span>

<span data-ttu-id="a29a0-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="a29a0-137">S_OK</span></span>
  
> <span data-ttu-id="a29a0-138">O conteúdo da mensagem foi preprocessada com êxito.</span><span class="sxs-lookup"><span data-stu-id="a29a0-138">Message contents were successfully preprocessed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a29a0-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="a29a0-139">Remarks</span></span>

<span data-ttu-id="a29a0-140">Um pré-processador de mensagem do provedor de transporte pode apresentar um indicador de progresso durante o pré-processamento da mensagem.</span><span class="sxs-lookup"><span data-stu-id="a29a0-140">A transport-provider message preprocessor can present a progress indicator during message preprocessing.</span></span> <span data-ttu-id="a29a0-141">No enTanto, ele nunca deve apresentar uma caixa de diálogo que exija interação do usuário durante o pré-processamento da mensagem.</span><span class="sxs-lookup"><span data-stu-id="a29a0-141">However, it should never present a dialog box requiring user interaction during message preprocessing.</span></span> 
  
<span data-ttu-id="a29a0-142">Quando um pré-processador adiciona grandes quantidades de dados a uma mensagem de saída, determinados procedimentos devem ser seguidos.</span><span class="sxs-lookup"><span data-stu-id="a29a0-142">When a preprocessor adds large amounts of data to an outbound message, certain procedures should be followed.</span></span> <span data-ttu-id="a29a0-143">Esse tipo de mensagem pode ser armazenado em um repositório de mensagens baseado em servidor, fazendo com que o pré-processador acesse um repositório remoto, um procedimento de consumo de tempo.</span><span class="sxs-lookup"><span data-stu-id="a29a0-143">This type of message can be stored in a server-based message store, causing the preprocessor to access a remote store, a time-consuming procedure.</span></span> <span data-ttu-id="a29a0-144">Para evitar ter que fazer isso, o pré-processador deve ter uma opção que permite que ele armazene dados que contenham uma grande quantidade de espaço em um repositório de mensagens local e forneça uma referência a esse repositório local na mensagem.</span><span class="sxs-lookup"><span data-stu-id="a29a0-144">To avoid having to do so, the preprocessor should have an option that enables it to store data that takes a large amount of space in a local message store and to provide a reference to that local store in the message.</span></span> 
  
<span data-ttu-id="a29a0-145">O pré-processador não deve liberar nenhum dos objetos passados originalmente para a função baseada em **PreprocessMessage** .</span><span class="sxs-lookup"><span data-stu-id="a29a0-145">The preprocessor should not release any of the objects originally passed to the **PreprocessMessage** based function.</span></span> 
  
<span data-ttu-id="a29a0-146">Antes que o spooler MAPI possa chamar uma função **PreprocessMessage** , o provedor de transporte deve ter registrado a função em uma chamada para o método [IMAPISupport:: RegisterPreprocessor](imapisupport-registerpreprocessor.md) .</span><span class="sxs-lookup"><span data-stu-id="a29a0-146">Before the MAPI spooler can call a **PreprocessMessage** function, the transport provider must have registered the function in a call to the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method.</span></span> <span data-ttu-id="a29a0-147">Depois de chamar uma função **PreprocessMessage** , o spooler não pode continuar enviando uma mensagem até que a função retorne.</span><span class="sxs-lookup"><span data-stu-id="a29a0-147">After calling a **PreprocessMessage** function, the spooler cannot continue submitting a message until the function returns.</span></span> 
  
<span data-ttu-id="a29a0-148">O spooler MAPI é proprietário da tarefa de envio de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a29a0-148">The MAPI spooler owns the task of submitting messages.</span></span> <span data-ttu-id="a29a0-149">Isso significa que a mensagem original nunca é colocada em uma matriz de ponteiros de mensagem e que uma chamada para os métodos **SubmitMessage** nunca é necessária.</span><span class="sxs-lookup"><span data-stu-id="a29a0-149">This means the original message is never placed in an array of message pointers and that a call to the **SubmitMessage** methods is never required.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a29a0-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="a29a0-150">See also</span></span>



[<span data-ttu-id="a29a0-151">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a29a0-151">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="a29a0-152">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="a29a0-152">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="a29a0-153">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a29a0-153">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

