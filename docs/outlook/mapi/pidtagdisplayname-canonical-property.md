---
title: Propriedade canônica PidTagDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayName
api_type:
- HeaderDef
ms.assetid: bd094e00-5c60-4bb3-9a45-b943fab52876
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 834141fe3e57fde5e6404776e0ad5ce3b438450e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360799"
---
# <a name="pidtagdisplayname-canonical-property"></a><span data-ttu-id="06832-103">Propriedade canônica PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="06832-103">PidTagDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="06832-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06832-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06832-105">Contém o nome para exibição de um determinado objeto MAPI.</span><span class="sxs-lookup"><span data-stu-id="06832-105">Contains the display name for a given MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="06832-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="06832-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="06832-107">PR_DISPLAY_NAME, PR_DISPLAY_NAME_A, PR_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="06832-107">PR_DISPLAY_NAME, PR_DISPLAY_NAME_A, PR_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="06832-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="06832-108">Identifier:</span></span>  <br/> |<span data-ttu-id="06832-109">0x3001</span><span class="sxs-lookup"><span data-stu-id="06832-109">0x3001</span></span>  <br/> |
|<span data-ttu-id="06832-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="06832-110">Data type:</span></span>  <br/> |<span data-ttu-id="06832-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="06832-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="06832-112">Área:</span><span class="sxs-lookup"><span data-stu-id="06832-112">Area:</span></span>  <br/> |<span data-ttu-id="06832-113">MAPI comum</span><span class="sxs-lookup"><span data-stu-id="06832-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="06832-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="06832-114">Remarks</span></span>

<span data-ttu-id="06832-115">As pastas exigem subpastas irmãs para ter nomes de exibição exclusivos.</span><span class="sxs-lookup"><span data-stu-id="06832-115">Folders require sibling subfolders to have unique display names.</span></span> <span data-ttu-id="06832-116">Por exemplo, se uma pasta contiver duas subpastas, as duas subpastas não poderão usar o mesmo valor para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="06832-116">For example, if a folder contains two subfolders, the two subfolders cannot use the same value for this property.</span></span> <span data-ttu-id="06832-117">Essa restrição não se aplica a outros contêineres, como catálogos de endereços e listas de distribuição.</span><span class="sxs-lookup"><span data-stu-id="06832-117">This restriction does not apply to other containers, such as address books and distribution lists.</span></span> 
  
<span data-ttu-id="06832-118">Os provedores de serviços devem definir o valor dessa propriedade para que contenham o tipo de provedor e informações de configuração.</span><span class="sxs-lookup"><span data-stu-id="06832-118">Service providers should set the value of this property so that it contains both the provider type and configuration information.</span></span> <span data-ttu-id="06832-119">As informações adicionais ajudam a distinguir entre instâncias de provedores do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="06832-119">The additional information helps to distinguish between instances of providers of the same type.</span></span> <span data-ttu-id="06832-120">Provedores não configurados devem usar uma cadeia de caracteres que nomeia o provedor.</span><span class="sxs-lookup"><span data-stu-id="06832-120">Unconfigured providers should use a string that names the provider.</span></span> <span data-ttu-id="06832-121">Os provedores conFigurados devem usar a mesma cadeia de caracteres seguida de uma cadeia de caracteres de distinção entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="06832-121">Configured providers should use the same string followed by a distinguishing string in parentheses.</span></span> <span data-ttu-id="06832-122">Por exemplo, um provedor de repositório de mensagens não configurado pode definir essas propriedades como:</span><span class="sxs-lookup"><span data-stu-id="06832-122">For example, an unconfigured message store provider might set these properties to:</span></span> 
  
<span data-ttu-id="06832-123">Repositório de informações pessoais</span><span class="sxs-lookup"><span data-stu-id="06832-123">Personal Information Store</span></span>
  
<span data-ttu-id="06832-124">A versão configurada pode então definir essas propriedades como:</span><span class="sxs-lookup"><span data-stu-id="06832-124">The configured version could then set these properties to:</span></span> 
  
<span data-ttu-id="06832-125">Repositório de informações pessoais (6 de fevereiro de 1998)</span><span class="sxs-lookup"><span data-stu-id="06832-125">Personal Information Store (February 6, 1998)</span></span>
  
<span data-ttu-id="06832-126">Para objetos status, essas propriedades contêm o nome do componente que pode ser exibido pela interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="06832-126">For status objects, these properties contain the name of the component that can be displayed by the user interface.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="06832-127">Pontos-e-vírgulas não podem ser usados em nomes de destinatários em mensagens MAPI.</span><span class="sxs-lookup"><span data-stu-id="06832-127">Semicolons cannot be used within recipient names in MAPI messaging.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="06832-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="06832-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="06832-129">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="06832-129">Protocol specifications</span></span>

<span data-ttu-id="06832-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06832-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06832-131">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="06832-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="06832-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06832-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06832-133">Manipula objetos Message e Attachment.</span><span class="sxs-lookup"><span data-stu-id="06832-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="06832-134">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06832-134">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06832-135">Controla as operações da pasta.</span><span class="sxs-lookup"><span data-stu-id="06832-135">Handles folder operations.</span></span>
    
<span data-ttu-id="06832-136">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06832-136">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06832-137">Especifica as propriedades e as operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="06832-137">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="06832-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06832-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06832-139">Especifica as propriedades e operações de listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="06832-139">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="06832-140">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06832-140">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06832-141">Converte as convenções de email padrão da Internet em objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="06832-141">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="06832-142">[[MS-XWDVSEC]](https://msdn.microsoft.com/library/dc043d09-6b76-4392-aea3-68f8e81c64d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06832-142">[[MS-XWDVSEC]](https://msdn.microsoft.com/library/dc043d09-6b76-4392-aea3-68f8e81c64d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06832-143">Estende o protocolo WebDAV que especifica como solicitar e definir o descritor de segurança do Exchange por meio de métodos WebDAV.</span><span class="sxs-lookup"><span data-stu-id="06832-143">Extends the WebDAV protocol that specifies how to request and set the Exchange security descriptor via WebDAV methods.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="06832-144">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="06832-144">Header files</span></span>

<span data-ttu-id="06832-145">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="06832-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="06832-146">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="06832-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="06832-147">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="06832-147">Mapitags.h</span></span>
  
> <span data-ttu-id="06832-148">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="06832-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="06832-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="06832-149">See also</span></span>



[<span data-ttu-id="06832-150">Propriedade canônica PidTagTransmittableDisplayName</span><span class="sxs-lookup"><span data-stu-id="06832-150">PidTagTransmittableDisplayName Canonical Property</span></span>](pidtagtransmittabledisplayname-canonical-property.md)


[<span data-ttu-id="06832-151">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="06832-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="06832-152">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="06832-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="06832-153">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="06832-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="06832-154">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="06832-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

