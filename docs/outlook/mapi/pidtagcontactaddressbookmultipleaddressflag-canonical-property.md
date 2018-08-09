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
ms.openlocfilehash: 42f164f09dbffcc05986771aa05f7ce14eee789c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769065"
---
# <a name="pidtagcontactaddressbookmultipleaddressflag-canonical-property"></a><span data-ttu-id="b4bfd-103">Propriedade canônica PidTagContactAddressBookMultipleAddressFlag</span><span class="sxs-lookup"><span data-stu-id="b4bfd-103">PidTagContactAddressBookMultipleAddressFlag Canonical Property</span></span>

  
  
<span data-ttu-id="b4bfd-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b4bfd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b4bfd-105">Contém um sinalizador que será TRUE quando o provedor oferece suporte a vários endereços de email por item de contato.</span><span class="sxs-lookup"><span data-stu-id="b4bfd-105">Contains a flag that is TRUE when the provider supports multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b4bfd-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="b4bfd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b4bfd-107">PR_CONTAB_MULTI_ADDR_FLAG</span><span class="sxs-lookup"><span data-stu-id="b4bfd-107">PR_CONTAB_MULTI_ADDR_FLAG</span></span>  <br/> |
|<span data-ttu-id="b4bfd-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b4bfd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b4bfd-109">0x6614</span><span class="sxs-lookup"><span data-stu-id="b4bfd-109">0x6614</span></span>  <br/> |
|<span data-ttu-id="b4bfd-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="b4bfd-110">Data type:</span></span>  <br/> |<span data-ttu-id="b4bfd-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="b4bfd-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="b4bfd-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b4bfd-112">Area:</span></span>  <br/> |<span data-ttu-id="b4bfd-113">Catálogo de endereços de contatos</span><span class="sxs-lookup"><span data-stu-id="b4bfd-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4bfd-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b4bfd-114">Remarks</span></span>

<span data-ttu-id="b4bfd-115">Se essa propriedade for TRUE, o provedor não permite contatos sem endereços de email.</span><span class="sxs-lookup"><span data-stu-id="b4bfd-115">If this property is TRUE, the provider does not allow contacts without email addresses.</span></span> <span data-ttu-id="b4bfd-116">Se for FALSE, o provedor mostra todos os contatos ou não terem um endereço de email primário.</span><span class="sxs-lookup"><span data-stu-id="b4bfd-116">If FALSE, the provider shows all contacts whether or not they have a primary email address.</span></span> <span data-ttu-id="b4bfd-117">Somente o endereço de email primário será atendido.</span><span class="sxs-lookup"><span data-stu-id="b4bfd-117">Only the primary email address will be honored.</span></span> <span data-ttu-id="b4bfd-118">Esta é uma propriedade em um contêiner de catálogo de endereços de contatos e uma coluna na tabela de contêineres do catálogo de endereços de contatos.</span><span class="sxs-lookup"><span data-stu-id="b4bfd-118">This is a property on a Contact Address Book container, and a column in the table of Contact Address Book containers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b4bfd-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b4bfd-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b4bfd-120">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b4bfd-120">Header files</span></span>

<span data-ttu-id="b4bfd-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b4bfd-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="b4bfd-122">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="b4bfd-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="b4bfd-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b4bfd-123">Mapitags.h</span></span>
  
> <span data-ttu-id="b4bfd-124">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="b4bfd-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b4bfd-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b4bfd-125">See also</span></span>



[<span data-ttu-id="b4bfd-126">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b4bfd-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b4bfd-127">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="b4bfd-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b4bfd-128">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="b4bfd-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b4bfd-129">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="b4bfd-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

