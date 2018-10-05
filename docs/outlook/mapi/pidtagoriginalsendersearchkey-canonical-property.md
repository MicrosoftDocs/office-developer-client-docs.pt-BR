---
title: Propriedade canônica PidTagOriginalSenderSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderSearchKey
api_type:
- COM
ms.assetid: 164eb9dd-e553-459e-99c1-3da0284bb01f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 97ab08d3da3725187ef2d5c70bec80e9142bdd21
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396460"
---
# <a name="pidtagoriginalsendersearchkey-canonical-property"></a><span data-ttu-id="dc4f7-103">Propriedade canônica PidTagOriginalSenderSearchKey</span><span class="sxs-lookup"><span data-stu-id="dc4f7-103">PidTagOriginalSenderSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="dc4f7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc4f7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc4f7-105">Contém a chave de pesquisa para o remetente da primeira versão de uma mensagem, ou seja, a mensagem antes que está sendo encaminhada ou respondida.</span><span class="sxs-lookup"><span data-stu-id="dc4f7-105">Contains the search key for the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dc4f7-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="dc4f7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dc4f7-107">PR_ORIGINAL_SENDER_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="dc4f7-107">PR_ORIGINAL_SENDER_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="dc4f7-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="dc4f7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dc4f7-109">0x005C</span><span class="sxs-lookup"><span data-stu-id="dc4f7-109">0x005C</span></span>  <br/> |
|<span data-ttu-id="dc4f7-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="dc4f7-110">Data type:</span></span>  <br/> |<span data-ttu-id="dc4f7-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="dc4f7-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="dc4f7-112">Área:</span><span class="sxs-lookup"><span data-stu-id="dc4f7-112">Area:</span></span>  <br/> |<span data-ttu-id="dc4f7-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="dc4f7-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dc4f7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="dc4f7-114">Remarks</span></span>

<span data-ttu-id="dc4f7-115">Essa propriedade é uma das propriedades de endereço do remetente original de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="dc4f7-115">This property is one of the address properties for the original sender of a message.</span></span> <span data-ttu-id="dc4f7-116">No primeiro envio da mensagem, o aplicativo cliente deve definir essa propriedade como o valor da propriedade **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="dc4f7-116">At first submission of the message, the client application should set this property to the value of the **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) property.</span></span> <span data-ttu-id="dc4f7-117">Ele nunca é alterado quando a mensagem for encaminhada ou respondida.</span><span class="sxs-lookup"><span data-stu-id="dc4f7-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="dc4f7-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="dc4f7-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dc4f7-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="dc4f7-119">Protocol specifications</span></span>

<span data-ttu-id="dc4f7-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc4f7-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dc4f7-121">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="dc4f7-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dc4f7-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc4f7-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dc4f7-123">Especifica as propriedades e operações que são permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="dc4f7-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dc4f7-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="dc4f7-124">Header files</span></span>

<span data-ttu-id="dc4f7-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dc4f7-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="dc4f7-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="dc4f7-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="dc4f7-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="dc4f7-127">Mapitags.h</span></span>
  
> <span data-ttu-id="dc4f7-128">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="dc4f7-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dc4f7-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc4f7-129">See also</span></span>



[<span data-ttu-id="dc4f7-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="dc4f7-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dc4f7-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="dc4f7-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dc4f7-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="dc4f7-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dc4f7-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="dc4f7-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

