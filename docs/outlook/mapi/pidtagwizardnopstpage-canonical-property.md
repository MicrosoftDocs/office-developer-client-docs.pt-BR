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
ms.openlocfilehash: b94e1f2d66f89d680cc738968342de0fbcee5cda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19770162"
---
# <a name="pidtagwizardnopstpage-canonical-property"></a><span data-ttu-id="973a4-103">Propriedade canônica PidTagWizardNoPstPage</span><span class="sxs-lookup"><span data-stu-id="973a4-103">PidTagWizardNoPstPage Canonical Property</span></span>

  
  
<span data-ttu-id="973a4-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="973a4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="973a4-105">Essa propriedade contém TRUE se o Assistente de perfil suprimir a página de repositório (. PST) da mensagem pessoal.</span><span class="sxs-lookup"><span data-stu-id="973a4-105">This property contains TRUE if the profile wizard is to suppress the personal message store (PST) page.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="973a4-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="973a4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="973a4-107">PR_WIZARD_NO_PST_PAGE</span><span class="sxs-lookup"><span data-stu-id="973a4-107">PR_WIZARD_NO_PST_PAGE</span></span>  <br/> |
|<span data-ttu-id="973a4-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="973a4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="973a4-109">0x6700</span><span class="sxs-lookup"><span data-stu-id="973a4-109">0x6700</span></span>  <br/> |
|<span data-ttu-id="973a4-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="973a4-110">Data type:</span></span>  <br/> |<span data-ttu-id="973a4-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="973a4-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="973a4-112">Área:</span><span class="sxs-lookup"><span data-stu-id="973a4-112">Area:</span></span>  <br/> |<span data-ttu-id="973a4-113">Exchange administrativa</span><span class="sxs-lookup"><span data-stu-id="973a4-113">Exchange Administrative</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="973a4-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="973a4-114">Remarks</span></span>

<span data-ttu-id="973a4-115">Provedores de serviços podem definir essa propriedade, ao chamar uma função com base no protótipo de função [LAUNCHWIZARDENTRY](launchwizardentry.md) .</span><span class="sxs-lookup"><span data-stu-id="973a4-115">Service providers can set this property when calling a function based on the [LAUNCHWIZARDENTRY](launchwizardentry.md) function prototype.</span></span> <span data-ttu-id="973a4-116">Esta propriedade instrui o Assistente de perfil que o provedor não deseja que a página de PST sejam exibidas durante a caixa de diálogo do usuário.</span><span class="sxs-lookup"><span data-stu-id="973a4-116">This property tells the profile wizard that the provider does not want the PST page to be displayed during the user dialog.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="973a4-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="973a4-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="973a4-118">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="973a4-118">Header files</span></span>

<span data-ttu-id="973a4-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="973a4-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="973a4-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="973a4-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="973a4-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="973a4-121">Mapitags.h</span></span>
  
> <span data-ttu-id="973a4-122">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="973a4-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="973a4-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="973a4-123">See also</span></span>



[<span data-ttu-id="973a4-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="973a4-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="973a4-125">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="973a4-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="973a4-126">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="973a4-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="973a4-127">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="973a4-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

