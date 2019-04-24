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
ms.openlocfilehash: 474ffaf2317cadd214074419f09bb913b1eee4ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327248"
---
# <a name="pidtagattachnumber-canonical-property"></a><span data-ttu-id="dfafa-103">Propriedade canônica PidTagAttachNumber</span><span class="sxs-lookup"><span data-stu-id="dfafa-103">PidTagAttachNumber Canonical Property</span></span>

  
  
<span data-ttu-id="dfafa-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dfafa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dfafa-105">Contém um número que identifica exclusivamente o anexo dentro de sua mensagem pai.</span><span class="sxs-lookup"><span data-stu-id="dfafa-105">Contains a number that uniquely identifies the attachment within its parent message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dfafa-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="dfafa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dfafa-107">PR_ATTACH_NUM</span><span class="sxs-lookup"><span data-stu-id="dfafa-107">PR_ATTACH_NUM</span></span>  <br/> |
|<span data-ttu-id="dfafa-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="dfafa-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dfafa-109">0x0E21</span><span class="sxs-lookup"><span data-stu-id="dfafa-109">0x0E21</span></span>  <br/> |
|<span data-ttu-id="dfafa-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="dfafa-110">Data type:</span></span>  <br/> |<span data-ttu-id="dfafa-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="dfafa-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="dfafa-112">Área:</span><span class="sxs-lookup"><span data-stu-id="dfafa-112">Area:</span></span>  <br/> |<span data-ttu-id="dfafa-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="dfafa-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dfafa-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="dfafa-114">Remarks</span></span>

<span data-ttu-id="dfafa-115">Os repositórios de mensagens geram e mantêm essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="dfafa-115">Message stores generate and maintain this property.</span></span> <span data-ttu-id="dfafa-116">O número de anexo é a chave de classificação secundária, após a posição de renderização, na tabela de anexos.</span><span class="sxs-lookup"><span data-stu-id="dfafa-116">The attachment number is the secondary sort key, after the rendering position, in the attachment table.</span></span> 
  
 <span data-ttu-id="dfafa-117">**PR_ATTACH_NUM** é usado para abrir o anexo com o método [IMessage:: OpenAttach](imessage-openattach.md) .</span><span class="sxs-lookup"><span data-stu-id="dfafa-117">**PR_ATTACH_NUM** is used to open the attachment with the [IMessage::OpenAttach](imessage-openattach.md) method.</span></span> <span data-ttu-id="dfafa-118">Dentro da sessão de um aplicativo cliente, a propriedade **PR_ATTACH_NUM** de um anexo de mensagem permanece constante, desde que a tabela de anexos esteja aberta.</span><span class="sxs-lookup"><span data-stu-id="dfafa-118">Within a client application's session, the **PR_ATTACH_NUM** property of a message attachment remains constant as long as the attachment table is open.</span></span> 
  
<span data-ttu-id="dfafa-119">O repositório de mensagens propaga as alterações para a tabela usando os métodos **IMessage:: CreateAttach** e **IMessage::D eleteattach** .</span><span class="sxs-lookup"><span data-stu-id="dfafa-119">The message store propagates changes to the table using the **IMessage::CreateAttach** and **IMessage::DeleteAttach** methods.</span></span> <span data-ttu-id="dfafa-120">Na sua opção, o repositório de mensagens pode gerar notificações de tabela em tabelas de anexo abertas para que os clientes possam sincronizar novamente com essas alterações.</span><span class="sxs-lookup"><span data-stu-id="dfafa-120">At its option the message store can generate table notifications on open attachment tables so that clients can resynchronize to those changes.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="dfafa-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="dfafa-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dfafa-122">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="dfafa-122">Protocol specifications</span></span>

<span data-ttu-id="dfafa-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dfafa-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dfafa-124">Manipula objetos Message e Attachment.</span><span class="sxs-lookup"><span data-stu-id="dfafa-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dfafa-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="dfafa-125">Header files</span></span>

<span data-ttu-id="dfafa-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="dfafa-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="dfafa-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="dfafa-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="dfafa-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="dfafa-128">Mapitags.h</span></span>
  
> <span data-ttu-id="dfafa-129">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="dfafa-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dfafa-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="dfafa-130">See also</span></span>



[<span data-ttu-id="dfafa-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="dfafa-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dfafa-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="dfafa-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dfafa-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="dfafa-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dfafa-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="dfafa-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

