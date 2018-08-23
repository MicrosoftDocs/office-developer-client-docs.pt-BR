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
ms.openlocfilehash: 27b967b885ef35c04d52699c289dd60248e9abd5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581080"
---
# <a name="pidtagorigincheck-canonical-property"></a><span data-ttu-id="93788-103">Propriedade canônica PidTagOriginCheck</span><span class="sxs-lookup"><span data-stu-id="93788-103">PidTagOriginCheck Canonical Property</span></span>

  
  
<span data-ttu-id="93788-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93788-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93788-105">Contém um valor binário de verificação que permite que um destinatário de relatório de entrega verificar a origem da mensagem original.</span><span class="sxs-lookup"><span data-stu-id="93788-105">Contains a binary verification value that enables a delivery report recipient to verify the origin of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="93788-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="93788-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="93788-107">PR_ORIGIN_CHECK</span><span class="sxs-lookup"><span data-stu-id="93788-107">PR_ORIGIN_CHECK</span></span>  <br/> |
|<span data-ttu-id="93788-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="93788-108">Identifier:</span></span>  <br/> |<span data-ttu-id="93788-109">0x0027</span><span class="sxs-lookup"><span data-stu-id="93788-109">0x0027</span></span>  <br/> |
|<span data-ttu-id="93788-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="93788-110">Data type:</span></span>  <br/> |<span data-ttu-id="93788-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="93788-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="93788-112">Área:</span><span class="sxs-lookup"><span data-stu-id="93788-112">Area:</span></span>  <br/> |<span data-ttu-id="93788-113">Servidor</span><span class="sxs-lookup"><span data-stu-id="93788-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="93788-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="93788-114">Remarks</span></span>

<span data-ttu-id="93788-115">Essa propriedade oferece um meio de um terceiro, como um agente de transferência de mensagem (MTA) ou um usuário receber uma notificação de entrega de mensagens para verificar a origem da mensagem enviada.</span><span class="sxs-lookup"><span data-stu-id="93788-115">This property provides a means for a third party, such as a message transfer agent (MTA) or a messaging user receiving a delivery report, to verify the submitted message's origin.</span></span> <span data-ttu-id="93788-116">Se estiverem presentes em uma mensagem recebida, esta propriedade deve ser copiada em qualquer relatório de entrega gerado em resposta à mensagem.</span><span class="sxs-lookup"><span data-stu-id="93788-116">If present on a received message, this property should be copied onto any delivery report generated in response to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="93788-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="93788-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="93788-118">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="93788-118">Header files</span></span>

<span data-ttu-id="93788-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="93788-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="93788-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="93788-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="93788-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="93788-121">Mapitags.h</span></span>
  
> <span data-ttu-id="93788-122">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="93788-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="93788-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="93788-123">See also</span></span>



[<span data-ttu-id="93788-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="93788-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="93788-125">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="93788-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="93788-126">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="93788-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="93788-127">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="93788-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

