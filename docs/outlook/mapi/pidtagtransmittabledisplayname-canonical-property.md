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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396880"
---
# <a name="pidtagtransmittabledisplayname-canonical-property"></a><span data-ttu-id="520e9-103">Propriedade canônica PidTagTransmittableDisplayName</span><span class="sxs-lookup"><span data-stu-id="520e9-103">PidTagTransmittableDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="520e9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="520e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="520e9-105">Contém o nome para exibição do destinatário em uma forma segura não pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="520e9-105">Contains a recipient's display name in a secure form that cannot be changed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="520e9-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="520e9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="520e9-107">PR_TRANSMITABLE_DISPLAY_NAME, PR_TRANSMITABLE_DISPLAY_NAME_A, PR_TRANSMITABLE_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="520e9-107">PR_TRANSMITABLE_DISPLAY_NAME, PR_TRANSMITABLE_DISPLAY_NAME_A, PR_TRANSMITABLE_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="520e9-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="520e9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="520e9-109">0x3A20</span><span class="sxs-lookup"><span data-stu-id="520e9-109">0x3A20</span></span>  <br/> |
|<span data-ttu-id="520e9-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="520e9-110">Data type:</span></span>  <br/> |<span data-ttu-id="520e9-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="520e9-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="520e9-112">Área:</span><span class="sxs-lookup"><span data-stu-id="520e9-112">Area:</span></span>  <br/> |<span data-ttu-id="520e9-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="520e9-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="520e9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="520e9-114">Remarks</span></span>

<span data-ttu-id="520e9-115">Essas propriedades devem ser implementadas por todos os provedores de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="520e9-115">These properties should be implemented by all address book providers.</span></span> <span data-ttu-id="520e9-116">Elas contêm a versão do nome de exibição do destinatário que é transmitido com a mensagem.</span><span class="sxs-lookup"><span data-stu-id="520e9-116">They contain the version of the recipient's display name that is transmitted with the message.</span></span> <span data-ttu-id="520e9-117">Essas propriedades não tem o mesmo valor que a propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) para a maioria dos provedores de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="520e9-117">For most address book providers these properties have the same value as the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="520e9-118">Provedores que não têm um nome de exibição seguro retornar o nome de exibição de alterações PT_ERROR e MAPI adicionando o nome entre aspas.</span><span class="sxs-lookup"><span data-stu-id="520e9-118">Providers that do not have a secure display name return PT_ERROR and MAPI changes the display name by adding quotation marks around the name.</span></span>
  
<span data-ttu-id="520e9-119">Um aplicativo cliente pode usar essa propriedade para impedir que a alteração ou "falsificação" de entradas.</span><span class="sxs-lookup"><span data-stu-id="520e9-119">A client application can use this property to prevent alteration or "spoofing" of entries.</span></span> <span data-ttu-id="520e9-120">Um exemplo de falsificação está transmitindo Carlos Grilo como (o que um Guy) de John Doe.</span><span class="sxs-lookup"><span data-stu-id="520e9-120">An example of spoofing is transmitting John Doe as John (What a Guy) Doe.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="520e9-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="520e9-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="520e9-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="520e9-122">Protocol specifications</span></span>

<span data-ttu-id="520e9-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="520e9-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="520e9-124">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="520e9-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="520e9-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="520e9-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="520e9-126">Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="520e9-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="520e9-127">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="520e9-127">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="520e9-128">Trata a comunicação do cliente com um servidor de nome serviço provedor NSPI (Interface).</span><span class="sxs-lookup"><span data-stu-id="520e9-128">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
<span data-ttu-id="520e9-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="520e9-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="520e9-130">Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="520e9-130">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="520e9-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="520e9-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="520e9-132">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="520e9-132">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="520e9-133">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="520e9-133">Header files</span></span>

<span data-ttu-id="520e9-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="520e9-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="520e9-135">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="520e9-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="520e9-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="520e9-136">Mapitags.h</span></span>
  
> <span data-ttu-id="520e9-137">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="520e9-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="520e9-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="520e9-138">See also</span></span>



[<span data-ttu-id="520e9-139">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="520e9-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="520e9-140">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="520e9-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="520e9-141">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="520e9-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="520e9-142">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="520e9-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

