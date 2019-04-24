---
title: Propriedade canônica PidTagIpmAppointmentEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmAppointmentEntryId
api_type:
- HeaderDef
ms.assetid: a6e8c8fb-b76a-4a73-b112-6399e4d94233
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d27506edf6eb40f6b244733336b8b381ea941442
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327913"
---
# <a name="pidtagipmappointmententryid-canonical-property"></a><span data-ttu-id="0ea00-103">Propriedade canônica PidTagIpmAppointmentEntryId</span><span class="sxs-lookup"><span data-stu-id="0ea00-103">PidTagIpmAppointmentEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="0ea00-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ea00-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ea00-105">Contém a **EntryID** da pasta de calendário do Outlook.</span><span class="sxs-lookup"><span data-stu-id="0ea00-105">Contains the **EntryID** of the Outlook Calendar folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0ea00-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="0ea00-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0ea00-107">PR_IPM_APPOINTMENT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="0ea00-107">PR_IPM_APPOINTMENT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="0ea00-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0ea00-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0ea00-109">0x36D0</span><span class="sxs-lookup"><span data-stu-id="0ea00-109">0x36D0</span></span>  <br/> |
|<span data-ttu-id="0ea00-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="0ea00-110">Data type:</span></span>  <br/> |<span data-ttu-id="0ea00-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0ea00-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0ea00-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0ea00-112">Area:</span></span>  <br/> |<span data-ttu-id="0ea00-113">Pasta</span><span class="sxs-lookup"><span data-stu-id="0ea00-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0ea00-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0ea00-114">Remarks</span></span>

<span data-ttu-id="0ea00-115">Essa propriedade é armazenada na pasta caixa de entrada e na pasta raiz do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="0ea00-115">This property is stored in the Inbox folder and in the root folder of the message store.</span></span> <span data-ttu-id="0ea00-116">Para acessar a propriedade em um repositório de mensagens específico, faça o seguinte.</span><span class="sxs-lookup"><span data-stu-id="0ea00-116">To access the property on a specific message store, do the following.</span></span> 
  
1. <span data-ttu-id="0ea00-117">Primeiro, procure a propriedade na pasta caixa de entrada.</span><span class="sxs-lookup"><span data-stu-id="0ea00-117">First, look for the property in the Inbox folder.</span></span> <span data-ttu-id="0ea00-118">Use [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md) para obter uma referência para a **EntryID** da pasta caixa de entrada.</span><span class="sxs-lookup"><span data-stu-id="0ea00-118">Use [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to obtain a reference to the **EntryID** for the Inbox folder.</span></span> 
    
2. <span data-ttu-id="0ea00-119">Se **IMsgStore:: GetReceiveFolder** for bem-sucedido, use a referência para a **EntryID** da caixa de entrada e [IMsgStore:: OpenEntry](imsgstore-openentry.md) para abrir a caixa de entrada e obter uma referência a um objeto **IMAPIFolder** .</span><span class="sxs-lookup"><span data-stu-id="0ea00-119">If **IMsgStore::GetReceiveFolder** is successful, then use the reference to the **EntryID** of the Inbox and [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and obtain a reference to an **IMAPIFolder** object.</span></span> 
    
3. <span data-ttu-id="0ea00-120">Se **IMsgStore:: OpenEntry** for bem-sucedido, use a referência retornada para o objeto **IMAPIFolder** e [IMAPIProp::](imapiprop-getprops.md) GetProps para obter a propriedade desejada.</span><span class="sxs-lookup"><span data-stu-id="0ea00-120">If **IMsgStore::OpenEntry** is successful, then use the returned reference to the **IMAPIFolder** object and [IMAPIProp::GetProps](imapiprop-getprops.md) to obtain the desired property.</span></span> 
    
4. <span data-ttu-id="0ea00-121">Se a etapa 1, 2 ou 3 falhar, procure a propriedade na pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="0ea00-121">If Step 1, 2, or 3 fails, look for the property in the root folder.</span></span> <span data-ttu-id="0ea00-122">Para fazer isso, use **IMsgStore:: OpenEntry**, especificando NULL para **lpEntryID**, para abrir a pasta raiz do repositório de mensagens e obter uma referência ao objeto **IMAPIFolder** .</span><span class="sxs-lookup"><span data-stu-id="0ea00-122">To do that, use **IMsgStore::OpenEntry**, specifying NULL for **lpEntryID**, to open the root folder of the message store and obtain a reference to the **IMAPIFolder** object.</span></span> 
    
5. <span data-ttu-id="0ea00-123">Se a abertura da pasta raiz for bem-sucedida, use a referência retornada ao objeto **IMAPIFolder** e **IMAPIProp::** GetProps para obter a propriedade desejada.</span><span class="sxs-lookup"><span data-stu-id="0ea00-123">If opening the root folder is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="0ea00-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0ea00-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0ea00-125">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="0ea00-125">Protocol specifications</span></span>

<span data-ttu-id="0ea00-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ea00-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ea00-127">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0ea00-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0ea00-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ea00-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ea00-129">Especifica as propriedades e operações para criar e localizar as pastas especiais em uma caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="0ea00-129">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0ea00-130">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0ea00-130">Header files</span></span>

<span data-ttu-id="0ea00-131">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="0ea00-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="0ea00-132">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="0ea00-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="0ea00-133">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="0ea00-133">Mapitags.h</span></span>
  
> <span data-ttu-id="0ea00-134">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="0ea00-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0ea00-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="0ea00-135">See also</span></span>



[<span data-ttu-id="0ea00-136">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0ea00-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0ea00-137">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="0ea00-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0ea00-138">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="0ea00-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0ea00-139">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="0ea00-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

