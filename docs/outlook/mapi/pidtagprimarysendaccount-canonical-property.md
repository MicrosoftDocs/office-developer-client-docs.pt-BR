---
title: Propriedade canônica PidTagPrimarySendAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagPrimarySendAccount
api_type:
- COM
ms.assetid: 2f268b3b-2e4c-4aea-8879-bdd0ac1df35c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a0f4ae75117dff3610175b785ab3f982cc7e7552
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590404"
---
# <a name="pidtagprimarysendaccount-canonical-property"></a><span data-ttu-id="6eff2-103">Propriedade canônica PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="6eff2-103">PidTagPrimarySendAccount Canonical Property</span></span>

  
  
<span data-ttu-id="6eff2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6eff2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6eff2-105">Contém uma cadeia de caracteres que nomeia o primeiro servidor que é usado para enviar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="6eff2-105">Contains a string that names the first server that is used to send the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6eff2-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="6eff2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6eff2-107">PR_PRIMARY_SEND_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6eff2-107">PR_PRIMARY_SEND_ACCOUNT</span></span>  <br/> |
|<span data-ttu-id="6eff2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="6eff2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6eff2-109">0x0E28</span><span class="sxs-lookup"><span data-stu-id="6eff2-109">0x0E28</span></span>  <br/> |
|<span data-ttu-id="6eff2-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="6eff2-110">Data type:</span></span>  <br/> |<span data-ttu-id="6eff2-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6eff2-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6eff2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="6eff2-112">Area:</span></span>  <br/> |<span data-ttu-id="6eff2-113">Conta</span><span class="sxs-lookup"><span data-stu-id="6eff2-113">Account</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6eff2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6eff2-114">Remarks</span></span>

<span data-ttu-id="6eff2-115">Especifica o primeiro servidor em que um cliente deve usar para enviar o email.</span><span class="sxs-lookup"><span data-stu-id="6eff2-115">Specifies the first server that a client should use to send the mail.</span></span> <span data-ttu-id="6eff2-116">O formato dessas propriedades é dependente de implementação.</span><span class="sxs-lookup"><span data-stu-id="6eff2-116">The format of these properties is implementation dependent.</span></span> <span data-ttu-id="6eff2-117">Essas propriedades pode ser usado pelo cliente para determinar em qual servidor para direcionar os emails por meio, mas é opcionais e o valor não tem significado para o servidor.</span><span class="sxs-lookup"><span data-stu-id="6eff2-117">These properties can be used by the client to determine which server to direct the mail through, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6eff2-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6eff2-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6eff2-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="6eff2-119">Protocol specifications</span></span>

<span data-ttu-id="6eff2-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6eff2-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6eff2-121">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6eff2-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6eff2-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6eff2-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6eff2-123">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="6eff2-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6eff2-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6eff2-124">Header files</span></span>

<span data-ttu-id="6eff2-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6eff2-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="6eff2-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="6eff2-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="6eff2-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6eff2-127">Mapitags.h</span></span>
  
> <span data-ttu-id="6eff2-128">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="6eff2-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6eff2-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="6eff2-129">See also</span></span>



[<span data-ttu-id="6eff2-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6eff2-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6eff2-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="6eff2-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6eff2-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="6eff2-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6eff2-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="6eff2-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

