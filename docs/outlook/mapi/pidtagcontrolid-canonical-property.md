---
title: Propriedade canônico de PidTagControlId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlId
api_type:
- HeaderDef
ms.assetid: 281bc3e0-7c69-461b-bf09-4281abbb5e1b
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 799f83b397cbef9d7dcb6c9a88154b88afe35675
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19769124"
---
# <a name="pidtagcontrolid-canonical-property"></a><span data-ttu-id="a0b84-103">Propriedade canônico de PidTagControlId</span><span class="sxs-lookup"><span data-stu-id="a0b84-103">PidTagControlId Canonical Property</span></span>

  
  
<span data-ttu-id="a0b84-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a0b84-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a0b84-105">Contém um identificador exclusivo para um controle usado em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a0b84-105">Contains a unique identifier for a control used in a dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a0b84-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a0b84-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a0b84-107">PR_CONTROL_ID</span><span class="sxs-lookup"><span data-stu-id="a0b84-107">PR_CONTROL_ID</span></span>  <br/> |
|<span data-ttu-id="a0b84-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a0b84-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a0b84-109">0x3F07</span><span class="sxs-lookup"><span data-stu-id="a0b84-109">0x3F07</span></span>  <br/> |
|<span data-ttu-id="a0b84-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a0b84-110">Data type:</span></span>  <br/> |<span data-ttu-id="a0b84-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a0b84-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a0b84-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a0b84-112">Area:</span></span>  <br/> |<span data-ttu-id="a0b84-113">Tabela de exibição MAPI</span><span class="sxs-lookup"><span data-stu-id="a0b84-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a0b84-114">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="a0b84-114">Remarks</span></span>

<span data-ttu-id="a0b84-115">Essa propriedade contém um identificador exclusivo para o controle.</span><span class="sxs-lookup"><span data-stu-id="a0b84-115">This property contains a unique identifier for the control.</span></span> <span data-ttu-id="a0b84-116">Esse identificador deve conter uma estrutura [GUID](guid.md) e um valor binário do tipo **LONG**.</span><span class="sxs-lookup"><span data-stu-id="a0b84-116">This identifier should contain a [GUID](guid.md) structure and a binary value of type **LONG**.</span></span> <span data-ttu-id="a0b84-117">Todos os controles na caixa de diálogo devem usar o mesmo **GUID** para identificar o provedor de serviço, e cada controle deve usar um único valor **longo** para garantir que os controles não coincidem.</span><span class="sxs-lookup"><span data-stu-id="a0b84-117">All controls in the dialog box should use the same **GUID** to identify the service provider, and each control should use a unique **LONG** value to ensure that the controls do not collide.</span></span> 
  
<span data-ttu-id="a0b84-118">Essa propriedade é usada em notificações.</span><span class="sxs-lookup"><span data-stu-id="a0b84-118">This property is used in notifications.</span></span> <span data-ttu-id="a0b84-119">Por exemplo, notificações enviadas na tabela exibição devem definir essa propriedade para identificar exclusivamente o controle a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="a0b84-119">For example, notifications sent on the display table must set this property to uniquely identify the control to update.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a0b84-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a0b84-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a0b84-121">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a0b84-121">Header files</span></span>

<span data-ttu-id="a0b84-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a0b84-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="a0b84-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a0b84-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="a0b84-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a0b84-124">Mapitags.h</span></span>
  
> <span data-ttu-id="a0b84-125">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="a0b84-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a0b84-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="a0b84-126">See also</span></span>



[<span data-ttu-id="a0b84-127">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a0b84-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a0b84-128">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="a0b84-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a0b84-129">Mapear nomes de propriedade canônico para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a0b84-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a0b84-130">Mapear nomes de MAPI para nomes de propriedade canônico</span><span class="sxs-lookup"><span data-stu-id="a0b84-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
