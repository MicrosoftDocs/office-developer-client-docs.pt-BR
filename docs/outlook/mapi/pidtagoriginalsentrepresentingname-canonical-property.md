---
title: Propriedade canônica PidTagOriginalSentRepresentingName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSentRepresentingName
api_type:
- COM
ms.assetid: 1be45cad-05a2-44cb-8c3d-7f6ac092fa0d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 771a7c9cdf37a94875c881d8d7e8fd292893a0ba
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401479"
---
# <a name="pidtagoriginalsentrepresentingname-canonical-property"></a><span data-ttu-id="7947f-103">Propriedade canônica PidTagOriginalSentRepresentingName</span><span class="sxs-lookup"><span data-stu-id="7947f-103">PidTagOriginalSentRepresentingName Canonical Property</span></span>

  
  
<span data-ttu-id="7947f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7947f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7947f-105">Contém o nome de exibição do usuário mensagens em nome do qual a mensagem original foi enviada.</span><span class="sxs-lookup"><span data-stu-id="7947f-105">Contains the display name of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7947f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="7947f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7947f-107">PR_ORIGINAL_SENT_REPRESENTING_NAME, PR_ORIGINAL_SENT_REPRESENTING_NAME_A, PR_ORIGINAL_SENT_REPRESENTING_NAME_W</span><span class="sxs-lookup"><span data-stu-id="7947f-107">PR_ORIGINAL_SENT_REPRESENTING_NAME, PR_ORIGINAL_SENT_REPRESENTING_NAME_A, PR_ORIGINAL_SENT_REPRESENTING_NAME_W</span></span>  <br/> |
|<span data-ttu-id="7947f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7947f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7947f-109">0x005D</span><span class="sxs-lookup"><span data-stu-id="7947f-109">0x005D</span></span>  <br/> |
|<span data-ttu-id="7947f-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="7947f-110">Data type:</span></span>  <br/> |<span data-ttu-id="7947f-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7947f-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7947f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7947f-112">Area:</span></span>  <br/> |<span data-ttu-id="7947f-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="7947f-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7947f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7947f-114">Remarks</span></span>

<span data-ttu-id="7947f-115">Estes exemplos de propriedades as propriedades de endereço de remetente de uma mensagem original representado.</span><span class="sxs-lookup"><span data-stu-id="7947f-115">These properties examples of the address properties for the original represented sender of a message.</span></span> <span data-ttu-id="7947f-116">Ele é usado em um segmento de conversação.</span><span class="sxs-lookup"><span data-stu-id="7947f-116">It is used in a conversation thread.</span></span>
  
<span data-ttu-id="7947f-117">Um aplicativo cliente enviar uma mensagem em nome de outro cliente deve definir essas propriedades com o valor da propriedade **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) no primeiro envio da mensagem.</span><span class="sxs-lookup"><span data-stu-id="7947f-117">A client application sending a message on behalf of another client should set these properties to the value of the **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="7947f-118">Depois de definido, ela nunca deve ser alterada.</span><span class="sxs-lookup"><span data-stu-id="7947f-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7947f-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7947f-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7947f-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="7947f-120">Protocol specifications</span></span>

<span data-ttu-id="7947f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7947f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7947f-122">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="7947f-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7947f-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7947f-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7947f-124">Especifica as propriedades e operações que são permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="7947f-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7947f-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7947f-125">Header files</span></span>

<span data-ttu-id="7947f-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7947f-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="7947f-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="7947f-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="7947f-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7947f-128">Mapitags.h</span></span>
  
> <span data-ttu-id="7947f-129">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="7947f-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7947f-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="7947f-130">See also</span></span>



[<span data-ttu-id="7947f-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7947f-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7947f-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="7947f-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7947f-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="7947f-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7947f-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="7947f-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

