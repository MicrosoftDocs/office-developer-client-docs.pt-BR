---
title: Propriedade canônica PidTagDisplayType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayType
api_type:
- HeaderDef
ms.assetid: ee2bc6ca-3769-4b56-a77d-81418d28f768
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: da26fd2a8643817cf60adbfa6f4e85da345b875c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393464"
---
# <a name="pidtagdisplaytype-canonical-property"></a><span data-ttu-id="3d98a-103">Propriedade canônica PidTagDisplayType</span><span class="sxs-lookup"><span data-stu-id="3d98a-103">PidTagDisplayType Canonical Property</span></span>

  
  
<span data-ttu-id="3d98a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d98a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d98a-105">Contém um valor usado para associar um ícone com uma linha específica de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="3d98a-105">Contains a value used to associate an icon with a particular row of a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3d98a-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="3d98a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3d98a-107">PR_DISPLAY_TYPE</span><span class="sxs-lookup"><span data-stu-id="3d98a-107">PR_DISPLAY_TYPE</span></span>  <br/> |
|<span data-ttu-id="3d98a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3d98a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3d98a-109">0x3900</span><span class="sxs-lookup"><span data-stu-id="3d98a-109">0x3900</span></span>  <br/> |
|<span data-ttu-id="3d98a-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="3d98a-110">Data type:</span></span>  <br/> |<span data-ttu-id="3d98a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3d98a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3d98a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3d98a-112">Area:</span></span>  <br/> |<span data-ttu-id="3d98a-113">Catálogo de endereços MAPI</span><span class="sxs-lookup"><span data-stu-id="3d98a-113">MAPI address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3d98a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3d98a-114">Remarks</span></span>

<span data-ttu-id="3d98a-115">Essa propriedade contém um inteiro longo que facilita o tratamento especial de entrada da tabela com base em seu tipo.</span><span class="sxs-lookup"><span data-stu-id="3d98a-115">This property contains a long integer that facilitates special treatment of the table entry based on its type.</span></span> <span data-ttu-id="3d98a-116">Este tratamento especial consiste tipicamente exibindo um ícone ou outro elemento de exibição, associado com o tipo de exibição.</span><span class="sxs-lookup"><span data-stu-id="3d98a-116">This special treatment typically consists of displaying an icon, or other display element, associated with the display type.</span></span> 
  
<span data-ttu-id="3d98a-117">Essa propriedade não é usada nas tabelas de conteúdo de pasta.</span><span class="sxs-lookup"><span data-stu-id="3d98a-117">This property is not used in folder contents tables.</span></span> <span data-ttu-id="3d98a-118">Aplicativos de cliente devem usar propriedade **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) e a interface de [IMAPIFormInfo](imapiforminfoimapiprop.md) apropriada de uma mensagem para obter o **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) e **PR_MINI_ICON** ([ PidTagMiniIcon](pidtagminiicon-canonical-property.md)) propriedades de mensagem.</span><span class="sxs-lookup"><span data-stu-id="3d98a-118">Client applications should use a message's **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property and appropriate [IMAPIFormInfo](imapiforminfoimapiprop.md) interface to get the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) and **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) properties for that message.</span></span> 
  
<span data-ttu-id="3d98a-119">Essa propriedade pode ter exatamente um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="3d98a-119">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="3d98a-120">DT_AGENT</span><span class="sxs-lookup"><span data-stu-id="3d98a-120">DT_AGENT</span></span> 
  
> <span data-ttu-id="3d98a-121">Um operador automatizado, como a citação do dia ou uma exibição de gráfico de clima.</span><span class="sxs-lookup"><span data-stu-id="3d98a-121">An automated agent, such as Quote-Of-The-Day or a weather chart display.</span></span>
    
<span data-ttu-id="3d98a-122">DT_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="3d98a-122">DT_DISTLIST</span></span> 
  
> <span data-ttu-id="3d98a-123">Uma lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="3d98a-123">A distribution list.</span></span>
    
<span data-ttu-id="3d98a-124">DT_FOLDER</span><span class="sxs-lookup"><span data-stu-id="3d98a-124">DT_FOLDER</span></span> 
  
> <span data-ttu-id="3d98a-125">Exibe o ícone de pasta padrão adjacente à pasta.</span><span class="sxs-lookup"><span data-stu-id="3d98a-125">Display default folder icon adjacent to folder.</span></span>
    
<span data-ttu-id="3d98a-126">DT_FOLDER_LINK</span><span class="sxs-lookup"><span data-stu-id="3d98a-126">DT_FOLDER_LINK</span></span> 
  
> <span data-ttu-id="3d98a-127">Exibe o ícone do link de pasta padrão adjacente à pasta em vez de um ícone de pasta padrão.</span><span class="sxs-lookup"><span data-stu-id="3d98a-127">Display default folder link icon adjacent to folder rather than the default folder icon.</span></span>
    
<span data-ttu-id="3d98a-128">DT_FOLDER_SPECIAL</span><span class="sxs-lookup"><span data-stu-id="3d98a-128">DT_FOLDER_SPECIAL</span></span> 
  
> <span data-ttu-id="3d98a-129">Exibe o ícone de uma pasta com uma distinção de aplicativo específico, como um tipo especial de pasta pública.</span><span class="sxs-lookup"><span data-stu-id="3d98a-129">Display icon for a folder with an application-specific distinction, such as a special type of public folder.</span></span>
    
<span data-ttu-id="3d98a-130">DT_FORUM</span><span class="sxs-lookup"><span data-stu-id="3d98a-130">DT_FORUM</span></span> 
  
> <span data-ttu-id="3d98a-131">Um fórum, como um serviço do quadro de avisos ou uma pasta pública ou compartilhada.</span><span class="sxs-lookup"><span data-stu-id="3d98a-131">A forum, such as a bulletin board service or a public or shared folder.</span></span>
    
<span data-ttu-id="3d98a-132">DT_GLOBAL</span><span class="sxs-lookup"><span data-stu-id="3d98a-132">DT_GLOBAL</span></span> 
  
> <span data-ttu-id="3d98a-133">Um catálogo de endereços global.</span><span class="sxs-lookup"><span data-stu-id="3d98a-133">A global address book.</span></span>
    
<span data-ttu-id="3d98a-134">DT_LOCAL</span><span class="sxs-lookup"><span data-stu-id="3d98a-134">DT_LOCAL</span></span> 
  
> <span data-ttu-id="3d98a-135">Catálogo de endereços local que você compartilha com um pequeno grupo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3d98a-135">A local address book that you share with a small workgroup.</span></span>
    
<span data-ttu-id="3d98a-136">DT_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="3d98a-136">DT_MAILUSER</span></span> 
  
> <span data-ttu-id="3d98a-137">Um usuário típico de mensagens.</span><span class="sxs-lookup"><span data-stu-id="3d98a-137">A typical messaging user.</span></span>
    
<span data-ttu-id="3d98a-138">DT_MODIFIABLE</span><span class="sxs-lookup"><span data-stu-id="3d98a-138">DT_MODIFIABLE</span></span> 
  
> <span data-ttu-id="3d98a-139">Pode ser modificado; o contêiner deve ser indicado como modificável na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="3d98a-139">Modifiable; the container should be denoted as modifiable in the user interface.</span></span>
    
<span data-ttu-id="3d98a-140">DT_NOT_SPECIFIC</span><span class="sxs-lookup"><span data-stu-id="3d98a-140">DT_NOT_SPECIFIC</span></span> 
  
> <span data-ttu-id="3d98a-141">Não corresponde a qualquer uma das outras configurações.</span><span class="sxs-lookup"><span data-stu-id="3d98a-141">Does not match any of the other settings.</span></span>
    
<span data-ttu-id="3d98a-142">DT_ORGANIZATION</span><span class="sxs-lookup"><span data-stu-id="3d98a-142">DT_ORGANIZATION</span></span> 
  
> <span data-ttu-id="3d98a-143">Um alias especial definido para um grupo grande, como assistência técnica, contabilidade ou coordenador sangue-unidade.</span><span class="sxs-lookup"><span data-stu-id="3d98a-143">A special alias defined for a large group, such as helpdesk, accounting, or blood-drive coordinator.</span></span>
    
<span data-ttu-id="3d98a-144">DT_PRIVATE_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="3d98a-144">DT_PRIVATE_DISTLIST</span></span> 
  
> <span data-ttu-id="3d98a-145">Uma privada, pessoalmente administrado a lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="3d98a-145">A private, personally administered distribution list.</span></span>
    
<span data-ttu-id="3d98a-146">DT_REMOTE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="3d98a-146">DT_REMOTE_MAILUSER</span></span> 
  
> <span data-ttu-id="3d98a-147">Um destinatário sabidamente de um sistema de mensagens estrangeiro ou remoto.</span><span class="sxs-lookup"><span data-stu-id="3d98a-147">A recipient known to be from a foreign or remote messaging system.</span></span>
    
<span data-ttu-id="3d98a-148">DT_WAN</span><span class="sxs-lookup"><span data-stu-id="3d98a-148">DT_WAN</span></span> 
  
> <span data-ttu-id="3d98a-149">Um catálogo de endereços de rede de longa distância.</span><span class="sxs-lookup"><span data-stu-id="3d98a-149">A wide area network address book.</span></span>
    
<span data-ttu-id="3d98a-150">Tabelas de conteúdo de catálogo de endereços usam os valores DT_AGENT, DT_DISTLIST, DT_FORUM, DT_MAILUSER, DT_ORGANIZATION, DT_PRIVATE_DISTLIST e DT_REMOTE_MAILUSER.</span><span class="sxs-lookup"><span data-stu-id="3d98a-150">Address book contents tables use the DT_AGENT, DT_DISTLIST, DT_FORUM, DT_MAILUSER, DT_ORGANIZATION, DT_PRIVATE_DISTLIST, and DT_REMOTE_MAILUSER values.</span></span> <span data-ttu-id="3d98a-151">Tabelas de hierarquias de catálogo de endereços e tabelas únicas usam os valores DT_GLOBAL, DT_LOCAL, DT_MODIFIABLE, DT_NOT_SPECIFIC e DT_WAN.</span><span class="sxs-lookup"><span data-stu-id="3d98a-151">Address book hierarchy tables and one-off tables use the DT_GLOBAL, DT_LOCAL, DT_MODIFIABLE, DT_NOT_SPECIFIC, and DT_WAN values.</span></span> <span data-ttu-id="3d98a-152">Tabelas de hierarquias de pasta usam os valores DT_FOLDER, DT_FOLDER_LINK e DT_FOLDER_SPECIAL.</span><span class="sxs-lookup"><span data-stu-id="3d98a-152">Folder hierarchy tables use the DT_FOLDER, DT_FOLDER_LINK, and DT_FOLDER_SPECIAL values.</span></span> 
  
<span data-ttu-id="3d98a-153">Se essa propriedade não estiver definida, o cliente deve presumir tipo padrão apropriado para a tabela, normalmente DT_FOLDER, DT_LOCAL ou DT_MAILUSER.</span><span class="sxs-lookup"><span data-stu-id="3d98a-153">If this property is not set, the client should assume the default type appropriate for the table, typically DT_FOLDER, DT_LOCAL, or DT_MAILUSER.</span></span> 
  
 <span data-ttu-id="3d98a-154">**Observação** Todos os valores não documentados são reservados para MAPI.</span><span class="sxs-lookup"><span data-stu-id="3d98a-154">**Note** All values not documented are reserved for MAPI.</span></span> <span data-ttu-id="3d98a-155">Aplicativos cliente não devem definir qualquer novos valores e devem estar preparados para lidar com um valor não documentado.</span><span class="sxs-lookup"><span data-stu-id="3d98a-155">Client applications must not define any new values and must be prepared to deal with an undocumented value.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3d98a-156">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3d98a-156">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3d98a-157">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="3d98a-157">Protocol specifications</span></span>

<span data-ttu-id="3d98a-158">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d98a-158">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d98a-159">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="3d98a-159">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3d98a-160">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d98a-160">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d98a-161">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="3d98a-161">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="3d98a-162">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d98a-162">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d98a-163">Especifica as propriedades e operações que são permitidas para modelos de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="3d98a-163">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
<span data-ttu-id="3d98a-164">[[MS-OXLDAP]](https://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d98a-164">[[MS-OXLDAP]](https://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d98a-165">Permite o acesso ao diretório.</span><span class="sxs-lookup"><span data-stu-id="3d98a-165">Enables directory access.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3d98a-166">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3d98a-166">Header files</span></span>

<span data-ttu-id="3d98a-167">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3d98a-167">Mapidefs.h</span></span>
  
> <span data-ttu-id="3d98a-168">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="3d98a-168">Provides data type definitions.</span></span>
    
<span data-ttu-id="3d98a-169">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3d98a-169">Mapitags.h</span></span>
  
> <span data-ttu-id="3d98a-170">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="3d98a-170">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3d98a-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="3d98a-171">See also</span></span>



[<span data-ttu-id="3d98a-172">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3d98a-172">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3d98a-173">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="3d98a-173">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3d98a-174">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="3d98a-174">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3d98a-175">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="3d98a-175">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

