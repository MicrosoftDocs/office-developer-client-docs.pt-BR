---
title: Propriedade canônica PidTagAddressBookChooseDirectoryAutomatically
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cecd0679-4bc2-4399-8f89-a4e17bb909a0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 41fdaf333084b7d567f4e67ae9fd2638a1731349
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359784"
---
# <a name="pidtagaddressbookchoosedirectoryautomatically-canonical-property"></a><span data-ttu-id="13278-103">Propriedade canônica PidTagAddressBookChooseDirectoryAutomatically</span><span class="sxs-lookup"><span data-stu-id="13278-103">PidTagAddressBookChooseDirectoryAutomatically Canonical Property</span></span>

  
  
<span data-ttu-id="13278-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13278-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13278-105">Permite que o Microsoft Outlook 2010 e o Microsoft Outlook 2013 escolha a lista de endereços global (GAL) ou a pasta de contatos mais apropriada para a caixa de correio atual.</span><span class="sxs-lookup"><span data-stu-id="13278-105">Enables Microsoft Outlook 2010 and Microsoft Outlook 2013 to choose the most appropriate global address list (GAL) or contact folder for the current mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="13278-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="13278-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="13278-107">PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY</span><span class="sxs-lookup"><span data-stu-id="13278-107">PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY</span></span>  <br/> |
|<span data-ttu-id="13278-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="13278-108">Identifier:</span></span>  <br/> |<span data-ttu-id="13278-109">0x3D1C000B</span><span class="sxs-lookup"><span data-stu-id="13278-109">0x3D1C000B</span></span>  <br/> |
|<span data-ttu-id="13278-110">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="13278-110">Property type:</span></span>  <br/> |<span data-ttu-id="13278-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="13278-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="13278-112">Área:</span><span class="sxs-lookup"><span data-stu-id="13278-112">Area:</span></span>  <br/> |<span data-ttu-id="13278-113">Catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="13278-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13278-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="13278-114">Remarks</span></span>

<span data-ttu-id="13278-115">Essa propriedade corresponde à opção **escolher automaticamente** na caixa de diálogo opções do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="13278-115">This property corresponds to the **Choose automatically** setting in the Address Book Options dialog.</span></span> <span data-ttu-id="13278-116">Quando essa propriedade existe na seção perfil do IID_CAPONE_PROF e é definida como **true**, a caixa de diálogo catálogo de endereços não é mais padrão para o contêiner especificado pelo método [SetDefaultDir](iaddrbook-setdefaultdir.md) , mas escolhe um catálogo de endereços que o Outlook 2010 ou o Outlook 2013 considera apropriado para o contexto no qual a caixa de diálogo foi exibida.</span><span class="sxs-lookup"><span data-stu-id="13278-116">When this property exists in the IID_CAPONE_PROF profile section and is set to **true**, the Address Book dialog no longer defaults to the container specified by the [SetDefaultDir](iaddrbook-setdefaultdir.md) method, but chooses an address book that Outlook 2010 or Outlook 2013 considers appropriate for the context in which the dialog was displayed.</span></span> <span data-ttu-id="13278-117">Observe que isso pode resultar em uma experiência ruim para provedores de catálogos de endereços de terceiros.</span><span class="sxs-lookup"><span data-stu-id="13278-117">Note that this may result in a poor experience for third-party address book providers.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="13278-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="13278-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="13278-119">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="13278-119">Header files</span></span>

<span data-ttu-id="13278-120">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="13278-120">Mapitags.h</span></span>
  
> <span data-ttu-id="13278-121">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="13278-121">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="13278-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="13278-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="13278-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="13278-123">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="13278-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="13278-124">See also</span></span>



[<span data-ttu-id="13278-125">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="13278-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="13278-126">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="13278-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="13278-127">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="13278-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="13278-128">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="13278-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="13278-129">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="13278-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

