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
ms.openlocfilehash: c8bccbfeb7f04745a66831618deff490bc651b02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415149"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a><span data-ttu-id="9d8eb-103">Propriedade canônica PidTagStoreEntryIdEmsmdbV1</span><span class="sxs-lookup"><span data-stu-id="9d8eb-103">PidTagStoreEntryIdEmsmdbV1 Canonical Property</span></span>

  
  
<span data-ttu-id="9d8eb-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d8eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d8eb-105">Contém o estilo antigo (Microsoft Outlook 2002 e versões anteriores) do identificador de entrada de um armazenamento de mensagens do Microsoft Exchange Server 2010 ou do Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9d8eb-105">Contains the old style (Microsoft Outlook 2002 and earlier versions) of the entry identifier of a Microsoft Exchange Server 2010 or Exchange Server 2013 message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9d8eb-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="9d8eb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9d8eb-107">PR_STORE_ENTRYID_EMSMDB_V1</span><span class="sxs-lookup"><span data-stu-id="9d8eb-107">PR_STORE_ENTRYID_EMSMDB_V1</span></span>  <br/> |
|<span data-ttu-id="9d8eb-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9d8eb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9d8eb-109">0x65F60102</span><span class="sxs-lookup"><span data-stu-id="9d8eb-109">0x65F60102</span></span>  <br/> |
|<span data-ttu-id="9d8eb-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="9d8eb-110">Data type:</span></span>  <br/> |<span data-ttu-id="9d8eb-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9d8eb-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9d8eb-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9d8eb-112">Area:</span></span>  <br/> |<span data-ttu-id="9d8eb-113">Propriedades de ID</span><span class="sxs-lookup"><span data-stu-id="9d8eb-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d8eb-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9d8eb-114">Remarks</span></span>

<span data-ttu-id="9d8eb-115">A partir do Microsoft Outlook 2003, os FQDNs do servidor foram integrados às IDs de entrada, evitando RPCs adicionais para indicações.</span><span class="sxs-lookup"><span data-stu-id="9d8eb-115">Starting with Microsoft Outlook 2003, the server FQDNs were integrated into the entry IDs, thereby avoiding additional RPCs for referrals.</span></span> <span data-ttu-id="9d8eb-116">No entanto, isso torna as IDs de entrada mais longas e apresenta mais cenários em que o **método CompareEntryIDs** deve ser usado para determinar se duas IDs de entrada são equivalentes.</span><span class="sxs-lookup"><span data-stu-id="9d8eb-116">However, this makes entry IDs longer and introduces more scenarios where the **CompareEntryIDs** method must be used to determine whether two entry IDs are equivalent.</span></span> <span data-ttu-id="9d8eb-117">A PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) acessa o formato mais antigo da ID de entrada do Exchange Server usada pelo Microsoft Outlook 2002 (Microsoft Office XP) e versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="9d8eb-117">The PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) property accesses the older format of the Exchange Server entry ID used by Microsoft Outlook 2002 (Microsoft Office XP) and earlier versions.</span></span> <span data-ttu-id="9d8eb-118">Isso pode economizar espaço e também reduzir o número de chamadas **CompareEntryIDs** necessárias para determinar quando as IDs de entrada são equivalentes.</span><span class="sxs-lookup"><span data-stu-id="9d8eb-118">This can save space and also reduce the number of **CompareEntryIDs** calls needed to determine when entry IDs are equivalent.</span></span> <span data-ttu-id="9d8eb-119">Observe que usar as IDs de entrada mais antigas para abrir uma caixa de correio pode incorrer em alguns RPCs adicionais se uma referência for necessária.</span><span class="sxs-lookup"><span data-stu-id="9d8eb-119">Note that using the older entry IDs to open a mailbox may incur some additional RPCs if a referral is required.</span></span> 
  
<span data-ttu-id="9d8eb-120">Para acessar a PR_STORE_ENTRYID_EMSMDB_V1 no modo em cache, você deve ignorar o cache usando o sinalizador MAPI_NO_CACHE com o método [IMAPIProp::GetProps.](imapiprop-getprops.md)</span><span class="sxs-lookup"><span data-stu-id="9d8eb-120">To access the PR_STORE_ENTRYID_EMSMDB_V1 property while in cached mode, you must bypass the cache using the MAPI_NO_CACHE flag with the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="9d8eb-121">Se **PR_STORE_ENTRYID_EMSMDB_V1** não estiver disponível, o código deverá voltar ao PR_STORE_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="9d8eb-121">If **PR_STORE_ENTRYID_EMSMDB_V1** isn't available, the code should fall back to PR_STORE_ENTRYID.</span></span> <span data-ttu-id="9d8eb-122">Somente o Outlook 2003 a Microsoft Outlook 2013 suporta a PR_STORE_ENTRYID_EMSMDB_V1 propriedade.</span><span class="sxs-lookup"><span data-stu-id="9d8eb-122">Only Outlook 2003 through Microsoft Outlook 2013 support the PR_STORE_ENTRYID_EMSMDB_V1 property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9d8eb-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d8eb-123">See also</span></span>



[<span data-ttu-id="9d8eb-124">Propriedade canônica PidTagStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="9d8eb-124">PidTagStoreEntryId Canonical Property</span></span>](pidtagstoreentryid-canonical-property.md)


[<span data-ttu-id="9d8eb-125">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9d8eb-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9d8eb-126">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="9d8eb-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9d8eb-127">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="9d8eb-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9d8eb-128">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="9d8eb-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

