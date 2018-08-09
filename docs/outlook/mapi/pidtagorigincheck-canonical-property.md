---
title: Propriedade canônica PidTagOriginCheck
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginCheck
api_type:
- COM
ms.assetid: 27e0ab2f-b373-41ae-b922-2f45f9671ac6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bbf09cb841c633b6f13ae12ec20e120ea3fd7ef7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769614"
---
# <a name="pidtagorigincheck-canonical-property"></a><span data-ttu-id="8165c-103">Propriedade canônica PidTagOriginCheck</span><span class="sxs-lookup"><span data-stu-id="8165c-103">PidTagOriginCheck Canonical Property</span></span>

  
  
<span data-ttu-id="8165c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8165c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8165c-105">Contém um valor binário de verificação que permite que um destinatário de relatório de entrega verificar a origem da mensagem original.</span><span class="sxs-lookup"><span data-stu-id="8165c-105">Contains a binary verification value that enables a delivery report recipient to verify the origin of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8165c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="8165c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8165c-107">PR_ORIGIN_CHECK</span><span class="sxs-lookup"><span data-stu-id="8165c-107">PR_ORIGIN_CHECK</span></span>  <br/> |
|<span data-ttu-id="8165c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8165c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8165c-109">0x0027</span><span class="sxs-lookup"><span data-stu-id="8165c-109">0x0027</span></span>  <br/> |
|<span data-ttu-id="8165c-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="8165c-110">Data type:</span></span>  <br/> |<span data-ttu-id="8165c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8165c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8165c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8165c-112">Area:</span></span>  <br/> |<span data-ttu-id="8165c-113">Servidor</span><span class="sxs-lookup"><span data-stu-id="8165c-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8165c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8165c-114">Remarks</span></span>

<span data-ttu-id="8165c-115">Essa propriedade oferece um meio de um terceiro, como um agente de transferência de mensagem (MTA) ou um usuário receber uma notificação de entrega de mensagens para verificar a origem da mensagem enviada.</span><span class="sxs-lookup"><span data-stu-id="8165c-115">This property provides a means for a third party, such as a message transfer agent (MTA) or a messaging user receiving a delivery report, to verify the submitted message's origin.</span></span> <span data-ttu-id="8165c-116">Se estiverem presentes em uma mensagem recebida, esta propriedade deve ser copiada em qualquer relatório de entrega gerado em resposta à mensagem.</span><span class="sxs-lookup"><span data-stu-id="8165c-116">If present on a received message, this property should be copied onto any delivery report generated in response to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8165c-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8165c-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8165c-118">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8165c-118">Header files</span></span>

<span data-ttu-id="8165c-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8165c-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="8165c-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8165c-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="8165c-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8165c-121">Mapitags.h</span></span>
  
> <span data-ttu-id="8165c-122">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="8165c-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8165c-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="8165c-123">See also</span></span>



[<span data-ttu-id="8165c-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8165c-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8165c-125">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="8165c-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8165c-126">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="8165c-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8165c-127">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="8165c-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

