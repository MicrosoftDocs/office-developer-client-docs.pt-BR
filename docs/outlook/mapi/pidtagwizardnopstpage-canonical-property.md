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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350719"
---
# <a name="pidtagwizardnopstpage-canonical-property"></a><span data-ttu-id="7c906-103">Propriedade canônica PidTagWizardNoPstPage</span><span class="sxs-lookup"><span data-stu-id="7c906-103">PidTagWizardNoPstPage Canonical Property</span></span>

  
  
<span data-ttu-id="7c906-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c906-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c906-105">Esta propriedade conterá TRUE se o assistente de perfil for suprimir a página de repositório de mensagens pessoais (PST).</span><span class="sxs-lookup"><span data-stu-id="7c906-105">This property contains TRUE if the profile wizard is to suppress the personal message store (PST) page.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7c906-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="7c906-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7c906-107">PR_WIZARD_NO_PST_PAGE</span><span class="sxs-lookup"><span data-stu-id="7c906-107">PR_WIZARD_NO_PST_PAGE</span></span>  <br/> |
|<span data-ttu-id="7c906-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7c906-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7c906-109">0x6700</span><span class="sxs-lookup"><span data-stu-id="7c906-109">0x6700</span></span>  <br/> |
|<span data-ttu-id="7c906-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="7c906-110">Data type:</span></span>  <br/> |<span data-ttu-id="7c906-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="7c906-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="7c906-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7c906-112">Area:</span></span>  <br/> |<span data-ttu-id="7c906-113">Administrativo do Exchange</span><span class="sxs-lookup"><span data-stu-id="7c906-113">Exchange Administrative</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7c906-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c906-114">Remarks</span></span>

<span data-ttu-id="7c906-115">Os provedores de serviços podem definir essa propriedade ao chamar uma função com base no protótipo de função [LAUNCHWIZARDENTRY](launchwizardentry.md) .</span><span class="sxs-lookup"><span data-stu-id="7c906-115">Service providers can set this property when calling a function based on the [LAUNCHWIZARDENTRY](launchwizardentry.md) function prototype.</span></span> <span data-ttu-id="7c906-116">Essa propriedade informa ao assistente de perfil que o provedor não quer que a página PST seja exibida durante a caixa de diálogo do usuário.</span><span class="sxs-lookup"><span data-stu-id="7c906-116">This property tells the profile wizard that the provider does not want the PST page to be displayed during the user dialog.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7c906-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7c906-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7c906-118">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7c906-118">Header files</span></span>

<span data-ttu-id="7c906-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7c906-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="7c906-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="7c906-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="7c906-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="7c906-121">Mapitags.h</span></span>
  
> <span data-ttu-id="7c906-122">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="7c906-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7c906-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c906-123">See also</span></span>



[<span data-ttu-id="7c906-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7c906-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7c906-125">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="7c906-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7c906-126">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="7c906-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7c906-127">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="7c906-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

