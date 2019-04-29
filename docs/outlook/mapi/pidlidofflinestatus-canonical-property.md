---
title: Propriedade canônica PidLidOfflineStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidOfflineStatus
api_type:
- COM
ms.assetid: ee69f0c4-b552-4cfd-8a39-a822d414549e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 537b45420390903d67722c074a1edcc04a0aede8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418831"
---
# <a name="pidlidofflinestatus-canonical-property"></a><span data-ttu-id="c9cb5-103">Propriedade canônica PidLidOfflineStatus</span><span class="sxs-lookup"><span data-stu-id="c9cb5-103">PidLidOfflineStatus Canonical Property</span></span>

  
  
<span data-ttu-id="c9cb5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9cb5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9cb5-105">Determina o estado de um arquivo de documento em um servidor que implementa [MS-LISTSWS].</span><span class="sxs-lookup"><span data-stu-id="c9cb5-105">Determines the state of a document file on a server that implements [MS-LISTSWS].</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c9cb5-106">Propriedades associadas</span><span class="sxs-lookup"><span data-stu-id="c9cb5-106">Associated properties</span></span>  <br/> |<span data-ttu-id="c9cb5-107">dispidOfflineStatus</span><span class="sxs-lookup"><span data-stu-id="c9cb5-107">dispidOfflineStatus</span></span>  <br/> |
|<span data-ttu-id="c9cb5-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="c9cb5-108">Property set:</span></span>  <br/> |<span data-ttu-id="c9cb5-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="c9cb5-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="c9cb5-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="c9cb5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c9cb5-111">0x000085B9</span><span class="sxs-lookup"><span data-stu-id="c9cb5-111">0x000085B9</span></span>  <br/> |
|<span data-ttu-id="c9cb5-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="c9cb5-112">Data type:</span></span>  <br/> |<span data-ttu-id="c9cb5-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c9cb5-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c9cb5-114">Área:</span><span class="sxs-lookup"><span data-stu-id="c9cb5-114">Area:</span></span>  <br/> |<span data-ttu-id="c9cb5-115">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="c9cb5-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9cb5-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9cb5-116">Remarks</span></span>

<span data-ttu-id="c9cb5-117">A tabela a seguir mostra os valores possíveis dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c9cb5-117">The following table shows the possible values of this property.</span></span>
  
|<span data-ttu-id="c9cb5-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c9cb5-118">**Value**</span></span>|<span data-ttu-id="c9cb5-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c9cb5-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c9cb5-120">,0</span><span class="sxs-lookup"><span data-stu-id="c9cb5-120">0</span></span>  <br/> |<span data-ttu-id="c9cb5-121">Não foi feito o check-out do documento.</span><span class="sxs-lookup"><span data-stu-id="c9cb5-121">Document is not checked out.</span></span>  <br/> |
|<span data-ttu-id="c9cb5-122">1</span><span class="sxs-lookup"><span data-stu-id="c9cb5-122">1</span></span>  <br/> |<span data-ttu-id="c9cb5-123">O documento está com check-out para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="c9cb5-123">Document is checked out to the current user.</span></span>  <br/> |
|<span data-ttu-id="c9cb5-124">duas</span><span class="sxs-lookup"><span data-stu-id="c9cb5-124">2</span></span>  <br/> |<span data-ttu-id="c9cb5-125">Não foi feito o check-out do documento, mas o usuário atual tem uma cópia do arquivo salvo para edição no computador atual.</span><span class="sxs-lookup"><span data-stu-id="c9cb5-125">Document is not checked out, but the current user has a copy of the file saved for editing on the current computer.</span></span>  <br/> |
   
<span data-ttu-id="c9cb5-126">Essa propriedade é calculada localmente e não é enviada a um servidor a qualquer momento, a menos que um usuário arraste o item para outra conta.</span><span class="sxs-lookup"><span data-stu-id="c9cb5-126">This property is calculated locally and is not sent to a server at any time unless a user drags the item to another account.</span></span> <span data-ttu-id="c9cb5-127">Nesse caso, ele é tratado como uma propriedade personalizada definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="c9cb5-127">In that case, it is treated as a user-defined custom property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c9cb5-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c9cb5-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c9cb5-129">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="c9cb5-129">Protocol specifications</span></span>

<span data-ttu-id="c9cb5-130">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="c9cb5-130">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="c9cb5-131">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="c9cb5-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c9cb5-132">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c9cb5-132">Header files</span></span>

<span data-ttu-id="c9cb5-133">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c9cb5-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="c9cb5-134">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c9cb5-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c9cb5-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9cb5-135">See also</span></span>



[<span data-ttu-id="c9cb5-136">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c9cb5-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c9cb5-137">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="c9cb5-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c9cb5-138">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="c9cb5-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c9cb5-139">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="c9cb5-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

