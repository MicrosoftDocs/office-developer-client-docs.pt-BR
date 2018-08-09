---
title: Propriedade canônica PidTagFolderType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderType
api_type:
- HeaderDef
ms.assetid: 2ab4681e-0013-4ba0-ba26-50517bbf3f5b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2520a7544eb4ba39cd83a7a0aa65b98bd8a67deb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769250"
---
# <a name="pidtagfoldertype-canonical-property"></a><span data-ttu-id="ad186-103">Propriedade canônica PidTagFolderType</span><span class="sxs-lookup"><span data-stu-id="ad186-103">PidTagFolderType Canonical Property</span></span>

  
  
<span data-ttu-id="ad186-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ad186-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ad186-105">Contém uma constante que indica o tipo de pasta.</span><span class="sxs-lookup"><span data-stu-id="ad186-105">Contains a constant that indicates the folder type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ad186-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="ad186-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ad186-107">PR_FOLDER_TYPE</span><span class="sxs-lookup"><span data-stu-id="ad186-107">PR_FOLDER_TYPE</span></span>  <br/> |
|<span data-ttu-id="ad186-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ad186-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ad186-109">0x3601</span><span class="sxs-lookup"><span data-stu-id="ad186-109">0x3601</span></span>  <br/> |
|<span data-ttu-id="ad186-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="ad186-110">Data type:</span></span>  <br/> |<span data-ttu-id="ad186-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ad186-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ad186-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ad186-112">Area:</span></span>  <br/> |<span data-ttu-id="ad186-113">Contêiner MAPI</span><span class="sxs-lookup"><span data-stu-id="ad186-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ad186-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ad186-114">Remarks</span></span>

<span data-ttu-id="ad186-115">Essa propriedade pode ter exatamente um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="ad186-115">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="ad186-116">FOLDER_GENERIC</span><span class="sxs-lookup"><span data-stu-id="ad186-116">FOLDER_GENERIC</span></span> 
  
> <span data-ttu-id="ad186-117">Uma pasta genérica que contém mensagens e outras pastas.</span><span class="sxs-lookup"><span data-stu-id="ad186-117">A generic folder that contains messages and other folders.</span></span>
    
<span data-ttu-id="ad186-118">FOLDER_ROOT</span><span class="sxs-lookup"><span data-stu-id="ad186-118">FOLDER_ROOT</span></span> 
  
> <span data-ttu-id="ad186-119">A pasta raiz da tabela de hierarquia de pasta, ou seja, uma pasta que não tenha nenhuma pasta pai.</span><span class="sxs-lookup"><span data-stu-id="ad186-119">The root folder of the folder hierarchy table, that is, a folder that has no parent folder.</span></span>
    
<span data-ttu-id="ad186-120">FOLDER_SEARCH</span><span class="sxs-lookup"><span data-stu-id="ad186-120">FOLDER_SEARCH</span></span> 
  
> <span data-ttu-id="ad186-121">Uma pasta que contém os resultados de uma pesquisa, na forma de links para mensagens que atendam aos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ad186-121">A folder that contains the results of a search, in the form of links to messages that meet search criteria.</span></span>
    
<span data-ttu-id="ad186-122">A raiz de um armazenamento de mensagens não deve ser confundida com a raiz da subárvore interpessoais mensagens (IPM) desse repositório.</span><span class="sxs-lookup"><span data-stu-id="ad186-122">The root of a message store should not be confused with the root of the interpersonal message (IPM) subtree in that store.</span></span> <span data-ttu-id="ad186-123">Pasta raiz da loja, o que não tem um pai, é obtida chamando o método [IMsgStore::OpenEntry](imsgstore-openentry.md) com um identificador de entrada nulo.</span><span class="sxs-lookup"><span data-stu-id="ad186-123">The store's root folder, which has no parent, is obtained by calling the [IMsgStore::OpenEntry](imsgstore-openentry.md) method with a null entry identifier.</span></span> <span data-ttu-id="ad186-124">Pasta raiz do subárvore IPM, que tem um pai, é obtida usando-se o valor da propriedade **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) para a chamada **OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="ad186-124">The IPM subtree's root folder, which does have a parent, is obtained by using the value of the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property for the **OpenEntry** call.</span></span> 
  
<span data-ttu-id="ad186-125">MAPI permite que apenas uma pasta raiz por repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="ad186-125">MAPI allows only one root folder per message store.</span></span> <span data-ttu-id="ad186-126">Essa pasta contém mensagens e outras pastas.</span><span class="sxs-lookup"><span data-stu-id="ad186-126">This folder contains messages and other folders.</span></span> <span data-ttu-id="ad186-127">Propriedade de **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) da pasta raiz contém o identificador de entrada da pasta.</span><span class="sxs-lookup"><span data-stu-id="ad186-127">The root folder's **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) property contains the folder's own entry identifier.</span></span>
  
<span data-ttu-id="ad186-128">As informações em uma pasta de resultados de pesquisa principalmente são armazenadas em sua tabela de conteúdo, que contém as mesmas colunas como uma tabela de conteúdo típico, bem como duas colunas adicionais que identifica a pasta na qual cada mensagem foi encontrada: **PR_PARENT_DISPLAY** ([ PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) (exibir o nome, necessário) e essa propriedade (identificador entrada, opcional).</span><span class="sxs-lookup"><span data-stu-id="ad186-128">The information in a search-results folder is mainly stored in its contents table, which contains the same columns as a typical contents table, as well as two extra columns identifying the folder in which each message was found: **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) (display name, required) and this property (entry identifier, optional).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ad186-129">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ad186-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ad186-130">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="ad186-130">Protocol specifications</span></span>

<span data-ttu-id="ad186-131">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ad186-131">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ad186-132">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ad186-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ad186-133">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ad186-133">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ad186-134">Trata as operações de pasta.</span><span class="sxs-lookup"><span data-stu-id="ad186-134">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ad186-135">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ad186-135">Header files</span></span>

<span data-ttu-id="ad186-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ad186-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="ad186-137">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ad186-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="ad186-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ad186-138">Mapitags.h</span></span>
  
> <span data-ttu-id="ad186-139">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="ad186-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ad186-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="ad186-140">See also</span></span>



[<span data-ttu-id="ad186-141">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ad186-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ad186-142">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="ad186-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ad186-143">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="ad186-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ad186-144">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="ad186-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

