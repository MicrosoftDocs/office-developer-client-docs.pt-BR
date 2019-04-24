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
ms.openlocfilehash: 2c32cc61fea63cd38215c30e04e8a467d4901cc9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339372"
---
# <a name="pidtagprimarysendaccount-canonical-property"></a><span data-ttu-id="a2a9f-103">Propriedade canônica PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="a2a9f-103">PidTagPrimarySendAccount Canonical Property</span></span>

  
  
<span data-ttu-id="a2a9f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a2a9f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a2a9f-105">Contém uma cadeia de caracteres que nomeia o primeiro servidor usado para enviar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="a2a9f-105">Contains a string that names the first server that is used to send the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a2a9f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a2a9f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a2a9f-107">PR_PRIMARY_SEND_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="a2a9f-107">PR_PRIMARY_SEND_ACCOUNT</span></span>  <br/> |
|<span data-ttu-id="a2a9f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a2a9f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a2a9f-109">0x0E28</span><span class="sxs-lookup"><span data-stu-id="a2a9f-109">0x0E28</span></span>  <br/> |
|<span data-ttu-id="a2a9f-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a2a9f-110">Data type:</span></span>  <br/> |<span data-ttu-id="a2a9f-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a2a9f-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a2a9f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a2a9f-112">Area:</span></span>  <br/> |<span data-ttu-id="a2a9f-113">Conta</span><span class="sxs-lookup"><span data-stu-id="a2a9f-113">Account</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a2a9f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2a9f-114">Remarks</span></span>

<span data-ttu-id="a2a9f-115">Especifica o primeiro servidor que um cliente deve usar para enviar o email.</span><span class="sxs-lookup"><span data-stu-id="a2a9f-115">Specifies the first server that a client should use to send the mail.</span></span> <span data-ttu-id="a2a9f-116">O formato dessas propriedades é dependente de implementação.</span><span class="sxs-lookup"><span data-stu-id="a2a9f-116">The format of these properties is implementation dependent.</span></span> <span data-ttu-id="a2a9f-117">Essas propriedades podem ser usadas pelo cliente para determinar em qual servidor direcionar o email, mas é opcional e o valor não tem significado para o servidor.</span><span class="sxs-lookup"><span data-stu-id="a2a9f-117">These properties can be used by the client to determine which server to direct the mail through, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a2a9f-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a2a9f-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a2a9f-119">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="a2a9f-119">Protocol specifications</span></span>

<span data-ttu-id="a2a9f-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a2a9f-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a2a9f-121">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a2a9f-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a2a9f-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a2a9f-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a2a9f-123">Especifica as propriedades e as operações que são permitidas para os objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="a2a9f-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a2a9f-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a2a9f-124">Header files</span></span>

<span data-ttu-id="a2a9f-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a2a9f-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="a2a9f-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a2a9f-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="a2a9f-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="a2a9f-127">Mapitags.h</span></span>
  
> <span data-ttu-id="a2a9f-128">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="a2a9f-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a2a9f-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2a9f-129">See also</span></span>



[<span data-ttu-id="a2a9f-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a2a9f-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a2a9f-131">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="a2a9f-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a2a9f-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a2a9f-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a2a9f-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="a2a9f-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

