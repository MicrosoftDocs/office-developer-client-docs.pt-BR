---
title: Propriedade canônica PidTagResponsibility
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResponsibility
api_type:
- COM
ms.assetid: 1e8ccef1-db0a-4230-9bd0-87540b53e890
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 15bf61e71a2c230f7891c738661f839ecddb52e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330118"
---
# <a name="pidtagresponsibility-canonical-property"></a><span data-ttu-id="b0fac-103">Propriedade canônica PidTagResponsibility</span><span class="sxs-lookup"><span data-stu-id="b0fac-103">PidTagResponsibility Canonical Property</span></span>

  
  
<span data-ttu-id="b0fac-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0fac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0fac-105">Contém TRUE se algum provedor de transporte já aceitou a responsabilidade por entregar a mensagem a esse destinatário e FALSE se o spooler MAPI considera que esse provedor de transporte deve aceitar a responsabilidade.</span><span class="sxs-lookup"><span data-stu-id="b0fac-105">Contains TRUE if some transport provider has already accepted responsibility for delivering the message to this recipient, and FALSE if the MAPI spooler considers that this transport provider should accept responsibility.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b0fac-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="b0fac-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b0fac-107">PR_RESPONSIBILITY</span><span class="sxs-lookup"><span data-stu-id="b0fac-107">PR_RESPONSIBILITY</span></span>  <br/> |
|<span data-ttu-id="b0fac-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b0fac-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b0fac-109">0x0E0F</span><span class="sxs-lookup"><span data-stu-id="b0fac-109">0x0E0F</span></span>  <br/> |
|<span data-ttu-id="b0fac-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="b0fac-110">Data type:</span></span>  <br/> |<span data-ttu-id="b0fac-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="b0fac-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="b0fac-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b0fac-112">Area:</span></span>  <br/> |<span data-ttu-id="b0fac-113">MAPI não transmitível</span><span class="sxs-lookup"><span data-stu-id="b0fac-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b0fac-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0fac-114">Remarks</span></span>

<span data-ttu-id="b0fac-115">Quando o spooler MAPI apresenta uma mensagem de saída para um provedor de transporte, por meio de [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), ele define essa propriedade como FALSE para todos os destinatários para os quais o spooler MAPI considera esse provedor de transporte responsável e VERDADEIRO para todos os outros destinatários.</span><span class="sxs-lookup"><span data-stu-id="b0fac-115">When the MAPI spooler presents an outbound message to a transport provider, through [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), it sets this property to FALSE for all recipients for which the MAPI spooler considers that transport provider responsible, and TRUE for all other recipients.</span></span> <span data-ttu-id="b0fac-116">O provedor de transporte deve tentar manipular todos os destinatários **com** PR_RESPONSIBILITY definido como FALSE.</span><span class="sxs-lookup"><span data-stu-id="b0fac-116">The transport provider should attempt to handle all recipients with **PR_RESPONSIBILITY** set to FALSE.</span></span> <span data-ttu-id="b0fac-117">Depois de enviar com êxito ou falhar ao enviar, para um destinatário, o provedor de transporte deve definir essa propriedade como TRUE na mensagem de origem para indicar que ele aceitou a responsabilidade por esse destinatário.</span><span class="sxs-lookup"><span data-stu-id="b0fac-117">After successfully sending, or conclusively failing to send, to a recipient, the transport provider should set this property to TRUE in the source message to indicate that it has accepted responsibility for that recipient.</span></span> 
  
<span data-ttu-id="b0fac-118">Se, depois de examinar um destinatário, um provedor de transporte decidir que ele não pode ou não deve lidar com ele, o provedor de transporte deve PR_RESPONSIBILITY **definido** como FALSE.</span><span class="sxs-lookup"><span data-stu-id="b0fac-118">If, after examining a recipient, a transport provider decides that it cannot or should not handle it, the transport provider should leave **PR_RESPONSIBILITY** set to FALSE.</span></span> <span data-ttu-id="b0fac-119">O spooler MAPI procurará outro provedor de transporte que possa lidar com esse destinatário.</span><span class="sxs-lookup"><span data-stu-id="b0fac-119">The MAPI spooler will then look for another transport provider that can handle that recipient.</span></span> <span data-ttu-id="b0fac-120">O spooler MAPI, em última análise, cria um relatório de não entrega para quaisquer destinatários para os quais nenhum provedor de transporte aceite responsabilidade.</span><span class="sxs-lookup"><span data-stu-id="b0fac-120">The MAPI spooler ultimately creates a nondelivery report for any recipients for which no transport provider accepts responsibility.</span></span> 
  
<span data-ttu-id="b0fac-121">Se o provedor de transporte tentar e falhar ao entregar a mensagem, ele deverá chamar o método [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) para indicar a MAPI os motivos da falha, para que o MAPI possa gerar um relatório de não entrega.</span><span class="sxs-lookup"><span data-stu-id="b0fac-121">If the transport provider attempts and fails to deliver the message, it should call the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to indicate to MAPI the reasons for the failure, so that MAPI can generate a nondelivery report.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b0fac-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b0fac-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b0fac-123">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="b0fac-123">Protocol specifications</span></span>

<span data-ttu-id="b0fac-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0fac-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b0fac-125">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b0fac-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b0fac-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0fac-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b0fac-127">Lida com a ordem e o fluxo para transferências de dados entre um cliente e um servidor.</span><span class="sxs-lookup"><span data-stu-id="b0fac-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b0fac-128">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="b0fac-128">Header files</span></span>

<span data-ttu-id="b0fac-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b0fac-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="b0fac-130">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="b0fac-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="b0fac-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b0fac-131">Mapitags.h</span></span>
  
> <span data-ttu-id="b0fac-132">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="b0fac-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b0fac-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0fac-133">See also</span></span>



[<span data-ttu-id="b0fac-134">Propriedade canônica PidTagDeleteAfterSubmit</span><span class="sxs-lookup"><span data-stu-id="b0fac-134">PidTagDeleteAfterSubmit Canonical Property</span></span>](pidtagdeleteaftersubmit-canonical-property.md)


[<span data-ttu-id="b0fac-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b0fac-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b0fac-136">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="b0fac-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b0fac-137">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="b0fac-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b0fac-138">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="b0fac-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

