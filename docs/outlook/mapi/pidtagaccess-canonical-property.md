---
title: Propriedade canônica PidTagAccess
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccess
api_type:
- HeaderDef
ms.assetid: 8c8a882e-62c1-4c57-8c63-ee5849f656b0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b453a7b0cfa04dd94da01089573427a931fb4d4f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398336"
---
# <a name="pidtagaccess-canonical-property"></a><span data-ttu-id="4301b-103">Propriedade canônica PidTagAccess</span><span class="sxs-lookup"><span data-stu-id="4301b-103">PidTagAccess Canonical Property</span></span>

  
  
<span data-ttu-id="4301b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4301b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4301b-105">Contém uma bitmask dos sinalizadores indicando as operações que estão disponíveis para o cliente para o objeto.</span><span class="sxs-lookup"><span data-stu-id="4301b-105">Contains a bitmask of flags indicating the operations that are available to the client for the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4301b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="4301b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4301b-107">PR_ACCESS</span><span class="sxs-lookup"><span data-stu-id="4301b-107">PR_ACCESS</span></span>  <br/> |
|<span data-ttu-id="4301b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4301b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4301b-109">0x0FF4</span><span class="sxs-lookup"><span data-stu-id="4301b-109">0x0FF4</span></span>  <br/> |
|<span data-ttu-id="4301b-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="4301b-110">Data type:</span></span>  <br/> |<span data-ttu-id="4301b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4301b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4301b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4301b-112">Area:</span></span>  <br/> |<span data-ttu-id="4301b-113">Propriedades de controle de acesso</span><span class="sxs-lookup"><span data-stu-id="4301b-113">Access Control Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4301b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4301b-114">Remarks</span></span>

<span data-ttu-id="4301b-115">Essa propriedade é somente leitura para o cliente.</span><span class="sxs-lookup"><span data-stu-id="4301b-115">This property is read-only for the client.</span></span> <span data-ttu-id="4301b-116">Ele deve ser um bit a bit **ou** de zero ou mais valores da tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4301b-116">It must be a bitwise **OR** of zero or more values from the following table.</span></span> 
  
|<span data-ttu-id="4301b-117">**Name**</span><span class="sxs-lookup"><span data-stu-id="4301b-117">**Name**</span></span>|<span data-ttu-id="4301b-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="4301b-118">**Value**</span></span>|<span data-ttu-id="4301b-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4301b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4301b-120">MAPI_ACCESS_MODIFY</span><span class="sxs-lookup"><span data-stu-id="4301b-120">MAPI_ACCESS_MODIFY</span></span>  <br/> |<span data-ttu-id="4301b-121">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4301b-121">0x00000001</span></span>  <br/> |<span data-ttu-id="4301b-122">Gravação</span><span class="sxs-lookup"><span data-stu-id="4301b-122">Write</span></span>  <br/> |
|<span data-ttu-id="4301b-123">MAPI_ACCESS_READ</span><span class="sxs-lookup"><span data-stu-id="4301b-123">MAPI_ACCESS_READ</span></span>  <br/> |<span data-ttu-id="4301b-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="4301b-124">0x00000002</span></span>  <br/> |<span data-ttu-id="4301b-125">Read</span><span class="sxs-lookup"><span data-stu-id="4301b-125">Read</span></span>  <br/> |
|<span data-ttu-id="4301b-126">MAPI_ACCESS_DELETE</span><span class="sxs-lookup"><span data-stu-id="4301b-126">MAPI_ACCESS_DELETE</span></span>  <br/> |<span data-ttu-id="4301b-127">0x00000004</span><span class="sxs-lookup"><span data-stu-id="4301b-127">0x00000004</span></span>  <br/> |<span data-ttu-id="4301b-128">Delete</span><span class="sxs-lookup"><span data-stu-id="4301b-128">Delete</span></span>  <br/> |
|<span data-ttu-id="4301b-129">MAPI_ACCESS_CREATE_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="4301b-129">MAPI_ACCESS_CREATE_HIERARCHY</span></span>  <br/> |<span data-ttu-id="4301b-130">0x00000008</span><span class="sxs-lookup"><span data-stu-id="4301b-130">0x00000008</span></span>  <br/> |<span data-ttu-id="4301b-131">Criar subpastas na hierarquia de pastas</span><span class="sxs-lookup"><span data-stu-id="4301b-131">Create subfolders in the folder hierarchy</span></span>  <br/> |
|<span data-ttu-id="4301b-132">MAPI_ACCESS_CREATE_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="4301b-132">MAPI_ACCESS_CREATE_CONTENTS</span></span>  <br/> |<span data-ttu-id="4301b-133">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4301b-133">0x00000010</span></span>  <br/> |<span data-ttu-id="4301b-134">Criar as mensagens de conteúdo</span><span class="sxs-lookup"><span data-stu-id="4301b-134">Create content messages</span></span>  <br/> |
|<span data-ttu-id="4301b-135">MAPI_ACCESS_CREATE_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="4301b-135">MAPI_ACCESS_CREATE_ASSOCIATED</span></span>  <br/> |<span data-ttu-id="4301b-136">0x00000020</span><span class="sxs-lookup"><span data-stu-id="4301b-136">0x00000020</span></span>  <br/> |<span data-ttu-id="4301b-137">Criar mensagens associadas de conteúdo</span><span class="sxs-lookup"><span data-stu-id="4301b-137">Create associated content messages</span></span>  <br/> |
   
<span data-ttu-id="4301b-138">Os sinalizadores MAPI_ACCESS_DELETE, MAPI_ACCESS_MODIFY e MAPI_ACCESS_READ são encontrados na pasta e objetos de mensagem e na coluna **PR_ACCESS** em tabelas de conteúdo e de conteúdo associado.</span><span class="sxs-lookup"><span data-stu-id="4301b-138">The MAPI_ACCESS_DELETE, MAPI_ACCESS_MODIFY, and MAPI_ACCESS_READ flags are found on folder and message objects and in the **PR_ACCESS** column in contents tables and associated contents tables.</span></span> <span data-ttu-id="4301b-139">Os sinalizadores MAPI_ACCESS_CREATE_ASSOCIATED, MAPI_ACCESS_CREATE_CONTENTS e MAPI_ACCESS_CREATE_HIERARCHY são encontrados em apenas os objetos de pasta.</span><span class="sxs-lookup"><span data-stu-id="4301b-139">The MAPI_ACCESS_CREATE_ASSOCIATED, MAPI_ACCESS_CREATE_CONTENTS, and MAPI_ACCESS_CREATE_HIERARCHY flags are found on folder objects only.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4301b-140">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4301b-140">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4301b-141">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="4301b-141">Protocol specifications</span></span>

<span data-ttu-id="4301b-142">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4301b-142">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4301b-143">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="4301b-143">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4301b-144">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4301b-144">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4301b-145">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="4301b-145">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4301b-146">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4301b-146">Header files</span></span>

<span data-ttu-id="4301b-147">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4301b-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="4301b-148">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="4301b-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="4301b-149">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4301b-149">Mapitags.h</span></span>
  
> <span data-ttu-id="4301b-150">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="4301b-150">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4301b-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="4301b-151">See also</span></span>



[<span data-ttu-id="4301b-152">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4301b-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4301b-153">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="4301b-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4301b-154">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="4301b-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4301b-155">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="4301b-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

