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
ms.openlocfilehash: 83a645b49e5bb48051bbaedb26058d2da053348b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342494"
---
# <a name="pidtagmemberentryid-canonical-property"></a><span data-ttu-id="f42be-103">Propriedade canônica PidTagMemberEntryId</span><span class="sxs-lookup"><span data-stu-id="f42be-103">PidTagMemberEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="f42be-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f42be-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f42be-105">Contém o identificador de entrada de objeto de diretório de um membro da tabela SACL (lista de controle de acesso do sistema).</span><span class="sxs-lookup"><span data-stu-id="f42be-105">Contains the directory object entry identifier of a system access control list (SACL) table member.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f42be-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="f42be-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f42be-107">PR_MEMBER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="f42be-107">PR_MEMBER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="f42be-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f42be-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f42be-109">0x0FFF</span><span class="sxs-lookup"><span data-stu-id="f42be-109">0x0FFF</span></span>  <br/> |
|<span data-ttu-id="f42be-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="f42be-110">Data type:</span></span>  <br/> |<span data-ttu-id="f42be-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f42be-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f42be-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f42be-112">Area:</span></span>  <br/> |<span data-ttu-id="f42be-113">Regras no servidor</span><span class="sxs-lookup"><span data-stu-id="f42be-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f42be-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f42be-114">Remarks</span></span>

<span data-ttu-id="f42be-115">Essa propriedade é usada pela interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) para identificar exclusivamente uma pessoa ou função à qual a SACL se aplica.</span><span class="sxs-lookup"><span data-stu-id="f42be-115">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to uniquely identify a person or role to whom the SACL applies.</span></span> <span data-ttu-id="f42be-116">Depois que um membro é criado na tabela SACL, a **EntryID** não pode ser alterada.</span><span class="sxs-lookup"><span data-stu-id="f42be-116">After a member is created in the SACL table, the **ENTRYID** cannot be changed.</span></span> <span data-ttu-id="f42be-117">Para alterá-la, você deve excluir o membro da tabela e recriá-lo \*\*\*\* com outra EntryID.</span><span class="sxs-lookup"><span data-stu-id="f42be-117">To change it, you must delete the table member and re-create it with a different **ENTRYID**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f42be-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f42be-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f42be-119">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f42be-119">Header files</span></span>

<span data-ttu-id="f42be-120">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f42be-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="f42be-121">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="f42be-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="f42be-122">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="f42be-122">Mapitags.h</span></span>
  
> <span data-ttu-id="f42be-123">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="f42be-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f42be-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="f42be-124">See also</span></span>



[<span data-ttu-id="f42be-125">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f42be-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f42be-126">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="f42be-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f42be-127">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="f42be-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f42be-128">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="f42be-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

