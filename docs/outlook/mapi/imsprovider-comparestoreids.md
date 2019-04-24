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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317266"
---
# <a name="imsprovidercomparestoreids"></a><span data-ttu-id="7a471-103">IMSProvider::CompareStoreIDs</span><span class="sxs-lookup"><span data-stu-id="7a471-103">IMSProvider::CompareStoreIDs</span></span>

  
  
<span data-ttu-id="7a471-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a471-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a471-105">Compara dois identificadores de entrada de repositório de mensagens para determinar se eles se referem ao mesmo objeto Store.</span><span class="sxs-lookup"><span data-stu-id="7a471-105">Compares two message store entry identifiers to determine whether they refer to the same store object.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="7a471-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a471-106">Parameters</span></span>

 <span data-ttu-id="7a471-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="7a471-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="7a471-108">no O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpEntryID1_ _._</span><span class="sxs-lookup"><span data-stu-id="7a471-108">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="7a471-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="7a471-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="7a471-110">no Um ponteiro para o primeiro identificador de entrada a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="7a471-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="7a471-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="7a471-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="7a471-112">no O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpEntryID2_ _._</span><span class="sxs-lookup"><span data-stu-id="7a471-112">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="7a471-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="7a471-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="7a471-114">no Um ponteiro para o segundo identificador de entrada ser comparado.</span><span class="sxs-lookup"><span data-stu-id="7a471-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="7a471-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7a471-115">_ulFlags_</span></span>
  
> <span data-ttu-id="7a471-116">no Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7a471-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="7a471-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="7a471-117">_lpulResult_</span></span>
  
> <span data-ttu-id="7a471-118">bota Um ponteiro para o resultado retornado da comparação.</span><span class="sxs-lookup"><span data-stu-id="7a471-118">[out] A pointer to the returned result of the comparison.</span></span> <span data-ttu-id="7a471-119">TRUE se os dois identificadores de entrada se referem ao mesmo objeto; caso contrário, FALSE.</span><span class="sxs-lookup"><span data-stu-id="7a471-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7a471-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7a471-120">Return value</span></span>

<span data-ttu-id="7a471-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="7a471-121">S_OK</span></span> 
  
> <span data-ttu-id="7a471-122">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="7a471-122">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7a471-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a471-123">Remarks</span></span>

<span data-ttu-id="7a471-124">MAPI chama o método **IMSProvider:: CompareStoreIDs** quando processa uma chamada para o método [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) .</span><span class="sxs-lookup"><span data-stu-id="7a471-124">MAPI calls the **IMSProvider::CompareStoreIDs** method when it processes a call to the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> <span data-ttu-id="7a471-125">**CompareStoreIDs** é chamado neste ponto para determinar qual seção de perfil, se houver, está associada ao armazenamento de mensagens que está sendo aberto.</span><span class="sxs-lookup"><span data-stu-id="7a471-125">**CompareStoreIDs** is called at this point to determine which profile section, if any, is associated with the message store being opened.</span></span> <span data-ttu-id="7a471-126">Uma chamada **CompareStoreIDs** pode ser feita quando não há repositórios de mensagens abertos para um provedor de repositório específico.</span><span class="sxs-lookup"><span data-stu-id="7a471-126">A **CompareStoreIDs** call can be made when no message stores are open for a particular store provider.</span></span> <span data-ttu-id="7a471-127">Além disso, o MAPI também chama **CompareStoreIDs** quando processa uma chamada do provedor de repositório para o método [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) .</span><span class="sxs-lookup"><span data-stu-id="7a471-127">In addition, MAPI also calls **CompareStoreIDs** when it processes a store provider call to the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method.</span></span> 
  
<span data-ttu-id="7a471-128">Os identificadores de entrada comparados por **CompareStoreIDs** são para a biblioteca de vínculo dinâmico (DLL) do provedor de repositório atual e são identificadores de entrada de repositório não encapsulados.</span><span class="sxs-lookup"><span data-stu-id="7a471-128">The entry identifiers compared by **CompareStoreIDs** are both for the current store provider's dynamic-link library (DLL) and are both unwrapped store entry identifiers.</span></span> <span data-ttu-id="7a471-129">Para obter mais informações sobre identificadores de entrada de repositório de enrolamento, consulte [IMAPISupport:: WrapStoreEntryID](imapisupport-wrapstoreentryid.md).</span><span class="sxs-lookup"><span data-stu-id="7a471-129">For more information about wrapping store entry identifiers, see [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md).</span></span>
  
<span data-ttu-id="7a471-130">A comparação de identificadores de entrada é útil porque um objeto pode ter mais de um identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="7a471-130">Comparing entry identifiers is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="7a471-131">Isso pode ocorrer, por exemplo, após a instalação de uma nova versão de um provedor de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="7a471-131">This can occur, for example, after a new version of a message store provider is installed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7a471-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a471-132">See also</span></span>



[<span data-ttu-id="7a471-133">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="7a471-133">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="7a471-134">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="7a471-134">IMAPISupport::OpenProfileSection</span></span>](imapisupport-openprofilesection.md)
  
[<span data-ttu-id="7a471-135">IMAPISupport::WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="7a471-135">IMAPISupport::WrapStoreEntryID</span></span>](imapisupport-wrapstoreentryid.md)
  
[<span data-ttu-id="7a471-136">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7a471-136">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

