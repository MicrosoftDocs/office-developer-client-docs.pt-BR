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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386415"
---
# <a name="pidtagdisplayname-canonical-property"></a><span data-ttu-id="79064-103">Propriedade canônica PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="79064-103">PidTagDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="79064-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79064-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79064-105">Contém o nome de exibição para um determinado objeto MAPI.</span><span class="sxs-lookup"><span data-stu-id="79064-105">Contains the display name for a given MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="79064-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="79064-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="79064-107">PR_DISPLAY_NAME, PR_DISPLAY_NAME_A, PR_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="79064-107">PR_DISPLAY_NAME, PR_DISPLAY_NAME_A, PR_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="79064-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="79064-108">Identifier:</span></span>  <br/> |<span data-ttu-id="79064-109">0x3001</span><span class="sxs-lookup"><span data-stu-id="79064-109">0x3001</span></span>  <br/> |
|<span data-ttu-id="79064-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="79064-110">Data type:</span></span>  <br/> |<span data-ttu-id="79064-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="79064-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="79064-112">Área:</span><span class="sxs-lookup"><span data-stu-id="79064-112">Area:</span></span>  <br/> |<span data-ttu-id="79064-113">MAPI comuns</span><span class="sxs-lookup"><span data-stu-id="79064-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="79064-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="79064-114">Remarks</span></span>

<span data-ttu-id="79064-115">As pastas requerem subpastas irmão tenham nomes para exibição exclusivos.</span><span class="sxs-lookup"><span data-stu-id="79064-115">Folders require sibling subfolders to have unique display names.</span></span> <span data-ttu-id="79064-116">Por exemplo, se uma pasta contém duas subpastas, as duas subpastas não podem usar o mesmo valor para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="79064-116">For example, if a folder contains two subfolders, the two subfolders cannot use the same value for this property.</span></span> <span data-ttu-id="79064-117">Essa restrição não se aplica a outros contêineres, como catálogos de endereços e listas de distribuição.</span><span class="sxs-lookup"><span data-stu-id="79064-117">This restriction does not apply to other containers, such as address books and distribution lists.</span></span> 
  
<span data-ttu-id="79064-118">Provedores de serviços devem definir o valor dessa propriedade para que ela contenha ambas as informações de configuração e o tipo de provedor.</span><span class="sxs-lookup"><span data-stu-id="79064-118">Service providers should set the value of this property so that it contains both the provider type and configuration information.</span></span> <span data-ttu-id="79064-119">As informações adicionais ajudam a diferenciar instâncias dos provedores do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="79064-119">The additional information helps to distinguish between instances of providers of the same type.</span></span> <span data-ttu-id="79064-120">Não configurados provedores devem usar uma cadeia de caracteres que nomeia o provedor.</span><span class="sxs-lookup"><span data-stu-id="79064-120">Unconfigured providers should use a string that names the provider.</span></span> <span data-ttu-id="79064-121">Provedores configurados devem usar a mesma cadeia seguida por uma cadeia de caracteres distintas entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="79064-121">Configured providers should use the same string followed by a distinguishing string in parentheses.</span></span> <span data-ttu-id="79064-122">Por exemplo, um provedor de armazenamento de mensagem não configurado pode definir essas propriedades:</span><span class="sxs-lookup"><span data-stu-id="79064-122">For example, an unconfigured message store provider might set these properties to:</span></span> 
  
<span data-ttu-id="79064-123">Armazenamento de informações pessoais</span><span class="sxs-lookup"><span data-stu-id="79064-123">Personal Information Store</span></span>
  
<span data-ttu-id="79064-124">A versão configurada, em seguida, pode definir essas propriedades:</span><span class="sxs-lookup"><span data-stu-id="79064-124">The configured version could then set these properties to:</span></span> 
  
<span data-ttu-id="79064-125">Armazenamento de informações pessoais (6 de fevereiro de 1998)</span><span class="sxs-lookup"><span data-stu-id="79064-125">Personal Information Store (February 6, 1998)</span></span>
  
<span data-ttu-id="79064-126">Para objetos de status, essas propriedades contêm o nome do componente que pode ser exibido pela interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="79064-126">For status objects, these properties contain the name of the component that can be displayed by the user interface.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="79064-127">Ponto e vírgula não pode ser usada em nomes de destinatário em mensagens de MAPI.</span><span class="sxs-lookup"><span data-stu-id="79064-127">Semicolons cannot be used within recipient names in MAPI messaging.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="79064-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="79064-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="79064-129">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="79064-129">Protocol specifications</span></span>

<span data-ttu-id="79064-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="79064-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="79064-131">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="79064-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="79064-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="79064-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="79064-133">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="79064-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="79064-134">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="79064-134">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="79064-135">Trata as operações de pasta.</span><span class="sxs-lookup"><span data-stu-id="79064-135">Handles folder operations.</span></span>
    
<span data-ttu-id="79064-136">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="79064-136">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="79064-137">Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="79064-137">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="79064-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="79064-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="79064-139">Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="79064-139">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="79064-140">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="79064-140">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="79064-141">Converte de convenções de email padrão da Internet para os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="79064-141">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="79064-142">[[MS-XWDVSEC]](https://msdn.microsoft.com/library/dc043d09-6b76-4392-aea3-68f8e81c64d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="79064-142">[[MS-XWDVSEC]](https://msdn.microsoft.com/library/dc043d09-6b76-4392-aea3-68f8e81c64d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="79064-143">Estende o protocolo WebDAV que especifica como solicitar e definir o descritor de segurança do Exchange por meio de métodos de WebDAV.</span><span class="sxs-lookup"><span data-stu-id="79064-143">Extends the WebDAV protocol that specifies how to request and set the Exchange security descriptor via WebDAV methods.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="79064-144">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="79064-144">Header files</span></span>

<span data-ttu-id="79064-145">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="79064-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="79064-146">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="79064-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="79064-147">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="79064-147">Mapitags.h</span></span>
  
> <span data-ttu-id="79064-148">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="79064-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="79064-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="79064-149">See also</span></span>



[<span data-ttu-id="79064-150">Propriedade canônica PidTagTransmittableDisplayName</span><span class="sxs-lookup"><span data-stu-id="79064-150">PidTagTransmittableDisplayName Canonical Property</span></span>](pidtagtransmittabledisplayname-canonical-property.md)


[<span data-ttu-id="79064-151">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="79064-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="79064-152">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="79064-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="79064-153">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="79064-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="79064-154">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="79064-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

