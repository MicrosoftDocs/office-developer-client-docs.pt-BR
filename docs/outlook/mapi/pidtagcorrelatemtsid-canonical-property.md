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
ms.openlocfilehash: 57da2d4c78914323b5dafa4f5ba5b7628d0e2f2f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769145"
---
# <a name="pidtagcorrelatemtsid-canonical-property"></a><span data-ttu-id="12cf0-103">Propriedade canônica PidTagCorrelateMtsid</span><span class="sxs-lookup"><span data-stu-id="12cf0-103">PidTagCorrelateMtsid Canonical Property</span></span>

  
  
<span data-ttu-id="12cf0-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="12cf0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="12cf0-105">Contém o identificador de sistema (MTS) de transferência de mensagem usado na correlação relatórios com as mensagens enviadas.</span><span class="sxs-lookup"><span data-stu-id="12cf0-105">Contains the message transfer system (MTS) identifier used in correlating reports with sent messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="12cf0-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="12cf0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="12cf0-107">PR_CORRELATE_MTSID</span><span class="sxs-lookup"><span data-stu-id="12cf0-107">PR_CORRELATE_MTSID</span></span>  <br/> |
|<span data-ttu-id="12cf0-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="12cf0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="12cf0-109">0x0E0D</span><span class="sxs-lookup"><span data-stu-id="12cf0-109">0x0E0D</span></span>  <br/> |
|<span data-ttu-id="12cf0-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="12cf0-110">Data type:</span></span>  <br/> |<span data-ttu-id="12cf0-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="12cf0-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="12cf0-112">Área:</span><span class="sxs-lookup"><span data-stu-id="12cf0-112">Area:</span></span>  <br/> |<span data-ttu-id="12cf0-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="12cf0-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="12cf0-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="12cf0-114">Remarks</span></span>

<span data-ttu-id="12cf0-115">Quando um provedor de transporte encontra uma mensagem enviada com esta propriedade é definida como TRUE, ele define essa propriedade para o identificador de MTS para essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="12cf0-115">When a transport provider encounters a submitted message with this property set to TRUE, it sets this property to the MTS identifier for that message.</span></span> <span data-ttu-id="12cf0-116">Após a transmissão, essa propriedade é armazenada com a mensagem na pasta Itens enviados interpessoais mensagens (IPM).</span><span class="sxs-lookup"><span data-stu-id="12cf0-116">Following transmission, this property is stored with the message in the interpersonal message (IPM) Sent Items folder.</span></span>
  
<span data-ttu-id="12cf0-117">Sistemas de mensagens que oferecem suporte a correlação pelo identificador MTS, como x. 400, retêm o identificador como parte do envelope transporte da mensagem original e também de quaisquer relatórios gerados em resposta a ele.</span><span class="sxs-lookup"><span data-stu-id="12cf0-117">Messaging systems that support correlation by MTS identifier, such as X.400, retain the identifier as part of the transport envelope of the original message and also of any reports generated in response to it.</span></span> <span data-ttu-id="12cf0-118">Quando um relatório é entregue de tal um sistema de mensagens, o provedor de transporte define essa propriedade para o identificador de MTS original do envelope de transporte do relatório.</span><span class="sxs-lookup"><span data-stu-id="12cf0-118">When a report is delivered from such a messaging system, the transport provider sets this property to the original MTS identifier from the report's transport envelope.</span></span> <span data-ttu-id="12cf0-119">Em seguida, essa propriedade é armazenada com o relatório.</span><span class="sxs-lookup"><span data-stu-id="12cf0-119">This property is then stored with the report.</span></span>
  
<span data-ttu-id="12cf0-120">Um aplicativo cliente pode manter uma pasta de resultados de pesquisa de todas as mensagens que têm essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="12cf0-120">A client application can maintain a search-results folder of all messages having this property.</span></span> <span data-ttu-id="12cf0-121">Quando um relatório entra dessa mensagem, o cliente pode aplicar restrições para a pasta de resultados de pesquisa, encontre a versão original da mensagem e correlacionar informações da mensagem original com as novas informações.</span><span class="sxs-lookup"><span data-stu-id="12cf0-121">When a report comes in for such a message, the client can apply restrictions to the search-results folder, find the original version of the message, and correlate the original message information with the new information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="12cf0-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="12cf0-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="12cf0-123">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="12cf0-123">Header files</span></span>

<span data-ttu-id="12cf0-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="12cf0-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="12cf0-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="12cf0-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="12cf0-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="12cf0-126">Mapitags.h</span></span>
  
> <span data-ttu-id="12cf0-127">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="12cf0-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="12cf0-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="12cf0-128">See also</span></span>



[<span data-ttu-id="12cf0-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="12cf0-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="12cf0-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="12cf0-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="12cf0-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="12cf0-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="12cf0-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="12cf0-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

