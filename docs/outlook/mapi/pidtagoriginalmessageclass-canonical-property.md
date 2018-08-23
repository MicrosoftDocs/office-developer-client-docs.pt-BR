---
title: Propriedade canônica PidTagOriginalMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalMessageClass
api_type:
- COM
ms.assetid: 49deb153-03c6-4be2-a3a5-53cca01accba
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a0abd3618f7a1586d8ca786fc1b6802c17e0f0f1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573114"
---
# <a name="pidtagoriginalmessageclass-canonical-property"></a><span data-ttu-id="6c48b-103">Propriedade canônica PidTagOriginalMessageClass</span><span class="sxs-lookup"><span data-stu-id="6c48b-103">PidTagOriginalMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="6c48b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c48b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c48b-105">Contém a classe da mensagem original para uso em um relatório.</span><span class="sxs-lookup"><span data-stu-id="6c48b-105">Contains the class of the original message for use in a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6c48b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="6c48b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6c48b-107">PR_ORIG_MESSAGE_CLASS, PR_ORIG_MESSAGE_CLASS_A, PR_ORIG_MESSAGE_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="6c48b-107">PR_ORIG_MESSAGE_CLASS, PR_ORIG_MESSAGE_CLASS_A, PR_ORIG_MESSAGE_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="6c48b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="6c48b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6c48b-109">0x004B</span><span class="sxs-lookup"><span data-stu-id="6c48b-109">0x004B</span></span>  <br/> |
|<span data-ttu-id="6c48b-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="6c48b-110">Data type:</span></span>  <br/> |<span data-ttu-id="6c48b-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6c48b-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6c48b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="6c48b-112">Area:</span></span>  <br/> |<span data-ttu-id="6c48b-113">Propriedades de mensagens de seguro</span><span class="sxs-lookup"><span data-stu-id="6c48b-113">Secure Messaging Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c48b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c48b-114">Remarks</span></span>

<span data-ttu-id="6c48b-115">Essas propriedades contêm uma cópia da propriedade **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) da mensagem para o qual o relatório está sendo gerado.</span><span class="sxs-lookup"><span data-stu-id="6c48b-115">These properties contain a copy of the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message for which the report is being generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6c48b-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6c48b-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6c48b-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="6c48b-117">Protocol specifications</span></span>

<span data-ttu-id="6c48b-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c48b-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c48b-119">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6c48b-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6c48b-120">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c48b-120">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c48b-121">Codifica e decodifica objetos de mensagem e o anexo em uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="6c48b-121">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6c48b-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6c48b-122">Header files</span></span>

<span data-ttu-id="6c48b-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6c48b-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="6c48b-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="6c48b-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="6c48b-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6c48b-125">Mapitags.h</span></span>
  
> <span data-ttu-id="6c48b-126">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="6c48b-126">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6c48b-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c48b-127">See also</span></span>



[<span data-ttu-id="6c48b-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6c48b-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6c48b-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="6c48b-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6c48b-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="6c48b-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6c48b-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="6c48b-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

