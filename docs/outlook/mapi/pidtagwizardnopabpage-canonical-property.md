---
title: Propriedade canônica PidTagWizardNoPabPage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagWizardNoPabPage
api_type:
- COM
ms.assetid: 9cec22cd-798d-41f6-9ebd-c7354f2162c2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cdb7dde4853188eb0621dc3c2f45c2dc713441d3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570237"
---
# <a name="pidtagwizardnopabpage-canonical-property"></a><span data-ttu-id="da4fa-103">Propriedade canônica PidTagWizardNoPabPage</span><span class="sxs-lookup"><span data-stu-id="da4fa-103">PidTagWizardNoPabPage Canonical Property</span></span>

  
  
<span data-ttu-id="da4fa-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da4fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da4fa-105">Essa propriedade contém TRUE se o Assistente de perfil suprimir a página de catálogo (PAB) particular de endereços.</span><span class="sxs-lookup"><span data-stu-id="da4fa-105">This property contains TRUE if the profile wizard is to suppress the personal address book (PAB) page.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="da4fa-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="da4fa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="da4fa-107">PR_WIZARD_NO_PAB_PAGE</span><span class="sxs-lookup"><span data-stu-id="da4fa-107">PR_WIZARD_NO_PAB_PAGE</span></span>  <br/> |
|<span data-ttu-id="da4fa-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="da4fa-108">Identifier:</span></span>  <br/> |<span data-ttu-id="da4fa-109">0x6701</span><span class="sxs-lookup"><span data-stu-id="da4fa-109">0x6701</span></span>  <br/> |
|<span data-ttu-id="da4fa-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="da4fa-110">Data type:</span></span>  <br/> |<span data-ttu-id="da4fa-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="da4fa-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="da4fa-112">Área:</span><span class="sxs-lookup"><span data-stu-id="da4fa-112">Area:</span></span>  <br/> |<span data-ttu-id="da4fa-113">Exchange administrativa</span><span class="sxs-lookup"><span data-stu-id="da4fa-113">Exchange Administrative</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="da4fa-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="da4fa-114">Remarks</span></span>

<span data-ttu-id="da4fa-115">Provedores de serviços podem definir essa propriedade, ao chamar uma função com base no protótipo de função [LAUNCHWIZARDENTRY](launchwizardentry.md) .</span><span class="sxs-lookup"><span data-stu-id="da4fa-115">Service providers can set this property when calling a function based on the [LAUNCHWIZARDENTRY](launchwizardentry.md) function prototype.</span></span> <span data-ttu-id="da4fa-116">Esta propriedade instrui o Assistente de perfil que o provedor não deseja que a página PAB sejam exibidas durante a caixa de diálogo do usuário.</span><span class="sxs-lookup"><span data-stu-id="da4fa-116">This property tells the profile wizard that the provider does not want the PAB page to be displayed during the user dialog.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="da4fa-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="da4fa-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="da4fa-118">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="da4fa-118">Header files</span></span>

<span data-ttu-id="da4fa-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="da4fa-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="da4fa-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="da4fa-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="da4fa-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="da4fa-121">Mapitags.h</span></span>
  
> <span data-ttu-id="da4fa-122">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="da4fa-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="da4fa-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="da4fa-123">See also</span></span>



[<span data-ttu-id="da4fa-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="da4fa-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="da4fa-125">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="da4fa-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="da4fa-126">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="da4fa-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="da4fa-127">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="da4fa-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

