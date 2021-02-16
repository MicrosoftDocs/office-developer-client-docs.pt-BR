---
title: Propriedade canônica PidLidHasPicture
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidHasPicture
api_type:
- COM
ms.assetid: c3bea11c-3197-4060-8672-f1b4bf352112
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3aef2fc1038751c9ad6fb97cf347c2dcab114fda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357747"
---
# <a name="pidlidhaspicture-canonical-property"></a><span data-ttu-id="41b8d-103">Propriedade canônica PidLidHasPicture</span><span class="sxs-lookup"><span data-stu-id="41b8d-103">PidLidHasPicture Canonical Property</span></span>

  
  
<span data-ttu-id="41b8d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="41b8d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="41b8d-105">Especifica se existe um anexo de foto para um contato.</span><span class="sxs-lookup"><span data-stu-id="41b8d-105">Specifies whether a photo attachment exists for a contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="41b8d-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="41b8d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="41b8d-107">dispidHasPicture</span><span class="sxs-lookup"><span data-stu-id="41b8d-107">dispidHasPicture</span></span>  <br/> |
|<span data-ttu-id="41b8d-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="41b8d-108">Property set:</span></span>  <br/> |<span data-ttu-id="41b8d-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="41b8d-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="41b8d-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="41b8d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="41b8d-111">0x00008015</span><span class="sxs-lookup"><span data-stu-id="41b8d-111">0x00008015</span></span>  <br/> |
|<span data-ttu-id="41b8d-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="41b8d-112">Data type:</span></span>  <br/> |<span data-ttu-id="41b8d-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="41b8d-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="41b8d-114">Área:</span><span class="sxs-lookup"><span data-stu-id="41b8d-114">Area:</span></span>  <br/> |<span data-ttu-id="41b8d-115">Contato</span><span class="sxs-lookup"><span data-stu-id="41b8d-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="41b8d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="41b8d-116">Remarks</span></span>

<span data-ttu-id="41b8d-117">Se essa propriedade existir e estiver definida como TRUE, a tabela de anexos do contato conterá um anexo com a propriedade **PR_ATTACHMENT_CONTACTPHOTO** ([PidTagAttachmentContactPhoto](pidtagattachmentcontactphoto-canonical-property.md)) definida como TRUE.</span><span class="sxs-lookup"><span data-stu-id="41b8d-117">If this property exists and is set to TRUE, the contact's attachment table contains an attachment with the **PR_ATTACHMENT_CONTACTPHOTO** ([PidTagAttachmentContactPhoto](pidtagattachmentcontactphoto-canonical-property.md)) property set to TRUE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="41b8d-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="41b8d-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="41b8d-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="41b8d-119">Protocol specifications</span></span>

<span data-ttu-id="41b8d-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="41b8d-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="41b8d-121">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="41b8d-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="41b8d-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="41b8d-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="41b8d-123">Especifica as propriedades e operações permitidas para contatos e listas de distribuição pessoais.</span><span class="sxs-lookup"><span data-stu-id="41b8d-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="41b8d-124">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="41b8d-124">Header files</span></span>

<span data-ttu-id="41b8d-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="41b8d-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="41b8d-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="41b8d-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="41b8d-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="41b8d-127">See also</span></span>



[<span data-ttu-id="41b8d-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="41b8d-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="41b8d-129">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="41b8d-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="41b8d-130">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="41b8d-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="41b8d-131">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="41b8d-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

