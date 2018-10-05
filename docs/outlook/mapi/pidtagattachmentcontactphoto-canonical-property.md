---
title: Propriedade canônica PidTagAttachmentContactPhoto
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachmentContactPhoto
api_type:
- HeaderDef
ms.assetid: ea5b77b7-8440-4e54-abd2-c475138c8f63
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5d61289349306b763d13a9a2111c2cd02ff3937e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384889"
---
# <a name="pidtagattachmentcontactphoto-canonical-property"></a><span data-ttu-id="f8ddc-103">Propriedade canônica PidTagAttachmentContactPhoto</span><span class="sxs-lookup"><span data-stu-id="f8ddc-103">PidTagAttachmentContactPhoto Canonical Property</span></span>

  
  
<span data-ttu-id="f8ddc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8ddc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8ddc-105">Indica a existência de um anexo de foto de um contato.</span><span class="sxs-lookup"><span data-stu-id="f8ddc-105">Indicates the existence of a photo attachment for a contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f8ddc-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="f8ddc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f8ddc-107">PR_ATTACHMENT_CONTACTPHOTO</span><span class="sxs-lookup"><span data-stu-id="f8ddc-107">PR_ATTACHMENT_CONTACTPHOTO</span></span>  <br/> |
|<span data-ttu-id="f8ddc-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f8ddc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f8ddc-109">0x7FFF</span><span class="sxs-lookup"><span data-stu-id="f8ddc-109">0x7FFF</span></span>  <br/> |
|<span data-ttu-id="f8ddc-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="f8ddc-110">Data type:</span></span>  <br/> |<span data-ttu-id="f8ddc-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f8ddc-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="f8ddc-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f8ddc-112">Area:</span></span>  <br/> |<span data-ttu-id="f8ddc-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="f8ddc-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f8ddc-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8ddc-114">Remarks</span></span>

<span data-ttu-id="f8ddc-115">Este valor de propriedade deve ser definida como TRUE e deve haver apenas um anexo em um determinado objeto de contato.</span><span class="sxs-lookup"><span data-stu-id="f8ddc-115">This property's value must be set to TRUE, and there should only be one attachment on a given Contact object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f8ddc-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f8ddc-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f8ddc-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="f8ddc-117">Protocol specifications</span></span>

<span data-ttu-id="f8ddc-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f8ddc-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f8ddc-119">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="f8ddc-119">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f8ddc-120">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f8ddc-120">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f8ddc-121">Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="f8ddc-121">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f8ddc-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f8ddc-122">Header files</span></span>

<span data-ttu-id="f8ddc-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f8ddc-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="f8ddc-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="f8ddc-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="f8ddc-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f8ddc-125">Mapitags.h</span></span>
  
> <span data-ttu-id="f8ddc-126">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="f8ddc-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f8ddc-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8ddc-127">See also</span></span>



[<span data-ttu-id="f8ddc-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f8ddc-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f8ddc-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="f8ddc-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f8ddc-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="f8ddc-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f8ddc-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="f8ddc-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

