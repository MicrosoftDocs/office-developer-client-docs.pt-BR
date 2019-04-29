---
title: Propriedade canônica PidTagIpmWastebasketEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmWastebasketEntryId
api_type:
- HeaderDef
ms.assetid: 0f8dd043-66f0-4193-9b95-853bc3827f73
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3794386c4461c90f973e4028132cb8220dfaa19b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426349"
---
# <a name="pidtagipmwastebasketentryid-canonical-property"></a><span data-ttu-id="b4e47-103">Propriedade canônica PidTagIpmWastebasketEntryId</span><span class="sxs-lookup"><span data-stu-id="b4e47-103">PidTagIpmWastebasketEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="b4e47-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4e47-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4e47-105">Contém o identificador de entrada da pasta itens excluídos padrão de mensagem interpessoa (IPM).</span><span class="sxs-lookup"><span data-stu-id="b4e47-105">Contains the entry identifier of the standard interpersonal message (IPM) Deleted Items folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b4e47-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="b4e47-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b4e47-107">PR_IPM_WASTEBASKET_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="b4e47-107">PR_IPM_WASTEBASKET_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="b4e47-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b4e47-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b4e47-109">0x35E3</span><span class="sxs-lookup"><span data-stu-id="b4e47-109">0x35E3</span></span>  <br/> |
|<span data-ttu-id="b4e47-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="b4e47-110">Data type:</span></span>  <br/> |<span data-ttu-id="b4e47-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b4e47-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b4e47-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b4e47-112">Area:</span></span>  <br/> |<span data-ttu-id="b4e47-113">Folder</span><span class="sxs-lookup"><span data-stu-id="b4e47-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4e47-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b4e47-114">Remarks</span></span>

<span data-ttu-id="b4e47-115">Um aplicativo cliente deve mover mensagens interpessoas excluídas para a pasta itens excluídos.</span><span class="sxs-lookup"><span data-stu-id="b4e47-115">A client application should move deleted interpersonal messages to the Deleted Items folder.</span></span> <span data-ttu-id="b4e47-116">Se a mensagem já estiver nesta pasta ou se essa propriedade não for suportada, o cliente deverá excluir a mensagem.</span><span class="sxs-lookup"><span data-stu-id="b4e47-116">If the message is already in this folder, or if this property is not supported, the client should delete the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b4e47-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b4e47-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b4e47-118">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b4e47-118">Header files</span></span>

<span data-ttu-id="b4e47-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b4e47-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="b4e47-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="b4e47-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="b4e47-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="b4e47-121">Mapitags.h</span></span>
  
> <span data-ttu-id="b4e47-122">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="b4e47-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b4e47-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="b4e47-123">See also</span></span>



[<span data-ttu-id="b4e47-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b4e47-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b4e47-125">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="b4e47-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b4e47-126">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="b4e47-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b4e47-127">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="b4e47-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

