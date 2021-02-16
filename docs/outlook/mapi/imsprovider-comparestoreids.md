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
ms.openlocfilehash: 734e53c1e897c902c72319aa6f2d3d7af2d23fb6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431705"
---
# <a name="imsprovidercomparestoreids"></a><span data-ttu-id="4b42f-103">IMSProvider::CompareStoreIDs</span><span class="sxs-lookup"><span data-stu-id="4b42f-103">IMSProvider::CompareStoreIDs</span></span>

  
  
<span data-ttu-id="4b42f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b42f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b42f-105">Compara dois identificadores de entrada do armazenamento de mensagens para determinar se eles se referem ao mesmo objeto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4b42f-105">Compares two message store entry identifiers to determine whether they refer to the same store object.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="4b42f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b42f-106">Parameters</span></span>

 <span data-ttu-id="4b42f-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="4b42f-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="4b42f-108">[in] O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro  _lpEntryID1_  _._</span><span class="sxs-lookup"><span data-stu-id="4b42f-108">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="4b42f-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="4b42f-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="4b42f-110">[in] Um ponteiro para o identificador da primeira entrada a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="4b42f-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="4b42f-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="4b42f-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="4b42f-112">[in] O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro  _lpEntryID2_  _._</span><span class="sxs-lookup"><span data-stu-id="4b42f-112">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="4b42f-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="4b42f-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="4b42f-114">[in] Um ponteiro para o segundo identificador de entrada a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="4b42f-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="4b42f-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4b42f-115">_ulFlags_</span></span>
  
> <span data-ttu-id="4b42f-116">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="4b42f-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="4b42f-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="4b42f-117">_lpulResult_</span></span>
  
> <span data-ttu-id="4b42f-118">[out] Um ponteiro para o resultado retornado da comparação.</span><span class="sxs-lookup"><span data-stu-id="4b42f-118">[out] A pointer to the returned result of the comparison.</span></span> <span data-ttu-id="4b42f-119">TRUE se os dois identificadores de entrada se referirem ao mesmo objeto; caso contrário, FALSE.</span><span class="sxs-lookup"><span data-stu-id="4b42f-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4b42f-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4b42f-120">Return value</span></span>

<span data-ttu-id="4b42f-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="4b42f-121">S_OK</span></span> 
  
> <span data-ttu-id="4b42f-122">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="4b42f-122">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4b42f-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b42f-123">Remarks</span></span>

<span data-ttu-id="4b42f-124">O MAPI chama o método **IMSProvider::CompareStoreIDs** quando ele processa uma chamada para o método [IMAPISession::OpenMsgStore.](imapisession-openmsgstore.md)</span><span class="sxs-lookup"><span data-stu-id="4b42f-124">MAPI calls the **IMSProvider::CompareStoreIDs** method when it processes a call to the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> <span data-ttu-id="4b42f-125">**CompareStoreIDs** é chamado neste ponto para determinar qual seção de perfil, se alguma, está associada ao repositório de mensagens que está sendo aberto.</span><span class="sxs-lookup"><span data-stu-id="4b42f-125">**CompareStoreIDs** is called at this point to determine which profile section, if any, is associated with the message store being opened.</span></span> <span data-ttu-id="4b42f-126">Uma **chamada CompareStoreIDs** pode ser feita quando nenhum repositório de mensagens está aberto para um provedor de repositório específico.</span><span class="sxs-lookup"><span data-stu-id="4b42f-126">A **CompareStoreIDs** call can be made when no message stores are open for a particular store provider.</span></span> <span data-ttu-id="4b42f-127">Além disso, o MAPI também chama **CompareStoreIDs** quando processa uma chamada de provedor de repositório para o método [IMAPISupport::OpenProfileSection.](imapisupport-openprofilesection.md)</span><span class="sxs-lookup"><span data-stu-id="4b42f-127">In addition, MAPI also calls **CompareStoreIDs** when it processes a store provider call to the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method.</span></span> 
  
<span data-ttu-id="4b42f-128">Os identificadores de entrada comparados por **CompareStoreIDs** são ambos para a biblioteca de vínculo dinâmico (DLL) do provedor de repositório atual e são identificadores de entrada de repositório não mapeados.</span><span class="sxs-lookup"><span data-stu-id="4b42f-128">The entry identifiers compared by **CompareStoreIDs** are both for the current store provider's dynamic-link library (DLL) and are both unwrapped store entry identifiers.</span></span> <span data-ttu-id="4b42f-129">Para obter mais informações sobre identificadores de entrada do repositório de quebra, consulte [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md).</span><span class="sxs-lookup"><span data-stu-id="4b42f-129">For more information about wrapping store entry identifiers, see [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md).</span></span>
  
<span data-ttu-id="4b42f-130">Comparar identificadores de entrada é útil porque um objeto pode ter mais de um identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="4b42f-130">Comparing entry identifiers is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="4b42f-131">Isso pode ocorrer, por exemplo, depois que uma nova versão de um provedor de armazenamento de mensagens é instalada.</span><span class="sxs-lookup"><span data-stu-id="4b42f-131">This can occur, for example, after a new version of a message store provider is installed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4b42f-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="4b42f-132">See also</span></span>



[<span data-ttu-id="4b42f-133">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="4b42f-133">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="4b42f-134">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="4b42f-134">IMAPISupport::OpenProfileSection</span></span>](imapisupport-openprofilesection.md)
  
[<span data-ttu-id="4b42f-135">IMAPISupport::WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="4b42f-135">IMAPISupport::WrapStoreEntryID</span></span>](imapisupport-wrapstoreentryid.md)
  
[<span data-ttu-id="4b42f-136">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4b42f-136">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

