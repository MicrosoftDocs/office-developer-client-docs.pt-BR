---
title: Propriedade canônica PidTagReceiveFolderSettings
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceiveFolderSettings
api_type:
- COM
ms.assetid: 2f0b1679-05b0-4580-b6d2-474fe3f9d012
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8590e357252089aaa49a71d443037b9b9ed77ee4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415051"
---
# <a name="pidtagreceivefoldersettings-canonical-property"></a><span data-ttu-id="7927a-103">Propriedade canônica PidTagReceiveFolderSettings</span><span class="sxs-lookup"><span data-stu-id="7927a-103">PidTagReceiveFolderSettings Canonical Property</span></span>

  
  
<span data-ttu-id="7927a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7927a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7927a-105">Contém uma tabela de configurações de pasta de recebimento de um armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="7927a-105">Contains a table of a message store's receive folder settings.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7927a-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="7927a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7927a-107">PR_RECEIVE_FOLDER_SETTINGS</span><span class="sxs-lookup"><span data-stu-id="7927a-107">PR_RECEIVE_FOLDER_SETTINGS</span></span>  <br/> |
|<span data-ttu-id="7927a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7927a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7927a-109">0x3415</span><span class="sxs-lookup"><span data-stu-id="7927a-109">0x3415</span></span>  <br/> |
|<span data-ttu-id="7927a-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="7927a-110">Data type:</span></span>  <br/> |<span data-ttu-id="7927a-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="7927a-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="7927a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7927a-112">Area:</span></span>  <br/> |<span data-ttu-id="7927a-113">Armazenamento de mensagens MAPI</span><span class="sxs-lookup"><span data-stu-id="7927a-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7927a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7927a-114">Remarks</span></span>

<span data-ttu-id="7927a-115">Essa propriedade pode ser excluída nas [operações IMAPIProp::CopyTo](imapiprop-copyto.md) ou incluída nas operações [IMAPIProp::CopyProps.](imapiprop-copyprops.md)</span><span class="sxs-lookup"><span data-stu-id="7927a-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="7927a-116">Como uma propriedade do tipo PT_OBJECT, ela não pode ser recuperada com êxito pelo método [IMAPIProp::GetProps;](imapiprop-getprops.md) seu conteúdo deve ser acessado pelo [método IMAPIProp::OpenProperty,](imapiprop-openproperty.md) solicitando a interface com identificador IID_IMAPITable.</span><span class="sxs-lookup"><span data-stu-id="7927a-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the interface with identifier IID_IMAPITable.</span></span> <span data-ttu-id="7927a-117">Os provedores de serviços devem reportá-lo para o método [IMAPIProp::GetPropList](imapiprop-getproplist.md) se ele estiver definido, mas, opcionalmente, pode reportá-lo ou não se ele não estiver definido.</span><span class="sxs-lookup"><span data-stu-id="7927a-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="7927a-118">Para recuperar o conteúdo da tabela, um aplicativo cliente deve chamar o método [IMsgStore::GetReceiveFolderTable.](imsgstore-getreceivefoldertable.md)</span><span class="sxs-lookup"><span data-stu-id="7927a-118">To retrieve table contents, a client application should call the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> <span data-ttu-id="7927a-119">Para obter mais informações, consulte [Tabelas de Pastas de Recebimento.](receive-folder-tables.md)</span><span class="sxs-lookup"><span data-stu-id="7927a-119">For more information, see [Receive Folder Tables](receive-folder-tables.md).</span></span>
  
<span data-ttu-id="7927a-120">Essa propriedade contém uma tabela de mapeamentos das pastas de recebimento para o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="7927a-120">This property contains a table of mappings of the receive folders for the message store.</span></span> <span data-ttu-id="7927a-121">Chamar **OpenProperty** nessa propriedade é equivalente a chamar **GetReceiveFolderTable** no armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="7927a-121">Calling **OpenProperty** on this property is equivalent to calling **GetReceiveFolderTable** on the message store.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7927a-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7927a-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7927a-123">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="7927a-123">Header files</span></span>

<span data-ttu-id="7927a-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7927a-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="7927a-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="7927a-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="7927a-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7927a-126">Mapitags.h</span></span>
  
> <span data-ttu-id="7927a-127">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="7927a-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7927a-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="7927a-128">See also</span></span>



[<span data-ttu-id="7927a-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7927a-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7927a-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="7927a-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7927a-131">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="7927a-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7927a-132">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="7927a-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

