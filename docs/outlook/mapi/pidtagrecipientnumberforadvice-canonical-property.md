---
title: Propriedade canônica PidTagRecipientNumberForAdvice
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientNumberForAdvice
api_type:
- COM
ms.assetid: 636c1e75-3024-43ca-a7dd-1bb480dfbb5b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 79ef85955f15e0ca829ac6f206dddc17031b0562
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420637"
---
# <a name="pidtagrecipientnumberforadvice-canonical-property"></a><span data-ttu-id="e843e-103">Propriedade canônica PidTagRecipientNumberForAdvice</span><span class="sxs-lookup"><span data-stu-id="e843e-103">PidTagRecipientNumberForAdvice Canonical Property</span></span>

  
  
<span data-ttu-id="e843e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e843e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e843e-105">Essa propriedade contém o número de telefone de um destinatário da mensagem a ser chamada para avisar sobre a entrega física de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="e843e-105">This property contains a message recipient's telephone number to call to advise of the physical delivery of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e843e-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="e843e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e843e-107">PR_RECIPIENT_NUMBER_FOR_ADVICE, PR_RECIPIENT_NUMBER_FOR_ADVICE_A, PR_RECIPIENT_NUMBER_FOR_ADVICE_W</span><span class="sxs-lookup"><span data-stu-id="e843e-107">PR_RECIPIENT_NUMBER_FOR_ADVICE, PR_RECIPIENT_NUMBER_FOR_ADVICE_A, PR_RECIPIENT_NUMBER_FOR_ADVICE_W</span></span>  <br/> |
|<span data-ttu-id="e843e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e843e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e843e-109">0x0C14</span><span class="sxs-lookup"><span data-stu-id="e843e-109">0x0C14</span></span>  <br/> |
|<span data-ttu-id="e843e-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="e843e-110">Data type:</span></span>  <br/> |<span data-ttu-id="e843e-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e843e-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e843e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e843e-112">Area:</span></span>  <br/> |<span data-ttu-id="e843e-113">Destinatário MAPI</span><span class="sxs-lookup"><span data-stu-id="e843e-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e843e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e843e-114">Remarks</span></span>

<span data-ttu-id="e843e-115">Essas propriedades devem ser usadas em conjunto com a entrega para um destino físico, em vez de uma caixa de correio eletrônica, quando o destinatário humano não deve estar presente na entrega.</span><span class="sxs-lookup"><span data-stu-id="e843e-115">These properties are meant to be used in conjunction with delivery to a physical destination, rather than an electronic mailbox, when the human recipient is not expected to be present at delivery.</span></span> <span data-ttu-id="e843e-116">Um exemplo é o número de telefone em uma folha de capa de fax.</span><span class="sxs-lookup"><span data-stu-id="e843e-116">An example is the telephone number on a fax cover sheet.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e843e-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e843e-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e843e-118">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="e843e-118">Header files</span></span>

<span data-ttu-id="e843e-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e843e-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="e843e-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e843e-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="e843e-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e843e-121">Mapitags.h</span></span>
  
> <span data-ttu-id="e843e-122">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="e843e-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e843e-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="e843e-123">See also</span></span>



[<span data-ttu-id="e843e-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e843e-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e843e-125">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="e843e-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e843e-126">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="e843e-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e843e-127">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="e843e-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

