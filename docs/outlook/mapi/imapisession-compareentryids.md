---
title: IMAPISessionCompareEntryIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.CompareEntryIDs
api_type:
- COM
ms.assetid: 319f10e9-db8d-4d16-aa1f-6cf5fef493eb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 745c1b10cbbb24389cace7911d7c5fd37fe09472
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586848"
---
# <a name="imapisessioncompareentryids"></a><span data-ttu-id="6dd92-103">IMAPISession::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="6dd92-103">IMAPISession::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="6dd92-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6dd92-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6dd92-105">Compara dois identificadores de entrada para determinar se eles se referem ao mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="6dd92-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> 
  
```cpp
HRESULT CompareEntryIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulResult
);
```

## <a name="parameters"></a><span data-ttu-id="6dd92-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6dd92-106">Parameters</span></span>

 <span data-ttu-id="6dd92-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="6dd92-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="6dd92-108">[in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID1_ .</span><span class="sxs-lookup"><span data-stu-id="6dd92-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="6dd92-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="6dd92-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="6dd92-110">[in] Um ponteiro para o primeiro identificador de entrada a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="6dd92-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="6dd92-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="6dd92-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="6dd92-112">[in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID2_ .</span><span class="sxs-lookup"><span data-stu-id="6dd92-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="6dd92-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="6dd92-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="6dd92-114">[in] Um ponteiro para o segundo identificador de entrada a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="6dd92-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="6dd92-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6dd92-115">_ulFlags_</span></span>
  
> <span data-ttu-id="6dd92-116">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6dd92-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="6dd92-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="6dd92-117">_lpulResult_</span></span>
  
> <span data-ttu-id="6dd92-118">[out] Um ponteiro para o resultado da comparação.</span><span class="sxs-lookup"><span data-stu-id="6dd92-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="6dd92-119">TRUE se os identificadores de dois entrada se referir ao mesmo objeto; Caso contrário, FALSE.</span><span class="sxs-lookup"><span data-stu-id="6dd92-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6dd92-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6dd92-120">Return value</span></span>

<span data-ttu-id="6dd92-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="6dd92-121">S_OK</span></span> 
  
> <span data-ttu-id="6dd92-122">A comparação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6dd92-122">The comparison was successful.</span></span>
    
<span data-ttu-id="6dd92-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="6dd92-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="6dd92-124">Um ou ambos os identificadores de entrada especificados como parâmetros não fazem referência a objetos, possivelmente porque esses objetos são atualmente não abertas e não está disponível.</span><span class="sxs-lookup"><span data-stu-id="6dd92-124">One or both of the entry identifiers specified as parameters do not refer to objects, possibly because these objects are currently unopened and unavailable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6dd92-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="6dd92-125">Remarks</span></span>

<span data-ttu-id="6dd92-126">O método **IMAPISession::CompareEntryIDs** compara dois identificadores de entrada que pertencem a um provedor de serviços único para determinar se eles se referem ao mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="6dd92-126">The **IMAPISession::CompareEntryIDs** method compares two entry identifiers that belong to a single service provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="6dd92-127">MAPI extrai a parte do [MAPIUID](mapiuid.md) dos identificadores de entrada para determinar o responsável para os objetos do provedor de serviço e, em seguida, chama o método de **CompareEntryIDs** do seu objeto logon para executar a comparação.</span><span class="sxs-lookup"><span data-stu-id="6dd92-127">MAPI extracts the [MAPIUID](mapiuid.md) portion from the entry identifiers to determine the service provider responsible for the objects and then calls its logon object's **CompareEntryIDs** method to perform the comparison.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6dd92-128">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="6dd92-128">Notes to callers</span></span>

<span data-ttu-id="6dd92-129">O método **CompareEntryIDs** é útil porque um objeto pode ter mais de um identificador de entrada válida.</span><span class="sxs-lookup"><span data-stu-id="6dd92-129">The **CompareEntryIDs** method is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="6dd92-130">Esta situação pode ocorrer, por exemplo, depois que uma nova versão de um provedor de serviço é instalada.</span><span class="sxs-lookup"><span data-stu-id="6dd92-130">This situation can occur, for example, after a new version of a service provider is installed.</span></span> 
  
<span data-ttu-id="6dd92-131">Se **CompareEntryIDs** retornará um erro, não terão qualquer ação baseada no resultado da comparação.</span><span class="sxs-lookup"><span data-stu-id="6dd92-131">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="6dd92-132">Em vez disso, a abordagem mais conservadora levar possíveis.</span><span class="sxs-lookup"><span data-stu-id="6dd92-132">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="6dd92-133">**CompareEntryIDs** pode falhar se, por exemplo, um ou ambos os identificadores de entrada contiverem um inválido **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="6dd92-133">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contain an invalid **MAPIUID**.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6dd92-134">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6dd92-134">MFCMAPI reference</span></span>

<span data-ttu-id="6dd92-135">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="6dd92-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6dd92-136">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="6dd92-136">**File**</span></span>|<span data-ttu-id="6dd92-137">**Function**</span><span class="sxs-lookup"><span data-stu-id="6dd92-137">**Function**</span></span>|<span data-ttu-id="6dd92-138">**Comment**</span><span class="sxs-lookup"><span data-stu-id="6dd92-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6dd92-139">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="6dd92-139">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="6dd92-140">CbaseDialog::OnCompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="6dd92-140">CbaseDialog::OnCompareEntryIDs</span></span>  <br/> |<span data-ttu-id="6dd92-141">MFCMAPI usa o método **IMAPISession::CompareEntryIDs** para comparar duas identificações de entrada que um usuário digita.</span><span class="sxs-lookup"><span data-stu-id="6dd92-141">MFCMAPI uses the **IMAPISession::CompareEntryIDs** method to compare two entry IDs that a user enters.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6dd92-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="6dd92-142">See also</span></span>



[<span data-ttu-id="6dd92-143">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="6dd92-143">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="6dd92-144">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6dd92-144">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="6dd92-145">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="6dd92-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

