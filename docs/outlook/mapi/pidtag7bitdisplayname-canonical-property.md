---
title: Propriedade canônica PidTag7BitDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTag7BitDisplayName
api_type:
- HeaderDef
ms.assetid: 803d7c4e-ed80-4d5b-988f-27068a8ccd63
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e5177d47749c2f60a883bd12fbba27045114c601
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315810"
---
# <a name="pidtag7bitdisplayname-canonical-property"></a><span data-ttu-id="5cfb2-103">Propriedade canônica PidTag7BitDisplayName</span><span class="sxs-lookup"><span data-stu-id="5cfb2-103">PidTag7BitDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="5cfb2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5cfb2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5cfb2-105">Contém uma representação ASCII de 7 bits do nome de um usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="5cfb2-105">Contains a 7-bit ASCII representation of a messaging user's name.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5cfb2-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="5cfb2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5cfb2-107">PR_7BIT_DISPLAY_NAME, PR_7BIT_DISPLAY_NAME_A, PR_7BIT_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="5cfb2-107">PR_7BIT_DISPLAY_NAME, PR_7BIT_DISPLAY_NAME_A, PR_7BIT_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="5cfb2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5cfb2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5cfb2-109">0x39FF</span><span class="sxs-lookup"><span data-stu-id="5cfb2-109">0x39FF</span></span>  <br/> |
|<span data-ttu-id="5cfb2-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="5cfb2-110">Data type:</span></span>  <br/> |<span data-ttu-id="5cfb2-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5cfb2-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5cfb2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5cfb2-112">Area:</span></span>  <br/> |<span data-ttu-id="5cfb2-113">Catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="5cfb2-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5cfb2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5cfb2-114">Remarks</span></span>

<span data-ttu-id="5cfb2-115">Essas propriedades mapeiam a propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) para um conjunto de caracteres de 7 bits.</span><span class="sxs-lookup"><span data-stu-id="5cfb2-115">These properties map the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property into a 7-bit character set.</span></span> <span data-ttu-id="5cfb2-116">Alguns sistemas de mensagens, como Internet e determinados links X. 400, estão limitados ao conjunto de códigos ASCII de 7 bits de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="5cfb2-116">Some messaging systems, such as Internet and certain X.400 links, are limited to the 128-character 7-bit ASCII code set.</span></span> <span data-ttu-id="5cfb2-117">Os gateways para sistemas de mensagens podem melhorar seu desempenho chamando o método [IAddrBook::P reparerecips](iaddrbook-preparerecips.md) diretamente para recuperar a propriedade, evitando assim o processamento adicional para a conversão de código.</span><span class="sxs-lookup"><span data-stu-id="5cfb2-117">Gateways to such messaging systems can improve their performance by calling the [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) method directly to retrieve the this property, thereby avoiding extra processing for code conversion.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5cfb2-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5cfb2-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5cfb2-119">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="5cfb2-119">Protocol specifications</span></span>

<span data-ttu-id="5cfb2-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5cfb2-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5cfb2-121">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5cfb2-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5cfb2-122">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5cfb2-122">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5cfb2-123">Especifica as propriedades e operações em listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="5cfb2-123">Specifies the properties and operations on lists of users, contacts, groups and resources.</span></span>
    
<span data-ttu-id="5cfb2-124">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5cfb2-124">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5cfb2-125">Lida com as comunicações de um cliente com um servidor NSPI.</span><span class="sxs-lookup"><span data-stu-id="5cfb2-125">Handles a client's communications with an NSPI server.</span></span>
    
<span data-ttu-id="5cfb2-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5cfb2-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5cfb2-127">Lida com a ordem e o fluxo de dados usados para transferir dados entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="5cfb2-127">Handles the order and data flow that is used to transfers data between client and server.</span></span>
    
<span data-ttu-id="5cfb2-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5cfb2-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5cfb2-129">Manipula objetos Message e Attachment.</span><span class="sxs-lookup"><span data-stu-id="5cfb2-129">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="5cfb2-130">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5cfb2-130">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5cfb2-131">Especifica as propriedades e as operações que são permitidas em mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="5cfb2-131">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5cfb2-132">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5cfb2-132">Header files</span></span>

<span data-ttu-id="5cfb2-133">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="5cfb2-133">Mapitags.h</span></span>
  
> <span data-ttu-id="5cfb2-134">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="5cfb2-134">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="5cfb2-135">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5cfb2-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="5cfb2-136">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="5cfb2-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5cfb2-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="5cfb2-137">See also</span></span>



[<span data-ttu-id="5cfb2-138">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5cfb2-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5cfb2-139">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="5cfb2-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5cfb2-140">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="5cfb2-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5cfb2-141">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="5cfb2-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

