---
title: Propriedade canônica PidTagIpmDraftsEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmDraftsEntryId
api_type:
- HeaderDef
ms.assetid: 17d64211-6265-41f4-b016-3677d75af966
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: be09b0f21017c81484fe538839e3bdd6137ff663
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582130"
---
# <a name="pidtagipmdraftsentryid-canonical-property"></a><span data-ttu-id="67e1c-103">Propriedade canônica PidTagIpmDraftsEntryId</span><span class="sxs-lookup"><span data-stu-id="67e1c-103">PidTagIpmDraftsEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="67e1c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="67e1c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="67e1c-105">Contém a **EntryID** da pasta Rascunhos do Outlook.</span><span class="sxs-lookup"><span data-stu-id="67e1c-105">Contains the **EntryID** of the Outlook Drafts folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="67e1c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="67e1c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="67e1c-107">PR_IPM_DRAFTS_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="67e1c-107">PR_IPM_DRAFTS_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="67e1c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="67e1c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="67e1c-109">0x36D7</span><span class="sxs-lookup"><span data-stu-id="67e1c-109">0x36D7</span></span>  <br/> |
|<span data-ttu-id="67e1c-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="67e1c-110">Data type:</span></span>  <br/> |<span data-ttu-id="67e1c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="67e1c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="67e1c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="67e1c-112">Area:</span></span>  <br/> |<span data-ttu-id="67e1c-113">Folder</span><span class="sxs-lookup"><span data-stu-id="67e1c-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="67e1c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="67e1c-114">Remarks</span></span>

<span data-ttu-id="67e1c-115">Essa propriedade é armazenada na pasta caixa de entrada, bem como a pasta raiz do armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="67e1c-115">This property is stored in the Inbox folder as well as the root folder of the message store.</span></span> <span data-ttu-id="67e1c-116">Para acessar a propriedade em um repositório de mensagem específicos, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="67e1c-116">To access the property on a specific message store, do the following:</span></span> 
  
1. <span data-ttu-id="67e1c-117">Em primeiro lugar, procure a propriedade na pasta caixa de entrada.</span><span class="sxs-lookup"><span data-stu-id="67e1c-117">First, look for the property in the Inbox folder.</span></span> <span data-ttu-id="67e1c-118">Use [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) para obter uma referência para a **EntryID** da pasta de caixa de entrada.</span><span class="sxs-lookup"><span data-stu-id="67e1c-118">Use [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to obtain a reference to the **EntryID** for the Inbox folder.</span></span> 
    
2. <span data-ttu-id="67e1c-119">Se **IMsgStore::GetReceiveFolder** for bem-sucedida, em seguida, use a referência a **EntryID** da caixa de entrada e [IMsgStore::OpenEntry](imsgstore-openentry.md) para abrir a caixa de entrada e obter uma referência a um objeto **IMAPIFolder** .</span><span class="sxs-lookup"><span data-stu-id="67e1c-119">If **IMsgStore::GetReceiveFolder** is successful, then use the reference to the **EntryID** of the Inbox and [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and obtain a reference to an **IMAPIFolder** object.</span></span> 
    
3. <span data-ttu-id="67e1c-120">Se **IMsgStore::OpenEntry** for bem-sucedida, em seguida, use a referência retornada ao objeto **IMAPIFolder** e [IMAPIProp::GetProps](imapiprop-getprops.md) para obter a propriedade desejada.</span><span class="sxs-lookup"><span data-stu-id="67e1c-120">If **IMsgStore::OpenEntry** is successful, then use the returned reference to the **IMAPIFolder** object and [IMAPIProp::GetProps](imapiprop-getprops.md) to obtain the desired property.</span></span> 
    
4. <span data-ttu-id="67e1c-121">Se a etapa 1, 2 ou 3 falhar, procure a propriedade na pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="67e1c-121">If Step 1, 2, or 3 fails, look for the property in the root folder.</span></span> <span data-ttu-id="67e1c-122">Para fazer isso, use **IMsgStore::OpenEntry**, especificando NULL para **lpEntryID**, para abrir a pasta raiz do armazenamento de mensagens e obter uma referência ao objeto **IMAPIFolder** .</span><span class="sxs-lookup"><span data-stu-id="67e1c-122">To do that, use **IMsgStore::OpenEntry**, specifying NULL for **lpEntryID**, to open the root folder of the message store and obtain a reference to the **IMAPIFolder** object.</span></span> 
    
5. <span data-ttu-id="67e1c-123">Se abrir a pasta raiz for bem-sucedida, em seguida, use a referência retornada ao objeto **IMAPIFolder** e **IMAPIProp::GetProps** para obter a propriedade desejada.</span><span class="sxs-lookup"><span data-stu-id="67e1c-123">If opening the root folder is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="67e1c-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="67e1c-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="67e1c-125">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="67e1c-125">Protocol specifications</span></span>

<span data-ttu-id="67e1c-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="67e1c-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="67e1c-127">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="67e1c-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="67e1c-128">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="67e1c-128">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="67e1c-129">Especifica as propriedades e operações para a criação e a localização de pastas especiais em uma caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="67e1c-129">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="67e1c-130">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="67e1c-130">Header files</span></span>

<span data-ttu-id="67e1c-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="67e1c-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="67e1c-132">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="67e1c-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="67e1c-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="67e1c-133">Mapitags.h</span></span>
  
> <span data-ttu-id="67e1c-134">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="67e1c-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="67e1c-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="67e1c-135">See also</span></span>



[<span data-ttu-id="67e1c-136">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="67e1c-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="67e1c-137">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="67e1c-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="67e1c-138">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="67e1c-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="67e1c-139">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="67e1c-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

