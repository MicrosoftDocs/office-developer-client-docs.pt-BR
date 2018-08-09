---
title: Propriedade canônica PidTagOriginalSensitivity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSensitivity
api_type:
- COM
ms.assetid: 70a87cf8-2011-4669-90fd-2711c3352e30
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6d461c88e96a3f749595b3e071737107480472aa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769591"
---
# <a name="pidtagoriginalsensitivity-canonical-property"></a><span data-ttu-id="69adf-103">Propriedade canônica PidTagOriginalSensitivity</span><span class="sxs-lookup"><span data-stu-id="69adf-103">PidTagOriginalSensitivity Canonical Property</span></span>

  
  
<span data-ttu-id="69adf-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="69adf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="69adf-105">Contém o valor de sensibilidade atribuído pelo remetente da primeira versão de uma mensagem ou seja, a mensagem antes que está sendo encaminhada ou respondida.</span><span class="sxs-lookup"><span data-stu-id="69adf-105">Contains the sensitivity value assigned by the sender of the first version of a message that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="69adf-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="69adf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="69adf-107">PR_ORIGINAL_SENSITIVITY</span><span class="sxs-lookup"><span data-stu-id="69adf-107">PR_ORIGINAL_SENSITIVITY</span></span>  <br/> |
|<span data-ttu-id="69adf-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="69adf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="69adf-109">0x002E</span><span class="sxs-lookup"><span data-stu-id="69adf-109">0x002E</span></span>  <br/> |
|<span data-ttu-id="69adf-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="69adf-110">Data type:</span></span>  <br/> |<span data-ttu-id="69adf-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="69adf-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="69adf-112">Área:</span><span class="sxs-lookup"><span data-stu-id="69adf-112">Area:</span></span>  <br/> |<span data-ttu-id="69adf-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="69adf-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69adf-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="69adf-114">Remarks</span></span>

<span data-ttu-id="69adf-115">Um aplicativo cliente deve definir essa propriedade com o mesmo valor conforme a propriedade **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) quando a mensagem é primeira enviados.</span><span class="sxs-lookup"><span data-stu-id="69adf-115">A client application should set this property to the same value as the **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) property when the message is first submitted.</span></span> <span data-ttu-id="69adf-116">Ele nunca deve ser alterado subsequentemente.</span><span class="sxs-lookup"><span data-stu-id="69adf-116">It should never be changed subsequently.</span></span>
  
<span data-ttu-id="69adf-117">Essa propriedade é usada pelo provedor de transporte para proteger a sensibilidade nas entradas copiadas.</span><span class="sxs-lookup"><span data-stu-id="69adf-117">This property is used by the transport provider to protect the sensitivity on copied entries.</span></span> <span data-ttu-id="69adf-118">Habilitá-lo, por exemplo, para bloquear a modificação do texto da mensagem original em um direta de ou responder a uma mensagem que originalmente foi marcada **SENSITIVITY_PRIVATE**.</span><span class="sxs-lookup"><span data-stu-id="69adf-118">It enables it, for example, to block modification of the original message text in a forward of or reply to a message that was originally marked **SENSITIVITY_PRIVATE**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="69adf-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="69adf-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="69adf-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="69adf-120">Protocol specifications</span></span>

<span data-ttu-id="69adf-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69adf-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69adf-122">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="69adf-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="69adf-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69adf-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69adf-124">Especifica as propriedades e operações que são permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="69adf-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="69adf-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="69adf-125">Header files</span></span>

<span data-ttu-id="69adf-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="69adf-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="69adf-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="69adf-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="69adf-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="69adf-128">Mapitags.h</span></span>
  
> <span data-ttu-id="69adf-129">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="69adf-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="69adf-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="69adf-130">See also</span></span>



[<span data-ttu-id="69adf-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="69adf-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="69adf-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="69adf-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="69adf-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="69adf-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="69adf-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="69adf-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
