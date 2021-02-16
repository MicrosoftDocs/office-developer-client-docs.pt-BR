---
title: Propriedade canônica PidTagJunkIncludeContacts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkIncludeContacts
api_type:
- HeaderDef
ms.assetid: 25368f6c-4fba-4381-840c-ca122bd31b5f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7e61e98d1db1ab3acb958da353d8d22870937632
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328711"
---
# <a name="pidtagjunkincludecontacts-canonical-property"></a><span data-ttu-id="a47fa-103">Propriedade canônica PidTagJunkIncludeContacts</span><span class="sxs-lookup"><span data-stu-id="a47fa-103">PidTagJunkIncludeContacts Canonical Property</span></span>

  
  
<span data-ttu-id="a47fa-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a47fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a47fa-105">Indica se os endereços de email dos contatos na pasta Contatos são tratados especialmente em relação ao filtro de spam.</span><span class="sxs-lookup"><span data-stu-id="a47fa-105">Indicates whether email addresses of the contacts in the Contacts folder are treated specially with respect to the spam filter.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a47fa-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a47fa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a47fa-107">PR_JUNK_INCLUDE_CONTACTS</span><span class="sxs-lookup"><span data-stu-id="a47fa-107">PR_JUNK_INCLUDE_CONTACTS</span></span>  <br/> |
|<span data-ttu-id="a47fa-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a47fa-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a47fa-109">0x6100</span><span class="sxs-lookup"><span data-stu-id="a47fa-109">0x6100</span></span>  <br/> |
|<span data-ttu-id="a47fa-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a47fa-110">Data type:</span></span>  <br/> |<span data-ttu-id="a47fa-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a47fa-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a47fa-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a47fa-112">Area:</span></span>  <br/> |<span data-ttu-id="a47fa-113">Spam</span><span class="sxs-lookup"><span data-stu-id="a47fa-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a47fa-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a47fa-114">Remarks</span></span>

<span data-ttu-id="a47fa-115">Se definido como "0x00000001", esses endereços de email deverão preencher a parte do endereço de email de contato "confiável" da Restrição de Regra de Lixo Eletrônico de forma que os emails desses endereços seja tratados como "não é lixo eletrônico".</span><span class="sxs-lookup"><span data-stu-id="a47fa-115">If set to "0x00000001", these email addresses must populate the "trusted" contact email address portion of the Junk E-Mail Rule Restriction such that mail from these addresses is treated as "not junk".</span></span> <span data-ttu-id="a47fa-116">Se definido como "0x00000000", os endereços de email da pasta Contatos não devem ser adicionados à Regra de Lixo Eletrônico e a seção da regra deve ser NULL.</span><span class="sxs-lookup"><span data-stu-id="a47fa-116">If set to "0x00000000", email addresses from the Contacts folder must not be added to the Junk E-Mail Rule, and the section of the rule must be NULL.</span></span>
  
<span data-ttu-id="a47fa-117">Se essa propriedade estiver presente com um valor de "0x00000001" e se o contato adicionado tiver endereços de email que ainda não estão incluídos na seção contatos confiáveis da Regra de Lixo Eletrônico, esses endereços de email deverão ser adicionados à restrição.</span><span class="sxs-lookup"><span data-stu-id="a47fa-117">If this property is present with a value of "0x00000001" and if the added contact has email addresses that are not yet included in the trusted contacts section of the Junk E-Mail Rule, those email addresses must be added to the restriction.</span></span> <span data-ttu-id="a47fa-118">Se essa propriedade for "0x00000000", nenhuma ação será necessária.</span><span class="sxs-lookup"><span data-stu-id="a47fa-118">If this property is "0x00000000", no action is required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a47fa-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a47fa-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a47fa-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="a47fa-120">Protocol specifications</span></span>

<span data-ttu-id="a47fa-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a47fa-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a47fa-122">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a47fa-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a47fa-123">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a47fa-123">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a47fa-124">Permite a manipulação de listas de bloqueio/autorização e a determinação de mensagens de lixo eletrônico.</span><span class="sxs-lookup"><span data-stu-id="a47fa-124">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a47fa-125">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="a47fa-125">Header files</span></span>

<span data-ttu-id="a47fa-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a47fa-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="a47fa-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a47fa-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="a47fa-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a47fa-128">Mapitags.h</span></span>
  
> <span data-ttu-id="a47fa-129">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="a47fa-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a47fa-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="a47fa-130">See also</span></span>



[<span data-ttu-id="a47fa-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a47fa-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a47fa-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="a47fa-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a47fa-133">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a47fa-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a47fa-134">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="a47fa-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

