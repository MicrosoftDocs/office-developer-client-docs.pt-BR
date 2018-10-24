---
title: IMSProviderCompareStoreIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.CompareStoreIDs
api_type:
- COM
ms.assetid: c3e3cfaa-9c4a-482a-9411-9c4ab01d312f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 57b8438d655b3bc5b708fd7ed6734554a3a23ac4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585987"
---
# <a name="imsprovidercomparestoreids"></a><span data-ttu-id="3ee18-103">IMSProvider::CompareStoreIDs</span><span class="sxs-lookup"><span data-stu-id="3ee18-103">IMSProvider::CompareStoreIDs</span></span>

  
  
<span data-ttu-id="3ee18-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ee18-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ee18-105">Compara dois mensagem repositório identificadores de entrada para determinar se eles se referem ao mesmo objeto store.</span><span class="sxs-lookup"><span data-stu-id="3ee18-105">Compares two message store entry identifiers to determine whether they refer to the same store object.</span></span>
  
```cpp
HRESULT CompareStoreIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulResult
);
```

## <a name="parameters"></a><span data-ttu-id="3ee18-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ee18-106">Parameters</span></span>

 <span data-ttu-id="3ee18-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="3ee18-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="3ee18-108">[in] O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpEntryID1_ _._</span><span class="sxs-lookup"><span data-stu-id="3ee18-108">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="3ee18-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="3ee18-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="3ee18-110">[in] Um ponteiro para o primeiro identificador de entrada a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="3ee18-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="3ee18-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="3ee18-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="3ee18-112">[in] O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpEntryID2_ _._</span><span class="sxs-lookup"><span data-stu-id="3ee18-112">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="3ee18-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="3ee18-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="3ee18-114">[in] Um ponteiro para o segundo identificador de entrada a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="3ee18-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="3ee18-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3ee18-115">_ulFlags_</span></span>
  
> <span data-ttu-id="3ee18-116">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="3ee18-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="3ee18-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="3ee18-117">_lpulResult_</span></span>
  
> <span data-ttu-id="3ee18-118">[out] Um ponteiro para o resultado da comparação.</span><span class="sxs-lookup"><span data-stu-id="3ee18-118">[out] A pointer to the returned result of the comparison.</span></span> <span data-ttu-id="3ee18-119">TRUE se os identificadores de dois entrada se referir ao mesmo objeto; Caso contrário, FALSE.</span><span class="sxs-lookup"><span data-stu-id="3ee18-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3ee18-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3ee18-120">Return value</span></span>

<span data-ttu-id="3ee18-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="3ee18-121">S_OK</span></span> 
  
> <span data-ttu-id="3ee18-122">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="3ee18-122">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3ee18-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ee18-123">Remarks</span></span>

<span data-ttu-id="3ee18-124">MAPI chama o método **IMSProvider::CompareStoreIDs** quando ele processa uma chamada ao método [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) .</span><span class="sxs-lookup"><span data-stu-id="3ee18-124">MAPI calls the **IMSProvider::CompareStoreIDs** method when it processes a call to the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> <span data-ttu-id="3ee18-125">**CompareStoreIDs** é chamado, nesse momento, para determinar qual seção de perfil, se houver, está associada com o armazenamento de mensagens está sendo aberto.</span><span class="sxs-lookup"><span data-stu-id="3ee18-125">**CompareStoreIDs** is called at this point to determine which profile section, if any, is associated with the message store being opened.</span></span> <span data-ttu-id="3ee18-126">Uma chamada de **CompareStoreIDs** pode ser feita quando nenhum armazenamentos de mensagem estão abertos para um provedor de armazenamento específica.</span><span class="sxs-lookup"><span data-stu-id="3ee18-126">A **CompareStoreIDs** call can be made when no message stores are open for a particular store provider.</span></span> <span data-ttu-id="3ee18-127">Além disso, o MAPI também chama **CompareStoreIDs** quando ele processa uma chamada do provedor de repositório para o método [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) .</span><span class="sxs-lookup"><span data-stu-id="3ee18-127">In addition, MAPI also calls **CompareStoreIDs** when it processes a store provider call to the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method.</span></span> 
  
<span data-ttu-id="3ee18-128">Os identificadores de entrada comparados por **CompareStoreIDs** são ambos para as atuais armazenam biblioteca do provedor de vínculo dinâmico (DLL) e são os dois identificadores de entrada do repositório desfeita.</span><span class="sxs-lookup"><span data-stu-id="3ee18-128">The entry identifiers compared by **CompareStoreIDs** are both for the current store provider's dynamic-link library (DLL) and are both unwrapped store entry identifiers.</span></span> <span data-ttu-id="3ee18-129">Para obter mais informações sobre identificadores de entrada do repositório de disposição, consulte [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md).</span><span class="sxs-lookup"><span data-stu-id="3ee18-129">For more information about wrapping store entry identifiers, see [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md).</span></span>
  
<span data-ttu-id="3ee18-130">Comparar os identificadores de entrada é útil porque um objeto pode ter mais de um identificador de entrada válida.</span><span class="sxs-lookup"><span data-stu-id="3ee18-130">Comparing entry identifiers is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="3ee18-131">Isso pode ocorrer, por exemplo, depois que uma nova versão de um provedor de armazenamento de mensagens é instalada.</span><span class="sxs-lookup"><span data-stu-id="3ee18-131">This can occur, for example, after a new version of a message store provider is installed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3ee18-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ee18-132">See also</span></span>



[<span data-ttu-id="3ee18-133">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="3ee18-133">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="3ee18-134">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="3ee18-134">IMAPISupport::OpenProfileSection</span></span>](imapisupport-openprofilesection.md)
  
[<span data-ttu-id="3ee18-135">IMAPISupport::WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="3ee18-135">IMAPISupport::WrapStoreEntryID</span></span>](imapisupport-wrapstoreentryid.md)
  
[<span data-ttu-id="3ee18-136">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3ee18-136">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

