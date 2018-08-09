---
title: Propriedade canônica PidTagRemindersOnlineEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemindersOnlineEntryId
api_type:
- COM
ms.assetid: cad25cca-248d-4845-9d60-7aa60f2dda62
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cba8de706e7262ff59abdb6367fb505a2303dcf3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769801"
---
# <a name="pidtagremindersonlineentryid-canonical-property"></a><span data-ttu-id="61718-103">Propriedade canônica PidTagRemindersOnlineEntryId</span><span class="sxs-lookup"><span data-stu-id="61718-103">PidTagRemindersOnlineEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="61718-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="61718-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="61718-105">Contém a **EntryID** da pasta lembretes.</span><span class="sxs-lookup"><span data-stu-id="61718-105">Contains the **EntryID** of the reminders folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="61718-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="61718-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="61718-107">PR_REM_ONLINE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="61718-107">PR_REM_ONLINE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="61718-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="61718-108">Identifier:</span></span>  <br/> |<span data-ttu-id="61718-109">0x36D5</span><span class="sxs-lookup"><span data-stu-id="61718-109">0x36D5</span></span>  <br/> |
|<span data-ttu-id="61718-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="61718-110">Data type:</span></span>  <br/> |<span data-ttu-id="61718-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="61718-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="61718-112">Área:</span><span class="sxs-lookup"><span data-stu-id="61718-112">Area:</span></span>  <br/> |<span data-ttu-id="61718-113">Contêiner MAPI</span><span class="sxs-lookup"><span data-stu-id="61718-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61718-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="61718-114">Remarks</span></span>

<span data-ttu-id="61718-115">Essa propriedade é armazenada na pasta caixa de entrada e na pasta raiz do repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="61718-115">This property is stored in the Inbox folder and in the root folder of the message store.</span></span> <span data-ttu-id="61718-116">Para acessar a propriedade em um repositório de mensagem específicos, faça o seguinte.</span><span class="sxs-lookup"><span data-stu-id="61718-116">To access the property on a specific message store, do the following.</span></span> 
  
1. <span data-ttu-id="61718-117">Em primeiro lugar, procure a propriedade na pasta caixa de entrada.</span><span class="sxs-lookup"><span data-stu-id="61718-117">First, look for the property in the Inbox folder.</span></span> <span data-ttu-id="61718-118">Use [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) para obter uma referência para a **EntryID** da pasta de caixa de entrada.</span><span class="sxs-lookup"><span data-stu-id="61718-118">Use [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to obtain a reference to the **EntryID** for the Inbox folder.</span></span> 
    
2. <span data-ttu-id="61718-119">Se **IMsgStore::GetReceiveFolder** for bem-sucedida, em seguida, use a referência a **EntryID** da caixa de entrada e [IMsgStore::OpenEntry](imsgstore-openentry.md) para abrir a caixa de entrada e obter uma referência a um objeto **IMAPIFolder** .</span><span class="sxs-lookup"><span data-stu-id="61718-119">If **IMsgStore::GetReceiveFolder** is successful, then use the reference to the **EntryID** of the Inbox and [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and obtain a reference to an **IMAPIFolder** object.</span></span> 
    
3. <span data-ttu-id="61718-120">Se **IMsgStore::OpenEntry** for bem-sucedida, em seguida, use a referência retornada ao objeto **IMAPIFolder** e [IMAPIProp::GetProps](imapiprop-getprops.md) para obter a propriedade desejada.</span><span class="sxs-lookup"><span data-stu-id="61718-120">If **IMsgStore::OpenEntry** is successful, then use the returned reference to the **IMAPIFolder** object and [IMAPIProp::GetProps](imapiprop-getprops.md) to obtain the desired property.</span></span> 
    
4. <span data-ttu-id="61718-121">Se a etapa 1, 2 ou 3 falhar, procure a propriedade na pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="61718-121">If Step 1, 2, or 3 fails, look for the property in the root folder.</span></span> <span data-ttu-id="61718-122">Para fazer isso, use **IMsgStore::OpenEntry**, especificando NULL para **lpEntryID**, para abrir a pasta raiz do armazenamento de mensagens e obter uma referência ao objeto **IMAPIFolder** .</span><span class="sxs-lookup"><span data-stu-id="61718-122">To do that, use **IMsgStore::OpenEntry**, specifying NULL for **lpEntryID**, to open the root folder of the message store and obtain a reference to the **IMAPIFolder** object.</span></span> 
    
5. <span data-ttu-id="61718-123">Se abrir a pasta raiz for bem-sucedida, em seguida, use a referência retornada ao objeto **IMAPIFolder** e **IMAPIProp::GetProps** para obter a propriedade desejada.</span><span class="sxs-lookup"><span data-stu-id="61718-123">If opening the root folder is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="61718-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="61718-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="61718-125">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="61718-125">Protocol specifications</span></span>

<span data-ttu-id="61718-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="61718-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="61718-127">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="61718-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="61718-128">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="61718-128">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="61718-129">Especifica as propriedades e operações para a criação e a localização de pastas especiais em uma caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="61718-129">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="61718-130">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="61718-130">Header files</span></span>

<span data-ttu-id="61718-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="61718-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="61718-132">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="61718-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="61718-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="61718-133">Mapitags.h</span></span>
  
> <span data-ttu-id="61718-134">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="61718-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="61718-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="61718-135">See also</span></span>



[<span data-ttu-id="61718-136">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="61718-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="61718-137">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="61718-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="61718-138">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="61718-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="61718-139">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="61718-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

