---
title: Propriedade canônica PidTagMessageSubmissionId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSubmissionId
api_type:
- HeaderDef
ms.assetid: 0a799fe5-04e2-4e1d-b0cd-9bdd2577d299
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 723affa054cb35a9cc7a2ee28e051e3b9a6d04e0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401661"
---
# <a name="pidtagmessagesubmissionid-canonical-property"></a><span data-ttu-id="4f7b4-103">Propriedade canônica PidTagMessageSubmissionId</span><span class="sxs-lookup"><span data-stu-id="4f7b4-103">PidTagMessageSubmissionId Canonical Property</span></span>

  
  
<span data-ttu-id="4f7b4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f7b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f7b4-105">Contém um identificador de sistema (MTS) de transferência de mensagem para o agente de transferência de mensagem (MTA).</span><span class="sxs-lookup"><span data-stu-id="4f7b4-105">Contains a message transfer system (MTS) identifier for the message transfer agent (MTA).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4f7b4-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="4f7b4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4f7b4-107">PR_MESSAGE_SUBMISSION_ID</span><span class="sxs-lookup"><span data-stu-id="4f7b4-107">PR_MESSAGE_SUBMISSION_ID</span></span>  <br/> |
|<span data-ttu-id="4f7b4-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4f7b4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4f7b4-109">0x0047</span><span class="sxs-lookup"><span data-stu-id="4f7b4-109">0x0047</span></span>  <br/> |
|<span data-ttu-id="4f7b4-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="4f7b4-110">Data type:</span></span>  <br/> |<span data-ttu-id="4f7b4-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4f7b4-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4f7b4-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4f7b4-112">Area:</span></span>  <br/> |<span data-ttu-id="4f7b4-113">Email</span><span class="sxs-lookup"><span data-stu-id="4f7b4-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f7b4-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f7b4-114">Remarks</span></span>

<span data-ttu-id="4f7b4-115">Essa propriedade é retornada por MTA após a conclusão bem-sucedida do envio da mensagem.</span><span class="sxs-lookup"><span data-stu-id="4f7b4-115">This property is returned by the MTA upon successful completion of message submission.</span></span> <span data-ttu-id="4f7b4-116">Qualquer contato futuro com o MTA sobre essa mensagem, como o solicitante cancelamento, usa o identificador MTS nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="4f7b4-116">Any future contact with the MTA regarding this message, such as requesting cancellation, uses the MTS identifier in this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4f7b4-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4f7b4-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4f7b4-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="4f7b4-118">Protocol specifications</span></span>

<span data-ttu-id="4f7b4-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f7b4-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4f7b4-120">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="4f7b4-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4f7b4-121">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f7b4-121">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4f7b4-122">Codifica e decodifica objetos de mensagem e o anexo em uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="4f7b4-122">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4f7b4-123">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4f7b4-123">Header files</span></span>

<span data-ttu-id="4f7b4-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4f7b4-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="4f7b4-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="4f7b4-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="4f7b4-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4f7b4-126">Mapitags.h</span></span>
  
> <span data-ttu-id="4f7b4-127">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="4f7b4-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4f7b4-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f7b4-128">See also</span></span>



[<span data-ttu-id="4f7b4-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4f7b4-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4f7b4-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="4f7b4-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4f7b4-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="4f7b4-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4f7b4-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="4f7b4-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

