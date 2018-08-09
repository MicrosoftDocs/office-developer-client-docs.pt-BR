---
title: Propriedade canônica PidTagDelegateFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDelegateFlags
api_type:
- HeaderDef
ms.assetid: 3a504594-204c-472c-8be7-dca154c94ea2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 160ddc53edf3d9681adf6f9d536a488c0c345a07
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769157"
---
# <a name="pidtagdelegateflags-canonical-property"></a><span data-ttu-id="984dc-103">Propriedade canônica PidTagDelegateFlags</span><span class="sxs-lookup"><span data-stu-id="984dc-103">PidTagDelegateFlags Canonical Property</span></span>

  
  
<span data-ttu-id="984dc-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="984dc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="984dc-105">Especifica se um representante pode exibir objetos de mensagem privada do representante.</span><span class="sxs-lookup"><span data-stu-id="984dc-105">Specifies whether a delegate can view the delegator's private message objects.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="984dc-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="984dc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="984dc-107">PR_DELEGATE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="984dc-107">PR_DELEGATE_FLAGS</span></span>  <br/> |
|<span data-ttu-id="984dc-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="984dc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="984dc-109">0x686B</span><span class="sxs-lookup"><span data-stu-id="984dc-109">0x686B</span></span>  <br/> |
|<span data-ttu-id="984dc-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="984dc-110">Data type:</span></span>  <br/> |<span data-ttu-id="984dc-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="984dc-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="984dc-112">Área:</span><span class="sxs-lookup"><span data-stu-id="984dc-112">Area:</span></span>  <br/> |<span data-ttu-id="984dc-113">Mensagem definida de classe transmittable</span><span class="sxs-lookup"><span data-stu-id="984dc-113">Message class-defined transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="984dc-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="984dc-114">Remarks</span></span>

<span data-ttu-id="984dc-115">Cada entrada dessa propriedade deve ser definida como um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="984dc-115">Each entry of this property must be set to one of the following values.</span></span>
  
|<span data-ttu-id="984dc-116">**Flag**</span><span class="sxs-lookup"><span data-stu-id="984dc-116">**Flag**</span></span>|<span data-ttu-id="984dc-117">**Valor**</span><span class="sxs-lookup"><span data-stu-id="984dc-117">**Value**</span></span>|<span data-ttu-id="984dc-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="984dc-118">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="984dc-119">HidePrivate</span><span class="sxs-lookup"><span data-stu-id="984dc-119">HidePrivate</span></span>  <br/> |<span data-ttu-id="984dc-120">0</span><span class="sxs-lookup"><span data-stu-id="984dc-120">0</span></span>  <br/> |<span data-ttu-id="984dc-121">O representante não deve ser permitido para exibir objetos de mensagem privada.</span><span class="sxs-lookup"><span data-stu-id="984dc-121">The delegate should not be allowed to view private message objects.</span></span>  <br/> |
|<span data-ttu-id="984dc-122">ShowPrivate</span><span class="sxs-lookup"><span data-stu-id="984dc-122">ShowPrivate</span></span>  <br/> |<span data-ttu-id="984dc-123">1</span><span class="sxs-lookup"><span data-stu-id="984dc-123">1</span></span>  <br/> |<span data-ttu-id="984dc-124">O delegado deve ter permissão para exibir objetos de mensagem privada.</span><span class="sxs-lookup"><span data-stu-id="984dc-124">The delegate should be allowed to view private message objects.</span></span>  <br/> |
   
<span data-ttu-id="984dc-125">Essa propriedade deverá ser definida no objeto de informações do representante.</span><span class="sxs-lookup"><span data-stu-id="984dc-125">This property must be set in the delegate information object.</span></span> <span data-ttu-id="984dc-126">O valor de "ShowPrivate" indica que o representante deseje tornar visíveis a objetos de mensagem privada.</span><span class="sxs-lookup"><span data-stu-id="984dc-126">The value of "ShowPrivate" indicates that the delegator wants to make private message objects visible.</span></span> <span data-ttu-id="984dc-127">Esta preferência é aplicável a todas as pastas para o qual o representante tem uma função do revisor, autor ou editor.</span><span class="sxs-lookup"><span data-stu-id="984dc-127">This preference is applicable to all folders for which the delegate has a role of reviewer, author, or editor.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="984dc-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="984dc-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="984dc-129">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="984dc-129">Protocol specifications</span></span>

<span data-ttu-id="984dc-130">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="984dc-130">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="984dc-131">Especifica os métodos para conexão e a configuração de caixas de correio conforme representantes e as interações com objetos de mensagem e o calendário quando eles ajam em nome de outro usuário.</span><span class="sxs-lookup"><span data-stu-id="984dc-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="984dc-132">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="984dc-132">Header files</span></span>

<span data-ttu-id="984dc-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="984dc-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="984dc-134">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="984dc-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="984dc-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="984dc-135">Mapitags.h</span></span>
  
> <span data-ttu-id="984dc-136">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="984dc-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="984dc-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="984dc-137">See also</span></span>



[<span data-ttu-id="984dc-138">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="984dc-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="984dc-139">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="984dc-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="984dc-140">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="984dc-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="984dc-141">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="984dc-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
