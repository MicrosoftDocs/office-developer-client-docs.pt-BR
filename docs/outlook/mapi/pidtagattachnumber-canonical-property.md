---
title: Propriedade canônica PidTagAttachNumber
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachNumber
api_type:
- HeaderDef
ms.assetid: 507e0f2c-383c-4e2f-917b-159913f7234d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f6de157864bff5be41b6e030d555be7b60dcda5e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594751"
---
# <a name="pidtagattachnumber-canonical-property"></a><span data-ttu-id="4b176-103">Propriedade canônica PidTagAttachNumber</span><span class="sxs-lookup"><span data-stu-id="4b176-103">PidTagAttachNumber Canonical Property</span></span>

  
  
<span data-ttu-id="4b176-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b176-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b176-105">Contém um número que identifica exclusivamente o anexo dentro de sua mensagem pai.</span><span class="sxs-lookup"><span data-stu-id="4b176-105">Contains a number that uniquely identifies the attachment within its parent message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4b176-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="4b176-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4b176-107">PR_ATTACH_NUM</span><span class="sxs-lookup"><span data-stu-id="4b176-107">PR_ATTACH_NUM</span></span>  <br/> |
|<span data-ttu-id="4b176-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4b176-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4b176-109">0x0E21</span><span class="sxs-lookup"><span data-stu-id="4b176-109">0x0E21</span></span>  <br/> |
|<span data-ttu-id="4b176-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="4b176-110">Data type:</span></span>  <br/> |<span data-ttu-id="4b176-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4b176-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4b176-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4b176-112">Area:</span></span>  <br/> |<span data-ttu-id="4b176-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="4b176-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4b176-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b176-114">Remarks</span></span>

<span data-ttu-id="4b176-115">Os armazenamentos de mensagem geram e manter essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="4b176-115">Message stores generate and maintain this property.</span></span> <span data-ttu-id="4b176-116">O número de anexo é a chave de classificação secundária, após a posição de renderização, na tabela de anexo.</span><span class="sxs-lookup"><span data-stu-id="4b176-116">The attachment number is the secondary sort key, after the rendering position, in the attachment table.</span></span> 
  
 <span data-ttu-id="4b176-117">**PR_ATTACH_NUM** é usado para abrir o anexo com o método [IMessage::OpenAttach](imessage-openattach.md) .</span><span class="sxs-lookup"><span data-stu-id="4b176-117">**PR_ATTACH_NUM** is used to open the attachment with the [IMessage::OpenAttach](imessage-openattach.md) method.</span></span> <span data-ttu-id="4b176-118">Dentro da sessão de um aplicativo cliente, a propriedade **PR_ATTACH_NUM** de anexo de uma mensagem permanece constante desde que a tabela de anexo está aberta.</span><span class="sxs-lookup"><span data-stu-id="4b176-118">Within a client application's session, the **PR_ATTACH_NUM** property of a message attachment remains constant as long as the attachment table is open.</span></span> 
  
<span data-ttu-id="4b176-119">O armazenamento de mensagens propaga as alterações na tabela usando os métodos **IMessage::CreateAttach** e **IMessage::DeleteAttach** .</span><span class="sxs-lookup"><span data-stu-id="4b176-119">The message store propagates changes to the table using the **IMessage::CreateAttach** and **IMessage::DeleteAttach** methods.</span></span> <span data-ttu-id="4b176-120">A seu critério o armazenamento de mensagens pode gerar notificações de tabela em tabelas abrir anexo para que os clientes podem sincronizar para essas alterações.</span><span class="sxs-lookup"><span data-stu-id="4b176-120">At its option the message store can generate table notifications on open attachment tables so that clients can resynchronize to those changes.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4b176-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4b176-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4b176-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="4b176-122">Protocol specifications</span></span>

<span data-ttu-id="4b176-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b176-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4b176-124">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="4b176-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4b176-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4b176-125">Header files</span></span>

<span data-ttu-id="4b176-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4b176-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="4b176-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="4b176-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="4b176-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4b176-128">Mapitags.h</span></span>
  
> <span data-ttu-id="4b176-129">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="4b176-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4b176-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="4b176-130">See also</span></span>



[<span data-ttu-id="4b176-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4b176-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4b176-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="4b176-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4b176-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="4b176-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4b176-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="4b176-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

