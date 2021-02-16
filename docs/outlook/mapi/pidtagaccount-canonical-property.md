---
title: Propriedade canônica PidTagAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccount
api_type:
- HeaderDef
ms.assetid: bec199b5-abfd-4686-ad59-21092212e1a5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2962f973aa87b88f237ded69573df9ef312a7bc5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359772"
---
# <a name="pidtagaccount-canonical-property"></a><span data-ttu-id="3eb89-103">Propriedade canônica PidTagAccount</span><span class="sxs-lookup"><span data-stu-id="3eb89-103">PidTagAccount Canonical Property</span></span>

  
  
<span data-ttu-id="3eb89-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3eb89-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3eb89-105">Contém o nome da conta do destinatário.</span><span class="sxs-lookup"><span data-stu-id="3eb89-105">Contains the recipient's account name.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3eb89-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="3eb89-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3eb89-107">PR_ACCOUNT, PR_ACCOUNT_A, PR_ACCOUNT_W</span><span class="sxs-lookup"><span data-stu-id="3eb89-107">PR_ACCOUNT, PR_ACCOUNT_A, PR_ACCOUNT_W</span></span>  <br/> |
|<span data-ttu-id="3eb89-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3eb89-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3eb89-109">0x3A00</span><span class="sxs-lookup"><span data-stu-id="3eb89-109">0x3A00</span></span>  <br/> |
|<span data-ttu-id="3eb89-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="3eb89-110">Data type:</span></span>  <br/> |<span data-ttu-id="3eb89-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3eb89-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3eb89-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3eb89-112">Area:</span></span>  <br/> |<span data-ttu-id="3eb89-113">Catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="3eb89-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3eb89-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3eb89-114">Remarks</span></span>

<span data-ttu-id="3eb89-115">Essas propriedades fornecem informações de identificação e acesso para um destinatário.</span><span class="sxs-lookup"><span data-stu-id="3eb89-115">These properties provide identification and access information for a recipient.</span></span> <span data-ttu-id="3eb89-116">Eles são definidos pelo destinatário e sua organização.</span><span class="sxs-lookup"><span data-stu-id="3eb89-116">They are defined by the recipient and their organization.</span></span>
  
<span data-ttu-id="3eb89-117">Essas propriedades geralmente contêm o nome de email do destinatário, ou seja, o componente final do endereço de email, que identifica exclusivamente o destinatário na organização local.</span><span class="sxs-lookup"><span data-stu-id="3eb89-117">These properties commonly contain the recipient's email name, that is, the final component of the email address, which uniquely identifies the recipient in the local organization.</span></span> <span data-ttu-id="3eb89-118">O nome de email corresponde ao nome diferenciado X.400, que deve ser um nome curto garantido como exclusivo em um determinado domínio de mensagens.</span><span class="sxs-lookup"><span data-stu-id="3eb89-118">The email name corresponds to the X.400 distinguished name, which is meant to be a short name guaranteed to be unique within a certain messaging domain.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3eb89-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3eb89-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3eb89-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="3eb89-120">Protocol specifications</span></span>

<span data-ttu-id="3eb89-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3eb89-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3eb89-122">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="3eb89-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3eb89-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3eb89-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3eb89-124">Especifica as propriedades e operações permitidas para contatos e listas de distribuição pessoais.</span><span class="sxs-lookup"><span data-stu-id="3eb89-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="3eb89-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3eb89-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3eb89-126">Especifica as propriedades e operações para listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="3eb89-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3eb89-127">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="3eb89-127">Header files</span></span>

<span data-ttu-id="3eb89-128">mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3eb89-128">mapitags.h</span></span>
  
> <span data-ttu-id="3eb89-129">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="3eb89-129">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="3eb89-130">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3eb89-130">mapidefs.h</span></span>
  
> <span data-ttu-id="3eb89-131">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="3eb89-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3eb89-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="3eb89-132">See also</span></span>



[<span data-ttu-id="3eb89-133">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3eb89-133">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md)


[<span data-ttu-id="3eb89-134">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="3eb89-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3eb89-135">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="3eb89-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3eb89-136">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="3eb89-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

