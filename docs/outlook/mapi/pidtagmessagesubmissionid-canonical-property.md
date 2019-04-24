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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329397"
---
# <a name="pidtagmessagesubmissionid-canonical-property"></a><span data-ttu-id="f56d7-103">Propriedade canônica PidTagMessageSubmissionId</span><span class="sxs-lookup"><span data-stu-id="f56d7-103">PidTagMessageSubmissionId Canonical Property</span></span>

  
  
<span data-ttu-id="f56d7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f56d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f56d7-105">Contém um identificador MTS (sistema de transferência de mensagens) para o MTA (agente de transferência de mensagens).</span><span class="sxs-lookup"><span data-stu-id="f56d7-105">Contains a message transfer system (MTS) identifier for the message transfer agent (MTA).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f56d7-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="f56d7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f56d7-107">PR_MESSAGE_SUBMISSION_ID</span><span class="sxs-lookup"><span data-stu-id="f56d7-107">PR_MESSAGE_SUBMISSION_ID</span></span>  <br/> |
|<span data-ttu-id="f56d7-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f56d7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f56d7-109">0x0047</span><span class="sxs-lookup"><span data-stu-id="f56d7-109">0x0047</span></span>  <br/> |
|<span data-ttu-id="f56d7-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="f56d7-110">Data type:</span></span>  <br/> |<span data-ttu-id="f56d7-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f56d7-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f56d7-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f56d7-112">Area:</span></span>  <br/> |<span data-ttu-id="f56d7-113">Email</span><span class="sxs-lookup"><span data-stu-id="f56d7-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f56d7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f56d7-114">Remarks</span></span>

<span data-ttu-id="f56d7-115">Essa propriedade é retornada pelo MTA após a conclusão bem-sucedida do envio de mensagens.</span><span class="sxs-lookup"><span data-stu-id="f56d7-115">This property is returned by the MTA upon successful completion of message submission.</span></span> <span data-ttu-id="f56d7-116">Qualquer contato futuro com o MTA referente a essa mensagem, como solicitar o cancelamento, usa o identificador MTS nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="f56d7-116">Any future contact with the MTA regarding this message, such as requesting cancellation, uses the MTS identifier in this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f56d7-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f56d7-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f56d7-118">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="f56d7-118">Protocol specifications</span></span>

<span data-ttu-id="f56d7-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f56d7-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f56d7-120">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f56d7-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f56d7-121">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f56d7-121">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f56d7-122">Codifica e decodifica objetos Message e Attachment para uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="f56d7-122">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f56d7-123">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f56d7-123">Header files</span></span>

<span data-ttu-id="f56d7-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f56d7-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="f56d7-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="f56d7-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="f56d7-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="f56d7-126">Mapitags.h</span></span>
  
> <span data-ttu-id="f56d7-127">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="f56d7-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f56d7-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="f56d7-128">See also</span></span>



[<span data-ttu-id="f56d7-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f56d7-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f56d7-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="f56d7-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f56d7-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="f56d7-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f56d7-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="f56d7-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

