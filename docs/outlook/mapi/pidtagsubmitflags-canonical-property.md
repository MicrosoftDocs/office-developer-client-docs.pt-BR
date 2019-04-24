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
ms.openlocfilehash: ca31aece48236227a03d8e2114f8af4b127b8f90
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339351"
---
# <a name="pidtagsubmitflags-canonical-property"></a><span data-ttu-id="a229a-103">Propriedade canônica PidTagSubmitFlags</span><span class="sxs-lookup"><span data-stu-id="a229a-103">PidTagSubmitFlags Canonical Property</span></span>

  
  
<span data-ttu-id="a229a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a229a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a229a-105">Contém uma bitmask de sinalizadores que indicam detalhes sobre um envio de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a229a-105">Contains a bitmask of flags indicating details about a message submission.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a229a-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a229a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a229a-107">PR_SUBMIT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="a229a-107">PR_SUBMIT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="a229a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a229a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a229a-109">0x0E14</span><span class="sxs-lookup"><span data-stu-id="a229a-109">0x0E14</span></span>  <br/> |
|<span data-ttu-id="a229a-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a229a-110">Data type:</span></span>  <br/> |<span data-ttu-id="a229a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a229a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a229a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a229a-112">Area:</span></span>  <br/> |<span data-ttu-id="a229a-113">MAPI não-transmittable</span><span class="sxs-lookup"><span data-stu-id="a229a-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a229a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a229a-114">Remarks</span></span>

<span data-ttu-id="a229a-115">Um ou mais dos seguintes sinalizadores podem ser definidos para o bitmask **PR_SUBMIT_FLAGS** :</span><span class="sxs-lookup"><span data-stu-id="a229a-115">One or more of the following flags can be set for the **PR_SUBMIT_FLAGS** bitmask:</span></span> 
  
<span data-ttu-id="a229a-116">SUBMITFLAG_LOCKED</span><span class="sxs-lookup"><span data-stu-id="a229a-116">SUBMITFLAG_LOCKED</span></span> 
  
> <span data-ttu-id="a229a-117">O spooler MAPI tem a mensagem bloqueada no momento.</span><span class="sxs-lookup"><span data-stu-id="a229a-117">The MAPI spooler currently has the message locked.</span></span> 
    
<span data-ttu-id="a229a-118">SUBMITFLAG_PREPROCESS</span><span class="sxs-lookup"><span data-stu-id="a229a-118">SUBMITFLAG_PREPROCESS</span></span> 
  
> <span data-ttu-id="a229a-119">A mensagem precisa de pré-processamento.</span><span class="sxs-lookup"><span data-stu-id="a229a-119">The message needs preprocessing.</span></span> <span data-ttu-id="a229a-120">Quando o spooler MAPI estiver realizando o pré-processamento dessa mensagem, ele deverá chamar o método [IMessage:: SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="a229a-120">When the MAPI spooler is done preprocessing this message, it should call the [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="a229a-121">O provedor de repositório de mensagens reconhece que o spooler, em vez do aplicativo cliente, chamou **SubmitMessage**, limpa o sinalizador e continua o envio da mensagem.</span><span class="sxs-lookup"><span data-stu-id="a229a-121">The message store provider recognizes that the spooler, rather than the client application, has called **SubmitMessage**, clears the flag, and continues message submission.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="a229a-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a229a-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a229a-123">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="a229a-123">Protocol specifications</span></span>

<span data-ttu-id="a229a-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a229a-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a229a-125">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a229a-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a229a-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a229a-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a229a-127">Converte entre o IETF RFC2445, o RFC2446 e o RFC2447 e os objetos de compromisso e reunião.</span><span class="sxs-lookup"><span data-stu-id="a229a-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a229a-128">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a229a-128">Header files</span></span>

<span data-ttu-id="a229a-129">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a229a-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="a229a-130">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a229a-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="a229a-131">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="a229a-131">Mapitags.h</span></span>
  
> <span data-ttu-id="a229a-132">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="a229a-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a229a-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="a229a-133">See also</span></span>



[<span data-ttu-id="a229a-134">IMsgStore::SetLockState</span><span class="sxs-lookup"><span data-stu-id="a229a-134">IMsgStore::SetLockState</span></span>](imsgstore-setlockstate.md)


[<span data-ttu-id="a229a-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a229a-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a229a-136">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="a229a-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a229a-137">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a229a-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a229a-138">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="a229a-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

