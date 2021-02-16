---
title: Propriedade canônica PidTagContactAddressBookMultipleAddressFlag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookMultipleAddressFlag
api_type:
- HeaderDef
ms.assetid: aefc34c5-1beb-44cf-a455-90f466e157ce
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6fabb03d552f195c200b0ecbd8fd69f470c0e1fd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431565"
---
# <a name="pidtagcontactaddressbookmultipleaddressflag-canonical-property"></a><span data-ttu-id="96df6-103">Propriedade canônica PidTagContactAddressBookMultipleAddressFlag</span><span class="sxs-lookup"><span data-stu-id="96df6-103">PidTagContactAddressBookMultipleAddressFlag Canonical Property</span></span>

  
  
<span data-ttu-id="96df6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="96df6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="96df6-105">Contém um sinalizador verdadeiro quando o provedor oferece suporte a vários endereços de email por item de contato.</span><span class="sxs-lookup"><span data-stu-id="96df6-105">Contains a flag that is TRUE when the provider supports multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="96df6-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="96df6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="96df6-107">PR_CONTAB_MULTI_ADDR_FLAG</span><span class="sxs-lookup"><span data-stu-id="96df6-107">PR_CONTAB_MULTI_ADDR_FLAG</span></span>  <br/> |
|<span data-ttu-id="96df6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="96df6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="96df6-109">0x6614</span><span class="sxs-lookup"><span data-stu-id="96df6-109">0x6614</span></span>  <br/> |
|<span data-ttu-id="96df6-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="96df6-110">Data type:</span></span>  <br/> |<span data-ttu-id="96df6-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="96df6-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="96df6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="96df6-112">Area:</span></span>  <br/> |<span data-ttu-id="96df6-113">Contact address book</span><span class="sxs-lookup"><span data-stu-id="96df6-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96df6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="96df6-114">Remarks</span></span>

<span data-ttu-id="96df6-115">Se essa propriedade for TRUE, o provedor não permitirá contatos sem endereços de email.</span><span class="sxs-lookup"><span data-stu-id="96df6-115">If this property is TRUE, the provider does not allow contacts without email addresses.</span></span> <span data-ttu-id="96df6-116">Se for FALSO, o provedor mostrará todos os contatos se eles têm ou não um endereço de email principal.</span><span class="sxs-lookup"><span data-stu-id="96df6-116">If FALSE, the provider shows all contacts whether or not they have a primary email address.</span></span> <span data-ttu-id="96df6-117">Somente o endereço de email principal será aumente.</span><span class="sxs-lookup"><span data-stu-id="96df6-117">Only the primary email address will be honored.</span></span> <span data-ttu-id="96df6-118">Esta é uma propriedade em um contêiner do Livro de Endereços de Contato e uma coluna na tabela de contêineres do Livro de Endereços de Contato.</span><span class="sxs-lookup"><span data-stu-id="96df6-118">This is a property on a Contact Address Book container, and a column in the table of Contact Address Book containers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="96df6-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="96df6-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="96df6-120">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="96df6-120">Header files</span></span>

<span data-ttu-id="96df6-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="96df6-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="96df6-122">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="96df6-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="96df6-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="96df6-123">Mapitags.h</span></span>
  
> <span data-ttu-id="96df6-124">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="96df6-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="96df6-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="96df6-125">See also</span></span>



[<span data-ttu-id="96df6-126">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="96df6-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="96df6-127">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="96df6-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="96df6-128">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="96df6-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="96df6-129">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="96df6-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

