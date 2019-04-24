---
title: OLFI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 44bfaadf-36f9-bd8e-6158-646533f6849e
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 027905721b5730b4c3d78f496022b88a8e6b84d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279750"
---
# <a name="olfi"></a><span data-ttu-id="8ea28-103">OLFI</span><span class="sxs-lookup"><span data-stu-id="8ea28-103">OLFI</span></span>

  
  
<span data-ttu-id="8ea28-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ea28-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ea28-105">Fila de estruturas de ID de longo prazo usadas pelo provedor de repositório de arquivos de pastas particulares (PST) para atribuir uma ID de entrada para uma nova mensagem ou pasta no modo offline.</span><span class="sxs-lookup"><span data-stu-id="8ea28-105">Queue of long-term ID structures used by the Personal Folders file (PST) store provider to assign an Entry ID for a new message or folder in offline mode.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8ea28-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="8ea28-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="8ea28-107">Membros</span><span class="sxs-lookup"><span data-stu-id="8ea28-107">Members</span></span>

 <span data-ttu-id="8ea28-108">_ulVersion_</span><span class="sxs-lookup"><span data-stu-id="8ea28-108">_ulVersion_</span></span>
  
- <span data-ttu-id="8ea28-109">Número de versão da estrutura.</span><span class="sxs-lookup"><span data-stu-id="8ea28-109">Version number for the structure.</span></span> 
    
 <span data-ttu-id="8ea28-110">_muidReserved_</span><span class="sxs-lookup"><span data-stu-id="8ea28-110">_muidReserved_</span></span>
  
- <span data-ttu-id="8ea28-111">Este membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="8ea28-111">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="8ea28-112">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="8ea28-112">_ulReserved_</span></span>
  
- <span data-ttu-id="8ea28-113">Este membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="8ea28-113">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="8ea28-114">_dwAlloc_</span><span class="sxs-lookup"><span data-stu-id="8ea28-114">_dwAlloc_</span></span>
  
- <span data-ttu-id="8ea28-115">O número de entradas disponíveis para alocação.</span><span class="sxs-lookup"><span data-stu-id="8ea28-115">The number of entries that are available for allocation.</span></span> <span data-ttu-id="8ea28-116">Essas entradas compartilham o mesmo identificador global exclusivo (GUID).</span><span class="sxs-lookup"><span data-stu-id="8ea28-116">These entries share the same globally unique identifier (GUID).</span></span>
    
 <span data-ttu-id="8ea28-117">_dwNextAlloc_</span><span class="sxs-lookup"><span data-stu-id="8ea28-117">_dwNextAlloc_</span></span>
  
- <span data-ttu-id="8ea28-118">O número de entradas disponíveis ao lado da alocação.</span><span class="sxs-lookup"><span data-stu-id="8ea28-118">The number of entries that are available next for allocation.</span></span> <span data-ttu-id="8ea28-119">Essas entradas compartilham o mesmo GUID.</span><span class="sxs-lookup"><span data-stu-id="8ea28-119">These entries share the same GUID.</span></span>
    
 <span data-ttu-id="8ea28-120">_ltidAlloc_</span><span class="sxs-lookup"><span data-stu-id="8ea28-120">_ltidAlloc_</span></span>
  
- <span data-ttu-id="8ea28-121">A estrutura de ID de longo prazo, **[ltid](ltid.md)**, identificando a entrada atualmente disponível para alocação.</span><span class="sxs-lookup"><span data-stu-id="8ea28-121">The long-term ID structure, **[LTID](ltid.md)**, identifying the entry currently available for allocation.</span></span> <span data-ttu-id="8ea28-122">A estrutura de ID de longo prazo contém um GUID e um índice que identifica um objeto no repositório.</span><span class="sxs-lookup"><span data-stu-id="8ea28-122">The long-term ID structure contains a GUID and an index identifying an object in the store.</span></span> <span data-ttu-id="8ea28-123">Juntos, o GUID e o índice podem formar uma ID de entrada exclusiva para um objeto.</span><span class="sxs-lookup"><span data-stu-id="8ea28-123">Together, the GUID and the index can form a unique Entry ID for an object.</span></span> 
    
 <span data-ttu-id="8ea28-124">_ltidNextAlloc_</span><span class="sxs-lookup"><span data-stu-id="8ea28-124">_ltidNextAlloc_</span></span>
  
- <span data-ttu-id="8ea28-125">Estrutura de ID de longo prazo identificando a próxima entrada disponível.</span><span class="sxs-lookup"><span data-stu-id="8ea28-125">Long-term ID structure identifying the next available entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8ea28-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="8ea28-126">Remarks</span></span>

<span data-ttu-id="8ea28-127">Uma ID de entrada é um identificador de entrada MAPI de 4 bytes para uma pasta ou uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="8ea28-127">An Entry ID is a 4-byte MAPI entry identifier for a folder or a message.</span></span> <span data-ttu-id="8ea28-128">Para obter mais informações, [](https://msdn.microsoft.com/library/ms836424)consulte EntryID.</span><span class="sxs-lookup"><span data-stu-id="8ea28-128">For more information, see [ENTRYID](https://msdn.microsoft.com/library/ms836424).</span></span>
  
<span data-ttu-id="8ea28-129">Quando um provedor de repositório PST atribui uma ID de entrada a um novo objeto, ele primeiro precisa de um GUID que identifique o servidor e um índice que identifique o objeto no repositório.</span><span class="sxs-lookup"><span data-stu-id="8ea28-129">When a PST store provider assigns an Entry ID to a new object, it first needs a GUID that identifies the server, and an index that identifies the object in the store.</span></span> <span data-ttu-id="8ea28-130">Mesmo que o GUID não seja exclusivo em todas as IDs de entrada, o GUID e o índice combinados fornecem uma entrada exclusiva.</span><span class="sxs-lookup"><span data-stu-id="8ea28-130">Even though the GUID is not unique across all Entry IDs, the GUID and the index combined provide a unique entry.</span></span> <span data-ttu-id="8ea28-131">Este par de GUIDs e de índice é rastreado por uma estrutura de ID de longo prazo, **ltid**, que é parte da estrutura **OLFI** .</span><span class="sxs-lookup"><span data-stu-id="8ea28-131">This GUID and index pair is tracked by a long-term ID structure, **LTID**, which is part of the **OLFI** structure.</span></span> 
  
<span data-ttu-id="8ea28-132">O provedor de repositório PST não mantém fisicamente no **OLFI** uma estrutura **ltid** para cada par GUID-index.</span><span class="sxs-lookup"><span data-stu-id="8ea28-132">The PST store provider does not physically keep in **OLFI** an **LTID** structure for each GUID-index pair.</span></span> <span data-ttu-id="8ea28-133">Ele mantém uma estrutura **ltid** , *ltidAlloc* , para o primeiro par de índice GUID disponível no momento; uma contagem, *dwAlloc* , do número de entradas disponíveis que compartilham esse mesmo GUID; e uma segunda estrutura **ltid** , *ltidNextAlloc* , para o próximo par de índice GUID disponível que tem um GUID diferente.</span><span class="sxs-lookup"><span data-stu-id="8ea28-133">It keeps one **LTID** structure,  *ltidAlloc*  , for the currently first available GUID-index pair; a count,  *dwAlloc*  , of the number of available entries that share this same GUID; and a second **LTID** structure,  *ltidNextAlloc*  , for the next available GUID-index pair that has a different GUID.</span></span> <span data-ttu-id="8ea28-134">O provedor de repositório PST usa a estrutura **OLFI** para controlar os GUIDs e índices que ele colocou. Em um nível virtual, o provedor mantém uma reserva de várias estruturas do **ltid** que estão prontas para serem alocadas.</span><span class="sxs-lookup"><span data-stu-id="8ea28-134">The PST store provider uses the **OLFI** structure to track the GUIDs and indexes that it has handed out. At a virtual level, the provider maintains a reserve of a number of **LTID** structures that are ready to be allocated.</span></span>  <span data-ttu-id="8ea28-135">*dwAlloc* mantém uma contagem das estruturas **ltid** disponíveis.</span><span class="sxs-lookup"><span data-stu-id="8ea28-135">*dwAlloc*  maintains a count of the available **LTID** structures.</span></span> 
  
<span data-ttu-id="8ea28-136">As solicitações de IDs de entrada são incluídas em blocos.</span><span class="sxs-lookup"><span data-stu-id="8ea28-136">Requests for Entry IDs come in blocks.</span></span> <span data-ttu-id="8ea28-137">Quando houver uma solicitação para um bloco, o provedor do repositório PST verificará se há reserva suficiente à mão comparando o tamanho solicitado com *dwAlloc* .</span><span class="sxs-lookup"><span data-stu-id="8ea28-137">When there is a request for a block, the PST store provider checks if there is sufficient reserve on hand by comparing the requested size with  *dwAlloc*  .</span></span> <span data-ttu-id="8ea28-138">Se houver uma reserva suficiente, ela retornará o GUID e o índice em *ltidAlloc* para alocação.</span><span class="sxs-lookup"><span data-stu-id="8ea28-138">If there is sufficient reserve, it returns the GUID and index in  *ltidAlloc*  for allocation.</span></span> <span data-ttu-id="8ea28-139">Em seguida, ele diminui *dwAlloc* pelo tamanho solicitado e incrementa o índice em *ltidAlloc* pelo tamanho solicitado.</span><span class="sxs-lookup"><span data-stu-id="8ea28-139">It then decreases  *dwAlloc*  by the requested size, and increments the index in  *ltidAlloc*  by the requested size.</span></span> <span data-ttu-id="8ea28-140">Isso prepara o provedor do repositório PST para alocar *ltidAlloc* na próxima solicitação para outro bloco de IDs de entrada.</span><span class="sxs-lookup"><span data-stu-id="8ea28-140">This prepares the PST store provider to allocate  *ltidAlloc*  on the next request for another block of Entry IDs.</span></span> <span data-ttu-id="8ea28-141">Observe que o GUID permanece o mesmo para a próxima solicitação.</span><span class="sxs-lookup"><span data-stu-id="8ea28-141">Note that the GUID remains the same for the next request.</span></span> 
  
<span data-ttu-id="8ea28-142">Se o tamanho de uma solicitação for maior do que *dwAlloc* , o provedor do repositório PST tentará usar o próximo na reserva, conforme especificado por *dwNextAlloc* e *ltidNextAlloc* .</span><span class="sxs-lookup"><span data-stu-id="8ea28-142">If the size of a request is larger than  *dwAlloc*  , the PST store provider tries to use what it has next in reserve, as specified by  *dwNextAlloc*  and  *ltidNextAlloc*  .</span></span> <span data-ttu-id="8ea28-143">Ele copia *dwNextAlloc* e *LtidNextAlloc* para o *dwAlloc* e o *ltidAlloc* respectivamente e define *dwNextAlloc* e *ltidNextAlloc* como nulo.</span><span class="sxs-lookup"><span data-stu-id="8ea28-143">It copies  *dwNextAlloc*  and  *ltidNextAlloc*  to  *dwAlloc*  and  *ltidAlloc*  respectively, and sets  *dwNextAlloc*  and  *ltidNextAlloc*  to NULL.</span></span> 
  
<span data-ttu-id="8ea28-144">Um provedor que encapsula o provedor de repositório PST deve verificar periodicamente o *ltidNextAlloc* para ver se ele é nulo.</span><span class="sxs-lookup"><span data-stu-id="8ea28-144">A provider that wraps the PST store provider should periodically check  *ltidNextAlloc*  to see if it is NULL.</span></span> <span data-ttu-id="8ea28-145">Se for, o provedor deverá preenchê-lo com um novo GUID e redefinir *dwNextAlloc* para que mais IDs de entrada possam ser alocadas.</span><span class="sxs-lookup"><span data-stu-id="8ea28-145">If it is, the provider should populate it with a new GUID and reset  *dwNextAlloc*  so that more entry IDs can be allocated.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8ea28-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="8ea28-146">See also</span></span>



[<span data-ttu-id="8ea28-147">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="8ea28-147">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="8ea28-148">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="8ea28-148">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="8ea28-149">LTID</span><span class="sxs-lookup"><span data-stu-id="8ea28-149">LTID</span></span>](ltid.md)

