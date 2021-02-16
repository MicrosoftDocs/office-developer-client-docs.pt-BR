---
title: Propriedade canônica PidTagParentEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagParentEntryId
api_type:
- COM
ms.assetid: 55e08ace-493c-4246-8ebf-c304f4abc56a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 65f5e6c5da88267ec2e63d0acf3ef6f8e10c893b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348227"
---
# <a name="pidtagparententryid-canonical-property"></a><span data-ttu-id="2f80f-103">Propriedade canônica PidTagParentEntryId</span><span class="sxs-lookup"><span data-stu-id="2f80f-103">PidTagParentEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="2f80f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f80f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2f80f-105">Contém o identificador de entrada da pasta que contém uma pasta ou mensagem.</span><span class="sxs-lookup"><span data-stu-id="2f80f-105">Contains the entry identifier of the folder that contains a folder or message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2f80f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="2f80f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2f80f-107">PR_PARENT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="2f80f-107">PR_PARENT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="2f80f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2f80f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2f80f-109">0x0E09</span><span class="sxs-lookup"><span data-stu-id="2f80f-109">0x0E09</span></span>  <br/> |
|<span data-ttu-id="2f80f-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="2f80f-110">Data type:</span></span>  <br/> |<span data-ttu-id="2f80f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2f80f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2f80f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2f80f-112">Area:</span></span>  <br/> |<span data-ttu-id="2f80f-113">Propriedades de ID</span><span class="sxs-lookup"><span data-stu-id="2f80f-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2f80f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2f80f-114">Remarks</span></span>

<span data-ttu-id="2f80f-115">Essa propriedade é calculada por armazenamentos de mensagens para todas as pastas e mensagens.</span><span class="sxs-lookup"><span data-stu-id="2f80f-115">This property is computed by message stores for all folders and messages.</span></span>
  
<span data-ttu-id="2f80f-116">Para uma pasta raiz do armazenamento de mensagens, essa propriedade contém o próprio identificador de entrada da pasta.</span><span class="sxs-lookup"><span data-stu-id="2f80f-116">For a message store root folder, this property contains the folder's own entry identifier.</span></span>
  
 <span data-ttu-id="2f80f-117">**PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) e essa propriedade não estão relacionadas entre si.</span><span class="sxs-lookup"><span data-stu-id="2f80f-117">**PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) and this property are not related to each other.</span></span> <span data-ttu-id="2f80f-118">Eles pertencem a contextos totalmente diferentes.</span><span class="sxs-lookup"><span data-stu-id="2f80f-118">They belong to entirely different contexts.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2f80f-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2f80f-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2f80f-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="2f80f-120">Protocol specifications</span></span>

<span data-ttu-id="2f80f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2f80f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2f80f-122">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="2f80f-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2f80f-123">[[MS-OXCDATA]](https://msdn.microsoft.com/library/ 1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2f80f-123">[[MS-OXCDATA]](https://msdn.microsoft.com/library/ 1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2f80f-124">Define as estruturas de dados básicas que são usadas em operações remotas.</span><span class="sxs-lookup"><span data-stu-id="2f80f-124">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="2f80f-125">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2f80f-125">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2f80f-126">Lida com operações de pasta.</span><span class="sxs-lookup"><span data-stu-id="2f80f-126">Handles folder operations.</span></span>
    
<span data-ttu-id="2f80f-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2f80f-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2f80f-128">Converte entre IETF RFC2445, RFC2446 e RFC2447 e objetos de compromisso e reunião.</span><span class="sxs-lookup"><span data-stu-id="2f80f-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="2f80f-129">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2f80f-129">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2f80f-130">Permite a manipulação de listas de bloqueio/autorização e a determinação de mensagens de lixo eletrônico.</span><span class="sxs-lookup"><span data-stu-id="2f80f-130">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="2f80f-131">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2f80f-131">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2f80f-132">Especifica as propriedades e operações para criar e localizar as pastas especiais em uma caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="2f80f-132">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="2f80f-133">[[MS-OXPFOAB]](https://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2f80f-133">[[MS-OXPFOAB]](https://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2f80f-134">Especifica o método de entrega de dados do OAB (address book) offline de servidor para cliente.</span><span class="sxs-lookup"><span data-stu-id="2f80f-134">Specifies the method of delivering offline address book (OAB) data from server to client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2f80f-135">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="2f80f-135">Header files</span></span>

<span data-ttu-id="2f80f-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2f80f-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="2f80f-137">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="2f80f-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="2f80f-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2f80f-138">Mapitags.h</span></span>
  
> <span data-ttu-id="2f80f-139">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="2f80f-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2f80f-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f80f-140">See also</span></span>



[<span data-ttu-id="2f80f-141">Propriedade canônica PidTagFolderType</span><span class="sxs-lookup"><span data-stu-id="2f80f-141">PidTagFolderType Canonical Property</span></span>](pidtagfoldertype-canonical-property.md)


[<span data-ttu-id="2f80f-142">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2f80f-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2f80f-143">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="2f80f-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2f80f-144">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="2f80f-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2f80f-145">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="2f80f-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

