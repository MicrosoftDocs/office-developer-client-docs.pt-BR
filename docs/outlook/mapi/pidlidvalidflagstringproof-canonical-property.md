---
title: Propriedade canônica PidLidValidFlagStringProof
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidValidFlagStringProof
api_type:
- COM
ms.assetid: e5a94968-7e84-4faf-8104-9ea36d35fa1a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: efbbffe184e965caae84db54383e1431dfb1a569
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585819"
---
# <a name="pidlidvalidflagstringproof-canonical-property"></a><span data-ttu-id="5bb7f-103">Propriedade canônica PidLidValidFlagStringProof</span><span class="sxs-lookup"><span data-stu-id="5bb7f-103">PidLidValidFlagStringProof Canonical Property</span></span>

  
  
<span data-ttu-id="5bb7f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5bb7f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5bb7f-105">Valida se o valor da propriedade **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) foi definido para um operador que sabia o valor da propriedade **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5bb7f-105">Validates whether the **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) property's value was set by an agent who knew the value of the **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5bb7f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="5bb7f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5bb7f-107">dispidValidFlagStringProof</span><span class="sxs-lookup"><span data-stu-id="5bb7f-107">dispidValidFlagStringProof</span></span>  <br/> |
|<span data-ttu-id="5bb7f-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="5bb7f-108">Property set:</span></span>  <br/> |<span data-ttu-id="5bb7f-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="5bb7f-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="5bb7f-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="5bb7f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5bb7f-111">0x000085BF</span><span class="sxs-lookup"><span data-stu-id="5bb7f-111">0x000085BF</span></span>  <br/> |
|<span data-ttu-id="5bb7f-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="5bb7f-112">Data type:</span></span>  <br/> |<span data-ttu-id="5bb7f-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="5bb7f-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="5bb7f-114">Área:</span><span class="sxs-lookup"><span data-stu-id="5bb7f-114">Area:</span></span>  <br/> |<span data-ttu-id="5bb7f-115">Task</span><span class="sxs-lookup"><span data-stu-id="5bb7f-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5bb7f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="5bb7f-116">Remarks</span></span>

<span data-ttu-id="5bb7f-117">Nos objetos não possa ser enviado (email recebido e objetos não sejam de email), os clientes devem definir esse valor como o valor de **PR_MESSAGE_DELIVERY_TIME** ao modificar **dispidRequest**.</span><span class="sxs-lookup"><span data-stu-id="5bb7f-117">On non-sendable objects (received mail and non-mail objects), clients should set this value to the value of **PR_MESSAGE_DELIVERY_TIME** when modifying **dispidRequest**.</span></span>
  
<span data-ttu-id="5bb7f-118">Como o valor da **PR_MESSAGE_DELIVERY_TIME** não pode ser previsto pelo remetente, se o valor dessa propriedade é igual ao valor de **PR_MESSAGE_DELIVERY_TIME**, ele é razoável certeza de que o valor da **dispidRequest** não especificou são originárias do remetente da mensagem.</span><span class="sxs-lookup"><span data-stu-id="5bb7f-118">Since the value of **PR_MESSAGE_DELIVERY_TIME** cannot be predicted by the sender, if the value of this property is equal to the value of **PR_MESSAGE_DELIVERY_TIME**, it is reasonably certain that the value of **dispidRequest** did not originate from the sender of the message.</span></span> <span data-ttu-id="5bb7f-119">Um cliente pode decidir como o valor presente de **dispidRequest** para o usuário final com base no resultado desta comparação de acordo com a diretiva de segurança específica do cliente.</span><span class="sxs-lookup"><span data-stu-id="5bb7f-119">A client can decide how to present the value of **dispidRequest** to the end user based on the result of this comparison in accordance with the specific security policy of the client.</span></span> <span data-ttu-id="5bb7f-120">Se o valor de **dispidRequest** será ignorado devido à presença de um valor para **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)), esta propriedade deve ser ignorada.</span><span class="sxs-lookup"><span data-stu-id="5bb7f-120">If the value of **dispidRequest** is ignored due to the presence of a value for **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)), this property must be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5bb7f-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5bb7f-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5bb7f-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="5bb7f-122">Protocol specifications</span></span>

<span data-ttu-id="5bb7f-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5bb7f-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5bb7f-124">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="5bb7f-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5bb7f-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5bb7f-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5bb7f-126">Especifica as propriedades e operações relacionadas a sinalização.</span><span class="sxs-lookup"><span data-stu-id="5bb7f-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5bb7f-127">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5bb7f-127">Header files</span></span>

<span data-ttu-id="5bb7f-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5bb7f-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="5bb7f-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="5bb7f-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5bb7f-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="5bb7f-130">See also</span></span>



[<span data-ttu-id="5bb7f-131">Propriedade canônica PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="5bb7f-131">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)


[<span data-ttu-id="5bb7f-132">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5bb7f-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5bb7f-133">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="5bb7f-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5bb7f-134">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="5bb7f-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5bb7f-135">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="5bb7f-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

