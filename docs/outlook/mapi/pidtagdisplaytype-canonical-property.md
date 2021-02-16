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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360778"
---
# <a name="pidtagdisplaytype-canonical-property"></a><span data-ttu-id="cd9db-103">Propriedade canônica PidTagDisplayType</span><span class="sxs-lookup"><span data-stu-id="cd9db-103">PidTagDisplayType Canonical Property</span></span>

  
  
<span data-ttu-id="cd9db-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd9db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd9db-105">Contém um valor usado para associar um ícone a uma linha específica de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="cd9db-105">Contains a value used to associate an icon with a particular row of a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cd9db-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="cd9db-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cd9db-107">PR_DISPLAY_TYPE</span><span class="sxs-lookup"><span data-stu-id="cd9db-107">PR_DISPLAY_TYPE</span></span>  <br/> |
|<span data-ttu-id="cd9db-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="cd9db-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cd9db-109">0x3900</span><span class="sxs-lookup"><span data-stu-id="cd9db-109">0x3900</span></span>  <br/> |
|<span data-ttu-id="cd9db-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="cd9db-110">Data type:</span></span>  <br/> |<span data-ttu-id="cd9db-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cd9db-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="cd9db-112">Área:</span><span class="sxs-lookup"><span data-stu-id="cd9db-112">Area:</span></span>  <br/> |<span data-ttu-id="cd9db-113">MapI address book</span><span class="sxs-lookup"><span data-stu-id="cd9db-113">MAPI address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd9db-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="cd9db-114">Remarks</span></span>

<span data-ttu-id="cd9db-115">Essa propriedade contém um inteiro longo que facilita o tratamento especial da entrada da tabela com base em seu tipo.</span><span class="sxs-lookup"><span data-stu-id="cd9db-115">This property contains a long integer that facilitates special treatment of the table entry based on its type.</span></span> <span data-ttu-id="cd9db-116">Esse tratamento especial geralmente consiste em exibir um ícone ou outro elemento de exibição associado ao tipo de exibição.</span><span class="sxs-lookup"><span data-stu-id="cd9db-116">This special treatment typically consists of displaying an icon, or other display element, associated with the display type.</span></span> 
  
<span data-ttu-id="cd9db-117">Essa propriedade não é usada em tabelas de conteúdo de pastas.</span><span class="sxs-lookup"><span data-stu-id="cd9db-117">This property is not used in folder contents tables.</span></span> <span data-ttu-id="cd9db-118">Os aplicativos cliente devem usar a propriedade **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) de uma mensagem e a interface [IMAPIFormInfo](imapiforminfoimapiprop.md) apropriada para obter as propriedades **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) e **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) para essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="cd9db-118">Client applications should use a message's **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property and appropriate [IMAPIFormInfo](imapiforminfoimapiprop.md) interface to get the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) and **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) properties for that message.</span></span> 
  
<span data-ttu-id="cd9db-119">Essa propriedade pode ter exatamente um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="cd9db-119">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="cd9db-120">DT_AGENT</span><span class="sxs-lookup"><span data-stu-id="cd9db-120">DT_AGENT</span></span> 
  
> <span data-ttu-id="cd9db-121">Um agente automatizado, como Quote-of-The-Day ou uma exibição de gráfico de previsão do tempo.</span><span class="sxs-lookup"><span data-stu-id="cd9db-121">An automated agent, such as Quote-Of-The-Day or a weather chart display.</span></span>
    
<span data-ttu-id="cd9db-122">DT_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="cd9db-122">DT_DISTLIST</span></span> 
  
> <span data-ttu-id="cd9db-123">Uma lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="cd9db-123">A distribution list.</span></span>
    
<span data-ttu-id="cd9db-124">DT_FOLDER</span><span class="sxs-lookup"><span data-stu-id="cd9db-124">DT_FOLDER</span></span> 
  
> <span data-ttu-id="cd9db-125">Exibe o ícone de pasta padrão adjacente à pasta.</span><span class="sxs-lookup"><span data-stu-id="cd9db-125">Display default folder icon adjacent to folder.</span></span>
    
<span data-ttu-id="cd9db-126">DT_FOLDER_LINK</span><span class="sxs-lookup"><span data-stu-id="cd9db-126">DT_FOLDER_LINK</span></span> 
  
> <span data-ttu-id="cd9db-127">Exibe o ícone de link de pasta padrão adjacente à pasta em vez do ícone de pasta padrão.</span><span class="sxs-lookup"><span data-stu-id="cd9db-127">Display default folder link icon adjacent to folder rather than the default folder icon.</span></span>
    
<span data-ttu-id="cd9db-128">DT_FOLDER_SPECIAL</span><span class="sxs-lookup"><span data-stu-id="cd9db-128">DT_FOLDER_SPECIAL</span></span> 
  
> <span data-ttu-id="cd9db-129">Ícone de exibição para uma pasta com uma distinção específica do aplicativo, como um tipo especial de pasta pública.</span><span class="sxs-lookup"><span data-stu-id="cd9db-129">Display icon for a folder with an application-specific distinction, such as a special type of public folder.</span></span>
    
<span data-ttu-id="cd9db-130">DT_FORUM</span><span class="sxs-lookup"><span data-stu-id="cd9db-130">DT_FORUM</span></span> 
  
> <span data-ttu-id="cd9db-131">Um fórum, como um serviço de quadro de boletins ou uma pasta pública ou compartilhada.</span><span class="sxs-lookup"><span data-stu-id="cd9db-131">A forum, such as a bulletin board service or a public or shared folder.</span></span>
    
<span data-ttu-id="cd9db-132">DT_GLOBAL</span><span class="sxs-lookup"><span data-stu-id="cd9db-132">DT_GLOBAL</span></span> 
  
> <span data-ttu-id="cd9db-133">Um livro de endereços global.</span><span class="sxs-lookup"><span data-stu-id="cd9db-133">A global address book.</span></span>
    
<span data-ttu-id="cd9db-134">DT_LOCAL</span><span class="sxs-lookup"><span data-stu-id="cd9db-134">DT_LOCAL</span></span> 
  
> <span data-ttu-id="cd9db-135">Um livro de endereços local que você compartilha com um pequeno grupo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="cd9db-135">A local address book that you share with a small workgroup.</span></span>
    
<span data-ttu-id="cd9db-136">DT_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="cd9db-136">DT_MAILUSER</span></span> 
  
> <span data-ttu-id="cd9db-137">Um usuário de mensagens típico.</span><span class="sxs-lookup"><span data-stu-id="cd9db-137">A typical messaging user.</span></span>
    
<span data-ttu-id="cd9db-138">DT_MODIFIABLE</span><span class="sxs-lookup"><span data-stu-id="cd9db-138">DT_MODIFIABLE</span></span> 
  
> <span data-ttu-id="cd9db-139">Modificável; o contêiner deve ser denodado como modificável na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="cd9db-139">Modifiable; the container should be denoted as modifiable in the user interface.</span></span>
    
<span data-ttu-id="cd9db-140">DT_NOT_SPECIFIC</span><span class="sxs-lookup"><span data-stu-id="cd9db-140">DT_NOT_SPECIFIC</span></span> 
  
> <span data-ttu-id="cd9db-141">Não é igual a nenhuma das outras configurações.</span><span class="sxs-lookup"><span data-stu-id="cd9db-141">Does not match any of the other settings.</span></span>
    
<span data-ttu-id="cd9db-142">DT_ORGANIZATION</span><span class="sxs-lookup"><span data-stu-id="cd9db-142">DT_ORGANIZATION</span></span> 
  
> <span data-ttu-id="cd9db-143">Um alias especial definido para um grupo grande, como helpdesk, accounting ou coordenador de unidade de sol.</span><span class="sxs-lookup"><span data-stu-id="cd9db-143">A special alias defined for a large group, such as helpdesk, accounting, or blood-drive coordinator.</span></span>
    
<span data-ttu-id="cd9db-144">DT_PRIVATE_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="cd9db-144">DT_PRIVATE_DISTLIST</span></span> 
  
> <span data-ttu-id="cd9db-145">Uma lista de distribuição privada e administrada pessoalmente.</span><span class="sxs-lookup"><span data-stu-id="cd9db-145">A private, personally administered distribution list.</span></span>
    
<span data-ttu-id="cd9db-146">DT_REMOTE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="cd9db-146">DT_REMOTE_MAILUSER</span></span> 
  
> <span data-ttu-id="cd9db-147">Um destinatário conhecido por ser de um sistema de mensagens externo ou remoto.</span><span class="sxs-lookup"><span data-stu-id="cd9db-147">A recipient known to be from a foreign or remote messaging system.</span></span>
    
<span data-ttu-id="cd9db-148">DT_WAN</span><span class="sxs-lookup"><span data-stu-id="cd9db-148">DT_WAN</span></span> 
  
> <span data-ttu-id="cd9db-149">Um livro de endereços de rede de área ampla.</span><span class="sxs-lookup"><span data-stu-id="cd9db-149">A wide area network address book.</span></span>
    
<span data-ttu-id="cd9db-150">As tabelas de conteúdo do livro de endereços usam os valores DT_AGENT, DT_DISTLIST, DT_FORUM, DT_MAILUSER, DT_ORGANIZATION, DT_PRIVATE_DISTLIST e DT_REMOTE_MAILUSER.</span><span class="sxs-lookup"><span data-stu-id="cd9db-150">Address book contents tables use the DT_AGENT, DT_DISTLIST, DT_FORUM, DT_MAILUSER, DT_ORGANIZATION, DT_PRIVATE_DISTLIST, and DT_REMOTE_MAILUSER values.</span></span> <span data-ttu-id="cd9db-151">As tabelas de hierarquia do livro de endereços e as tabelas one-off usam os valores DT_GLOBAL, DT_LOCAL, DT_MODIFIABLE, DT_NOT_SPECIFIC e DT_WAN dados.</span><span class="sxs-lookup"><span data-stu-id="cd9db-151">Address book hierarchy tables and one-off tables use the DT_GLOBAL, DT_LOCAL, DT_MODIFIABLE, DT_NOT_SPECIFIC, and DT_WAN values.</span></span> <span data-ttu-id="cd9db-152">As tabelas de hierarquia de pastas usam DT_FOLDER, DT_FOLDER_LINK e DT_FOLDER_SPECIAL pasta.</span><span class="sxs-lookup"><span data-stu-id="cd9db-152">Folder hierarchy tables use the DT_FOLDER, DT_FOLDER_LINK, and DT_FOLDER_SPECIAL values.</span></span> 
  
<span data-ttu-id="cd9db-153">Se essa propriedade não estiver definida, o cliente deverá assumir o tipo padrão apropriado para a tabela, normalmente DT_FOLDER, DT_LOCAL ou DT_MAILUSER.</span><span class="sxs-lookup"><span data-stu-id="cd9db-153">If this property is not set, the client should assume the default type appropriate for the table, typically DT_FOLDER, DT_LOCAL, or DT_MAILUSER.</span></span> 
  
 <span data-ttu-id="cd9db-154">**Observação** Todos os valores não documentados são reservados para MAPI.</span><span class="sxs-lookup"><span data-stu-id="cd9db-154">**Note** All values not documented are reserved for MAPI.</span></span> <span data-ttu-id="cd9db-155">Os aplicativos cliente não devem definir novos valores e devem estar preparados para lidar com um valor não documentado.</span><span class="sxs-lookup"><span data-stu-id="cd9db-155">Client applications must not define any new values and must be prepared to deal with an undocumented value.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cd9db-156">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cd9db-156">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cd9db-157">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="cd9db-157">Protocol specifications</span></span>

<span data-ttu-id="cd9db-158">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd9db-158">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd9db-159">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="cd9db-159">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cd9db-160">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd9db-160">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd9db-161">Lida com objetos de mensagem e anexo.</span><span class="sxs-lookup"><span data-stu-id="cd9db-161">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="cd9db-162">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd9db-162">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd9db-163">Especifica as propriedades e operações que são permitidas para modelos de livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="cd9db-163">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
<span data-ttu-id="cd9db-164">[[MS-OXLDAP]](https://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd9db-164">[[MS-OXLDAP]](https://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd9db-165">Habilita o acesso ao diretório.</span><span class="sxs-lookup"><span data-stu-id="cd9db-165">Enables directory access.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cd9db-166">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="cd9db-166">Header files</span></span>

<span data-ttu-id="cd9db-167">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cd9db-167">Mapidefs.h</span></span>
  
> <span data-ttu-id="cd9db-168">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="cd9db-168">Provides data type definitions.</span></span>
    
<span data-ttu-id="cd9db-169">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cd9db-169">Mapitags.h</span></span>
  
> <span data-ttu-id="cd9db-170">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="cd9db-170">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cd9db-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd9db-171">See also</span></span>



[<span data-ttu-id="cd9db-172">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cd9db-172">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cd9db-173">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="cd9db-173">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cd9db-174">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="cd9db-174">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cd9db-175">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="cd9db-175">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

