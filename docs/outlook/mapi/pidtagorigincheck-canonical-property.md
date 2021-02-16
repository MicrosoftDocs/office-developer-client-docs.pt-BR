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
ms.openlocfilehash: a82b1351c9d2d19c32e34b03a537a12bf93deb8a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435758"
---
# <a name="pidtagorigincheck-canonical-property"></a><span data-ttu-id="3742b-103">Propriedade canônica PidTagOriginCheck</span><span class="sxs-lookup"><span data-stu-id="3742b-103">PidTagOriginCheck Canonical Property</span></span>

  
  
<span data-ttu-id="3742b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3742b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3742b-105">Contém um valor de verificação binária que permite que um destinatário de relatório de entrega verifique a origem da mensagem original.</span><span class="sxs-lookup"><span data-stu-id="3742b-105">Contains a binary verification value that enables a delivery report recipient to verify the origin of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3742b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="3742b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3742b-107">PR_ORIGIN_CHECK</span><span class="sxs-lookup"><span data-stu-id="3742b-107">PR_ORIGIN_CHECK</span></span>  <br/> |
|<span data-ttu-id="3742b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3742b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3742b-109">0x0027</span><span class="sxs-lookup"><span data-stu-id="3742b-109">0x0027</span></span>  <br/> |
|<span data-ttu-id="3742b-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="3742b-110">Data type:</span></span>  <br/> |<span data-ttu-id="3742b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3742b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3742b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3742b-112">Area:</span></span>  <br/> |<span data-ttu-id="3742b-113">Servidor</span><span class="sxs-lookup"><span data-stu-id="3742b-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3742b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3742b-114">Remarks</span></span>

<span data-ttu-id="3742b-115">Essa propriedade fornece um meio para terceiros, como um agente de transferência de mensagens (MTA) ou um usuário de mensagens receber um relatório de entrega, para verificar a origem da mensagem enviada.</span><span class="sxs-lookup"><span data-stu-id="3742b-115">This property provides a means for a third party, such as a message transfer agent (MTA) or a messaging user receiving a delivery report, to verify the submitted message's origin.</span></span> <span data-ttu-id="3742b-116">Se presente em uma mensagem recebida, essa propriedade deve ser copiada para qualquer relatório de entrega gerado em resposta à mensagem.</span><span class="sxs-lookup"><span data-stu-id="3742b-116">If present on a received message, this property should be copied onto any delivery report generated in response to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3742b-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3742b-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="3742b-118">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="3742b-118">Header files</span></span>

<span data-ttu-id="3742b-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3742b-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="3742b-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="3742b-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="3742b-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3742b-121">Mapitags.h</span></span>
  
> <span data-ttu-id="3742b-122">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="3742b-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3742b-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="3742b-123">See also</span></span>



[<span data-ttu-id="3742b-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3742b-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3742b-125">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="3742b-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3742b-126">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="3742b-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3742b-127">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="3742b-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

