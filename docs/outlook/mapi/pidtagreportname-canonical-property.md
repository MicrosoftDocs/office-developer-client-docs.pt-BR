---
title: Propriedade canônica PidTagReportName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportName
api_type:
- COM
ms.assetid: 4ec3100f-7cf1-4702-b326-e6da586a7bb2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3c1a848eec84c7d81792a95baa3f47fa6779e95f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569579"
---
# <a name="pidtagreportname-canonical-property"></a><span data-ttu-id="b78c7-103">Propriedade canônica PidTagReportName</span><span class="sxs-lookup"><span data-stu-id="b78c7-103">PidTagReportName Canonical Property</span></span>

  
  
<span data-ttu-id="b78c7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b78c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b78c7-105">Contém o nome de exibição para o destinatário que deve obter relatórios para esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="b78c7-105">Contains the display name for the recipient that should get reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b78c7-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="b78c7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b78c7-107">PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W</span><span class="sxs-lookup"><span data-stu-id="b78c7-107">PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W</span></span>  <br/> |
|<span data-ttu-id="b78c7-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b78c7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b78c7-109">0x003A</span><span class="sxs-lookup"><span data-stu-id="b78c7-109">0x003A</span></span>  <br/> |
|<span data-ttu-id="b78c7-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="b78c7-110">Data type:</span></span>  <br/> |<span data-ttu-id="b78c7-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b78c7-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b78c7-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b78c7-112">Area:</span></span>  <br/> |<span data-ttu-id="b78c7-113">Envelope MAPI</span><span class="sxs-lookup"><span data-stu-id="b78c7-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b78c7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b78c7-114">Remarks</span></span>

<span data-ttu-id="b78c7-115">Essas propriedades são exemplos das propriedades de endereço do destinatário que o remetente tenha delegada para receber qualquer relatórios gerados para esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="b78c7-115">These properties are examples of the address properties for the recipient that the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="b78c7-116">Um aplicativo cliente que deve rotear relatórios para outro usuário deve definir essas propriedades em tempo de envio de mensagem.</span><span class="sxs-lookup"><span data-stu-id="b78c7-116">A client application that must route reports to another user should set these properties at message submission time.</span></span> <span data-ttu-id="b78c7-117">Se não estiver definidas, os relatórios são enviados para o remetente da mensagem.</span><span class="sxs-lookup"><span data-stu-id="b78c7-117">If they are not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b78c7-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b78c7-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b78c7-119">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b78c7-119">Header files</span></span>

<span data-ttu-id="b78c7-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b78c7-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="b78c7-121">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="b78c7-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="b78c7-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b78c7-122">Mapitags.h</span></span>
  
> <span data-ttu-id="b78c7-123">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="b78c7-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b78c7-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="b78c7-124">See also</span></span>



[<span data-ttu-id="b78c7-125">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b78c7-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b78c7-126">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="b78c7-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b78c7-127">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="b78c7-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b78c7-128">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="b78c7-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

