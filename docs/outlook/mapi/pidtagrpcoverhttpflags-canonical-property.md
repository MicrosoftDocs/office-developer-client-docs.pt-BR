---
title: Propriedade canônico de PidTagRpcOverHttpFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c8b30768-cf83-450d-9fe2-567a5e0c2f57
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 151aa730f2ae6a4d39ffa474eb7ecd79ed5602eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769858"
---
# <a name="pidtagrpcoverhttpflags-canonical-property"></a><span data-ttu-id="6de80-103">Propriedade canônico de PidTagRpcOverHttpFlags</span><span class="sxs-lookup"><span data-stu-id="6de80-103">PidTagRpcOverHttpFlags Canonical Property</span></span>

  
  
<span data-ttu-id="6de80-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6de80-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6de80-105">Contém as configurações em um perfil usado pelo Microsoft Office Outlook para se conectar ao Microsoft Exchange Server usando uma chamada de procedimento remoto (RPC) sobre HTTP (Hypertext Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="6de80-105">Contains the settings in a profile used by Microsoft Office Outlook to connect to Microsoft Exchange Server by using a remote procedure call (RPC) over Hypertext Transfer Protocol (HTTP).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6de80-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="6de80-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6de80-107">PR_ROH_FLAGS</span><span class="sxs-lookup"><span data-stu-id="6de80-107">PR_ROH_FLAGS</span></span>  <br/> |
|<span data-ttu-id="6de80-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="6de80-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6de80-109">0x6623</span><span class="sxs-lookup"><span data-stu-id="6de80-109">0x6623</span></span>  <br/> |
|<span data-ttu-id="6de80-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="6de80-110">Data type:</span></span>  <br/> |<span data-ttu-id="6de80-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6de80-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6de80-112">Área:</span><span class="sxs-lookup"><span data-stu-id="6de80-112">Area:</span></span>  <br/> |<span data-ttu-id="6de80-113">Diversos</span><span class="sxs-lookup"><span data-stu-id="6de80-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6de80-114">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="6de80-114">Remarks</span></span>

<span data-ttu-id="6de80-115">A propriedade **PR_ROH_FLAGS** é armazenada na seção perfil Global de um perfil de Messaging Application Programming Interface (MAPI).</span><span class="sxs-lookup"><span data-stu-id="6de80-115">The **PR_ROH_FLAGS** property is stored in the Global Profile Section of a Messaging Application Programming Interface (MAPI) profile.</span></span> <span data-ttu-id="6de80-116">O valor de **PR_ROH_FLAGS** é uma bitmask que é composta de um ou mais dos seguintes sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="6de80-116">The value of **PR_ROH_FLAGS** is a bitmask that is made up of one or more of the following flags.</span></span> 
  
|<span data-ttu-id="6de80-117">**Name**</span><span class="sxs-lookup"><span data-stu-id="6de80-117">**Name**</span></span>|<span data-ttu-id="6de80-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6de80-118">**Value**</span></span>|<span data-ttu-id="6de80-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6de80-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6de80-120">**ROHFLAGS_USE_ROH**</span><span class="sxs-lookup"><span data-stu-id="6de80-120">**ROHFLAGS_USE_ROH**</span></span> <br/> |<span data-ttu-id="6de80-121">0x1</span><span class="sxs-lookup"><span data-stu-id="6de80-121">0x1</span></span>  <br/> |<span data-ttu-id="6de80-122">Conecte-se ao servidor do Exchange usando RPC sobre HTTP.</span><span class="sxs-lookup"><span data-stu-id="6de80-122">Connect to the Exchange Server using RPC over HTTP.</span></span>  <br/> |
|<span data-ttu-id="6de80-123">**ROHFLAGS_SSL_ONLY**</span><span class="sxs-lookup"><span data-stu-id="6de80-123">**ROHFLAGS_SSL_ONLY**</span></span> <br/> |<span data-ttu-id="6de80-124">0x2</span><span class="sxs-lookup"><span data-stu-id="6de80-124">0x2</span></span>  <br/> |<span data-ttu-id="6de80-125">Conecte-se ao servidor do Exchange usando apenas o Secure Socket Layer (SSL).</span><span class="sxs-lookup"><span data-stu-id="6de80-125">Connect to the Exchange Server using Secure Socket Layer (SSL) only.</span></span>  <br/> |
|<span data-ttu-id="6de80-126">**ROHFLAGS_MUTUAL_AUTH**</span><span class="sxs-lookup"><span data-stu-id="6de80-126">**ROHFLAGS_MUTUAL_AUTH**</span></span> <br/> |<span data-ttu-id="6de80-127">0x4</span><span class="sxs-lookup"><span data-stu-id="6de80-127">0x4</span></span>  <br/> |<span data-ttu-id="6de80-128">Autenticar mutuamente a sessão durante a conexão usando SSL.</span><span class="sxs-lookup"><span data-stu-id="6de80-128">Mutually authenticate the session when connecting by using SSL.</span></span>  <br/> |
|<span data-ttu-id="6de80-129">**ROHFLAGS_HTTP_FIRST_ON_FAST**</span><span class="sxs-lookup"><span data-stu-id="6de80-129">**ROHFLAGS_HTTP_FIRST_ON_FAST**</span></span> <br/> |<span data-ttu-id="6de80-130">0x8</span><span class="sxs-lookup"><span data-stu-id="6de80-130">0x8</span></span>  <br/> |<span data-ttu-id="6de80-131">Em redes rápidas, conecte usando HTTP primeiro.</span><span class="sxs-lookup"><span data-stu-id="6de80-131">On fast networks, connect by using HTTP first.</span></span> <span data-ttu-id="6de80-132">Em seguida, conecte usando TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="6de80-132">Then, connect by using TCP/IP.</span></span>  <br/> |
|<span data-ttu-id="6de80-133">**ROHFLAGS_HTTP_FIRST_ON_SLOW**</span><span class="sxs-lookup"><span data-stu-id="6de80-133">**ROHFLAGS_HTTP_FIRST_ON_SLOW**</span></span> <br/> |<span data-ttu-id="6de80-134">0x20</span><span class="sxs-lookup"><span data-stu-id="6de80-134">0x20</span></span>  <br/> |<span data-ttu-id="6de80-135">Em redes lentas, conecte usando HTTP primeiro.</span><span class="sxs-lookup"><span data-stu-id="6de80-135">On slow networks, connect by using HTTP first.</span></span> <span data-ttu-id="6de80-136">Em seguida, conecte usando TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="6de80-136">Then, connect by using TCP/IP.</span></span>  <br/> |
   
<span data-ttu-id="6de80-137">Por exemplo, para definir o **PR_ROH_FLAGS** propriedade ativem RPC sobre HTTP, para exigir SSL e para especificar que o protocolo HTTP deve ser usado pela primeira vez em conexões lentas, defina o valor da propriedade **PR_ROH_FLAGS** como `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` que é igual a 0x23.</span><span class="sxs-lookup"><span data-stu-id="6de80-137">For example, to set the **PR_ROH_FLAGS** property to turn on RPC over HTTP, to require SSL, and to specify that the HTTP protocol should be used first on slow connections, set the value of the **PR_ROH_FLAGS** property to  `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` which is equal to 0x23.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6de80-138">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6de80-138">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6de80-139">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="6de80-139">Protocol specifications</span></span>

<span data-ttu-id="6de80-140">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6de80-140">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6de80-141">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6de80-141">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6de80-142">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6de80-142">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6de80-143">Define as estruturas de dados básicos que são usadas em operações remotas.</span><span class="sxs-lookup"><span data-stu-id="6de80-143">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="6de80-144">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6de80-144">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6de80-145">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="6de80-145">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6de80-146">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6de80-146">Header files</span></span>

<span data-ttu-id="6de80-147">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6de80-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="6de80-148">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="6de80-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="6de80-149">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6de80-149">Mapitags.h</span></span>
  
> <span data-ttu-id="6de80-150">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="6de80-150">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6de80-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="6de80-151">See also</span></span>



[<span data-ttu-id="6de80-152">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6de80-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6de80-153">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="6de80-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6de80-154">Mapear nomes de propriedade canônico para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="6de80-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6de80-155">Mapear nomes de MAPI para nomes de propriedade canônico</span><span class="sxs-lookup"><span data-stu-id="6de80-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

