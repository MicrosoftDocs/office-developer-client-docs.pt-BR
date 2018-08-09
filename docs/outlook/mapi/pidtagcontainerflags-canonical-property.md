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
ms.openlocfilehash: c13acd1c3b759602a5fbe07c21ca8b784e0fe4d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769084"
---
# <a name="pidtagcontainerflags-canonical-property"></a><span data-ttu-id="7370f-103">Propriedade canônica PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="7370f-103">PidTagContainerFlags Canonical Property</span></span>

  
  
<span data-ttu-id="7370f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7370f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7370f-105">Contém uma bitmask dos sinalizadores que descrevem os recursos de um contêiner de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="7370f-105">Contains a bitmask of flags describing capabilities of an address book container.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7370f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="7370f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7370f-107">PR_CONTAINER_FLAGS</span><span class="sxs-lookup"><span data-stu-id="7370f-107">PR_CONTAINER_FLAGS</span></span>  <br/> |
|<span data-ttu-id="7370f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7370f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7370f-109">0x3600</span><span class="sxs-lookup"><span data-stu-id="7370f-109">0x3600</span></span>  <br/> |
|<span data-ttu-id="7370f-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="7370f-110">Data type:</span></span>  <br/> |<span data-ttu-id="7370f-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7370f-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7370f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7370f-112">Area:</span></span>  <br/> |<span data-ttu-id="7370f-113">Catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="7370f-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7370f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7370f-114">Remarks</span></span>

<span data-ttu-id="7370f-115">Um ou mais dos seguintes sinalizadores podem ser definido para a máscara de bits:</span><span class="sxs-lookup"><span data-stu-id="7370f-115">One or more of the following flags can be set for the bitmask:</span></span>
  
<span data-ttu-id="7370f-116">AB_FIND_ON_OPEN</span><span class="sxs-lookup"><span data-stu-id="7370f-116">AB_FIND_ON_OPEN</span></span> 
  
> <span data-ttu-id="7370f-117">Exibe uma caixa de diálogo para solicitar uma restrição antes de exibir qualquer conteúdo do contêiner.</span><span class="sxs-lookup"><span data-stu-id="7370f-117">Displays a dialog box to request a restriction before displaying any contents of the container.</span></span> 
    
<span data-ttu-id="7370f-118">AB_MODIFIABLE</span><span class="sxs-lookup"><span data-stu-id="7370f-118">AB_MODIFIABLE</span></span> 
  
> <span data-ttu-id="7370f-119">Entradas podem ser adicionadas ao e removidas do contêiner.</span><span class="sxs-lookup"><span data-stu-id="7370f-119">Entries can be added to and removed from the container.</span></span> <span data-ttu-id="7370f-120">Esse sinalizador não indica se as entradas no contêiner podem ser modificadas.</span><span class="sxs-lookup"><span data-stu-id="7370f-120">This flag does not indicate whether any entries in the container can be modified.</span></span>
    
<span data-ttu-id="7370f-121">AB_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="7370f-121">AB_RECIPIENTS</span></span> 
  
> <span data-ttu-id="7370f-122">O contêiner pode manter os destinatários.</span><span class="sxs-lookup"><span data-stu-id="7370f-122">The container can hold recipients.</span></span> <span data-ttu-id="7370f-123">Esse sinalizador não indica se quaisquer destinatários estão realmente presentes no contêiner ou se eles podem ser adicionados ou removidos.</span><span class="sxs-lookup"><span data-stu-id="7370f-123">This flag does not indicate whether any recipients are actually present in the container, or whether they can be added or removed.</span></span> 
    
<span data-ttu-id="7370f-124">AB_SUBCONTAINERS</span><span class="sxs-lookup"><span data-stu-id="7370f-124">AB_SUBCONTAINERS</span></span> 
  
> <span data-ttu-id="7370f-125">O contêiner pode manter filho contêineres.</span><span class="sxs-lookup"><span data-stu-id="7370f-125">The container can hold child containers.</span></span> <span data-ttu-id="7370f-126">Esse sinalizador não indica se qualquer subcontêineres são realmente presentes no contêiner, nem se eles podem ser adicionados ou removidos.</span><span class="sxs-lookup"><span data-stu-id="7370f-126">This flag does not indicate whether any subcontainers are actually present in the container, nor whether they can be added or removed.</span></span> <span data-ttu-id="7370f-127">AB_SUBCONTAINERS deve ser definida para o contêiner oferecer suporte a [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md).</span><span class="sxs-lookup"><span data-stu-id="7370f-127">AB_SUBCONTAINERS must be set for the container to support [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md).</span></span> 
    
<span data-ttu-id="7370f-128">AB_UNMODIFIABLE</span><span class="sxs-lookup"><span data-stu-id="7370f-128">AB_UNMODIFIABLE</span></span> 
  
> <span data-ttu-id="7370f-129">As entradas não podem ser adicionadas ou removidas do contêiner.</span><span class="sxs-lookup"><span data-stu-id="7370f-129">Entries cannot be added to or removed from the container.</span></span> <span data-ttu-id="7370f-130">Esse sinalizador não indica se as entradas no contêiner podem ser modificadas.</span><span class="sxs-lookup"><span data-stu-id="7370f-130">This flag does not indicate whether any entries in the container can be modified.</span></span> 
    
<span data-ttu-id="7370f-131">O sinalizador AB_FIND_ON_OPEN é altamente recomendável para contêineres usados com os serviços online ou com conexões lentas aos servidores.</span><span class="sxs-lookup"><span data-stu-id="7370f-131">The AB_FIND_ON_OPEN flag is highly recommended for containers used with online services or with slow connections to servers.</span></span> <span data-ttu-id="7370f-132">Quando for aberto um contêiner que tenha AB_FIND_ON_OPEN definida, uma caixa de diálogo **Localizar** é apresentada ao usuário para restringir os usuários de mensagens exibidos.</span><span class="sxs-lookup"><span data-stu-id="7370f-132">When a container is opened that has AB_FIND_ON_OPEN set, a **Find** dialog box is presented to the user to restrict the displayed messaging users.</span></span> <span data-ttu-id="7370f-133">Mesmo uma especificação parcial limitando os usuários de mensagens pode acelerar drasticamente uma exibição do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="7370f-133">Even a partial specification limiting the messaging users can dramatically speed up a display of the contents.</span></span> 
  
<span data-ttu-id="7370f-134">Sinalizador a AB_MODIFIABLE ou AB_UNMODIFIABLE deve ser definida.</span><span class="sxs-lookup"><span data-stu-id="7370f-134">Either the AB_MODIFIABLE or AB_UNMODIFIABLE flag must be set.</span></span> <span data-ttu-id="7370f-135">Ambos os sinalizadores podem ser definidos para indicar que o contêiner não sabe se ele pode ser modificado ou não, por exemplo, se a modificação depende de direitos de acesso do usuário.</span><span class="sxs-lookup"><span data-stu-id="7370f-135">Both flags can be set to indicate that the container does not know whether it can be modified or not, for example if modification depends on the user's access rights.</span></span> <span data-ttu-id="7370f-136">Nesse caso, um aplicativo cliente deve executar uma tentativa de uma chamada e examinar o código de retorno para determinar os recursos do contêiner.</span><span class="sxs-lookup"><span data-stu-id="7370f-136">In this case, a client application must attempt a call and examine the return code to determine the container's capabilities.</span></span> <span data-ttu-id="7370f-137">Geralmente, um cliente inicia examinando AB_MODIFIABLE.</span><span class="sxs-lookup"><span data-stu-id="7370f-137">A client typically starts by examining AB_MODIFIABLE.</span></span> <span data-ttu-id="7370f-138">Se ele estiver definido, o cliente faz uma chamada que tenta modificar o contêiner e verifica se o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="7370f-138">If it is set, the client makes a call that attempts to modify the container and checks the return value.</span></span> 
  
<span data-ttu-id="7370f-139">O sinalizador AB_MODIFIABLE não indica quais tipos de entradas podem ser adicionados ao contêiner.</span><span class="sxs-lookup"><span data-stu-id="7370f-139">The AB_MODIFIABLE flag does not indicate what types of entries can be added to the container.</span></span> <span data-ttu-id="7370f-140">Para determinar isso, o cliente deve usar o método [OpenProperty](imapiprop-openproperty.md) apropriado para abrir a propriedade de **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) do contêiner.</span><span class="sxs-lookup"><span data-stu-id="7370f-140">To determine this, the client should use the appropriate [OpenProperty](imapiprop-openproperty.md) method to open the container's **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> <span data-ttu-id="7370f-141">Abertura **PR_CREATE_TEMPLATES** causas one-off do contêiner de tabela para serem retornadas, listando os tipos de entradas que podem ser criados no contêiner.</span><span class="sxs-lookup"><span data-stu-id="7370f-141">Opening **PR_CREATE_TEMPLATES** causes the container's one-off table to be returned, listing the kinds of entries that can be created in the container.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7370f-142">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7370f-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7370f-143">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="7370f-143">Protocol specifications</span></span>

<span data-ttu-id="7370f-144">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7370f-144">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7370f-145">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="7370f-145">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7370f-146">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7370f-146">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7370f-147">Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="7370f-147">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="7370f-148">[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7370f-148">[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7370f-149">Trata a comunicação do cliente com um servidor de nome serviço provedor NSPI (Interface).</span><span class="sxs-lookup"><span data-stu-id="7370f-149">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7370f-150">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7370f-150">Header files</span></span>

<span data-ttu-id="7370f-151">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7370f-151">Mapidefs.h</span></span>
  
> <span data-ttu-id="7370f-152">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="7370f-152">Provides data type definitions.</span></span>
    
<span data-ttu-id="7370f-153">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7370f-153">Mapitags.h</span></span>
  
> <span data-ttu-id="7370f-154">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="7370f-154">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7370f-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="7370f-155">See also</span></span>



[<span data-ttu-id="7370f-156">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7370f-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7370f-157">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="7370f-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7370f-158">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="7370f-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7370f-159">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="7370f-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

