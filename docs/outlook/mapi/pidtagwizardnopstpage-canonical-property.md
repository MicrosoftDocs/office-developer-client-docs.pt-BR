---
title: Propriedade canônica PidTagWizardNoPstPage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagWizardNoPstPage
api_type:
- COM
ms.assetid: 1ac09578-892b-4c72-92f6-c2419ac2efe8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e816af2ce60b4c06ae14f720cf7c36d58468d09d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422884"
---
# <a name="pidtagwizardnopstpage-canonical-property"></a><span data-ttu-id="989cc-103">Propriedade canônica PidTagWizardNoPstPage</span><span class="sxs-lookup"><span data-stu-id="989cc-103">PidTagWizardNoPstPage Canonical Property</span></span>

  
  
<span data-ttu-id="989cc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="989cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="989cc-105">Essa propriedade conterá TRUE se o assistente de perfil for suprimir a página PST (armazenamento de mensagens pessoais).</span><span class="sxs-lookup"><span data-stu-id="989cc-105">This property contains TRUE if the profile wizard is to suppress the personal message store (PST) page.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="989cc-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="989cc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="989cc-107">PR_WIZARD_NO_PST_PAGE</span><span class="sxs-lookup"><span data-stu-id="989cc-107">PR_WIZARD_NO_PST_PAGE</span></span>  <br/> |
|<span data-ttu-id="989cc-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="989cc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="989cc-109">0x6700</span><span class="sxs-lookup"><span data-stu-id="989cc-109">0x6700</span></span>  <br/> |
|<span data-ttu-id="989cc-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="989cc-110">Data type:</span></span>  <br/> |<span data-ttu-id="989cc-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="989cc-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="989cc-112">Área:</span><span class="sxs-lookup"><span data-stu-id="989cc-112">Area:</span></span>  <br/> |<span data-ttu-id="989cc-113">Exchange Administrative</span><span class="sxs-lookup"><span data-stu-id="989cc-113">Exchange Administrative</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="989cc-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="989cc-114">Remarks</span></span>

<span data-ttu-id="989cc-115">Os provedores de serviços podem definir essa propriedade ao chamar uma função com base no protótipo de [função LAUNCHWIZARDENTRY.](launchwizardentry.md)</span><span class="sxs-lookup"><span data-stu-id="989cc-115">Service providers can set this property when calling a function based on the [LAUNCHWIZARDENTRY](launchwizardentry.md) function prototype.</span></span> <span data-ttu-id="989cc-116">Essa propriedade informa ao assistente de perfil que o provedor não deseja que a página PST seja exibida durante a caixa de diálogo do usuário.</span><span class="sxs-lookup"><span data-stu-id="989cc-116">This property tells the profile wizard that the provider does not want the PST page to be displayed during the user dialog.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="989cc-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="989cc-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="989cc-118">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="989cc-118">Header files</span></span>

<span data-ttu-id="989cc-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="989cc-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="989cc-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="989cc-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="989cc-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="989cc-121">Mapitags.h</span></span>
  
> <span data-ttu-id="989cc-122">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="989cc-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="989cc-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="989cc-123">See also</span></span>



[<span data-ttu-id="989cc-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="989cc-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="989cc-125">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="989cc-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="989cc-126">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="989cc-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="989cc-127">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="989cc-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

