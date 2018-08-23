---
title: Propriedade canônica PidTagMemberEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberEntryId
api_type:
- HeaderDef
ms.assetid: b1e166fd-7e15-4371-8510-63001317fb90
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 27659b69e0ae050206de18c1258ee593737fbd3b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592945"
---
# <a name="pidtagmemberentryid-canonical-property"></a><span data-ttu-id="c2384-103">Propriedade canônica PidTagMemberEntryId</span><span class="sxs-lookup"><span data-stu-id="c2384-103">PidTagMemberEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="c2384-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c2384-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c2384-105">Contém o identificador de entrada de objeto de diretório de um membro de tabela do sistema acesso controle SACL (lista).</span><span class="sxs-lookup"><span data-stu-id="c2384-105">Contains the directory object entry identifier of a system access control list (SACL) table member.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c2384-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="c2384-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c2384-107">PR_MEMBER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="c2384-107">PR_MEMBER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="c2384-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c2384-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c2384-109">0x0FFF</span><span class="sxs-lookup"><span data-stu-id="c2384-109">0x0FFF</span></span>  <br/> |
|<span data-ttu-id="c2384-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="c2384-110">Data type:</span></span>  <br/> |<span data-ttu-id="c2384-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c2384-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c2384-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c2384-112">Area:</span></span>  <br/> |<span data-ttu-id="c2384-113">Regras do lado servidor</span><span class="sxs-lookup"><span data-stu-id="c2384-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c2384-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2384-114">Remarks</span></span>

<span data-ttu-id="c2384-115">Essa propriedade é usada pela interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) para identificar exclusivamente uma pessoa ou função aos quais se aplica a SACL.</span><span class="sxs-lookup"><span data-stu-id="c2384-115">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to uniquely identify a person or role to whom the SACL applies.</span></span> <span data-ttu-id="c2384-116">Depois que o membro é criado na tabela a SACL, **ENTRYID** não pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="c2384-116">After a member is created in the SACL table, the **ENTRYID** cannot be changed.</span></span> <span data-ttu-id="c2384-117">Para alterá-lo, você deve excluir o membro de tabela e recriá-la com um diferentes **ENTRYID**.</span><span class="sxs-lookup"><span data-stu-id="c2384-117">To change it, you must delete the table member and re-create it with a different **ENTRYID**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c2384-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c2384-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c2384-119">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c2384-119">Header files</span></span>

<span data-ttu-id="c2384-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c2384-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="c2384-121">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c2384-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="c2384-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c2384-122">Mapitags.h</span></span>
  
> <span data-ttu-id="c2384-123">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="c2384-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c2384-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2384-124">See also</span></span>



[<span data-ttu-id="c2384-125">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c2384-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c2384-126">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="c2384-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c2384-127">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="c2384-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c2384-128">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="c2384-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

