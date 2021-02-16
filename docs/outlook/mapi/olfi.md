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
# <a name="olfi"></a><span data-ttu-id="d97df-103">OLFI</span><span class="sxs-lookup"><span data-stu-id="d97df-103">OLFI</span></span>

  
  
<span data-ttu-id="d97df-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d97df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d97df-105">Fila de estruturas de ID de longo prazo usadas pelo provedor de armazenamento do arquivo de Pastas Particulares (PST) para atribuir uma ID de entrada para uma nova mensagem ou pasta no modo offline.</span><span class="sxs-lookup"><span data-stu-id="d97df-105">Queue of long-term ID structures used by the Personal Folders file (PST) store provider to assign an Entry ID for a new message or folder in offline mode.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d97df-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="d97df-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="d97df-107">Membros</span><span class="sxs-lookup"><span data-stu-id="d97df-107">Members</span></span>

 <span data-ttu-id="d97df-108">_ulVersion_</span><span class="sxs-lookup"><span data-stu-id="d97df-108">_ulVersion_</span></span>
  
- <span data-ttu-id="d97df-109">Número da versão da estrutura.</span><span class="sxs-lookup"><span data-stu-id="d97df-109">Version number for the structure.</span></span> 
    
 <span data-ttu-id="d97df-110">_muidReserved_</span><span class="sxs-lookup"><span data-stu-id="d97df-110">_muidReserved_</span></span>
  
- <span data-ttu-id="d97df-111">Este membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="d97df-111">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="d97df-112">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="d97df-112">_ulReserved_</span></span>
  
- <span data-ttu-id="d97df-113">Este membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="d97df-113">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="d97df-114">_dwAlloc_</span><span class="sxs-lookup"><span data-stu-id="d97df-114">_dwAlloc_</span></span>
  
- <span data-ttu-id="d97df-115">O número de entradas disponíveis para alocação.</span><span class="sxs-lookup"><span data-stu-id="d97df-115">The number of entries that are available for allocation.</span></span> <span data-ttu-id="d97df-116">Essas entradas compartilham o mesmo identificador global exclusivo (GUID).</span><span class="sxs-lookup"><span data-stu-id="d97df-116">These entries share the same globally unique identifier (GUID).</span></span>
    
 <span data-ttu-id="d97df-117">_dwNextAlloc_</span><span class="sxs-lookup"><span data-stu-id="d97df-117">_dwNextAlloc_</span></span>
  
- <span data-ttu-id="d97df-118">O número de entradas disponíveis em seguida para alocação.</span><span class="sxs-lookup"><span data-stu-id="d97df-118">The number of entries that are available next for allocation.</span></span> <span data-ttu-id="d97df-119">Essas entradas compartilham o mesmo GUID.</span><span class="sxs-lookup"><span data-stu-id="d97df-119">These entries share the same GUID.</span></span>
    
 <span data-ttu-id="d97df-120">_ltidAlloc_</span><span class="sxs-lookup"><span data-stu-id="d97df-120">_ltidAlloc_</span></span>
  
- <span data-ttu-id="d97df-121">A estrutura de ID de longo prazo, **[LTID](ltid.md)**, identificando a entrada atualmente disponível para alocação.</span><span class="sxs-lookup"><span data-stu-id="d97df-121">The long-term ID structure, **[LTID](ltid.md)**, identifying the entry currently available for allocation.</span></span> <span data-ttu-id="d97df-122">A estrutura de ID de longo prazo contém um GUID e um índice que identifica um objeto no armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d97df-122">The long-term ID structure contains a GUID and an index identifying an object in the store.</span></span> <span data-ttu-id="d97df-123">Juntos, o GUID e o índice podem formar uma ID de entrada exclusiva para um objeto.</span><span class="sxs-lookup"><span data-stu-id="d97df-123">Together, the GUID and the index can form a unique Entry ID for an object.</span></span> 
    
 <span data-ttu-id="d97df-124">_ltidNextAlloc_</span><span class="sxs-lookup"><span data-stu-id="d97df-124">_ltidNextAlloc_</span></span>
  
- <span data-ttu-id="d97df-125">Estrutura de ID de longo prazo identificando a próxima entrada disponível.</span><span class="sxs-lookup"><span data-stu-id="d97df-125">Long-term ID structure identifying the next available entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d97df-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="d97df-126">Remarks</span></span>

<span data-ttu-id="d97df-127">Uma identificação de entrada é um identificador de entrada MAPI de 4 byte para uma pasta ou uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="d97df-127">An Entry ID is a 4-byte MAPI entry identifier for a folder or a message.</span></span> <span data-ttu-id="d97df-128">Para obter mais informações, consulte [ENTRYID](https://msdn.microsoft.com/library/ms836424).</span><span class="sxs-lookup"><span data-stu-id="d97df-128">For more information, see [ENTRYID](https://msdn.microsoft.com/library/ms836424).</span></span>
  
<span data-ttu-id="d97df-129">Quando um provedor de armazenamento PST atribui uma identificação de entrada a um novo objeto, ele primeiro precisa de um GUID que identifica o servidor e um índice que identifica o objeto no armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d97df-129">When a PST store provider assigns an Entry ID to a new object, it first needs a GUID that identifies the server, and an index that identifies the object in the store.</span></span> <span data-ttu-id="d97df-130">Embora o GUID não seja exclusivo em todas as IDs de entrada, o GUID e o índice combinados fornecem uma entrada exclusiva.</span><span class="sxs-lookup"><span data-stu-id="d97df-130">Even though the GUID is not unique across all Entry IDs, the GUID and the index combined provide a unique entry.</span></span> <span data-ttu-id="d97df-131">Esse GUID e par de índices são acompanhados por uma estrutura de ID de longo prazo, **LTID**, que faz parte da **estrutura OLFI.**</span><span class="sxs-lookup"><span data-stu-id="d97df-131">This GUID and index pair is tracked by a long-term ID structure, **LTID**, which is part of the **OLFI** structure.</span></span> 
  
<span data-ttu-id="d97df-132">O provedor de armazenamento PST não mantém fisicamente em **OLFI** uma estrutura **LTID** para cada par guid-índice.</span><span class="sxs-lookup"><span data-stu-id="d97df-132">The PST store provider does not physically keep in **OLFI** an **LTID** structure for each GUID-index pair.</span></span> <span data-ttu-id="d97df-133">Ele mantém uma **estrutura LTID,**  *ltidAlloc*  , para o primeiro par de guid-índice disponível no momento; uma contagem,  *dwAlloc*  , do número de entradas disponíveis que compartilham esse mesmo GUID; e uma segunda **estrutura LTID,**  *ltidNextAlloc*  , para o próximo par de índice GUID disponível que tem um GUID diferente.</span><span class="sxs-lookup"><span data-stu-id="d97df-133">It keeps one **LTID** structure,  *ltidAlloc*  , for the currently first available GUID-index pair; a count,  *dwAlloc*  , of the number of available entries that share this same GUID; and a second **LTID** structure,  *ltidNextAlloc*  , for the next available GUID-index pair that has a different GUID.</span></span> <span data-ttu-id="d97df-134">O provedor de armazenamento PST usa a estrutura **OLFI** para controlar os GUIDs e índices que ele distribuiu. Em um nível virtual, o provedor mantém uma reserva de várias estruturas **LTID** que estão prontas para serem alocadas.</span><span class="sxs-lookup"><span data-stu-id="d97df-134">The PST store provider uses the **OLFI** structure to track the GUIDs and indexes that it has handed out. At a virtual level, the provider maintains a reserve of a number of **LTID** structures that are ready to be allocated.</span></span>  <span data-ttu-id="d97df-135">*dwAlloc*  mantém uma contagem das estruturas **LTID** disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d97df-135">*dwAlloc*  maintains a count of the available **LTID** structures.</span></span> 
  
<span data-ttu-id="d97df-136">As solicitações de IDs de entrada vêm em blocos.</span><span class="sxs-lookup"><span data-stu-id="d97df-136">Requests for Entry IDs come in blocks.</span></span> <span data-ttu-id="d97df-137">Quando há uma solicitação de bloqueio, o provedor de armazenamento PST verifica se há reserva suficiente disponível comparando o tamanho solicitado com  *dwAlloc*  .</span><span class="sxs-lookup"><span data-stu-id="d97df-137">When there is a request for a block, the PST store provider checks if there is sufficient reserve on hand by comparing the requested size with  *dwAlloc*  .</span></span> <span data-ttu-id="d97df-138">Se houver reserva suficiente, ele retornará o GUID e o índice em  *ltidAlloc*  para alocação.</span><span class="sxs-lookup"><span data-stu-id="d97df-138">If there is sufficient reserve, it returns the GUID and index in  *ltidAlloc*  for allocation.</span></span> <span data-ttu-id="d97df-139">Em seguida, diminui  *dwAlloc*  pelo tamanho solicitado e incrementa o índice em  *ltidAlloc*  pelo tamanho solicitado.</span><span class="sxs-lookup"><span data-stu-id="d97df-139">It then decreases  *dwAlloc*  by the requested size, and increments the index in  *ltidAlloc*  by the requested size.</span></span> <span data-ttu-id="d97df-140">Isso prepara o provedor de armazenamento PST para alocar  *ltidAlloc*  na próxima solicitação para outro bloco de IDs de entrada.</span><span class="sxs-lookup"><span data-stu-id="d97df-140">This prepares the PST store provider to allocate  *ltidAlloc*  on the next request for another block of Entry IDs.</span></span> <span data-ttu-id="d97df-141">Observe que o GUID permanece o mesmo para a próxima solicitação.</span><span class="sxs-lookup"><span data-stu-id="d97df-141">Note that the GUID remains the same for the next request.</span></span> 
  
<span data-ttu-id="d97df-142">Se o tamanho de uma solicitação for maior que  *dwAlloc*  , o provedor de armazenamento PST tenta usar o que tem em seguida na reserva, conforme especificado por  *dwNextAlloc*  e  *ltidNextAlloc*  .</span><span class="sxs-lookup"><span data-stu-id="d97df-142">If the size of a request is larger than  *dwAlloc*  , the PST store provider tries to use what it has next in reserve, as specified by  *dwNextAlloc*  and  *ltidNextAlloc*  .</span></span> <span data-ttu-id="d97df-143">Ela copia  *dwNextAlloc*  e  *ltidNextAlloc*  *para dwAlloc*  e  *ltidAlloc,*  respectivamente, e define  *dwNextAlloc*  e  *ltidNextAlloc*  como NULL.</span><span class="sxs-lookup"><span data-stu-id="d97df-143">It copies  *dwNextAlloc*  and  *ltidNextAlloc*  to  *dwAlloc*  and  *ltidAlloc*  respectively, and sets  *dwNextAlloc*  and  *ltidNextAlloc*  to NULL.</span></span> 
  
<span data-ttu-id="d97df-144">Um provedor que envolve o provedor de armazenamento PST deve verificar  *periodicamente ltidNextAlloc*  para ver se ele é NULL.</span><span class="sxs-lookup"><span data-stu-id="d97df-144">A provider that wraps the PST store provider should periodically check  *ltidNextAlloc*  to see if it is NULL.</span></span> <span data-ttu-id="d97df-145">Se estiver, o provedor deve preencher com um novo GUID e redefinir  *dwNextAlloc*  para que mais IDs de entrada possam ser alocadas.</span><span class="sxs-lookup"><span data-stu-id="d97df-145">If it is, the provider should populate it with a new GUID and reset  *dwNextAlloc*  so that more entry IDs can be allocated.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d97df-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="d97df-146">See also</span></span>



[<span data-ttu-id="d97df-147">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="d97df-147">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="d97df-148">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="d97df-148">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="d97df-149">LTID</span><span class="sxs-lookup"><span data-stu-id="d97df-149">LTID</span></span>](ltid.md)

