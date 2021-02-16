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
ms.openlocfilehash: 3a87beaa3873b5ccb449e5b1497262bad5bf1497
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282365"
---
# <a name="pidtagjunkaddrecipientstosafesenderslist-canonical-property"></a><span data-ttu-id="8d034-103">Propriedade canônica PidTagJunkAddRecipientsToSafeSendersList</span><span class="sxs-lookup"><span data-stu-id="8d034-103">PidTagJunkAddRecipientsToSafeSendersList Canonical Property</span></span>

  
  
<span data-ttu-id="8d034-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d034-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d034-105">Indica se os destinatários de email devem ou não ser adicionados à lista de destinatários seguros.</span><span class="sxs-lookup"><span data-stu-id="8d034-105">Indicates whether or not the mail recipients are to be added to the safe senders list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8d034-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="8d034-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8d034-107">PR_JUNK_ADD_RECIPS_TO_SSL</span><span class="sxs-lookup"><span data-stu-id="8d034-107">PR_JUNK_ADD_RECIPS_TO_SSL</span></span>  <br/> |
|<span data-ttu-id="8d034-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8d034-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8d034-109">0x6103</span><span class="sxs-lookup"><span data-stu-id="8d034-109">0x6103</span></span>  <br/> |
|<span data-ttu-id="8d034-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="8d034-110">Data type:</span></span>  <br/> |<span data-ttu-id="8d034-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8d034-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8d034-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8d034-112">Area:</span></span>  <br/> |<span data-ttu-id="8d034-113">Spam</span><span class="sxs-lookup"><span data-stu-id="8d034-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d034-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8d034-114">Remarks</span></span>

<span data-ttu-id="8d034-115">Se presente, essa propriedade deve ser definida como 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="8d034-115">If present, this property must be set to 0 or 1.</span></span> <span data-ttu-id="8d034-116">Um valor 1 indica que os destinatários de email devem ser adicionados à lista de destinatários seguros.</span><span class="sxs-lookup"><span data-stu-id="8d034-116">A value of 1 indicates that the mail recipients are to be added to the safe senders list.</span></span> <span data-ttu-id="8d034-117">Um valor 0 indica que os destinatários de email não devem ser adicionados à lista de destinatários seguros.</span><span class="sxs-lookup"><span data-stu-id="8d034-117">A value of 0 indicates that the mail recipients are not to be added to the safe senders list.</span></span>
  
<span data-ttu-id="8d034-118">Se essa propriedade estiver presente com um valor de 1, os endereços SMTP dos destinatários de email deverão ser adicionados à cláusula de envios confiáveis da condição Regra de Lixo Eletrônico.</span><span class="sxs-lookup"><span data-stu-id="8d034-118">If this property is present with a value of 1, the SMTP addresses of the email recipients must be added to trusted senders clause of the Junk E-Mail Rule condition.</span></span> <span data-ttu-id="8d034-119">Se essa propriedade for 0, nenhuma ação será necessária.</span><span class="sxs-lookup"><span data-stu-id="8d034-119">If this property is 0, no action is required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8d034-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8d034-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8d034-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="8d034-121">Protocol specifications</span></span>

<span data-ttu-id="8d034-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d034-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d034-123">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8d034-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8d034-124">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d034-124">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d034-125">Permite a manipulação de listas de bloqueio/autorização e a determinação de mensagens de lixo eletrônico.</span><span class="sxs-lookup"><span data-stu-id="8d034-125">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8d034-126">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="8d034-126">Header files</span></span>

<span data-ttu-id="8d034-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8d034-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="8d034-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8d034-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="8d034-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8d034-129">Mapitags.h</span></span>
  
> <span data-ttu-id="8d034-130">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="8d034-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8d034-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="8d034-131">See also</span></span>



[<span data-ttu-id="8d034-132">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8d034-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8d034-133">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="8d034-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8d034-134">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="8d034-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8d034-135">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="8d034-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

