---
title: Propriedade canônica PidTagIpmContactEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmContactEntryId
api_type:
- HeaderDef
ms.assetid: fccbbb15-dd08-4310-83d7-bf57eb3ed5de
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8f0c79fa098b8bca0518921a25d88a229e23e955
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391126"
---
# <a name="pidtagipmcontactentryid-canonical-property"></a><span data-ttu-id="57356-103">Propriedade canônica PidTagIpmContactEntryId</span><span class="sxs-lookup"><span data-stu-id="57356-103">PidTagIpmContactEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="57356-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57356-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57356-105">Contém a **EntryID** da pasta Contatos do Outlook.</span><span class="sxs-lookup"><span data-stu-id="57356-105">Contains the **EntryID** of the Outlook Contacts folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="57356-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="57356-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="57356-107">PR_IPM_CONTACT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="57356-107">PR_IPM_CONTACT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="57356-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="57356-108">Identifier:</span></span>  <br/> |<span data-ttu-id="57356-109">0x36D1</span><span class="sxs-lookup"><span data-stu-id="57356-109">0x36D1</span></span>  <br/> |
|<span data-ttu-id="57356-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="57356-110">Data type:</span></span>  <br/> |<span data-ttu-id="57356-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="57356-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="57356-112">Área:</span><span class="sxs-lookup"><span data-stu-id="57356-112">Area:</span></span>  <br/> |<span data-ttu-id="57356-113">Folder</span><span class="sxs-lookup"><span data-stu-id="57356-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="57356-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="57356-114">Remarks</span></span>

<span data-ttu-id="57356-115">Essa propriedade é armazenada na pasta caixa de entrada e na pasta raiz do repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="57356-115">This property is stored in the Inbox folder and in the root folder of the message store.</span></span> <span data-ttu-id="57356-116">Para acessar a propriedade em um repositório de mensagem específicos, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="57356-116">To access the property on a specific message store, do the following:</span></span> 
  
1. <span data-ttu-id="57356-117">Em primeiro lugar, procure a propriedade na pasta caixa de entrada.</span><span class="sxs-lookup"><span data-stu-id="57356-117">First, look for the property in the Inbox folder.</span></span> <span data-ttu-id="57356-118">Use **IMsgStore::GetReceiveFolder** para obter uma referência para a **EntryID** da pasta de caixa de entrada.</span><span class="sxs-lookup"><span data-stu-id="57356-118">Use **IMsgStore::GetReceiveFolder** to obtain a reference to the **EntryID** for the Inbox folder.</span></span> 
    
2. <span data-ttu-id="57356-119">Se **IMsgStore::GetReceiveFolder** for bem-sucedida, em seguida, use a referência a **EntryID** da caixa de entrada e **IMsgStore::OpenEntry** para abrir a caixa de entrada e obter uma referência a um objeto **IMAPIFolder** .</span><span class="sxs-lookup"><span data-stu-id="57356-119">If **IMsgStore::GetReceiveFolder** is successful, then use the reference to the **EntryID** of the Inbox and **IMsgStore::OpenEntry** to open the Inbox and obtain a reference to an **IMAPIFolder** object.</span></span> 
    
3. <span data-ttu-id="57356-120">Se **IMsgStore::OpenEntry** for bem-sucedida, em seguida, use a referência retornada ao objeto **IMAPIFolder** e **IMAPIProp::GetProps** para obter a propriedade desejada.</span><span class="sxs-lookup"><span data-stu-id="57356-120">If **IMsgStore::OpenEntry** is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
4. <span data-ttu-id="57356-121">Se a etapa 1, 2 ou 3 falhar, procure a propriedade na pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="57356-121">If Step 1, 2, or 3 fails, look for the property in the root folder.</span></span> <span data-ttu-id="57356-122">Para fazer isso, use **IMsgStore::OpenEntry**, especificando nulo para \* \* lpEntryID \* \*, para abrir a pasta raiz do armazenamento de mensagens e obter uma referência ao objeto **IMAPIFolder** .</span><span class="sxs-lookup"><span data-stu-id="57356-122">To do that, use **IMsgStore::OpenEntry**, specifying NULL for \*\* lpEntryID \*\*, to open the root folder of the message store and obtain a reference to the **IMAPIFolder** object.</span></span> 
    
5. <span data-ttu-id="57356-123">Se abrir a pasta raiz for bem-sucedida, em seguida, use a referência retornada ao objeto **IMAPIFolder** e **IMAPIProp::GetProps** para obter a propriedade desejada.</span><span class="sxs-lookup"><span data-stu-id="57356-123">If opening the root folder is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="57356-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="57356-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="57356-125">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="57356-125">Protocol specifications</span></span>

<span data-ttu-id="57356-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="57356-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="57356-127">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="57356-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="57356-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="57356-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="57356-129">Especifica as propriedades e operações para a criação e a localização de pastas especiais em uma caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="57356-129">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="57356-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="57356-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="57356-131">Especifica os métodos para conexão e a configuração de caixas de correio conforme representantes e as interações com objetos de mensagem e o calendário quando eles ajam em nome de outro usuário.</span><span class="sxs-lookup"><span data-stu-id="57356-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="57356-132">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="57356-132">Header files</span></span>

<span data-ttu-id="57356-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="57356-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="57356-134">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="57356-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="57356-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="57356-135">Mapitags.h</span></span>
  
> <span data-ttu-id="57356-136">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="57356-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="57356-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="57356-137">See also</span></span>



[<span data-ttu-id="57356-138">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="57356-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="57356-139">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="57356-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="57356-140">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="57356-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="57356-141">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="57356-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

