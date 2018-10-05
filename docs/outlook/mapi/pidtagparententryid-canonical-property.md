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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401213"
---
# <a name="pidtagparententryid-canonical-property"></a><span data-ttu-id="073da-103">Propriedade canônica PidTagParentEntryId</span><span class="sxs-lookup"><span data-stu-id="073da-103">PidTagParentEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="073da-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="073da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="073da-105">Contém o identificador de entrada da pasta que contém uma pasta ou mensagem.</span><span class="sxs-lookup"><span data-stu-id="073da-105">Contains the entry identifier of the folder that contains a folder or message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="073da-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="073da-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="073da-107">PR_PARENT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="073da-107">PR_PARENT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="073da-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="073da-108">Identifier:</span></span>  <br/> |<span data-ttu-id="073da-109">0x0E09</span><span class="sxs-lookup"><span data-stu-id="073da-109">0x0E09</span></span>  <br/> |
|<span data-ttu-id="073da-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="073da-110">Data type:</span></span>  <br/> |<span data-ttu-id="073da-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="073da-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="073da-112">Área:</span><span class="sxs-lookup"><span data-stu-id="073da-112">Area:</span></span>  <br/> |<span data-ttu-id="073da-113">Propriedades de identificação</span><span class="sxs-lookup"><span data-stu-id="073da-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="073da-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="073da-114">Remarks</span></span>

<span data-ttu-id="073da-115">Essa propriedade é computada pelo repositórios de mensagem para todas as mensagens e pastas.</span><span class="sxs-lookup"><span data-stu-id="073da-115">This property is computed by message stores for all folders and messages.</span></span>
  
<span data-ttu-id="073da-116">Para uma pasta de raiz do repositório de mensagem, essa propriedade contém o identificador de entrada da pasta.</span><span class="sxs-lookup"><span data-stu-id="073da-116">For a message store root folder, this property contains the folder's own entry identifier.</span></span>
  
 <span data-ttu-id="073da-117">**PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) e essa propriedade não estão relacionados entre si.</span><span class="sxs-lookup"><span data-stu-id="073da-117">**PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) and this property are not related to each other.</span></span> <span data-ttu-id="073da-118">Eles pertencem ao contextos completamente diferentes.</span><span class="sxs-lookup"><span data-stu-id="073da-118">They belong to entirely different contexts.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="073da-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="073da-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="073da-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="073da-120">Protocol specifications</span></span>

<span data-ttu-id="073da-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="073da-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="073da-122">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="073da-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="073da-123">[[MS-OXCDATA]](https://msdn.microsoft.com/library/ 1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="073da-123">[[MS-OXCDATA]](https://msdn.microsoft.com/library/ 1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="073da-124">Define as estruturas de dados básicos que são usadas em operações remotas.</span><span class="sxs-lookup"><span data-stu-id="073da-124">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="073da-125">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="073da-125">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="073da-126">Trata as operações de pasta.</span><span class="sxs-lookup"><span data-stu-id="073da-126">Handles folder operations.</span></span>
    
<span data-ttu-id="073da-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="073da-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="073da-128">Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.</span><span class="sxs-lookup"><span data-stu-id="073da-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="073da-129">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="073da-129">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="073da-130">Permite a manipulação das listas de permitir/bloquear e a determinação das mensagens de lixo eletrônico.</span><span class="sxs-lookup"><span data-stu-id="073da-130">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="073da-131">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="073da-131">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="073da-132">Especifica as propriedades e operações para a criação e a localização de pastas especiais em uma caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="073da-132">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="073da-133">[[MS-OXPFOAB]](https://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="073da-133">[[MS-OXPFOAB]](https://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="073da-134">Especifica o método de fornecimento de dados do OAB (catálogo) de endereços offline do servidor para o cliente.</span><span class="sxs-lookup"><span data-stu-id="073da-134">Specifies the method of delivering offline address book (OAB) data from server to client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="073da-135">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="073da-135">Header files</span></span>

<span data-ttu-id="073da-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="073da-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="073da-137">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="073da-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="073da-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="073da-138">Mapitags.h</span></span>
  
> <span data-ttu-id="073da-139">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="073da-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="073da-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="073da-140">See also</span></span>



[<span data-ttu-id="073da-141">Propriedade canônica PidTagFolderType</span><span class="sxs-lookup"><span data-stu-id="073da-141">PidTagFolderType Canonical Property</span></span>](pidtagfoldertype-canonical-property.md)


[<span data-ttu-id="073da-142">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="073da-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="073da-143">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="073da-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="073da-144">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="073da-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="073da-145">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="073da-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

