---
title: Propriedade canônica PidTagJunkAddRecipientsToSafeSendersList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkAddRecipientsToSafeSendersList
api_type:
- HeaderDef
ms.assetid: 78543caa-e6ec-4ac7-bfdd-70c56f8fd955
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8c104af106a885f42f8063bcf5fb55d654f2688e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769399"
---
# <a name="pidtagjunkaddrecipientstosafesenderslist-canonical-property"></a><span data-ttu-id="45786-103">Propriedade canônica PidTagJunkAddRecipientsToSafeSendersList</span><span class="sxs-lookup"><span data-stu-id="45786-103">PidTagJunkAddRecipientsToSafeSendersList Canonical Property</span></span>

  
  
<span data-ttu-id="45786-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="45786-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="45786-105">Indica se ou não os destinatários de email a ser adicionado à lista de remetentes confiáveis.</span><span class="sxs-lookup"><span data-stu-id="45786-105">Indicates whether or not the mail recipients are to be added to the safe senders list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="45786-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="45786-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="45786-107">PR_JUNK_ADD_RECIPS_TO_SSL</span><span class="sxs-lookup"><span data-stu-id="45786-107">PR_JUNK_ADD_RECIPS_TO_SSL</span></span>  <br/> |
|<span data-ttu-id="45786-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="45786-108">Identifier:</span></span>  <br/> |<span data-ttu-id="45786-109">0x6103</span><span class="sxs-lookup"><span data-stu-id="45786-109">0x6103</span></span>  <br/> |
|<span data-ttu-id="45786-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="45786-110">Data type:</span></span>  <br/> |<span data-ttu-id="45786-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="45786-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="45786-112">Área:</span><span class="sxs-lookup"><span data-stu-id="45786-112">Area:</span></span>  <br/> |<span data-ttu-id="45786-113">Spam</span><span class="sxs-lookup"><span data-stu-id="45786-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45786-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="45786-114">Remarks</span></span>

<span data-ttu-id="45786-115">Se houver, essa propriedade deverá ser definida como 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="45786-115">If present, this property must be set to 0 or 1.</span></span> <span data-ttu-id="45786-116">Um valor de 1 indica que os destinatários de email devem ser adicionados à lista de remetentes confiáveis.</span><span class="sxs-lookup"><span data-stu-id="45786-116">A value of 1 indicates that the mail recipients are to be added to the safe senders list.</span></span> <span data-ttu-id="45786-117">Um valor 0 indica que os destinatários de email não são a ser adicionado à lista de remetentes confiáveis.</span><span class="sxs-lookup"><span data-stu-id="45786-117">A value of 0 indicates that the mail recipients are not to be added to the safe senders list.</span></span>
  
<span data-ttu-id="45786-118">Se essa propriedade estiver presente com um valor de 1, os endereços SMTP os destinatários do email devem ser adicionados à cláusula de remetentes confiáveis da condição de regra do lixo eletrônico.</span><span class="sxs-lookup"><span data-stu-id="45786-118">If this property is present with a value of 1, the SMTP addresses of the email recipients must be added to trusted senders clause of the Junk E-Mail Rule condition.</span></span> <span data-ttu-id="45786-119">Se essa propriedade for 0, nenhuma ação é necessária.</span><span class="sxs-lookup"><span data-stu-id="45786-119">If this property is 0, no action is required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="45786-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="45786-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="45786-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="45786-121">Protocol specifications</span></span>

<span data-ttu-id="45786-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45786-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45786-123">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="45786-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="45786-124">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45786-124">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45786-125">Permite a manipulação das listas de permitir/bloquear e a determinação das mensagens de lixo eletrônico.</span><span class="sxs-lookup"><span data-stu-id="45786-125">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="45786-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="45786-126">Header files</span></span>

<span data-ttu-id="45786-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="45786-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="45786-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="45786-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="45786-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="45786-129">Mapitags.h</span></span>
  
> <span data-ttu-id="45786-130">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="45786-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="45786-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="45786-131">See also</span></span>



[<span data-ttu-id="45786-132">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="45786-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="45786-133">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="45786-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="45786-134">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="45786-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="45786-135">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="45786-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

