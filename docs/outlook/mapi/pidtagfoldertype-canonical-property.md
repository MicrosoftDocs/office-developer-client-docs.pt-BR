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
ms.openlocfilehash: 7cca884eae2111a94d87cc24a6d30542148ab845
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316314"
---
# <a name="pidtagfoldertype-canonical-property"></a><span data-ttu-id="6c2ab-103">Propriedade canônica PidTagFolderType</span><span class="sxs-lookup"><span data-stu-id="6c2ab-103">PidTagFolderType Canonical Property</span></span>

  
  
<span data-ttu-id="6c2ab-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c2ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c2ab-105">Contém uma constante que indica o tipo de pasta.</span><span class="sxs-lookup"><span data-stu-id="6c2ab-105">Contains a constant that indicates the folder type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6c2ab-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="6c2ab-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6c2ab-107">PR_FOLDER_TYPE</span><span class="sxs-lookup"><span data-stu-id="6c2ab-107">PR_FOLDER_TYPE</span></span>  <br/> |
|<span data-ttu-id="6c2ab-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="6c2ab-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6c2ab-109">0x3601</span><span class="sxs-lookup"><span data-stu-id="6c2ab-109">0x3601</span></span>  <br/> |
|<span data-ttu-id="6c2ab-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="6c2ab-110">Data type:</span></span>  <br/> |<span data-ttu-id="6c2ab-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6c2ab-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6c2ab-112">Área:</span><span class="sxs-lookup"><span data-stu-id="6c2ab-112">Area:</span></span>  <br/> |<span data-ttu-id="6c2ab-113">Contêiner MAPI</span><span class="sxs-lookup"><span data-stu-id="6c2ab-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c2ab-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c2ab-114">Remarks</span></span>

<span data-ttu-id="6c2ab-115">Essa propriedade pode ter exatamente um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="6c2ab-115">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="6c2ab-116">FOLDER_GENERIC</span><span class="sxs-lookup"><span data-stu-id="6c2ab-116">FOLDER_GENERIC</span></span> 
  
> <span data-ttu-id="6c2ab-117">Uma pasta genérica que contém mensagens e outras pastas.</span><span class="sxs-lookup"><span data-stu-id="6c2ab-117">A generic folder that contains messages and other folders.</span></span>
    
<span data-ttu-id="6c2ab-118">FOLDER_ROOT</span><span class="sxs-lookup"><span data-stu-id="6c2ab-118">FOLDER_ROOT</span></span> 
  
> <span data-ttu-id="6c2ab-119">A pasta raiz da tabela de hierarquia de pastas, ou seja, uma pasta que não tem uma pasta pai.</span><span class="sxs-lookup"><span data-stu-id="6c2ab-119">The root folder of the folder hierarchy table, that is, a folder that has no parent folder.</span></span>
    
<span data-ttu-id="6c2ab-120">FOLDER_SEARCH</span><span class="sxs-lookup"><span data-stu-id="6c2ab-120">FOLDER_SEARCH</span></span> 
  
> <span data-ttu-id="6c2ab-121">Uma pasta que contém os resultados de uma pesquisa, na forma de links para mensagens que atendem aos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="6c2ab-121">A folder that contains the results of a search, in the form of links to messages that meet search criteria.</span></span>
    
<span data-ttu-id="6c2ab-122">A raiz de um repositório de mensagens não deve ser confundida com a raiz da sub-árvore da mensagem interpessoal (IPM) nesse repositório.</span><span class="sxs-lookup"><span data-stu-id="6c2ab-122">The root of a message store should not be confused with the root of the interpersonal message (IPM) subtree in that store.</span></span> <span data-ttu-id="6c2ab-123">A pasta raiz do repositório, que não tem um pai, é obtida chamando o método [IMsgStore:: OpenEntry](imsgstore-openentry.md) com um identificador de entrada nulo.</span><span class="sxs-lookup"><span data-stu-id="6c2ab-123">The store's root folder, which has no parent, is obtained by calling the [IMsgStore::OpenEntry](imsgstore-openentry.md) method with a null entry identifier.</span></span> <span data-ttu-id="6c2ab-124">A pasta raiz da sub-árvore IPM, que tem um pai, é obtida usando o valor da propriedade **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) para a chamada **OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="6c2ab-124">The IPM subtree's root folder, which does have a parent, is obtained by using the value of the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property for the **OpenEntry** call.</span></span> 
  
<span data-ttu-id="6c2ab-125">MAPI permite apenas uma pasta raiz por repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="6c2ab-125">MAPI allows only one root folder per message store.</span></span> <span data-ttu-id="6c2ab-126">Esta pasta contém mensagens e outras pastas.</span><span class="sxs-lookup"><span data-stu-id="6c2ab-126">This folder contains messages and other folders.</span></span> <span data-ttu-id="6c2ab-127">A propriedade **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) da pasta raiz contém o próprio identificador de entrada da pasta.</span><span class="sxs-lookup"><span data-stu-id="6c2ab-127">The root folder's **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) property contains the folder's own entry identifier.</span></span>
  
<span data-ttu-id="6c2ab-128">As informações em uma pasta de resultados de pesquisa são principalmente armazenadas na tabela de conteúdo, que contém as mesmas colunas de uma tabela de conteúdo típica, bem como duas colunas extras que identificam a pasta na qual cada mensagem foi encontrada: **PR_PARENT_DISPLAY** ([ PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) (nome para exibição, obrigatório) e essa propriedade (identificador de entrada, opcional).</span><span class="sxs-lookup"><span data-stu-id="6c2ab-128">The information in a search-results folder is mainly stored in its contents table, which contains the same columns as a typical contents table, as well as two extra columns identifying the folder in which each message was found: **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) (display name, required) and this property (entry identifier, optional).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6c2ab-129">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6c2ab-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6c2ab-130">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="6c2ab-130">Protocol specifications</span></span>

<span data-ttu-id="6c2ab-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c2ab-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c2ab-132">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6c2ab-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6c2ab-133">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c2ab-133">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c2ab-134">Controla as operações da pasta.</span><span class="sxs-lookup"><span data-stu-id="6c2ab-134">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6c2ab-135">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6c2ab-135">Header files</span></span>

<span data-ttu-id="6c2ab-136">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="6c2ab-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="6c2ab-137">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="6c2ab-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="6c2ab-138">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="6c2ab-138">Mapitags.h</span></span>
  
> <span data-ttu-id="6c2ab-139">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="6c2ab-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6c2ab-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c2ab-140">See also</span></span>



[<span data-ttu-id="6c2ab-141">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6c2ab-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6c2ab-142">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="6c2ab-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6c2ab-143">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="6c2ab-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6c2ab-144">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="6c2ab-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

