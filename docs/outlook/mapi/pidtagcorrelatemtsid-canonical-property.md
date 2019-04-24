---
title: Propriedade canônica PidTagCorrelateMtsid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCorrelateMtsid
api_type:
- HeaderDef
ms.assetid: d0fc4e91-ed90-4d27-bd23-f01e99728e2d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 96bfc184752b6a3e15434ad67ac8c2b4b26cac4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359931"
---
# <a name="pidtagcorrelatemtsid-canonical-property"></a><span data-ttu-id="80e53-103">Propriedade canônica PidTagCorrelateMtsid</span><span class="sxs-lookup"><span data-stu-id="80e53-103">PidTagCorrelateMtsid Canonical Property</span></span>

  
  
<span data-ttu-id="80e53-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80e53-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80e53-105">Contém o identificador MTS (sistema de transferência de mensagens) usado na correlação de relatórios com mensagens enviadas.</span><span class="sxs-lookup"><span data-stu-id="80e53-105">Contains the message transfer system (MTS) identifier used in correlating reports with sent messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="80e53-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="80e53-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="80e53-107">PR_CORRELATE_MTSID</span><span class="sxs-lookup"><span data-stu-id="80e53-107">PR_CORRELATE_MTSID</span></span>  <br/> |
|<span data-ttu-id="80e53-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="80e53-108">Identifier:</span></span>  <br/> |<span data-ttu-id="80e53-109">0x0E0D</span><span class="sxs-lookup"><span data-stu-id="80e53-109">0x0E0D</span></span>  <br/> |
|<span data-ttu-id="80e53-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="80e53-110">Data type:</span></span>  <br/> |<span data-ttu-id="80e53-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="80e53-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="80e53-112">Área:</span><span class="sxs-lookup"><span data-stu-id="80e53-112">Area:</span></span>  <br/> |<span data-ttu-id="80e53-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="80e53-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="80e53-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="80e53-114">Remarks</span></span>

<span data-ttu-id="80e53-115">Quando um provedor de transporte encontra uma mensagem enviada com essa propriedade definida como TRUE, ela define essa propriedade como o identificador MTS para essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="80e53-115">When a transport provider encounters a submitted message with this property set to TRUE, it sets this property to the MTS identifier for that message.</span></span> <span data-ttu-id="80e53-116">Após a transmissão, essa propriedade é armazenada com a mensagem na pasta Itens enviados da mensagem de interpessoa (IPM).</span><span class="sxs-lookup"><span data-stu-id="80e53-116">Following transmission, this property is stored with the message in the interpersonal message (IPM) Sent Items folder.</span></span>
  
<span data-ttu-id="80e53-117">Os sistemas de mensagens que dão suporte à correlação pelo identificador MTS, como X. 400, retêm o identificador como parte do envelope de transporte da mensagem original e também de quaisquer relatórios gerados em resposta a ele.</span><span class="sxs-lookup"><span data-stu-id="80e53-117">Messaging systems that support correlation by MTS identifier, such as X.400, retain the identifier as part of the transport envelope of the original message and also of any reports generated in response to it.</span></span> <span data-ttu-id="80e53-118">Quando um relatório é entregue a partir de um sistema de mensagens, o provedor de transporte define essa propriedade para o identificador MTS original do envelope de transporte do relatório.</span><span class="sxs-lookup"><span data-stu-id="80e53-118">When a report is delivered from such a messaging system, the transport provider sets this property to the original MTS identifier from the report's transport envelope.</span></span> <span data-ttu-id="80e53-119">Essa propriedade é então armazenada com o relatório.</span><span class="sxs-lookup"><span data-stu-id="80e53-119">This property is then stored with the report.</span></span>
  
<span data-ttu-id="80e53-120">Um aplicativo cliente pode manter uma pasta de resultados de pesquisa de todas as mensagens com esta propriedade.</span><span class="sxs-lookup"><span data-stu-id="80e53-120">A client application can maintain a search-results folder of all messages having this property.</span></span> <span data-ttu-id="80e53-121">Quando um relatório chega a uma mensagem, o cliente pode aplicar restrições à pasta Search-Results, localizar a versão original da mensagem e correlacionar as informações da mensagem original com as novas informações.</span><span class="sxs-lookup"><span data-stu-id="80e53-121">When a report comes in for such a message, the client can apply restrictions to the search-results folder, find the original version of the message, and correlate the original message information with the new information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="80e53-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="80e53-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="80e53-123">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="80e53-123">Header files</span></span>

<span data-ttu-id="80e53-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="80e53-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="80e53-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="80e53-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="80e53-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="80e53-126">Mapitags.h</span></span>
  
> <span data-ttu-id="80e53-127">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="80e53-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="80e53-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="80e53-128">See also</span></span>



[<span data-ttu-id="80e53-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="80e53-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="80e53-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="80e53-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="80e53-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="80e53-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="80e53-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="80e53-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

