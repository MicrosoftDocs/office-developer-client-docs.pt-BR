---
title: Propriedade canônica PidTagOriginalSubject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSubject
api_type:
- COM
ms.assetid: 8668ba4f-3236-4a87-a5aa-9cf7eea3d87b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: de957c33165cc96eec82bf95c8f292c5b323676a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331140"
---
# <a name="pidtagoriginalsubject-canonical-property"></a><span data-ttu-id="d9a09-103">Propriedade canônica PidTagOriginalSubject</span><span class="sxs-lookup"><span data-stu-id="d9a09-103">PidTagOriginalSubject Canonical Property</span></span>

  
  
<span data-ttu-id="d9a09-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9a09-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9a09-105">Contém o assunto de uma mensagem original para uso em um relatório sobre a mensagem.</span><span class="sxs-lookup"><span data-stu-id="d9a09-105">Contains the subject of an original message for use in a report about the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d9a09-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="d9a09-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d9a09-107">PR_ORIGINAL_SUBJECT, PR_ORIGINAL_SUBJECT_A, PR_ORIGINAL_SUBJECT_W</span><span class="sxs-lookup"><span data-stu-id="d9a09-107">PR_ORIGINAL_SUBJECT, PR_ORIGINAL_SUBJECT_A, PR_ORIGINAL_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="d9a09-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d9a09-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d9a09-109">0x0049</span><span class="sxs-lookup"><span data-stu-id="d9a09-109">0x0049</span></span>  <br/> |
|<span data-ttu-id="d9a09-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="d9a09-110">Data type:</span></span>  <br/> |<span data-ttu-id="d9a09-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d9a09-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d9a09-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d9a09-112">Area:</span></span>  <br/> |<span data-ttu-id="d9a09-113">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="d9a09-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d9a09-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d9a09-114">Remarks</span></span>

<span data-ttu-id="d9a09-115">Essas propriedades são originalmente definidas com o mesmo valor que a **propriedade PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d9a09-115">These properties are originally set to the same value as the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="d9a09-116">As propriedades de assunto são normalmente pequenas cadeias de caracteres com menos de 256 caracteres, e um provedor de armazenamento de mensagens não é obrigado a dar suporte à interface **IStream** de vinculação e incorporação de objetos (OLE) neles.</span><span class="sxs-lookup"><span data-stu-id="d9a09-116">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the Object Linking and Embedding (OLE) **IStream** interface on them.</span></span> <span data-ttu-id="d9a09-117">O cliente deve sempre tentar acessar pela interface **IMAPIProp** primeiro e recorrer a **IStream** somente **se** MAPI_E_NOT_ENOUGH_MEMORY for retornado.</span><span class="sxs-lookup"><span data-stu-id="d9a09-117">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d9a09-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d9a09-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d9a09-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="d9a09-119">Protocol specifications</span></span>

<span data-ttu-id="d9a09-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9a09-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9a09-121">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d9a09-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d9a09-122">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9a09-122">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9a09-123">Lida com a sincronização de dados de objeto de mensagens entre um servidor e um cliente.</span><span class="sxs-lookup"><span data-stu-id="d9a09-123">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="d9a09-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9a09-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9a09-125">Especifica as propriedades e operações permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="d9a09-125">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d9a09-126">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="d9a09-126">Header files</span></span>

<span data-ttu-id="d9a09-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d9a09-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="d9a09-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d9a09-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="d9a09-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d9a09-129">Mapitags.h</span></span>
  
> <span data-ttu-id="d9a09-130">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="d9a09-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d9a09-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="d9a09-131">See also</span></span>



[<span data-ttu-id="d9a09-132">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d9a09-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d9a09-133">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="d9a09-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d9a09-134">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="d9a09-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d9a09-135">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="d9a09-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

