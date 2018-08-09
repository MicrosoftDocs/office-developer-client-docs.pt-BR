---
title: Propriedade canônica PidTagNextSendAcct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNextSendAcct
api_type:
- HeaderDef
ms.assetid: b7429c2e-0d9d-4921-9f56-9ecad817f8cb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 517d0900e968ea55cedf6b17b31d97795fcf61c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769507"
---
# <a name="pidtagnextsendacct-canonical-property"></a><span data-ttu-id="46e62-103">Propriedade canônica PidTagNextSendAcct</span><span class="sxs-lookup"><span data-stu-id="46e62-103">PidTagNextSendAcct Canonical Property</span></span>

  
  
<span data-ttu-id="46e62-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="46e62-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="46e62-105">Especifica o servidor que um cliente atualmente está tentando usar para enviar email.</span><span class="sxs-lookup"><span data-stu-id="46e62-105">Specifies the server that a client is currently attempting to use to send email.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="46e62-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="46e62-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="46e62-107">PR_NEXT_SEND_ACCT</span><span class="sxs-lookup"><span data-stu-id="46e62-107">PR_NEXT_SEND_ACCT</span></span>  <br/> |
|<span data-ttu-id="46e62-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="46e62-108">Identifier:</span></span>  <br/> |<span data-ttu-id="46e62-109">0x0E29</span><span class="sxs-lookup"><span data-stu-id="46e62-109">0x0E29</span></span>  <br/> |
|<span data-ttu-id="46e62-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="46e62-110">Data type:</span></span>  <br/> |<span data-ttu-id="46e62-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="46e62-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="46e62-112">Área:</span><span class="sxs-lookup"><span data-stu-id="46e62-112">Area:</span></span>  <br/> |<span data-ttu-id="46e62-113">Aplicativo do Outlook</span><span class="sxs-lookup"><span data-stu-id="46e62-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="46e62-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="46e62-114">Remarks</span></span>

<span data-ttu-id="46e62-115">O formato dessa propriedade é dependente de implementação.</span><span class="sxs-lookup"><span data-stu-id="46e62-115">The format of this property is implementation dependent.</span></span> <span data-ttu-id="46e62-116">Essa propriedade pode ser usada pelo cliente para determinar em qual servidor para direcionar o e-mail para, mas é opcional e o valor não tem significado para o servidor.</span><span class="sxs-lookup"><span data-stu-id="46e62-116">This property can be used by the client to determine which server to direct the email to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="46e62-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="46e62-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="46e62-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="46e62-118">Protocol specifications</span></span>

<span data-ttu-id="46e62-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46e62-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46e62-120">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="46e62-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="46e62-121">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46e62-121">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46e62-122">Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.</span><span class="sxs-lookup"><span data-stu-id="46e62-122">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="46e62-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46e62-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46e62-124">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="46e62-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="46e62-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="46e62-125">Header files</span></span>

<span data-ttu-id="46e62-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="46e62-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="46e62-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="46e62-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="46e62-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="46e62-128">Mapitags.h</span></span>
  
> <span data-ttu-id="46e62-129">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="46e62-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="46e62-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="46e62-130">See also</span></span>



[<span data-ttu-id="46e62-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="46e62-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="46e62-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="46e62-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="46e62-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="46e62-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="46e62-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="46e62-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
