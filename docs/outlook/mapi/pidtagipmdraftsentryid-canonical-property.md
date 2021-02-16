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
ms.openlocfilehash: e259c86803147d782469c8d86b23694d8b54e69d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327885"
---
# <a name="pidtagipmdraftsentryid-canonical-property"></a><span data-ttu-id="a5355-103">Propriedade canônica PidTagIpmDraftsEntryId</span><span class="sxs-lookup"><span data-stu-id="a5355-103">PidTagIpmDraftsEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="a5355-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5355-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5355-105">Contém a **EntryID** da pasta Rascunhos do Outlook.</span><span class="sxs-lookup"><span data-stu-id="a5355-105">Contains the **EntryID** of the Outlook Drafts folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a5355-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a5355-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a5355-107">PR_IPM_DRAFTS_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="a5355-107">PR_IPM_DRAFTS_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="a5355-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a5355-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a5355-109">0x36D7</span><span class="sxs-lookup"><span data-stu-id="a5355-109">0x36D7</span></span>  <br/> |
|<span data-ttu-id="a5355-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a5355-110">Data type:</span></span>  <br/> |<span data-ttu-id="a5355-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a5355-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a5355-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a5355-112">Area:</span></span>  <br/> |<span data-ttu-id="a5355-113">Folder</span><span class="sxs-lookup"><span data-stu-id="a5355-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a5355-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5355-114">Remarks</span></span>

<span data-ttu-id="a5355-115">Essa propriedade é armazenada na pasta Caixa de Entrada, bem como na pasta raiz do armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a5355-115">This property is stored in the Inbox folder as well as the root folder of the message store.</span></span> <span data-ttu-id="a5355-116">Para acessar a propriedade em um armazenamento de mensagens específico, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a5355-116">To access the property on a specific message store, do the following:</span></span> 
  
1. <span data-ttu-id="a5355-117">Primeiro, procure a propriedade na pasta Caixa de Entrada.</span><span class="sxs-lookup"><span data-stu-id="a5355-117">First, look for the property in the Inbox folder.</span></span> <span data-ttu-id="a5355-118">Use [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) para obter uma referência para **a EntryID** da pasta Caixa de Entrada.</span><span class="sxs-lookup"><span data-stu-id="a5355-118">Use [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to obtain a reference to the **EntryID** for the Inbox folder.</span></span> 
    
2. <span data-ttu-id="a5355-119">Se **IMsgStore::GetReceiveFolder** for bem-sucedida, use a referência para **EntryID** da Caixa de Entrada e [IMsgStore::OpenEntry](imsgstore-openentry.md) para abrir a Caixa de Entrada e obter uma referência a um objeto **IMAPIFolder.**</span><span class="sxs-lookup"><span data-stu-id="a5355-119">If **IMsgStore::GetReceiveFolder** is successful, then use the reference to the **EntryID** of the Inbox and [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and obtain a reference to an **IMAPIFolder** object.</span></span> 
    
3. <span data-ttu-id="a5355-120">Se **IMsgStore::OpenEntry** for bem-sucedida, use a referência retornada para o objeto **IMAPIFolder** e [IMAPIProp::GetProps](imapiprop-getprops.md) para obter a propriedade desejada.</span><span class="sxs-lookup"><span data-stu-id="a5355-120">If **IMsgStore::OpenEntry** is successful, then use the returned reference to the **IMAPIFolder** object and [IMAPIProp::GetProps](imapiprop-getprops.md) to obtain the desired property.</span></span> 
    
4. <span data-ttu-id="a5355-121">Se a etapa 1, 2 ou 3 falhar, procure a propriedade na pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="a5355-121">If Step 1, 2, or 3 fails, look for the property in the root folder.</span></span> <span data-ttu-id="a5355-122">Para fazer isso, use **IMsgStore::OpenEntry**, especificando NULL para **lpEntryID**, para abrir a pasta raiz do repositório de mensagens e obter uma referência para o objeto **IMAPIFolder** .</span><span class="sxs-lookup"><span data-stu-id="a5355-122">To do that, use **IMsgStore::OpenEntry**, specifying NULL for **lpEntryID**, to open the root folder of the message store and obtain a reference to the **IMAPIFolder** object.</span></span> 
    
5. <span data-ttu-id="a5355-123">Se a abertura da pasta raiz for bem-sucedida, use a referência retornada para o objeto **IMAPIFolder** e **IMAPIProp::GetProps** para obter a propriedade desejada.</span><span class="sxs-lookup"><span data-stu-id="a5355-123">If opening the root folder is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="a5355-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a5355-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a5355-125">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="a5355-125">Protocol specifications</span></span>

<span data-ttu-id="a5355-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5355-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5355-127">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a5355-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a5355-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5355-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5355-129">Especifica as propriedades e operações para criar e localizar as pastas especiais em uma caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="a5355-129">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a5355-130">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="a5355-130">Header files</span></span>

<span data-ttu-id="a5355-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a5355-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="a5355-132">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a5355-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="a5355-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a5355-133">Mapitags.h</span></span>
  
> <span data-ttu-id="a5355-134">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="a5355-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a5355-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5355-135">See also</span></span>



[<span data-ttu-id="a5355-136">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a5355-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a5355-137">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="a5355-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a5355-138">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a5355-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a5355-139">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="a5355-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

