---
title: Propriedade canônica PidTagSubmitFlags
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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 444d98c4e8e32e0cc7d2eb8af753a394af1f020c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770107"
---
# <a name="pidtagsubmitflags-canonical-property"></a><span data-ttu-id="f1ebf-103">Propriedade canônica PidTagSubmitFlags</span><span class="sxs-lookup"><span data-stu-id="f1ebf-103">PidTagSubmitFlags Canonical Property</span></span>

  
  
<span data-ttu-id="f1ebf-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f1ebf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f1ebf-105">Contém uma bitmask dos sinalizadores indicando detalhes sobre o envio de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="f1ebf-105">Contains a bitmask of flags indicating details about a message submission.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f1ebf-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="f1ebf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f1ebf-107">PR_SUBMIT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="f1ebf-107">PR_SUBMIT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="f1ebf-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f1ebf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f1ebf-109">0x0E14</span><span class="sxs-lookup"><span data-stu-id="f1ebf-109">0x0E14</span></span>  <br/> |
|<span data-ttu-id="f1ebf-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="f1ebf-110">Data type:</span></span>  <br/> |<span data-ttu-id="f1ebf-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f1ebf-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f1ebf-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f1ebf-112">Area:</span></span>  <br/> |<span data-ttu-id="f1ebf-113">MAPI não transmittable</span><span class="sxs-lookup"><span data-stu-id="f1ebf-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f1ebf-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1ebf-114">Remarks</span></span>

<span data-ttu-id="f1ebf-115">Um ou mais dos seguintes sinalizadores podem ser definidas para o bitmask **PR_SUBMIT_FLAGS** :</span><span class="sxs-lookup"><span data-stu-id="f1ebf-115">One or more of the following flags can be set for the **PR_SUBMIT_FLAGS** bitmask:</span></span> 
  
<span data-ttu-id="f1ebf-116">SUBMITFLAG_LOCKED</span><span class="sxs-lookup"><span data-stu-id="f1ebf-116">SUBMITFLAG_LOCKED</span></span> 
  
> <span data-ttu-id="f1ebf-117">O MAPI spooler atualmente tem a mensagem protegida.</span><span class="sxs-lookup"><span data-stu-id="f1ebf-117">The MAPI spooler currently has the message locked.</span></span> 
    
<span data-ttu-id="f1ebf-118">SUBMITFLAG_PREPROCESS</span><span class="sxs-lookup"><span data-stu-id="f1ebf-118">SUBMITFLAG_PREPROCESS</span></span> 
  
> <span data-ttu-id="f1ebf-119">A mensagem precisa pré-processamento.</span><span class="sxs-lookup"><span data-stu-id="f1ebf-119">The message needs preprocessing.</span></span> <span data-ttu-id="f1ebf-120">Quando terminar do MAPI spooler pré-processamento essa mensagem, ele deve chamar o método [IMessage::SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="f1ebf-120">When the MAPI spooler is done preprocessing this message, it should call the [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="f1ebf-121">O provedor de armazenamento de mensagem reconhece que o spooler, em vez do aplicativo cliente, tenha chamado **SubmitMessage**, limpa o sinalizador e continua o envio de mensagem.</span><span class="sxs-lookup"><span data-stu-id="f1ebf-121">The message store provider recognizes that the spooler, rather than the client application, has called **SubmitMessage**, clears the flag, and continues message submission.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="f1ebf-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f1ebf-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f1ebf-123">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="f1ebf-123">Protocol specifications</span></span>

<span data-ttu-id="f1ebf-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f1ebf-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f1ebf-125">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f1ebf-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f1ebf-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f1ebf-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f1ebf-127">Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.</span><span class="sxs-lookup"><span data-stu-id="f1ebf-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f1ebf-128">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f1ebf-128">Header files</span></span>

<span data-ttu-id="f1ebf-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f1ebf-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="f1ebf-130">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="f1ebf-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="f1ebf-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f1ebf-131">Mapitags.h</span></span>
  
> <span data-ttu-id="f1ebf-132">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="f1ebf-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f1ebf-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1ebf-133">See also</span></span>



[<span data-ttu-id="f1ebf-134">IMsgStore::SetLockState</span><span class="sxs-lookup"><span data-stu-id="f1ebf-134">IMsgStore::SetLockState</span></span>](imsgstore-setlockstate.md)


[<span data-ttu-id="f1ebf-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f1ebf-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f1ebf-136">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="f1ebf-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f1ebf-137">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="f1ebf-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f1ebf-138">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="f1ebf-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

