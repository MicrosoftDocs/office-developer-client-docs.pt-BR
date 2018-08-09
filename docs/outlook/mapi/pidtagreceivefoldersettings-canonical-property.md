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
ms.openlocfilehash: e93325873f1d9e89bb591d136df04aa27403375f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769770"
---
# <a name="pidtagreceivefoldersettings-canonical-property"></a><span data-ttu-id="02f93-103">Propriedade canônica PidTagReceiveFolderSettings</span><span class="sxs-lookup"><span data-stu-id="02f93-103">PidTagReceiveFolderSettings Canonical Property</span></span>

  
  
<span data-ttu-id="02f93-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="02f93-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="02f93-105">Contém uma tabela de uma mensagem repositório receberão as configurações de pasta.</span><span class="sxs-lookup"><span data-stu-id="02f93-105">Contains a table of a message store's receive folder settings.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="02f93-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="02f93-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="02f93-107">PR_RECEIVE_FOLDER_SETTINGS</span><span class="sxs-lookup"><span data-stu-id="02f93-107">PR_RECEIVE_FOLDER_SETTINGS</span></span>  <br/> |
|<span data-ttu-id="02f93-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="02f93-108">Identifier:</span></span>  <br/> |<span data-ttu-id="02f93-109">0x3415</span><span class="sxs-lookup"><span data-stu-id="02f93-109">0x3415</span></span>  <br/> |
|<span data-ttu-id="02f93-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="02f93-110">Data type:</span></span>  <br/> |<span data-ttu-id="02f93-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="02f93-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="02f93-112">Área:</span><span class="sxs-lookup"><span data-stu-id="02f93-112">Area:</span></span>  <br/> |<span data-ttu-id="02f93-113">Armazenamento de mensagens MAPI</span><span class="sxs-lookup"><span data-stu-id="02f93-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02f93-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="02f93-114">Remarks</span></span>

<span data-ttu-id="02f93-115">Essa propriedade pode ser excluída em operações [IMAPIProp::CopyTo](imapiprop-copyto.md) ou incluída nas operações da [IMAPIProp::CopyProps](imapiprop-copyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="02f93-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="02f93-116">Como uma propriedade do tipo PT_OBJECT, ele não pode ser recuperado com êxito pelo método [IMAPIProp::GetProps](imapiprop-getprops.md) ; seu conteúdo deve ser acessado pelo método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , solicitando a interface com o identificador IID_IMAPITable.</span><span class="sxs-lookup"><span data-stu-id="02f93-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the interface with identifier IID_IMAPITable.</span></span> <span data-ttu-id="02f93-117">Provedores de serviços devem relatá-la para o método [IMAPIProp::GetPropList](imapiprop-getproplist.md) se ele estiver definido, mas pode, opcionalmente, relatá-la ou não se não estiver definida.</span><span class="sxs-lookup"><span data-stu-id="02f93-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="02f93-118">Para recuperar o conteúdo da tabela, um aplicativo cliente deve chamar o método [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) .</span><span class="sxs-lookup"><span data-stu-id="02f93-118">To retrieve table contents, a client application should call the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> <span data-ttu-id="02f93-119">Para obter mais informações, consulte as [Tabelas de pasta de recebimento](receive-folder-tables.md).</span><span class="sxs-lookup"><span data-stu-id="02f93-119">For more information, see [Receive Folder Tables](receive-folder-tables.md).</span></span>
  
<span data-ttu-id="02f93-120">Essa propriedade contém uma tabela de mapeamento das pastas de recebimento para o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="02f93-120">This property contains a table of mappings of the receive folders for the message store.</span></span> <span data-ttu-id="02f93-121">Chamar **OpenProperty** sobre esta propriedade é equivalente a chamar **GetReceiveFolderTable** no armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="02f93-121">Calling **OpenProperty** on this property is equivalent to calling **GetReceiveFolderTable** on the message store.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="02f93-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="02f93-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="02f93-123">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="02f93-123">Header files</span></span>

<span data-ttu-id="02f93-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="02f93-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="02f93-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="02f93-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="02f93-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="02f93-126">Mapitags.h</span></span>
  
> <span data-ttu-id="02f93-127">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="02f93-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="02f93-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="02f93-128">See also</span></span>



[<span data-ttu-id="02f93-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="02f93-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="02f93-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="02f93-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="02f93-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="02f93-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="02f93-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="02f93-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

