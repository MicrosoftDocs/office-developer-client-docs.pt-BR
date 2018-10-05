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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400513"
---
# <a name="pidtagattachtransportname-canonical-property"></a><span data-ttu-id="82db2-103">Propriedade canônica PidTagAttachTransportName</span><span class="sxs-lookup"><span data-stu-id="82db2-103">PidTagAttachTransportName Canonical Property</span></span>

  
  
<span data-ttu-id="82db2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82db2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82db2-105">Contém o nome de um arquivo de anexo modificado de modo que ela pode ser associada a mensagens TNEF.</span><span class="sxs-lookup"><span data-stu-id="82db2-105">Contains the name of an attachment file modified so that it can be associated with TNEF messages.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="82db2-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="82db2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="82db2-107">PR_ATTACH_TRANSPORT_NAME, PR_ATTACH_TRANSPORT_NAME_A, PR_ATTACH_TRANSPORT_NAME_W</span><span class="sxs-lookup"><span data-stu-id="82db2-107">PR_ATTACH_TRANSPORT_NAME, PR_ATTACH_TRANSPORT_NAME_A, PR_ATTACH_TRANSPORT_NAME_W</span></span>  <br/> |
|<span data-ttu-id="82db2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="82db2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="82db2-109">0x370C</span><span class="sxs-lookup"><span data-stu-id="82db2-109">0x370C</span></span>  <br/> |
|<span data-ttu-id="82db2-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="82db2-110">Data type:</span></span>  <br/> |<span data-ttu-id="82db2-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="82db2-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="82db2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="82db2-112">Area:</span></span>  <br/> |<span data-ttu-id="82db2-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="82db2-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="82db2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="82db2-114">Remarks</span></span>

<span data-ttu-id="82db2-115">TNEF e o provedor de transporte utilizar essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="82db2-115">TNEF and the transport provider use these properties.</span></span> <span data-ttu-id="82db2-116">Eles geralmente não estão disponíveis para os aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="82db2-116">They are usually not available to client applications.</span></span> 
  
<span data-ttu-id="82db2-117">Essas propriedades são usadas pelo TNEF quando o sistema de mensagens subjacente não oferece suporte a nomes de arquivo fornecido.</span><span class="sxs-lookup"><span data-stu-id="82db2-117">These properties are commonly used by TNEF when the underlying messaging system does not support the supplied filenames.</span></span> <span data-ttu-id="82db2-118">Por exemplo, eles são usados quando o usuário anexa vários arquivos com o mesmo nome, como arquivos de cinco chamado CONFIG. SYS.</span><span class="sxs-lookup"><span data-stu-id="82db2-118">For example, they are used when the user attaches multiple files with the same name, such as five files named CONFIG.SYS.</span></span> <span data-ttu-id="82db2-119">O provedor de transporte deve modificar os nomes para garantir que eles sejam exclusivos.</span><span class="sxs-lookup"><span data-stu-id="82db2-119">The transport provider must modify the names to make sure they are unique.</span></span> <span data-ttu-id="82db2-120">Cada nome modificado aparece no **PR_ATTACH_TRANSPORT_NAME** de seu anexo e propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="82db2-120">Each modified name appears in its attachment's **PR_ATTACH_TRANSPORT_NAME** and associated properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="82db2-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="82db2-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="82db2-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="82db2-122">Protocol specifications</span></span>

<span data-ttu-id="82db2-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82db2-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82db2-124">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="82db2-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="82db2-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="82db2-125">Header files</span></span>

<span data-ttu-id="82db2-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="82db2-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="82db2-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="82db2-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="82db2-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="82db2-128">Mapitags.h</span></span>
  
> <span data-ttu-id="82db2-129">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="82db2-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="82db2-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="82db2-130">See also</span></span>



[<span data-ttu-id="82db2-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="82db2-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="82db2-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="82db2-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="82db2-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="82db2-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="82db2-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="82db2-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

