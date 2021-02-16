---
title: Propriedade canônica PidTagAccessControlListTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccess
api_type:
- HeaderDef
ms.assetid: 48667fda-ddc4-42ac-9231-761db0a4c1a9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9c71a2b806b810906c13ea4750e5491b1544f640
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424501"
---
# <a name="pidtagaccesscontrollisttable-canonical-property"></a><span data-ttu-id="74953-103">Propriedade canônica PidTagAccessControlListTable</span><span class="sxs-lookup"><span data-stu-id="74953-103">PidTagAccessControlListTable Canonical Property</span></span>

  
  
<span data-ttu-id="74953-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74953-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74953-105">Contém uma tabela que consiste em todas as listas de controle de acesso do sistema (SACL) aplicadas a uma pasta.</span><span class="sxs-lookup"><span data-stu-id="74953-105">Contains a table that consists of all the system access control lists (SACL) applied to a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="74953-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="74953-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="74953-107">PR_ACL_TABLE</span><span class="sxs-lookup"><span data-stu-id="74953-107">PR_ACL_TABLE</span></span>  <br/> |
|<span data-ttu-id="74953-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="74953-108">Identifier:</span></span>  <br/> |<span data-ttu-id="74953-109">0x3FE0</span><span class="sxs-lookup"><span data-stu-id="74953-109">0x3FE0</span></span>  <br/> |
|<span data-ttu-id="74953-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="74953-110">Data type:</span></span>  <br/> |<span data-ttu-id="74953-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="74953-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="74953-112">Área:</span><span class="sxs-lookup"><span data-stu-id="74953-112">Area:</span></span>  <br/> |<span data-ttu-id="74953-113">Controle de Acesso</span><span class="sxs-lookup"><span data-stu-id="74953-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="74953-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="74953-114">Remarks</span></span>

<span data-ttu-id="74953-115">Essa propriedade está presente em todos os objetos de pasta em um Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="74953-115">This property is present on all folder objects on an Exchange Server.</span></span> <span data-ttu-id="74953-116">Os valores incluídos nessa propriedade são usados para ler e modificar listas de controle de acesso (ACLs) em pastas.</span><span class="sxs-lookup"><span data-stu-id="74953-116">Values included in this property are used for reading and modifying access control lists (ACLs) on folders.</span></span> <span data-ttu-id="74953-117">Você pode usar o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) com o identificador de interface IID_IExchangeModifyTable para obter uma interface [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) para **a** tabela ACL em uma pasta.</span><span class="sxs-lookup"><span data-stu-id="74953-117">You can use the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with the **IID_IExchangeModifyTable** interface identifier to obtain an [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to the ACL table on a folder.</span></span> <span data-ttu-id="74953-118">Você pode usar essa interface para ler e modificar essas ACLs.</span><span class="sxs-lookup"><span data-stu-id="74953-118">You can use this interface to read and modify those ACLs.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="74953-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="74953-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="74953-120">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="74953-120">Header files</span></span>

<span data-ttu-id="74953-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="74953-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="74953-122">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="74953-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="74953-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="74953-123">Mapitags.h</span></span>
  
> <span data-ttu-id="74953-124">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="74953-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="74953-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="74953-125">See also</span></span>



[<span data-ttu-id="74953-126">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="74953-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="74953-127">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="74953-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="74953-128">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="74953-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="74953-129">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="74953-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

