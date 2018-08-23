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
ms.openlocfilehash: b685fd0ebe4a2d0bfcfd8aab3015602b84932db7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564938"
---
# <a name="pidtagaddressbookchoosedirectoryautomatically-canonical-property"></a><span data-ttu-id="e03eb-103">Propriedade canônica PidTagAddressBookChooseDirectoryAutomatically</span><span class="sxs-lookup"><span data-stu-id="e03eb-103">PidTagAddressBookChooseDirectoryAutomatically Canonical Property</span></span>

  
  
<span data-ttu-id="e03eb-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e03eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e03eb-105">Permite que o Microsoft Outlook 2010 e o Microsoft Outlook 2013 escolher a lista de endereços global (GAL) mais apropriada ou pasta de contatos para a caixa de correio atual.</span><span class="sxs-lookup"><span data-stu-id="e03eb-105">Enables Microsoft Outlook 2010 and Microsoft Outlook 2013 to choose the most appropriate global address list (GAL) or contact folder for the current mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e03eb-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="e03eb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e03eb-107">PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY</span><span class="sxs-lookup"><span data-stu-id="e03eb-107">PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY</span></span>  <br/> |
|<span data-ttu-id="e03eb-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e03eb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e03eb-109">0x3D1C000B</span><span class="sxs-lookup"><span data-stu-id="e03eb-109">0x3D1C000B</span></span>  <br/> |
|<span data-ttu-id="e03eb-110">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="e03eb-110">Property type:</span></span>  <br/> |<span data-ttu-id="e03eb-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="e03eb-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="e03eb-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e03eb-112">Area:</span></span>  <br/> |<span data-ttu-id="e03eb-113">Catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="e03eb-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e03eb-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e03eb-114">Remarks</span></span>

<span data-ttu-id="e03eb-115">Essa propriedade corresponde à configuração da **Escolha automaticamente** na caixa de diálogo Opções do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="e03eb-115">This property corresponds to the **Choose automatically** setting in the Address Book Options dialog.</span></span> <span data-ttu-id="e03eb-116">Quando essa propriedade existe na seção de perfil IID_CAPONE_PROF e estiver definida como **true**, o catálogo de endereços diálogo não mais padrões para o contêiner especificado pelo método [SetDefaultDir](iaddrbook-setdefaultdir.md) , mas escolhe um catálogo de endereços que o Outlook 2010 ou Outlook 2013 considera apropriada para o contexto no qual a caixa de diálogo foi exibida.</span><span class="sxs-lookup"><span data-stu-id="e03eb-116">When this property exists in the IID_CAPONE_PROF profile section and is set to **true**, the Address Book dialog no longer defaults to the container specified by the [SetDefaultDir](iaddrbook-setdefaultdir.md) method, but chooses an address book that Outlook 2010 or Outlook 2013 considers appropriate for the context in which the dialog was displayed.</span></span> <span data-ttu-id="e03eb-117">Observe que isso pode resultar em uma experiência ruim para provedores de catálogo de endereços de terceiros.</span><span class="sxs-lookup"><span data-stu-id="e03eb-117">Note that this may result in a poor experience for third-party address book providers.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e03eb-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e03eb-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e03eb-119">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e03eb-119">Header files</span></span>

<span data-ttu-id="e03eb-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e03eb-120">Mapitags.h</span></span>
  
> <span data-ttu-id="e03eb-121">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="e03eb-121">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="e03eb-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e03eb-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="e03eb-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e03eb-123">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e03eb-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="e03eb-124">See also</span></span>



[<span data-ttu-id="e03eb-125">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e03eb-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e03eb-126">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="e03eb-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e03eb-127">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="e03eb-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="e03eb-128">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="e03eb-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e03eb-129">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="e03eb-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

