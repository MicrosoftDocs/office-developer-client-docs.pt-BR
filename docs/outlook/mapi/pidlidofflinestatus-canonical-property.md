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
ms.openlocfilehash: 34f50766c2c45d85bbb0bd9e12d32c5dd87e3cac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768553"
---
# <a name="pidlidofflinestatus-canonical-property"></a><span data-ttu-id="d4cc4-103">Propriedade canônica PidLidOfflineStatus</span><span class="sxs-lookup"><span data-stu-id="d4cc4-103">PidLidOfflineStatus Canonical Property</span></span>

  
  
<span data-ttu-id="d4cc4-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d4cc4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d4cc4-105">Determina o estado de um arquivo de documento em um servidor que implementa [MS-LISTSWS].</span><span class="sxs-lookup"><span data-stu-id="d4cc4-105">Determines the state of a document file on a server that implements [MS-LISTSWS].</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d4cc4-106">Propriedades associadas</span><span class="sxs-lookup"><span data-stu-id="d4cc4-106">Associated properties</span></span>  <br/> |<span data-ttu-id="d4cc4-107">dispidOfflineStatus</span><span class="sxs-lookup"><span data-stu-id="d4cc4-107">dispidOfflineStatus</span></span>  <br/> |
|<span data-ttu-id="d4cc4-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="d4cc4-108">Property set:</span></span>  <br/> |<span data-ttu-id="d4cc4-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="d4cc4-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="d4cc4-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="d4cc4-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d4cc4-111">0x000085B9</span><span class="sxs-lookup"><span data-stu-id="d4cc4-111">0x000085B9</span></span>  <br/> |
|<span data-ttu-id="d4cc4-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="d4cc4-112">Data type:</span></span>  <br/> |<span data-ttu-id="d4cc4-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d4cc4-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d4cc4-114">Área:</span><span class="sxs-lookup"><span data-stu-id="d4cc4-114">Area:</span></span>  <br/> |<span data-ttu-id="d4cc4-115">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="d4cc4-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4cc4-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4cc4-116">Remarks</span></span>

<span data-ttu-id="d4cc4-117">A tabela a seguir mostra os possíveis valores dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="d4cc4-117">The following table shows the possible values of this property.</span></span>
  
|<span data-ttu-id="d4cc4-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d4cc4-118">**Value**</span></span>|<span data-ttu-id="d4cc4-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d4cc4-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d4cc4-120">0</span><span class="sxs-lookup"><span data-stu-id="d4cc4-120">0</span></span>  <br/> |<span data-ttu-id="d4cc4-121">Documento não está com check-out.</span><span class="sxs-lookup"><span data-stu-id="d4cc4-121">Document is not checked out.</span></span>  <br/> |
|<span data-ttu-id="d4cc4-122">1</span><span class="sxs-lookup"><span data-stu-id="d4cc4-122">1</span></span>  <br/> |<span data-ttu-id="d4cc4-123">Documento está com check-out para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="d4cc4-123">Document is checked out to the current user.</span></span>  <br/> |
|<span data-ttu-id="d4cc4-124">2</span><span class="sxs-lookup"><span data-stu-id="d4cc4-124">2</span></span>  <br/> |<span data-ttu-id="d4cc4-125">Documento não está com check-out, mas o usuário atual tem uma cópia do arquivo salvo para edição no computador atual.</span><span class="sxs-lookup"><span data-stu-id="d4cc4-125">Document is not checked out, but the current user has a copy of the file saved for editing on the current computer.</span></span>  <br/> |
   
<span data-ttu-id="d4cc4-126">Essa propriedade é calculada localmente e não é enviada para um servidor a qualquer momento, a menos que um usuário arrasta o item para outra conta.</span><span class="sxs-lookup"><span data-stu-id="d4cc4-126">This property is calculated locally and is not sent to a server at any time unless a user drags the item to another account.</span></span> <span data-ttu-id="d4cc4-127">Nesse caso, ela será tratada como uma propriedade personalizada definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="d4cc4-127">In that case, it is treated as a user-defined custom property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d4cc4-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d4cc4-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d4cc4-129">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="d4cc4-129">Protocol specifications</span></span>

<span data-ttu-id="d4cc4-130">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="d4cc4-130">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="d4cc4-131">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="d4cc4-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d4cc4-132">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d4cc4-132">Header files</span></span>

<span data-ttu-id="d4cc4-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d4cc4-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="d4cc4-134">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d4cc4-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d4cc4-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="d4cc4-135">See also</span></span>



[<span data-ttu-id="d4cc4-136">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d4cc4-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d4cc4-137">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="d4cc4-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d4cc4-138">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="d4cc4-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d4cc4-139">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="d4cc4-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

