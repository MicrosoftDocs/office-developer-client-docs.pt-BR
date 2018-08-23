---
title: Propriedade canônica PidTagObjectType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagObjectType
api_type:
- HeaderDef
ms.assetid: 37da4ff5-300d-479f-a8b4-6fc36df997d9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8b2d435e132bf453cf41ec141d5a946bf54f9c66
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591048"
---
# <a name="pidtagobjecttype-canonical-property"></a><span data-ttu-id="c4d20-103">Propriedade canônica PidTagObjectType</span><span class="sxs-lookup"><span data-stu-id="c4d20-103">PidTagObjectType Canonical Property</span></span>

  
  
<span data-ttu-id="c4d20-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4d20-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4d20-105">Contém o tipo de um objeto.</span><span class="sxs-lookup"><span data-stu-id="c4d20-105">Contains the type of an object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c4d20-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="c4d20-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c4d20-107">PR_OBJECT_TYPE</span><span class="sxs-lookup"><span data-stu-id="c4d20-107">PR_OBJECT_TYPE</span></span>  <br/> |
|<span data-ttu-id="c4d20-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c4d20-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c4d20-109">0x0FFE</span><span class="sxs-lookup"><span data-stu-id="c4d20-109">0x0FFE</span></span>  <br/> |
|<span data-ttu-id="c4d20-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="c4d20-110">Data type:</span></span>  <br/> |<span data-ttu-id="c4d20-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c4d20-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c4d20-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c4d20-112">Area:</span></span>  <br/> |<span data-ttu-id="c4d20-113">Comuns</span><span class="sxs-lookup"><span data-stu-id="c4d20-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4d20-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c4d20-114">Remarks</span></span>

<span data-ttu-id="c4d20-115">O tipo de objeto contido nessa propriedade corresponde à interface principal disponível para um objeto acessível por meio da interface **OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="c4d20-115">The object type contained in this property corresponds to the primary interface available for an object accessible through the **OpenEntry** interface.</span></span> <span data-ttu-id="c4d20-116">Ele geralmente é obtido consultando o parâmetro _lpulObjType_ retornado pelo método **OpenEntry** apropriado.</span><span class="sxs-lookup"><span data-stu-id="c4d20-116">It is usually obtained by consulting the  _lpulObjType_ parameter returned by the appropriate **OpenEntry** method.</span></span> <span data-ttu-id="c4d20-117">Quando a interface é obtida de outras maneiras, chame [IMAPIProp::GetProps](imapiprop-getprops.md) para obter o valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c4d20-117">When the interface is obtained in other ways, call [IMAPIProp::GetProps](imapiprop-getprops.md) to obtain the value for this property.</span></span> 
  
<span data-ttu-id="c4d20-118">Essa propriedade pode ter exatamente um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="c4d20-118">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="c4d20-119">MAPI_ABCONT</span><span class="sxs-lookup"><span data-stu-id="c4d20-119">MAPI_ABCONT</span></span> 
  
> <span data-ttu-id="c4d20-120">Objeto de contêiner de catálogos de endereços</span><span class="sxs-lookup"><span data-stu-id="c4d20-120">Address book container object</span></span> 
    
<span data-ttu-id="c4d20-121">MAPI_ADDRBOOK</span><span class="sxs-lookup"><span data-stu-id="c4d20-121">MAPI_ADDRBOOK</span></span> 
  
> <span data-ttu-id="c4d20-122">Objeto de catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="c4d20-122">Address book object</span></span> 
    
<span data-ttu-id="c4d20-123">MAPI_ATTACH</span><span class="sxs-lookup"><span data-stu-id="c4d20-123">MAPI_ATTACH</span></span> 
  
> <span data-ttu-id="c4d20-124">Objeto de anexo de Message</span><span class="sxs-lookup"><span data-stu-id="c4d20-124">Message attachment object</span></span> 
    
<span data-ttu-id="c4d20-125">MAPI_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="c4d20-125">MAPI_DISTLIST</span></span> 
  
> <span data-ttu-id="c4d20-126">Objeto de lista de distribuição</span><span class="sxs-lookup"><span data-stu-id="c4d20-126">Distribution list object</span></span> 
    
<span data-ttu-id="c4d20-127">MAPI_FOLDER</span><span class="sxs-lookup"><span data-stu-id="c4d20-127">MAPI_FOLDER</span></span> 
  
> <span data-ttu-id="c4d20-128">Objeto Folder</span><span class="sxs-lookup"><span data-stu-id="c4d20-128">Folder object</span></span> 
    
<span data-ttu-id="c4d20-129">MAPI_FORMINFO</span><span class="sxs-lookup"><span data-stu-id="c4d20-129">MAPI_FORMINFO</span></span> 
  
> <span data-ttu-id="c4d20-130">Objeto Form</span><span class="sxs-lookup"><span data-stu-id="c4d20-130">Form object</span></span> 
    
<span data-ttu-id="c4d20-131">MAPI_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="c4d20-131">MAPI_MAILUSER</span></span> 
  
> <span data-ttu-id="c4d20-132">Objeto de usuário de mensagens</span><span class="sxs-lookup"><span data-stu-id="c4d20-132">Messaging user object</span></span> 
    
<span data-ttu-id="c4d20-133">MAPI_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="c4d20-133">MAPI_MESSAGE</span></span> 
  
> <span data-ttu-id="c4d20-134">Objeto de mensagem</span><span class="sxs-lookup"><span data-stu-id="c4d20-134">Message object</span></span> 
    
<span data-ttu-id="c4d20-135">MAPI_PROFSECT</span><span class="sxs-lookup"><span data-stu-id="c4d20-135">MAPI_PROFSECT</span></span> 
  
> <span data-ttu-id="c4d20-136">Objeto section de perfil</span><span class="sxs-lookup"><span data-stu-id="c4d20-136">Profile section object</span></span> 
    
<span data-ttu-id="c4d20-137">MAPI_SESSION</span><span class="sxs-lookup"><span data-stu-id="c4d20-137">MAPI_SESSION</span></span> 
  
> <span data-ttu-id="c4d20-138">Objeto da sessão</span><span class="sxs-lookup"><span data-stu-id="c4d20-138">Session object</span></span> 
    
<span data-ttu-id="c4d20-139">MAPI_STATUS</span><span class="sxs-lookup"><span data-stu-id="c4d20-139">MAPI_STATUS</span></span> 
  
> <span data-ttu-id="c4d20-140">Objeto de status</span><span class="sxs-lookup"><span data-stu-id="c4d20-140">Status object</span></span> 
    
<span data-ttu-id="c4d20-141">MAPI_STORE</span><span class="sxs-lookup"><span data-stu-id="c4d20-141">MAPI_STORE</span></span> 
  
> <span data-ttu-id="c4d20-142">Objeto de repositório de mensagem</span><span class="sxs-lookup"><span data-stu-id="c4d20-142">Message store object</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="c4d20-143">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c4d20-143">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c4d20-144">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="c4d20-144">Protocol specifications</span></span>

<span data-ttu-id="c4d20-145">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4d20-145">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4d20-146">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c4d20-146">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c4d20-147">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4d20-147">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4d20-148">Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="c4d20-148">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="c4d20-149">[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4d20-149">[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4d20-150">Trata a comunicação do cliente com um servidor de nome serviço provedor NSPI (Interface).</span><span class="sxs-lookup"><span data-stu-id="c4d20-150">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
<span data-ttu-id="c4d20-151">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4d20-151">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4d20-152">Trata as operações de pasta.</span><span class="sxs-lookup"><span data-stu-id="c4d20-152">Handles folder operations.</span></span>
    
<span data-ttu-id="c4d20-153">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4d20-153">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4d20-154">Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="c4d20-154">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="c4d20-155">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4d20-155">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4d20-156">Converte de convenções de email padrão da Internet para os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="c4d20-156">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="c4d20-157">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4d20-157">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4d20-158">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="c4d20-158">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="c4d20-159">[[MS-OXOAB]](http://msdn.microsoft.com/library/b4750386-66ec-4e69-abb6-208dd131c7de%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4d20-159">[[MS-OXOAB]](http://msdn.microsoft.com/library/b4750386-66ec-4e69-abb6-208dd131c7de%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4d20-160">Especifica os formatos de arquivo do OAB (catálogo) de endereços offline para o cache de objetos do catálogo de endereço local.</span><span class="sxs-lookup"><span data-stu-id="c4d20-160">Specifies the offline address book (OAB) file formats for the local address book objects cache.</span></span>
    
<span data-ttu-id="c4d20-161">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4d20-161">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4d20-162">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="c4d20-162">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="c4d20-163">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4d20-163">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4d20-164">Especifica as propriedades e operações para a manipulação de uma configuração de lista da pasta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c4d20-164">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c4d20-165">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c4d20-165">Header files</span></span>

<span data-ttu-id="c4d20-166">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c4d20-166">Mapidefs.h</span></span>
  
> <span data-ttu-id="c4d20-167">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c4d20-167">Provides data type definitions.</span></span>
    
<span data-ttu-id="c4d20-168">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c4d20-168">Mapitags.h</span></span>
  
> <span data-ttu-id="c4d20-169">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="c4d20-169">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c4d20-170">Confira também</span><span class="sxs-lookup"><span data-stu-id="c4d20-170">See also</span></span>



[<span data-ttu-id="c4d20-171">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c4d20-171">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c4d20-172">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="c4d20-172">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c4d20-173">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="c4d20-173">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c4d20-174">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="c4d20-174">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

