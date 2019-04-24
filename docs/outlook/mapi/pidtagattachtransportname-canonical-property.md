---
title: Propriedade canônica PidTagAttachTransportName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachTransportName
api_type:
- HeaderDef
ms.assetid: 701fca52-0f96-4019-80cd-c0ccd059ff9b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bd3a22bf55d03f3a9f06bf5c19650407bcc5627d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361065"
---
# <a name="pidtagattachtransportname-canonical-property"></a><span data-ttu-id="bbd63-103">Propriedade canônica PidTagAttachTransportName</span><span class="sxs-lookup"><span data-stu-id="bbd63-103">PidTagAttachTransportName Canonical Property</span></span>

  
  
<span data-ttu-id="bbd63-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bbd63-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bbd63-105">Contém o nome de um arquivo de anexo modificado para que ele possa ser associado a mensagens TNEF.</span><span class="sxs-lookup"><span data-stu-id="bbd63-105">Contains the name of an attachment file modified so that it can be associated with TNEF messages.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bbd63-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="bbd63-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bbd63-107">PR_ATTACH_TRANSPORT_NAME, PR_ATTACH_TRANSPORT_NAME_A, PR_ATTACH_TRANSPORT_NAME_W</span><span class="sxs-lookup"><span data-stu-id="bbd63-107">PR_ATTACH_TRANSPORT_NAME, PR_ATTACH_TRANSPORT_NAME_A, PR_ATTACH_TRANSPORT_NAME_W</span></span>  <br/> |
|<span data-ttu-id="bbd63-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="bbd63-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bbd63-109">0x370C</span><span class="sxs-lookup"><span data-stu-id="bbd63-109">0x370C</span></span>  <br/> |
|<span data-ttu-id="bbd63-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="bbd63-110">Data type:</span></span>  <br/> |<span data-ttu-id="bbd63-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bbd63-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="bbd63-112">Área:</span><span class="sxs-lookup"><span data-stu-id="bbd63-112">Area:</span></span>  <br/> |<span data-ttu-id="bbd63-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="bbd63-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bbd63-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="bbd63-114">Remarks</span></span>

<span data-ttu-id="bbd63-115">O TNEF e o provedor de transporte usam essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="bbd63-115">TNEF and the transport provider use these properties.</span></span> <span data-ttu-id="bbd63-116">Normalmente, elas não estão disponíveis para aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="bbd63-116">They are usually not available to client applications.</span></span> 
  
<span data-ttu-id="bbd63-117">Essas propriedades são comumente usadas por TNEF quando o sistema de mensagens subjacente não é compatível com os nomes de filefornecidos.</span><span class="sxs-lookup"><span data-stu-id="bbd63-117">These properties are commonly used by TNEF when the underlying messaging system does not support the supplied filenames.</span></span> <span data-ttu-id="bbd63-118">Por exemplo, eles são usados quando o usuário anexa vários arquivos com o mesmo nome, como cinco arquivos denominados CONFIG. Sistema.</span><span class="sxs-lookup"><span data-stu-id="bbd63-118">For example, they are used when the user attaches multiple files with the same name, such as five files named CONFIG.SYS.</span></span> <span data-ttu-id="bbd63-119">O provedor de transporte deve modificar os nomes para garantir que sejam exclusivos.</span><span class="sxs-lookup"><span data-stu-id="bbd63-119">The transport provider must modify the names to make sure they are unique.</span></span> <span data-ttu-id="bbd63-120">Cada nome modificado aparece no **PR_ATTACH_TRANSPORT_NAME** do anexo e nas propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="bbd63-120">Each modified name appears in its attachment's **PR_ATTACH_TRANSPORT_NAME** and associated properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bbd63-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="bbd63-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bbd63-122">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="bbd63-122">Protocol specifications</span></span>

<span data-ttu-id="bbd63-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bbd63-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bbd63-124">Manipula objetos Message e Attachment.</span><span class="sxs-lookup"><span data-stu-id="bbd63-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bbd63-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bbd63-125">Header files</span></span>

<span data-ttu-id="bbd63-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="bbd63-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="bbd63-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="bbd63-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="bbd63-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="bbd63-128">Mapitags.h</span></span>
  
> <span data-ttu-id="bbd63-129">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="bbd63-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bbd63-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="bbd63-130">See also</span></span>



[<span data-ttu-id="bbd63-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="bbd63-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bbd63-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="bbd63-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bbd63-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="bbd63-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bbd63-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="bbd63-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

