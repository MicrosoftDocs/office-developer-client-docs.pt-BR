---
title: Propriedade canônica PidTagContainerFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerFlags
api_type:
- HeaderDef
ms.assetid: 66b8d333-227e-464d-8cf9-cd8a5ff15efb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c9c446097213e5b743a47ec32db17ec0afe63b78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357544"
---
# <a name="pidtagcontainerflags-canonical-property"></a><span data-ttu-id="1edc5-103">Propriedade canônica PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="1edc5-103">PidTagContainerFlags Canonical Property</span></span>

  
  
<span data-ttu-id="1edc5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1edc5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1edc5-105">Contém uma bitmask de sinalizadores que descrevem os recursos de um contêiner de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="1edc5-105">Contains a bitmask of flags describing capabilities of an address book container.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1edc5-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="1edc5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1edc5-107">PR_CONTAINER_FLAGS</span><span class="sxs-lookup"><span data-stu-id="1edc5-107">PR_CONTAINER_FLAGS</span></span>  <br/> |
|<span data-ttu-id="1edc5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1edc5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1edc5-109">0x3600</span><span class="sxs-lookup"><span data-stu-id="1edc5-109">0x3600</span></span>  <br/> |
|<span data-ttu-id="1edc5-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="1edc5-110">Data type:</span></span>  <br/> |<span data-ttu-id="1edc5-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1edc5-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1edc5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1edc5-112">Area:</span></span>  <br/> |<span data-ttu-id="1edc5-113">Catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="1edc5-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1edc5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1edc5-114">Remarks</span></span>

<span data-ttu-id="1edc5-115">Um ou mais dos seguintes sinalizadores podem ser definidos para a bitmask:</span><span class="sxs-lookup"><span data-stu-id="1edc5-115">One or more of the following flags can be set for the bitmask:</span></span>
  
<span data-ttu-id="1edc5-116">AB_FIND_ON_OPEN</span><span class="sxs-lookup"><span data-stu-id="1edc5-116">AB_FIND_ON_OPEN</span></span> 
  
> <span data-ttu-id="1edc5-117">Exibe uma caixa de diálogo para solicitar uma restrição antes de exibir qualquer conteúdo do contêiner.</span><span class="sxs-lookup"><span data-stu-id="1edc5-117">Displays a dialog box to request a restriction before displaying any contents of the container.</span></span> 
    
<span data-ttu-id="1edc5-118">AB_MODIFIABLE</span><span class="sxs-lookup"><span data-stu-id="1edc5-118">AB_MODIFIABLE</span></span> 
  
> <span data-ttu-id="1edc5-119">As entradas podem ser adicionadas e removidas do contêiner.</span><span class="sxs-lookup"><span data-stu-id="1edc5-119">Entries can be added to and removed from the container.</span></span> <span data-ttu-id="1edc5-120">Este sinalizador não indica se qualquer entrada no contêiner pode ser modificada.</span><span class="sxs-lookup"><span data-stu-id="1edc5-120">This flag does not indicate whether any entries in the container can be modified.</span></span>
    
<span data-ttu-id="1edc5-121">AB_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="1edc5-121">AB_RECIPIENTS</span></span> 
  
> <span data-ttu-id="1edc5-122">O contêiner pode conter destinatários.</span><span class="sxs-lookup"><span data-stu-id="1edc5-122">The container can hold recipients.</span></span> <span data-ttu-id="1edc5-123">Este sinalizador não indica se algum destinatário está realmente presente no contêiner ou se pode ser adicionado ou removido.</span><span class="sxs-lookup"><span data-stu-id="1edc5-123">This flag does not indicate whether any recipients are actually present in the container, or whether they can be added or removed.</span></span> 
    
<span data-ttu-id="1edc5-124">AB_SUBCONTAINERS</span><span class="sxs-lookup"><span data-stu-id="1edc5-124">AB_SUBCONTAINERS</span></span> 
  
> <span data-ttu-id="1edc5-125">O contêiner pode conter contêineres filhos.</span><span class="sxs-lookup"><span data-stu-id="1edc5-125">The container can hold child containers.</span></span> <span data-ttu-id="1edc5-126">Este sinalizador não indica se os sub-recipientes estão realmente presentes no contêiner, nem se eles podem ser adicionados ou removidos.</span><span class="sxs-lookup"><span data-stu-id="1edc5-126">This flag does not indicate whether any subcontainers are actually present in the container, nor whether they can be added or removed.</span></span> <span data-ttu-id="1edc5-127">AB_SUBCONTAINERS deve ser definido para o contêiner para dar suporte a [IMAPIContainer::](imapicontainer-gethierarchytable.md)GetHierarchyTable.</span><span class="sxs-lookup"><span data-stu-id="1edc5-127">AB_SUBCONTAINERS must be set for the container to support [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md).</span></span> 
    
<span data-ttu-id="1edc5-128">AB_UNMODIFIABLE</span><span class="sxs-lookup"><span data-stu-id="1edc5-128">AB_UNMODIFIABLE</span></span> 
  
> <span data-ttu-id="1edc5-129">As entradas não podem ser adicionadas ou removidas do contêiner.</span><span class="sxs-lookup"><span data-stu-id="1edc5-129">Entries cannot be added to or removed from the container.</span></span> <span data-ttu-id="1edc5-130">Este sinalizador não indica se qualquer entrada no contêiner pode ser modificada.</span><span class="sxs-lookup"><span data-stu-id="1edc5-130">This flag does not indicate whether any entries in the container can be modified.</span></span> 
    
<span data-ttu-id="1edc5-131">O sinalizador AB_FIND_ON_OPEN é altamente recomendado para contêineres usados com serviços online ou com conexões lentas com os servidores.</span><span class="sxs-lookup"><span data-stu-id="1edc5-131">The AB_FIND_ON_OPEN flag is highly recommended for containers used with online services or with slow connections to servers.</span></span> <span data-ttu-id="1edc5-132">Quando um contêiner é aberto com AB_FIND_ON_OPEN definido, uma caixa de diálogo **Localizar** é apresentada ao usuário para restringir os usuários de mensagens exibidos.</span><span class="sxs-lookup"><span data-stu-id="1edc5-132">When a container is opened that has AB_FIND_ON_OPEN set, a **Find** dialog box is presented to the user to restrict the displayed messaging users.</span></span> <span data-ttu-id="1edc5-133">Mesmo uma especificação parcial limitar os usuários de mensagens pode acelerar drasticamente uma exibição do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="1edc5-133">Even a partial specification limiting the messaging users can dramatically speed up a display of the contents.</span></span> 
  
<span data-ttu-id="1edc5-134">O sinalizador AB_MODIFIABLE ou AB_UNMODIFIABLE deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="1edc5-134">Either the AB_MODIFIABLE or AB_UNMODIFIABLE flag must be set.</span></span> <span data-ttu-id="1edc5-135">Ambos os sinalizadores podem ser definidos para indicar que o contêiner não sabe se pode ser modificado ou não, por exemplo, se a modificação depender dos direitos de acesso do usuário.</span><span class="sxs-lookup"><span data-stu-id="1edc5-135">Both flags can be set to indicate that the container does not know whether it can be modified or not, for example if modification depends on the user's access rights.</span></span> <span data-ttu-id="1edc5-136">Nesse caso, um aplicativo cliente deve tentar uma chamada e examinar o código de retorno para determinar os recursos do contêiner.</span><span class="sxs-lookup"><span data-stu-id="1edc5-136">In this case, a client application must attempt a call and examine the return code to determine the container's capabilities.</span></span> <span data-ttu-id="1edc5-137">Um cliente geralmente começa examinando AB_MODIFIABLE.</span><span class="sxs-lookup"><span data-stu-id="1edc5-137">A client typically starts by examining AB_MODIFIABLE.</span></span> <span data-ttu-id="1edc5-138">Se estiver definida, o cliente faz uma chamada que tenta modificar o contêiner e verifica o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="1edc5-138">If it is set, the client makes a call that attempts to modify the container and checks the return value.</span></span> 
  
<span data-ttu-id="1edc5-139">O sinalizador AB_MODIFIABLE não indica quais tipos de entradas podem ser adicionadas ao contêiner.</span><span class="sxs-lookup"><span data-stu-id="1edc5-139">The AB_MODIFIABLE flag does not indicate what types of entries can be added to the container.</span></span> <span data-ttu-id="1edc5-140">Para determinar isso, o cliente deve usar o método [OpenProperty](imapiprop-openproperty.md) apropriado para abrir a propriedade **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) do contêiner.</span><span class="sxs-lookup"><span data-stu-id="1edc5-140">To determine this, the client should use the appropriate [OpenProperty](imapiprop-openproperty.md) method to open the container's **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> <span data-ttu-id="1edc5-141">A abertura de **PR_CREATE_TEMPLATES** faz com que a tabela única do contêiner seja retornada, listando os tipos de entradas que podem ser criados no contêiner.</span><span class="sxs-lookup"><span data-stu-id="1edc5-141">Opening **PR_CREATE_TEMPLATES** causes the container's one-off table to be returned, listing the kinds of entries that can be created in the container.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1edc5-142">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1edc5-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1edc5-143">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="1edc5-143">Protocol specifications</span></span>

<span data-ttu-id="1edc5-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1edc5-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1edc5-145">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1edc5-145">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1edc5-146">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1edc5-146">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1edc5-147">Especifica as propriedades e operações de listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="1edc5-147">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="1edc5-148">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1edc5-148">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1edc5-149">Lida com as comunicações de um cliente com um servidor de interface de provedor de serviços de nome (NSPI).</span><span class="sxs-lookup"><span data-stu-id="1edc5-149">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1edc5-150">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1edc5-150">Header files</span></span>

<span data-ttu-id="1edc5-151">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="1edc5-151">Mapidefs.h</span></span>
  
> <span data-ttu-id="1edc5-152">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="1edc5-152">Provides data type definitions.</span></span>
    
<span data-ttu-id="1edc5-153">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="1edc5-153">Mapitags.h</span></span>
  
> <span data-ttu-id="1edc5-154">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="1edc5-154">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1edc5-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="1edc5-155">See also</span></span>



[<span data-ttu-id="1edc5-156">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1edc5-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1edc5-157">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="1edc5-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1edc5-158">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="1edc5-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1edc5-159">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="1edc5-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

