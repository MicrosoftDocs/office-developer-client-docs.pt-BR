---
title: Propriedade canônica PidTagStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatus
api_type:
- COM
ms.assetid: 8b947660-eafe-47e1-9595-bd3ab7d455bf
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: de2342ef4d3e9d06f198e06dc19c65b7b144624f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278789"
---
# <a name="pidtagstatus-canonical-property"></a><span data-ttu-id="75cc7-103">Propriedade canônica PidTagStatus</span><span class="sxs-lookup"><span data-stu-id="75cc7-103">PidTagStatus Canonical Property</span></span>

  
  
<span data-ttu-id="75cc7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75cc7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75cc7-105">Contém um bitmask de 32 bits de sinalizadores que definem o status da pasta.</span><span class="sxs-lookup"><span data-stu-id="75cc7-105">Contains a 32-bit bitmask of flags that define folder status.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="75cc7-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="75cc7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="75cc7-107">PR_STATUS</span><span class="sxs-lookup"><span data-stu-id="75cc7-107">PR_STATUS</span></span>  <br/> |
|<span data-ttu-id="75cc7-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="75cc7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="75cc7-109">0x360B</span><span class="sxs-lookup"><span data-stu-id="75cc7-109">0x360B</span></span>  <br/> |
|<span data-ttu-id="75cc7-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="75cc7-110">Data type:</span></span>  <br/> |<span data-ttu-id="75cc7-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="75cc7-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="75cc7-112">Área:</span><span class="sxs-lookup"><span data-stu-id="75cc7-112">Area:</span></span>  <br/> |<span data-ttu-id="75cc7-113">Contêiner MAPI</span><span class="sxs-lookup"><span data-stu-id="75cc7-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="75cc7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="75cc7-114">Remarks</span></span>

<span data-ttu-id="75cc7-115">Essa propriedade para Folders é análoga à propriedade **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) para mensagens.</span><span class="sxs-lookup"><span data-stu-id="75cc7-115">This property for folders is analogous to the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property for messages.</span></span> <span data-ttu-id="75cc7-116">Seus sinalizadores são fornecidos apenas para o aplicativo cliente e não afetam o repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="75cc7-116">Its flags are provided for the client application only and do not affect the message store.</span></span> <span data-ttu-id="75cc7-117">Os clientes podem usar ou ignorar essas configurações.</span><span class="sxs-lookup"><span data-stu-id="75cc7-117">Clients can use or ignore these settings.</span></span> <span data-ttu-id="75cc7-118">O cliente também pode definir seus próprios valores para os bits definíveis pelo cliente dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="75cc7-118">The client can also define its own values for the client-definable bits of this property.</span></span>
  
<span data-ttu-id="75cc7-119">Um ou mais dos seguintes sinalizadores podem ser definidos para a bitmask:</span><span class="sxs-lookup"><span data-stu-id="75cc7-119">One or more of the following flags can be set for the bitmask:</span></span>
  
<span data-ttu-id="75cc7-120">FLDSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="75cc7-120">FLDSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="75cc7-121">A pasta está marcada para exclusão.</span><span class="sxs-lookup"><span data-stu-id="75cc7-121">The folder is marked for deletion.</span></span> <span data-ttu-id="75cc7-122">O aplicativo cliente define esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="75cc7-122">The client application sets this flag.</span></span>
    
<span data-ttu-id="75cc7-123">FLDSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="75cc7-123">FLDSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="75cc7-124">A pasta está oculta.</span><span class="sxs-lookup"><span data-stu-id="75cc7-124">The folder is hidden.</span></span>
    
<span data-ttu-id="75cc7-125">FLDSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="75cc7-125">FLDSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="75cc7-126">A pasta é realçada, por exemplo, mostrada em vídeo inverso.</span><span class="sxs-lookup"><span data-stu-id="75cc7-126">The folder is highlighted, for example, shown in reverse video.</span></span>
    
<span data-ttu-id="75cc7-127">FLDSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="75cc7-127">FLDSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="75cc7-128">A pasta está marcada.</span><span class="sxs-lookup"><span data-stu-id="75cc7-128">The folder is tagged.</span></span>
    
<span data-ttu-id="75cc7-129">Provedores de repositórios de mensagens defina essa propriedade em uma pasta como um ou mais desses valores e clientes interpretam o status conforme apropriado para seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="75cc7-129">Message store providers set this property on a folder to one or more of these values and clients interpret the status as appropriate for their applications.</span></span> <span data-ttu-id="75cc7-130">Por exemplo, um cliente pode usar o status da pasta para diferenciar visualmente entre pastas em uma tabela de hierarquia, exibindo pastas com o mesmo status da mesma maneira.</span><span class="sxs-lookup"><span data-stu-id="75cc7-130">For example, a client can use the folder status to visually differentiate between folders in a hierarchy table, displaying folders with the same status in the same way.</span></span> <span data-ttu-id="75cc7-131">Pastas reAlçadas podem ser mostradas no vídeo inverso, pastas marcadas e pastas marcadas para exclusão podem ser exibidas com um ícone significativo e pastas ocultas podem ser ocultadas.</span><span class="sxs-lookup"><span data-stu-id="75cc7-131">Highlighted folders can be shown in reverse video, tagged folders and folders marked for deletion can be shown with a meaningful icon, and hidden folders can be concealed.</span></span>
  
<span data-ttu-id="75cc7-132">Os bits 16 a 31 ("0x10000" por meio de "0x80000000") dessa propriedade estão disponíveis para uso pelo aplicativo cliente IPM.</span><span class="sxs-lookup"><span data-stu-id="75cc7-132">Bits 16 through 31 ("0x10000" through "0x80000000") of this property are available for use by the IPM client application.</span></span> <span data-ttu-id="75cc7-133">Todos os outros bits são reservados para uso por MAPI; os não definidos na lista anterior devem ser inicialmente definidos como zero e não alterados.</span><span class="sxs-lookup"><span data-stu-id="75cc7-133">All other bits are reserved for use by MAPI; those not defined in the preceding list should be initially set to zero and not altered.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="75cc7-134">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="75cc7-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="75cc7-135">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="75cc7-135">Protocol specifications</span></span>

<span data-ttu-id="75cc7-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75cc7-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75cc7-137">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="75cc7-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="75cc7-138">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75cc7-138">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75cc7-139">Manipula objetos Message e Attachment.</span><span class="sxs-lookup"><span data-stu-id="75cc7-139">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="75cc7-140">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="75cc7-140">Header files</span></span>

<span data-ttu-id="75cc7-141">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="75cc7-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="75cc7-142">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="75cc7-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="75cc7-143">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="75cc7-143">Mapitags.h</span></span>
  
> <span data-ttu-id="75cc7-144">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="75cc7-144">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="75cc7-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="75cc7-145">See also</span></span>



[<span data-ttu-id="75cc7-146">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="75cc7-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="75cc7-147">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="75cc7-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="75cc7-148">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="75cc7-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="75cc7-149">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="75cc7-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

