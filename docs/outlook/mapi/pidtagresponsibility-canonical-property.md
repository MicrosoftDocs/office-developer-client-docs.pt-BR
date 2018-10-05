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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393801"
---
# <a name="pidtagresponsibility-canonical-property"></a><span data-ttu-id="120d1-103">Propriedade canônica PidTagResponsibility</span><span class="sxs-lookup"><span data-stu-id="120d1-103">PidTagResponsibility Canonical Property</span></span>

  
  
<span data-ttu-id="120d1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="120d1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="120d1-105">Contém TRUE se algum provedor de transporte já aceita responsabilidade para entregar a mensagem para este destinatário e FALSE se o MAPI spooler considera que esse provedor de transporte deve aceitar a responsabilidade.</span><span class="sxs-lookup"><span data-stu-id="120d1-105">Contains TRUE if some transport provider has already accepted responsibility for delivering the message to this recipient, and FALSE if the MAPI spooler considers that this transport provider should accept responsibility.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="120d1-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="120d1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="120d1-107">PR_RESPONSIBILITY</span><span class="sxs-lookup"><span data-stu-id="120d1-107">PR_RESPONSIBILITY</span></span>  <br/> |
|<span data-ttu-id="120d1-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="120d1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="120d1-109">0x0E0F</span><span class="sxs-lookup"><span data-stu-id="120d1-109">0x0E0F</span></span>  <br/> |
|<span data-ttu-id="120d1-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="120d1-110">Data type:</span></span>  <br/> |<span data-ttu-id="120d1-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="120d1-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="120d1-112">Área:</span><span class="sxs-lookup"><span data-stu-id="120d1-112">Area:</span></span>  <br/> |<span data-ttu-id="120d1-113">MAPI não transmittable</span><span class="sxs-lookup"><span data-stu-id="120d1-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="120d1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="120d1-114">Remarks</span></span>

<span data-ttu-id="120d1-115">Quando o MAPI spooler apresenta uma mensagem de saída para um provedor de transporte, por meio de [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), ela define essa propriedade como FALSE para todos os destinatários para os quais o MAPI spooler considera desse provedor de transporte responsável e TRUE para todos outros destinatários.</span><span class="sxs-lookup"><span data-stu-id="120d1-115">When the MAPI spooler presents an outbound message to a transport provider, through [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), it sets this property to FALSE for all recipients for which the MAPI spooler considers that transport provider responsible, and TRUE for all other recipients.</span></span> <span data-ttu-id="120d1-116">O provedor de transporte deve tentar lidar com todos os destinatários com **PR_RESPONSIBILITY** definido como FALSE.</span><span class="sxs-lookup"><span data-stu-id="120d1-116">The transport provider should attempt to handle all recipients with **PR_RESPONSIBILITY** set to FALSE.</span></span> <span data-ttu-id="120d1-117">Após enviar com êxito, ou definitivamente falhando enviar, para um destinatário, o provedor de transporte deve definir essa propriedade como TRUE na mensagem de origem para indicar que ela aceita a responsabilidade para que o destinatário.</span><span class="sxs-lookup"><span data-stu-id="120d1-117">After successfully sending, or conclusively failing to send, to a recipient, the transport provider should set this property to TRUE in the source message to indicate that it has accepted responsibility for that recipient.</span></span> 
  
<span data-ttu-id="120d1-118">Se, depois de examinar um destinatário, um provedor de transporte decidir que ele não pode ou não deveria tratar, o provedor de transporte deverá manter **PR_RESPONSIBILITY** definido como FALSE.</span><span class="sxs-lookup"><span data-stu-id="120d1-118">If, after examining a recipient, a transport provider decides that it cannot or should not handle it, the transport provider should leave **PR_RESPONSIBILITY** set to FALSE.</span></span> <span data-ttu-id="120d1-119">O MAPI spooler então procurará outro provedor de transporte que pode lidar com que o destinatário.</span><span class="sxs-lookup"><span data-stu-id="120d1-119">The MAPI spooler will then look for another transport provider that can handle that recipient.</span></span> <span data-ttu-id="120d1-120">O MAPI spooler basicamente criará um relatório de não entrega para quaisquer destinatários para os quais nenhum provedor de transporte aceita responsabilidade.</span><span class="sxs-lookup"><span data-stu-id="120d1-120">The MAPI spooler ultimately creates a nondelivery report for any recipients for which no transport provider accepts responsibility.</span></span> 
  
<span data-ttu-id="120d1-121">Se o provedor de transporte tentará e falha entregar a mensagem, ele deve chamar o método [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) para indicar ao MAPI os motivos para a falha, para que o MAPI pode gerar um relatório de não entrega.</span><span class="sxs-lookup"><span data-stu-id="120d1-121">If the transport provider attempts and fails to deliver the message, it should call the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to indicate to MAPI the reasons for the failure, so that MAPI can generate a nondelivery report.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="120d1-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="120d1-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="120d1-123">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="120d1-123">Protocol specifications</span></span>

<span data-ttu-id="120d1-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="120d1-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="120d1-125">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="120d1-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="120d1-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="120d1-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="120d1-127">Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="120d1-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="120d1-128">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="120d1-128">Header files</span></span>

<span data-ttu-id="120d1-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="120d1-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="120d1-130">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="120d1-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="120d1-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="120d1-131">Mapitags.h</span></span>
  
> <span data-ttu-id="120d1-132">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="120d1-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="120d1-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="120d1-133">See also</span></span>



[<span data-ttu-id="120d1-134">Propriedade canônica PidTagDeleteAfterSubmit</span><span class="sxs-lookup"><span data-stu-id="120d1-134">PidTagDeleteAfterSubmit Canonical Property</span></span>](pidtagdeleteaftersubmit-canonical-property.md)


[<span data-ttu-id="120d1-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="120d1-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="120d1-136">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="120d1-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="120d1-137">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="120d1-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="120d1-138">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="120d1-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

