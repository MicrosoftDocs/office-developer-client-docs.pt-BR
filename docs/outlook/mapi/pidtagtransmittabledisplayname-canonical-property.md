---
title: Propriedade canônica PidTagTransmittableDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTransmittableDisplayName
api_type:
- COM
ms.assetid: aadd9086-b936-4067-bf7d-f54fc50e3c83
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e66fe8d3621c122ccc19bdde169f20f7d47a148d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331854"
---
# <a name="pidtagtransmittabledisplayname-canonical-property"></a><span data-ttu-id="e2781-103">Propriedade canônica PidTagTransmittableDisplayName</span><span class="sxs-lookup"><span data-stu-id="e2781-103">PidTagTransmittableDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="e2781-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2781-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2781-105">Contém o nome de exibição de um destinatário em um formulário seguro que não pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="e2781-105">Contains a recipient's display name in a secure form that cannot be changed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e2781-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="e2781-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e2781-107">PR_TRANSMITABLE_DISPLAY_NAME, PR_TRANSMITABLE_DISPLAY_NAME_A, PR_TRANSMITABLE_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="e2781-107">PR_TRANSMITABLE_DISPLAY_NAME, PR_TRANSMITABLE_DISPLAY_NAME_A, PR_TRANSMITABLE_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="e2781-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e2781-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e2781-109">0x3A20</span><span class="sxs-lookup"><span data-stu-id="e2781-109">0x3A20</span></span>  <br/> |
|<span data-ttu-id="e2781-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="e2781-110">Data type:</span></span>  <br/> |<span data-ttu-id="e2781-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="e2781-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="e2781-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e2781-112">Area:</span></span>  <br/> |<span data-ttu-id="e2781-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="e2781-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2781-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2781-114">Remarks</span></span>

<span data-ttu-id="e2781-115">Essas propriedades devem ser implementadas por todos os provedores de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="e2781-115">These properties should be implemented by all address book providers.</span></span> <span data-ttu-id="e2781-116">Eles contêm a versão do nome de exibição do destinatário que é transmitida com a mensagem.</span><span class="sxs-lookup"><span data-stu-id="e2781-116">They contain the version of the recipient's display name that is transmitted with the message.</span></span> <span data-ttu-id="e2781-117">Para a maioria dos provedores de catálogo de endereços, essas propriedades têm o mesmo valor que a propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e2781-117">For most address book providers these properties have the same value as the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="e2781-118">Os provedores que não têm um nome de exibição seguro retornam PT_ERROR e MAPI altera o nome de exibição adicionando aspas ao redor do nome.</span><span class="sxs-lookup"><span data-stu-id="e2781-118">Providers that do not have a secure display name return PT_ERROR and MAPI changes the display name by adding quotation marks around the name.</span></span>
  
<span data-ttu-id="e2781-119">Um aplicativo cliente pode usar essa propriedade para impedir a alteração ou "falsificação" de entradas.</span><span class="sxs-lookup"><span data-stu-id="e2781-119">A client application can use this property to prevent alteration or "spoofing" of entries.</span></span> <span data-ttu-id="e2781-120">Um exemplo de falsificação é transmitir John Doe como John (o que é uma pessoa) Doe.</span><span class="sxs-lookup"><span data-stu-id="e2781-120">An example of spoofing is transmitting John Doe as John (What a Guy) Doe.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e2781-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e2781-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e2781-122">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="e2781-122">Protocol specifications</span></span>

<span data-ttu-id="e2781-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2781-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2781-124">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e2781-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e2781-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2781-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2781-126">Especifica as propriedades e operações de listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="e2781-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="e2781-127">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2781-127">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2781-128">Lida com as comunicações de um cliente com um servidor de interface de provedor de serviços de nome (NSPI).</span><span class="sxs-lookup"><span data-stu-id="e2781-128">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
<span data-ttu-id="e2781-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2781-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2781-130">Lida com a ordem e o fluxo para transferência de dados entre um cliente e um servidor.</span><span class="sxs-lookup"><span data-stu-id="e2781-130">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="e2781-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2781-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2781-132">Manipula objetos Message e Attachment.</span><span class="sxs-lookup"><span data-stu-id="e2781-132">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e2781-133">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e2781-133">Header files</span></span>

<span data-ttu-id="e2781-134">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e2781-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="e2781-135">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e2781-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="e2781-136">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="e2781-136">Mapitags.h</span></span>
  
> <span data-ttu-id="e2781-137">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="e2781-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e2781-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2781-138">See also</span></span>



[<span data-ttu-id="e2781-139">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e2781-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e2781-140">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="e2781-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e2781-141">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="e2781-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e2781-142">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="e2781-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

