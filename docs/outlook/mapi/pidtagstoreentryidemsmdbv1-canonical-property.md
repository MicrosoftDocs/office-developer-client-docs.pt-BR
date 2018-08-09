---
title: Propriedade canônica PidTagStoreEntryIdEmsmdbV1
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 40161358-4d41-43cf-83c7-fdd843bec87b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 74626b735599a5f1485b26fcb65d907b552b3089
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770083"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a><span data-ttu-id="d6ae1-103">Propriedade canônica PidTagStoreEntryIdEmsmdbV1</span><span class="sxs-lookup"><span data-stu-id="d6ae1-103">PidTagStoreEntryIdEmsmdbV1 Canonical Property</span></span>

  
  
<span data-ttu-id="d6ae1-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d6ae1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d6ae1-105">Contém o estilo antigo (Microsoft Outlook 2002 e versões anteriores) do identificador de entrada de um armazenamento de mensagens do Microsoft Exchange Server 2010 ou Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d6ae1-105">Contains the old style (Microsoft Outlook 2002 and earlier versions) of the entry identifier of a Microsoft Exchange Server 2010 or Exchange Server 2013 message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d6ae1-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="d6ae1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d6ae1-107">PR_STORE_ENTRYID_EMSMDB_V1</span><span class="sxs-lookup"><span data-stu-id="d6ae1-107">PR_STORE_ENTRYID_EMSMDB_V1</span></span>  <br/> |
|<span data-ttu-id="d6ae1-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d6ae1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d6ae1-109">0x65F60102</span><span class="sxs-lookup"><span data-stu-id="d6ae1-109">0x65F60102</span></span>  <br/> |
|<span data-ttu-id="d6ae1-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="d6ae1-110">Data type:</span></span>  <br/> |<span data-ttu-id="d6ae1-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d6ae1-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d6ae1-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d6ae1-112">Area:</span></span>  <br/> |<span data-ttu-id="d6ae1-113">Propriedades de identificação</span><span class="sxs-lookup"><span data-stu-id="d6ae1-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d6ae1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6ae1-114">Remarks</span></span>

<span data-ttu-id="d6ae1-115">Começando com o Microsoft Outlook 2003, os FQDNs de servidor foram integrados nas identificações de entrada, evitando RPCs adicionais para referências.</span><span class="sxs-lookup"><span data-stu-id="d6ae1-115">Starting with Microsoft Outlook 2003, the server FQDNs were integrated into the entry IDs, thereby avoiding additional RPCs for referrals.</span></span> <span data-ttu-id="d6ae1-116">No entanto, isso torna mais de identificações de entrada e introduz mais cenários em que o método **CompareEntryIDs** deve ser usado para determinar se dois entrada IDs são equivalentes.</span><span class="sxs-lookup"><span data-stu-id="d6ae1-116">However, this makes entry IDs longer and introduces more scenarios where the **CompareEntryIDs** method must be used to determine whether two entry IDs are equivalent.</span></span> <span data-ttu-id="d6ae1-117">O PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) propriedade acessa o formato mais antigo da identificação de entrada do Exchange Server usada pelo Microsoft Outlook 2002 (Microsoft Office XP) e versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="d6ae1-117">The PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) property accesses the older format of the Exchange Server entry ID used by Microsoft Outlook 2002 (Microsoft Office XP) and earlier versions.</span></span> <span data-ttu-id="d6ae1-118">Isso pode economizar espaço e também reduzir o número de chamadas **CompareEntryIDs** necessários para determinar quando a entrada IDs são equivalentes.</span><span class="sxs-lookup"><span data-stu-id="d6ae1-118">This can save space and also reduce the number of **CompareEntryIDs** calls needed to determine when entry IDs are equivalent.</span></span> <span data-ttu-id="d6ae1-119">Observe que usando a entrada mais antiga IDs para abrir uma caixa de correio pode incorrer em alguns RPCs adicionais se uma referência é necessária.</span><span class="sxs-lookup"><span data-stu-id="d6ae1-119">Note that using the older entry IDs to open a mailbox may incur some additional RPCs if a referral is required.</span></span> 
  
<span data-ttu-id="d6ae1-120">Para acessar a propriedade PR_STORE_ENTRYID_EMSMDB_V1 enquanto estiver no modo de cache, você deve ignorar o cache usando o sinalizador MAPI_NO_CACHE com o método [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="d6ae1-120">To access the PR_STORE_ENTRYID_EMSMDB_V1 property while in cached mode, you must bypass the cache using the MAPI_NO_CACHE flag with the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="d6ae1-121">Se **PR_STORE_ENTRYID_EMSMDB_V1** não estiver disponível, o código deve descriptografado PR_STORE_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="d6ae1-121">If **PR_STORE_ENTRYID_EMSMDB_V1** isn't available, the code should fall back to PR_STORE_ENTRYID.</span></span> <span data-ttu-id="d6ae1-122">Somente o Outlook 2003 por meio do Microsoft Outlook 2013 suporta a propriedade PR_STORE_ENTRYID_EMSMDB_V1.</span><span class="sxs-lookup"><span data-stu-id="d6ae1-122">Only Outlook 2003 through Microsoft Outlook 2013 support the PR_STORE_ENTRYID_EMSMDB_V1 property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d6ae1-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6ae1-123">See also</span></span>



[<span data-ttu-id="d6ae1-124">Propriedade canônica PidTagStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="d6ae1-124">PidTagStoreEntryId Canonical Property</span></span>](pidtagstoreentryid-canonical-property.md)


[<span data-ttu-id="d6ae1-125">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d6ae1-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d6ae1-126">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="d6ae1-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d6ae1-127">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="d6ae1-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d6ae1-128">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="d6ae1-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

