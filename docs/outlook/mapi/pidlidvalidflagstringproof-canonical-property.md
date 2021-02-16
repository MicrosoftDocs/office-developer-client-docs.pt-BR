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
ms.openlocfilehash: dfe3b57c246e247eda365bed46af2e0f35f0e54b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315383"
---
# <a name="pidlidvalidflagstringproof-canonical-property"></a><span data-ttu-id="a2fbc-103">Propriedade canônica PidLidValidFlagStringProof</span><span class="sxs-lookup"><span data-stu-id="a2fbc-103">PidLidValidFlagStringProof Canonical Property</span></span>

  
  
<span data-ttu-id="a2fbc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a2fbc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a2fbc-105">Valida se o valor da propriedade **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) foi definido por um agente que sabia o valor da propriedade **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a2fbc-105">Validates whether the **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) property's value was set by an agent who knew the value of the **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a2fbc-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a2fbc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a2fbc-107">dispidValidFlagStringProof</span><span class="sxs-lookup"><span data-stu-id="a2fbc-107">dispidValidFlagStringProof</span></span>  <br/> |
|<span data-ttu-id="a2fbc-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="a2fbc-108">Property set:</span></span>  <br/> |<span data-ttu-id="a2fbc-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="a2fbc-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="a2fbc-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="a2fbc-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a2fbc-111">0x000085BF</span><span class="sxs-lookup"><span data-stu-id="a2fbc-111">0x000085BF</span></span>  <br/> |
|<span data-ttu-id="a2fbc-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a2fbc-112">Data type:</span></span>  <br/> |<span data-ttu-id="a2fbc-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="a2fbc-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="a2fbc-114">Área:</span><span class="sxs-lookup"><span data-stu-id="a2fbc-114">Area:</span></span>  <br/> |<span data-ttu-id="a2fbc-115">Tarefas</span><span class="sxs-lookup"><span data-stu-id="a2fbc-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a2fbc-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2fbc-116">Remarks</span></span>

<span data-ttu-id="a2fbc-117">Em objetos não enviáveis (emails recebidos e objetos que não são  de email), os clientes devem definir esse valor como o valor de PR_MESSAGE_DELIVERY_TIME ao modificar **dispidRequest**.</span><span class="sxs-lookup"><span data-stu-id="a2fbc-117">On non-sendable objects (received mail and non-mail objects), clients should set this value to the value of **PR_MESSAGE_DELIVERY_TIME** when modifying **dispidRequest**.</span></span>
  
<span data-ttu-id="a2fbc-118">Como o valor de **PR_MESSAGE_DELIVERY_TIME** não pode ser previsto pelo remetente, se o valor dessa propriedade for igual ao valor de **PR_MESSAGE_DELIVERY_TIME**, é razoavelmente certo que o valor de **dispidRequest** não se originou do remetente da mensagem.</span><span class="sxs-lookup"><span data-stu-id="a2fbc-118">Since the value of **PR_MESSAGE_DELIVERY_TIME** cannot be predicted by the sender, if the value of this property is equal to the value of **PR_MESSAGE_DELIVERY_TIME**, it is reasonably certain that the value of **dispidRequest** did not originate from the sender of the message.</span></span> <span data-ttu-id="a2fbc-119">Um cliente pode decidir como apresentar o valor de **dispidRequest** para o usuário final com base no resultado dessa comparação, de acordo com a política de segurança específica do cliente.</span><span class="sxs-lookup"><span data-stu-id="a2fbc-119">A client can decide how to present the value of **dispidRequest** to the end user based on the result of this comparison in accordance with the specific security policy of the client.</span></span> <span data-ttu-id="a2fbc-120">Se o valor de **dispidRequest** for ignorado devido à presença de um valor para **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)), essa propriedade deverá ser ignorada.</span><span class="sxs-lookup"><span data-stu-id="a2fbc-120">If the value of **dispidRequest** is ignored due to the presence of a value for **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)), this property must be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a2fbc-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a2fbc-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a2fbc-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="a2fbc-122">Protocol specifications</span></span>

<span data-ttu-id="a2fbc-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a2fbc-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a2fbc-124">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a2fbc-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a2fbc-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a2fbc-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a2fbc-126">Especifica as propriedades e operações relacionadas à sinalização.</span><span class="sxs-lookup"><span data-stu-id="a2fbc-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a2fbc-127">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="a2fbc-127">Header files</span></span>

<span data-ttu-id="a2fbc-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a2fbc-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="a2fbc-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a2fbc-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a2fbc-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2fbc-130">See also</span></span>



[<span data-ttu-id="a2fbc-131">Propriedade canônica PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="a2fbc-131">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)


[<span data-ttu-id="a2fbc-132">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a2fbc-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a2fbc-133">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="a2fbc-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a2fbc-134">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a2fbc-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a2fbc-135">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="a2fbc-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

