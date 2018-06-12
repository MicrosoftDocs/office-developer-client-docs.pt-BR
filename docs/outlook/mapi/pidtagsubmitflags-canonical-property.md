---
title: Propriedade canônico de PidTagSubmitFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubmitFlags
api_type:
- COM
ms.assetid: 9ea1c029-d53c-4c28-b413-560083b6215a
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 444d98c4e8e32e0cc7d2eb8af753a394af1f020c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770107"
---
# <a name="pidtagsubmitflags-canonical-property"></a><span data-ttu-id="e4539-103">Propriedade canônico de PidTagSubmitFlags</span><span class="sxs-lookup"><span data-stu-id="e4539-103">PidTagSubmitFlags Canonical Property</span></span>

  
  
<span data-ttu-id="e4539-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e4539-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e4539-105">Contém uma bitmask dos sinalizadores indicando detalhes sobre o envio de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="e4539-105">Contains a bitmask of flags indicating details about a message submission.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e4539-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="e4539-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e4539-107">PR_SUBMIT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="e4539-107">PR_SUBMIT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="e4539-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e4539-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e4539-109">0x0E14</span><span class="sxs-lookup"><span data-stu-id="e4539-109">0x0E14</span></span>  <br/> |
|<span data-ttu-id="e4539-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="e4539-110">Data type:</span></span>  <br/> |<span data-ttu-id="e4539-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e4539-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e4539-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e4539-112">Area:</span></span>  <br/> |<span data-ttu-id="e4539-113">MAPI não transmittable</span><span class="sxs-lookup"><span data-stu-id="e4539-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e4539-114">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="e4539-114">Remarks</span></span>

<span data-ttu-id="e4539-115">Um ou mais dos seguintes sinalizadores podem ser definidas para o bitmask **PR_SUBMIT_FLAGS** :</span><span class="sxs-lookup"><span data-stu-id="e4539-115">One or more of the following flags can be set for the **PR_SUBMIT_FLAGS** bitmask:</span></span> 
  
<span data-ttu-id="e4539-116">SUBMITFLAG_LOCKED</span><span class="sxs-lookup"><span data-stu-id="e4539-116">SUBMITFLAG_LOCKED</span></span> 
  
> <span data-ttu-id="e4539-117">O MAPI spooler atualmente tem a mensagem protegida.</span><span class="sxs-lookup"><span data-stu-id="e4539-117">The MAPI spooler currently has the message locked.</span></span> 
    
<span data-ttu-id="e4539-118">SUBMITFLAG_PREPROCESS</span><span class="sxs-lookup"><span data-stu-id="e4539-118">SUBMITFLAG_PREPROCESS</span></span> 
  
> <span data-ttu-id="e4539-119">A mensagem precisa pré-processamento.</span><span class="sxs-lookup"><span data-stu-id="e4539-119">The message needs preprocessing.</span></span> <span data-ttu-id="e4539-120">Quando terminar do MAPI spooler pré-processamento essa mensagem, ele deve chamar o método [IMessage::SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="e4539-120">When the MAPI spooler is done preprocessing this message, it should call the [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="e4539-121">O provedor de armazenamento de mensagem reconhece que o spooler, em vez do aplicativo cliente, tenha chamado **SubmitMessage**, limpa o sinalizador e continua o envio de mensagem.</span><span class="sxs-lookup"><span data-stu-id="e4539-121">The message store provider recognizes that the spooler, rather than the client application, has called **SubmitMessage**, clears the flag, and continues message submission.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="e4539-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e4539-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e4539-123">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="e4539-123">Protocol specifications</span></span>

<span data-ttu-id="e4539-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e4539-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e4539-125">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e4539-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e4539-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e4539-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e4539-127">Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.</span><span class="sxs-lookup"><span data-stu-id="e4539-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e4539-128">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e4539-128">Header files</span></span>

<span data-ttu-id="e4539-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e4539-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="e4539-130">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e4539-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="e4539-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e4539-131">Mapitags.h</span></span>
  
> <span data-ttu-id="e4539-132">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="e4539-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e4539-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4539-133">See also</span></span>



[<span data-ttu-id="e4539-134">IMsgStore::SetLockState</span><span class="sxs-lookup"><span data-stu-id="e4539-134">IMsgStore::SetLockState</span></span>](imsgstore-setlockstate.md)


[<span data-ttu-id="e4539-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e4539-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e4539-136">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="e4539-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e4539-137">Mapear nomes de propriedade canônico para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="e4539-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e4539-138">Mapear nomes de MAPI para nomes de propriedade canônico</span><span class="sxs-lookup"><span data-stu-id="e4539-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

