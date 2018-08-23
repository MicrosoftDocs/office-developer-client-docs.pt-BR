---
title: OLFI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 44bfaadf-36f9-bd8e-6158-646533f6849e
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 7d01f07b5eb5ca34b4bd825b62b7d1520b853d6b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564259"
---
# <a name="olfi"></a><span data-ttu-id="3c57e-103">OLFI</span><span class="sxs-lookup"><span data-stu-id="3c57e-103">OLFI</span></span>

  
  
<span data-ttu-id="3c57e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c57e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c57e-105">Fila de longo prazo estruturas de ID usado pelo provedor de repositório de pastas particulares (. PST) do arquivo para atribuir uma ID de entrada para uma nova mensagem ou a pasta no modo offline.</span><span class="sxs-lookup"><span data-stu-id="3c57e-105">Queue of long-term ID structures used by the Personal Folders file (PST) store provider to assign an Entry ID for a new message or folder in offline mode.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="3c57e-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="3c57e-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG    ulVersion; 
    MAPIUID  muidReserved; 
    ULONG    ulReserved; 
    DWORD    dwAlloc; 
    DWORD    dwNextAlloc; 
    LTID     ltidAlloc; 
    LTID     ltidNextAlloc; 
} OLFI, *POLFI;
```

## <a name="members"></a><span data-ttu-id="3c57e-107">Members</span><span class="sxs-lookup"><span data-stu-id="3c57e-107">Members</span></span>

 <span data-ttu-id="3c57e-108">_ulVersion_</span><span class="sxs-lookup"><span data-stu-id="3c57e-108">_ulVersion_</span></span>
  
- <span data-ttu-id="3c57e-109">Número de versão para a estrutura.</span><span class="sxs-lookup"><span data-stu-id="3c57e-109">Version number for the structure.</span></span> 
    
 <span data-ttu-id="3c57e-110">_muidReserved_</span><span class="sxs-lookup"><span data-stu-id="3c57e-110">_muidReserved_</span></span>
  
- <span data-ttu-id="3c57e-111">Este membro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="3c57e-111">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="3c57e-112">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="3c57e-112">_ulReserved_</span></span>
  
- <span data-ttu-id="3c57e-113">Este membro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="3c57e-113">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="3c57e-114">_dwAlloc_</span><span class="sxs-lookup"><span data-stu-id="3c57e-114">_dwAlloc_</span></span>
  
- <span data-ttu-id="3c57e-115">O número de entradas que estão disponíveis para alocação.</span><span class="sxs-lookup"><span data-stu-id="3c57e-115">The number of entries that are available for allocation.</span></span> <span data-ttu-id="3c57e-116">Essas entradas compartilham o mesmo identificador globalmente exclusivo (GUID).</span><span class="sxs-lookup"><span data-stu-id="3c57e-116">These entries share the same globally unique identifier (GUID).</span></span>
    
 <span data-ttu-id="3c57e-117">_dwNextAlloc_</span><span class="sxs-lookup"><span data-stu-id="3c57e-117">_dwNextAlloc_</span></span>
  
- <span data-ttu-id="3c57e-118">O número de entradas que estão disponíveis em seguida para alocação.</span><span class="sxs-lookup"><span data-stu-id="3c57e-118">The number of entries that are available next for allocation.</span></span> <span data-ttu-id="3c57e-119">Essas entradas compartilham o mesmo GUID.</span><span class="sxs-lookup"><span data-stu-id="3c57e-119">These entries share the same GUID.</span></span>
    
 <span data-ttu-id="3c57e-120">_ltidAlloc_</span><span class="sxs-lookup"><span data-stu-id="3c57e-120">_ltidAlloc_</span></span>
  
- <span data-ttu-id="3c57e-121">A longo prazo ID estrutura, **[LTID](ltid.md)**, que identifica a entrada atualmente disponível para alocação.</span><span class="sxs-lookup"><span data-stu-id="3c57e-121">The long-term ID structure, **[LTID](ltid.md)**, identifying the entry currently available for allocation.</span></span> <span data-ttu-id="3c57e-122">A estrutura de ID de longo prazo contém um GUID e um índice identificando um objeto no repositório.</span><span class="sxs-lookup"><span data-stu-id="3c57e-122">The long-term ID structure contains a GUID and an index identifying an object in the store.</span></span> <span data-ttu-id="3c57e-123">Juntos, o GUID e o índice podem formar uma ID exclusiva de entrada para um objeto.</span><span class="sxs-lookup"><span data-stu-id="3c57e-123">Together, the GUID and the index can form a unique Entry ID for an object.</span></span> 
    
 <span data-ttu-id="3c57e-124">_ltidNextAlloc_</span><span class="sxs-lookup"><span data-stu-id="3c57e-124">_ltidNextAlloc_</span></span>
  
- <span data-ttu-id="3c57e-125">Estrutura de ID longo prazo identificando a próxima entrada disponível.</span><span class="sxs-lookup"><span data-stu-id="3c57e-125">Long-term ID structure identifying the next available entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3c57e-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c57e-126">Remarks</span></span>

<span data-ttu-id="3c57e-127">Uma identificação de entrada é um identificador de entrada MAPI de 4 bytes para uma pasta ou uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="3c57e-127">An Entry ID is a 4-byte MAPI entry identifier for a folder or a message.</span></span> <span data-ttu-id="3c57e-128">Para obter mais informações, consulte [ENTRYID](http://msdn.microsoft.com/en-us/library/ms836424).</span><span class="sxs-lookup"><span data-stu-id="3c57e-128">For more information, see [ENTRYID](http://msdn.microsoft.com/en-us/library/ms836424).</span></span>
  
<span data-ttu-id="3c57e-129">Quando um provedor de armazenamento de PST atribui uma identificação de entrada para um novo objeto, ele primeiro precisa um GUID que identifica o servidor e um índice que identifica o objeto no repositório.</span><span class="sxs-lookup"><span data-stu-id="3c57e-129">When a PST store provider assigns an Entry ID to a new object, it first needs a GUID that identifies the server, and an index that identifies the object in the store.</span></span> <span data-ttu-id="3c57e-130">Embora não seja o GUID exclusivo entre todas as identificações de entrada, o GUID e o índice combinados fornecem uma entrada única.</span><span class="sxs-lookup"><span data-stu-id="3c57e-130">Even though the GUID is not unique across all Entry IDs, the GUID and the index combined provide a unique entry.</span></span> <span data-ttu-id="3c57e-131">Esse par GUID e o índice é controlado por uma longo prazo estrutura de ID, **LTID**, que é parte da estrutura de **OLFI** .</span><span class="sxs-lookup"><span data-stu-id="3c57e-131">This GUID and index pair is tracked by a long-term ID structure, **LTID**, which is part of the **OLFI** structure.</span></span> 
  
<span data-ttu-id="3c57e-132">O provedor de repositórios de PST não fisicamente lembre **OLFI** uma estrutura **LTID** para cada par de índice de GUID.</span><span class="sxs-lookup"><span data-stu-id="3c57e-132">The PST store provider does not physically keep in **OLFI** an **LTID** structure for each GUID-index pair.</span></span> <span data-ttu-id="3c57e-133">Ele mantém uma estrutura **LTID** , *ltidAlloc* , para o par de índice do GUID disponível atualmente primeiro; uma contagem, *dwAlloc* , do número de entradas disponíveis que compartilham esse mesmo GUID; e uma estrutura **LTID** segunda, *ltidNextAlloc* , para o próximo par de índice do GUID disponível que tenha um GUID diferente.</span><span class="sxs-lookup"><span data-stu-id="3c57e-133">It keeps one **LTID** structure,  *ltidAlloc*  , for the currently first available GUID-index pair; a count,  *dwAlloc*  , of the number of available entries that share this same GUID; and a second **LTID** structure,  *ltidNextAlloc*  , for the next available GUID-index pair that has a different GUID.</span></span> <span data-ttu-id="3c57e-134">O PST armazenar provedor usa a estrutura **OLFI** para controlar os GUIDs e índices que ele tem atribuídas. Em um nível virtual, o provedor mantém uma reserva de um número de estruturas **LTID** que estão prontos para ser alocado.</span><span class="sxs-lookup"><span data-stu-id="3c57e-134">The PST store provider uses the **OLFI** structure to track the GUIDs and indexes that it has handed out. At a virtual level, the provider maintains a reserve of a number of **LTID** structures that are ready to be allocated.</span></span>  <span data-ttu-id="3c57e-135">*dwAlloc* mantém uma contagem das estruturas **LTID** disponíveis.</span><span class="sxs-lookup"><span data-stu-id="3c57e-135">*dwAlloc*  maintains a count of the available **LTID** structures.</span></span> 
  
<span data-ttu-id="3c57e-136">Solicitações de identificações de entrada vêm em blocos.</span><span class="sxs-lookup"><span data-stu-id="3c57e-136">Requests for Entry IDs come in blocks.</span></span> <span data-ttu-id="3c57e-137">Quando há uma solicitação para um bloco, o provedor de repositórios de PST verifica se há reserva suficiente disponível, comparando o tamanho solicitado com *dwAlloc* .</span><span class="sxs-lookup"><span data-stu-id="3c57e-137">When there is a request for a block, the PST store provider checks if there is sufficient reserve on hand by comparing the requested size with  *dwAlloc*  .</span></span> <span data-ttu-id="3c57e-138">Se houver reserva suficiente, ele retorna o GUID e o índice *ltidAlloc* para alocação.</span><span class="sxs-lookup"><span data-stu-id="3c57e-138">If there is sufficient reserve, it returns the GUID and index in  *ltidAlloc*  for allocation.</span></span> <span data-ttu-id="3c57e-139">Ela diminui *dwAlloc* pelo tamanho solicitado e incrementa o índice em *ltidAlloc* pelo tamanho solicitado.</span><span class="sxs-lookup"><span data-stu-id="3c57e-139">It then decreases  *dwAlloc*  by the requested size, and increments the index in  *ltidAlloc*  by the requested size.</span></span> <span data-ttu-id="3c57e-140">Prepara o provedor de repositórios de PST alocar *ltidAlloc* na próxima solicitação para outro bloco de identificações de entrada.</span><span class="sxs-lookup"><span data-stu-id="3c57e-140">This prepares the PST store provider to allocate  *ltidAlloc*  on the next request for another block of Entry IDs.</span></span> <span data-ttu-id="3c57e-141">Observe que o GUID permanece o mesmo para a próxima solicitação.</span><span class="sxs-lookup"><span data-stu-id="3c57e-141">Note that the GUID remains the same for the next request.</span></span> 
  
<span data-ttu-id="3c57e-142">Se o tamanho de uma solicitação for maior que *dwAlloc* , o provedor de repositórios de PST tenta usar o que ele tem Avançar na reserva, conforme especificado por *dwNextAlloc* e *ltidNextAlloc* .</span><span class="sxs-lookup"><span data-stu-id="3c57e-142">If the size of a request is larger than  *dwAlloc*  , the PST store provider tries to use what it has next in reserve, as specified by  *dwNextAlloc*  and  *ltidNextAlloc*  .</span></span> <span data-ttu-id="3c57e-143">Ela copia *dwNextAlloc* e *ltidNextAlloc* *dwAlloc* e *ltidAlloc* , respectivamente e define *dwNextAlloc* e *ltidNextAlloc* como NULL.</span><span class="sxs-lookup"><span data-stu-id="3c57e-143">It copies  *dwNextAlloc*  and  *ltidNextAlloc*  to  *dwAlloc*  and  *ltidAlloc*  respectively, and sets  *dwNextAlloc*  and  *ltidNextAlloc*  to NULL.</span></span> 
  
<span data-ttu-id="3c57e-144">Um provedor que envolve o provedor de repositório PST deve verificar periodicamente *ltidNextAlloc* para ver se ele é NULL.</span><span class="sxs-lookup"><span data-stu-id="3c57e-144">A provider that wraps the PST store provider should periodically check  *ltidNextAlloc*  to see if it is NULL.</span></span> <span data-ttu-id="3c57e-145">Se estiver, o provedor deve preenchê-lo com um novo GUID e redefinir *dwNextAlloc* , de modo que as IDs de entradas mais podem ser alocada.</span><span class="sxs-lookup"><span data-stu-id="3c57e-145">If it is, the provider should populate it with a new GUID and reset  *dwNextAlloc*  so that more entry IDs can be allocated.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3c57e-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="3c57e-146">See also</span></span>



[<span data-ttu-id="3c57e-147">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="3c57e-147">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="3c57e-148">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="3c57e-148">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="3c57e-149">LTID</span><span class="sxs-lookup"><span data-stu-id="3c57e-149">LTID</span></span>](ltid.md)

