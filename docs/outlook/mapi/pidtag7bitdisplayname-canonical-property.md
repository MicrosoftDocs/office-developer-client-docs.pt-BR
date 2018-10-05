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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401066"
---
# <a name="pidtag7bitdisplayname-canonical-property"></a><span data-ttu-id="78c9c-103">Propriedade canônica PidTag7BitDisplayName</span><span class="sxs-lookup"><span data-stu-id="78c9c-103">PidTag7BitDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="78c9c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78c9c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78c9c-105">Contém uma representação de ASCII de 7 bits de mensagens do nome de usuário.</span><span class="sxs-lookup"><span data-stu-id="78c9c-105">Contains a 7-bit ASCII representation of a messaging user's name.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="78c9c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="78c9c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="78c9c-107">PR_7BIT_DISPLAY_NAME, PR_7BIT_DISPLAY_NAME_A, PR_7BIT_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="78c9c-107">PR_7BIT_DISPLAY_NAME, PR_7BIT_DISPLAY_NAME_A, PR_7BIT_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="78c9c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="78c9c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="78c9c-109">0x39FF</span><span class="sxs-lookup"><span data-stu-id="78c9c-109">0x39FF</span></span>  <br/> |
|<span data-ttu-id="78c9c-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="78c9c-110">Data type:</span></span>  <br/> |<span data-ttu-id="78c9c-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="78c9c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="78c9c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="78c9c-112">Area:</span></span>  <br/> |<span data-ttu-id="78c9c-113">Catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="78c9c-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="78c9c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="78c9c-114">Remarks</span></span>

<span data-ttu-id="78c9c-115">Essas propriedades mapeiam a propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) em um conjunto de caracteres de 7 bits.</span><span class="sxs-lookup"><span data-stu-id="78c9c-115">These properties map the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property into a 7-bit character set.</span></span> <span data-ttu-id="78c9c-116">Alguns sistemas de mensagens, como a Internet e determinados links de x. 400, são limitados para o conjunto de código de ASCII de 7 bits de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="78c9c-116">Some messaging systems, such as Internet and certain X.400 links, are limited to the 128-character 7-bit ASCII code set.</span></span> <span data-ttu-id="78c9c-117">Gateways para tais sistemas de mensagens podem melhorar seu desempenho chamando o método [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) diretamente para recuperar esta propriedade, evitando processamento extra para conversão de código.</span><span class="sxs-lookup"><span data-stu-id="78c9c-117">Gateways to such messaging systems can improve their performance by calling the [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) method directly to retrieve the this property, thereby avoiding extra processing for code conversion.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="78c9c-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="78c9c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="78c9c-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="78c9c-119">Protocol specifications</span></span>

<span data-ttu-id="78c9c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="78c9c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="78c9c-121">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="78c9c-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="78c9c-122">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="78c9c-122">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="78c9c-123">Especifica as propriedades e operações em listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="78c9c-123">Specifies the properties and operations on lists of users, contacts, groups and resources.</span></span>
    
<span data-ttu-id="78c9c-124">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="78c9c-124">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="78c9c-125">Trata a comunicação do cliente com um servidor NSPI.</span><span class="sxs-lookup"><span data-stu-id="78c9c-125">Handles a client's communications with an NSPI server.</span></span>
    
<span data-ttu-id="78c9c-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="78c9c-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="78c9c-127">Manipula o fluxo de dados e a ordem que é usado para transferências de dados entre cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="78c9c-127">Handles the order and data flow that is used to transfers data between client and server.</span></span>
    
<span data-ttu-id="78c9c-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="78c9c-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="78c9c-129">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="78c9c-129">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="78c9c-130">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="78c9c-130">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="78c9c-131">Especifica as propriedades e operações que são permitidas em mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="78c9c-131">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="78c9c-132">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="78c9c-132">Header files</span></span>

<span data-ttu-id="78c9c-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="78c9c-133">Mapitags.h</span></span>
  
> <span data-ttu-id="78c9c-134">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="78c9c-134">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="78c9c-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="78c9c-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="78c9c-136">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="78c9c-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="78c9c-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="78c9c-137">See also</span></span>



[<span data-ttu-id="78c9c-138">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="78c9c-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="78c9c-139">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="78c9c-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="78c9c-140">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="78c9c-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="78c9c-141">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="78c9c-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

