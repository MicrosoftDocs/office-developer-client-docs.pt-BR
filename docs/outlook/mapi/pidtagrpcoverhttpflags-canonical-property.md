---
title: Propriedade canônica PidTagRpcOverHttpFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c8b30768-cf83-450d-9fe2-567a5e0c2f57
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cf1f3b4d72426fb5f80decdc074a622b140657c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327444"
---
# <a name="pidtagrpcoverhttpflags-canonical-property"></a><span data-ttu-id="a5f66-103">Propriedade canônica PidTagRpcOverHttpFlags</span><span class="sxs-lookup"><span data-stu-id="a5f66-103">PidTagRpcOverHttpFlags Canonical Property</span></span>

  
  
<span data-ttu-id="a5f66-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5f66-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5f66-105">Contém as configurações em um perfil usado pelo Microsoft Office Outlook para se conectar ao Microsoft Exchange Server usando uma chamada de procedimento remoto (RPC) sobre Protocolo de Transferência de Hipertexto (HTTP).</span><span class="sxs-lookup"><span data-stu-id="a5f66-105">Contains the settings in a profile used by Microsoft Office Outlook to connect to Microsoft Exchange Server by using a remote procedure call (RPC) over Hypertext Transfer Protocol (HTTP).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a5f66-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a5f66-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a5f66-107">PR_ROH_FLAGS</span><span class="sxs-lookup"><span data-stu-id="a5f66-107">PR_ROH_FLAGS</span></span>  <br/> |
|<span data-ttu-id="a5f66-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a5f66-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a5f66-109">0x6623</span><span class="sxs-lookup"><span data-stu-id="a5f66-109">0x6623</span></span>  <br/> |
|<span data-ttu-id="a5f66-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a5f66-110">Data type:</span></span>  <br/> |<span data-ttu-id="a5f66-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a5f66-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a5f66-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a5f66-112">Area:</span></span>  <br/> |<span data-ttu-id="a5f66-113">Diversos</span><span class="sxs-lookup"><span data-stu-id="a5f66-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a5f66-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5f66-114">Remarks</span></span>

<span data-ttu-id="a5f66-115">A **PR_ROH_FLAGS** é armazenada na Seção de Perfil Global de um perfil MAPI (Messaging Application Programming Interface).</span><span class="sxs-lookup"><span data-stu-id="a5f66-115">The **PR_ROH_FLAGS** property is stored in the Global Profile Section of a Messaging Application Programming Interface (MAPI) profile.</span></span> <span data-ttu-id="a5f66-116">O valor de **PR_ROH_FLAGS** é uma bitmask que é feita de um ou mais dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a5f66-116">The value of **PR_ROH_FLAGS** is a bitmask that is made up of one or more of the following flags.</span></span> 
  
|<span data-ttu-id="a5f66-117">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a5f66-117">**Name**</span></span>|<span data-ttu-id="a5f66-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a5f66-118">**Value**</span></span>|<span data-ttu-id="a5f66-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a5f66-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a5f66-120">**ROHFLAGS_USE_ROH**</span><span class="sxs-lookup"><span data-stu-id="a5f66-120">**ROHFLAGS_USE_ROH**</span></span> <br/> |<span data-ttu-id="a5f66-121">0x1</span><span class="sxs-lookup"><span data-stu-id="a5f66-121">0x1</span></span>  <br/> |<span data-ttu-id="a5f66-122">Conecte-se ao Exchange Server usando RPC sobre HTTP.</span><span class="sxs-lookup"><span data-stu-id="a5f66-122">Connect to the Exchange Server using RPC over HTTP.</span></span>  <br/> |
|<span data-ttu-id="a5f66-123">**ROHFLAGS_SSL_ONLY**</span><span class="sxs-lookup"><span data-stu-id="a5f66-123">**ROHFLAGS_SSL_ONLY**</span></span> <br/> |<span data-ttu-id="a5f66-124">0x2</span><span class="sxs-lookup"><span data-stu-id="a5f66-124">0x2</span></span>  <br/> |<span data-ttu-id="a5f66-125">Conecte-se ao Exchange Server usando somente SSL (Secure Socket Layer).</span><span class="sxs-lookup"><span data-stu-id="a5f66-125">Connect to the Exchange Server using Secure Socket Layer (SSL) only.</span></span>  <br/> |
|<span data-ttu-id="a5f66-126">**ROHFLAGS_MUTUAL_AUTH**</span><span class="sxs-lookup"><span data-stu-id="a5f66-126">**ROHFLAGS_MUTUAL_AUTH**</span></span> <br/> |<span data-ttu-id="a5f66-127">0x4</span><span class="sxs-lookup"><span data-stu-id="a5f66-127">0x4</span></span>  <br/> |<span data-ttu-id="a5f66-128">Autenticar mutuamente a sessão ao se conectar usando SSL.</span><span class="sxs-lookup"><span data-stu-id="a5f66-128">Mutually authenticate the session when connecting by using SSL.</span></span>  <br/> |
|<span data-ttu-id="a5f66-129">**ROHFLAGS_HTTP_FIRST_ON_FAST**</span><span class="sxs-lookup"><span data-stu-id="a5f66-129">**ROHFLAGS_HTTP_FIRST_ON_FAST**</span></span> <br/> |<span data-ttu-id="a5f66-130">0x8</span><span class="sxs-lookup"><span data-stu-id="a5f66-130">0x8</span></span>  <br/> |<span data-ttu-id="a5f66-131">Em redes rápidas, conecte-se usando HTTP primeiro.</span><span class="sxs-lookup"><span data-stu-id="a5f66-131">On fast networks, connect by using HTTP first.</span></span> <span data-ttu-id="a5f66-132">Em seguida, conecte-se usando TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="a5f66-132">Then, connect by using TCP/IP.</span></span>  <br/> |
|<span data-ttu-id="a5f66-133">**ROHFLAGS_HTTP_FIRST_ON_SLOW**</span><span class="sxs-lookup"><span data-stu-id="a5f66-133">**ROHFLAGS_HTTP_FIRST_ON_SLOW**</span></span> <br/> |<span data-ttu-id="a5f66-134">0x20</span><span class="sxs-lookup"><span data-stu-id="a5f66-134">0x20</span></span>  <br/> |<span data-ttu-id="a5f66-135">Em redes lentas, conecte-se usando HTTP primeiro.</span><span class="sxs-lookup"><span data-stu-id="a5f66-135">On slow networks, connect by using HTTP first.</span></span> <span data-ttu-id="a5f66-136">Em seguida, conecte-se usando TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="a5f66-136">Then, connect by using TCP/IP.</span></span>  <br/> |
   
<span data-ttu-id="a5f66-137">Por exemplo, para definir a propriedade **PR_ROH_FLAGS** para ativar RPC sobre HTTP, para exigir SSL e especificar que o protocolo HTTP deve ser usado primeiro em conexões lentas, defina o valor da propriedade **PR_ROH_FLAGS** com o qual é igual a  `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` 0x23.</span><span class="sxs-lookup"><span data-stu-id="a5f66-137">For example, to set the **PR_ROH_FLAGS** property to turn on RPC over HTTP, to require SSL, and to specify that the HTTP protocol should be used first on slow connections, set the value of the **PR_ROH_FLAGS** property to  `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` which is equal to 0x23.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a5f66-138">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a5f66-138">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a5f66-139">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="a5f66-139">Protocol specifications</span></span>

<span data-ttu-id="a5f66-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5f66-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5f66-141">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a5f66-141">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a5f66-142">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5f66-142">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5f66-143">Define as estruturas de dados básicas que são usadas em operações remotas.</span><span class="sxs-lookup"><span data-stu-id="a5f66-143">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="a5f66-144">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5f66-144">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5f66-145">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="a5f66-145">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a5f66-146">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="a5f66-146">Header files</span></span>

<span data-ttu-id="a5f66-147">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a5f66-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="a5f66-148">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a5f66-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="a5f66-149">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a5f66-149">Mapitags.h</span></span>
  
> <span data-ttu-id="a5f66-150">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="a5f66-150">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a5f66-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5f66-151">See also</span></span>



[<span data-ttu-id="a5f66-152">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a5f66-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a5f66-153">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="a5f66-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a5f66-154">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a5f66-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a5f66-155">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="a5f66-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

