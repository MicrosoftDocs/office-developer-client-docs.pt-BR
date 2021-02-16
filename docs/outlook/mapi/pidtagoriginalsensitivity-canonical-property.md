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
ms.openlocfilehash: e712a4cc49541ee4330f479d7a03af323bdbc887
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341227"
---
# <a name="pidtagoriginalsensitivity-canonical-property"></a><span data-ttu-id="48ccf-103">Propriedade canônica PidTagOriginalSensitivity</span><span class="sxs-lookup"><span data-stu-id="48ccf-103">PidTagOriginalSensitivity Canonical Property</span></span>

  
  
<span data-ttu-id="48ccf-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48ccf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48ccf-105">Contém o valor de sensibilidade atribuído pelo remetente da primeira versão de uma mensagem, ou seja, a mensagem antes de ser encaminhada ou respondida.</span><span class="sxs-lookup"><span data-stu-id="48ccf-105">Contains the sensitivity value assigned by the sender of the first version of a message that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="48ccf-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="48ccf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="48ccf-107">PR_ORIGINAL_SENSITIVITY</span><span class="sxs-lookup"><span data-stu-id="48ccf-107">PR_ORIGINAL_SENSITIVITY</span></span>  <br/> |
|<span data-ttu-id="48ccf-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="48ccf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="48ccf-109">0x002E</span><span class="sxs-lookup"><span data-stu-id="48ccf-109">0x002E</span></span>  <br/> |
|<span data-ttu-id="48ccf-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="48ccf-110">Data type:</span></span>  <br/> |<span data-ttu-id="48ccf-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="48ccf-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="48ccf-112">Área:</span><span class="sxs-lookup"><span data-stu-id="48ccf-112">Area:</span></span>  <br/> |<span data-ttu-id="48ccf-113">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="48ccf-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="48ccf-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="48ccf-114">Remarks</span></span>

<span data-ttu-id="48ccf-115">Um aplicativo cliente deve definir essa propriedade com o mesmo valor que a propriedade **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) quando a mensagem é enviada pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="48ccf-115">A client application should set this property to the same value as the **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) property when the message is first submitted.</span></span> <span data-ttu-id="48ccf-116">Ele nunca deve ser alterado posteriormente.</span><span class="sxs-lookup"><span data-stu-id="48ccf-116">It should never be changed subsequently.</span></span>
  
<span data-ttu-id="48ccf-117">Essa propriedade é usada pelo provedor de transporte para proteger a sensibilidade nas entradas copiadas.</span><span class="sxs-lookup"><span data-stu-id="48ccf-117">This property is used by the transport provider to protect the sensitivity on copied entries.</span></span> <span data-ttu-id="48ccf-118">Ele permite, por exemplo, bloquear a modificação do texto da mensagem original em um encaminhamento ou responder a uma mensagem que foi originalmente marcada como **SENSITIVITY_PRIVATE**.</span><span class="sxs-lookup"><span data-stu-id="48ccf-118">It enables it, for example, to block modification of the original message text in a forward of or reply to a message that was originally marked **SENSITIVITY_PRIVATE**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="48ccf-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="48ccf-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="48ccf-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="48ccf-120">Protocol specifications</span></span>

<span data-ttu-id="48ccf-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="48ccf-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="48ccf-122">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="48ccf-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="48ccf-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="48ccf-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="48ccf-124">Especifica as propriedades e operações que são permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="48ccf-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="48ccf-125">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="48ccf-125">Header files</span></span>

<span data-ttu-id="48ccf-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="48ccf-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="48ccf-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="48ccf-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="48ccf-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="48ccf-128">Mapitags.h</span></span>
  
> <span data-ttu-id="48ccf-129">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="48ccf-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="48ccf-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="48ccf-130">See also</span></span>



[<span data-ttu-id="48ccf-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="48ccf-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="48ccf-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="48ccf-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="48ccf-133">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="48ccf-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="48ccf-134">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="48ccf-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

