---
title: IMsgStoreCompareEntryIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.CompareEntryIDs
api_type:
- COM
ms.assetid: 33d70748-0d3f-4be4-bcb5-7ec048887944
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 640923511241b08e5a86e9733aab5cc2e9237c23
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576572"
---
# <a name="imsgstorecompareentryids"></a><span data-ttu-id="fc7b1-103">IMsgStore::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="fc7b1-103">IMsgStore::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="fc7b1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc7b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc7b1-105">Compara dois identificadores de entrada para determinar se eles se referem a mesma entrada em um repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="fc7b1-105">Compares two entry identifiers to determine whether they refer to the same entry in a message store.</span></span> <span data-ttu-id="fc7b1-106">MAPI passa essa chamada para um provedor de serviço somente se os identificadores exclusivos (UIDs) em ambos os identificadores de entrada a ser comparada são manipulados por esse provedor.</span><span class="sxs-lookup"><span data-stu-id="fc7b1-106">MAPI passes this call to a service provider only if the unique identifiers (UIDs) in both entry identifiers to be compared are handled by that provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="fc7b1-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fc7b1-107">Parameters</span></span>

 <span data-ttu-id="fc7b1-108">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="fc7b1-108">_cbEntryID1_</span></span>
  
> <span data-ttu-id="fc7b1-109">[in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID1_ _._</span><span class="sxs-lookup"><span data-stu-id="fc7b1-109">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="fc7b1-110">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="fc7b1-110">_lpEntryID1_</span></span>
  
> <span data-ttu-id="fc7b1-111">[in] Um ponteiro para o primeiro identificador de entrada a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="fc7b1-111">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="fc7b1-112">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="fc7b1-112">_cbEntryID2_</span></span>
  
> <span data-ttu-id="fc7b1-113">[in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID2_ _._</span><span class="sxs-lookup"><span data-stu-id="fc7b1-113">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="fc7b1-114">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="fc7b1-114">_lpEntryID2_</span></span>
  
> <span data-ttu-id="fc7b1-115">[in] Um ponteiro para o segundo identificador de entrada a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="fc7b1-115">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="fc7b1-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fc7b1-116">_ulFlags_</span></span>
  
> <span data-ttu-id="fc7b1-117">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="fc7b1-117">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="fc7b1-118">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="fc7b1-118">_lpulResult_</span></span>
  
> <span data-ttu-id="fc7b1-119">[out] Um ponteiro para o resultado da comparação.</span><span class="sxs-lookup"><span data-stu-id="fc7b1-119">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="fc7b1-120">TRUE se os identificadores de dois entrada se referir ao mesmo objeto; Caso contrário, FALSE.</span><span class="sxs-lookup"><span data-stu-id="fc7b1-120">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fc7b1-121">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="fc7b1-121">Return value</span></span>

<span data-ttu-id="fc7b1-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="fc7b1-122">S_OK</span></span> 
  
> <span data-ttu-id="fc7b1-123">A comparação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="fc7b1-123">The comparison was successful.</span></span>
    
<span data-ttu-id="fc7b1-124">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="fc7b1-124">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="fc7b1-125">Um ou ambos os identificadores de entrada especificados como parâmetros não fazem referência a objetos, possivelmente porque os objetos correspondentes são não abertas e não está disponível em apresentam.</span><span class="sxs-lookup"><span data-stu-id="fc7b1-125">One or both of the entry identifiers specified as parameters do not refer to objects, possibly because the corresponding objects are unopened and unavailable at present.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fc7b1-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc7b1-126">Remarks</span></span>

<span data-ttu-id="fc7b1-127">O método **IMsgStore::CompareEntryIDs** compara dois identificadores de entrada que pertencem ao repositório de mensagem para determinar se eles se referem ao mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="fc7b1-127">The **IMsgStore::CompareEntryIDs** method compares two entry identifiers that belong to the message store to determine whether they refer to the same object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="fc7b1-128">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="fc7b1-128">Notes to callers</span></span>

 <span data-ttu-id="fc7b1-129">**CompareEntryIDs** é útil porque um objeto pode ter mais de um identificador de entrada válida (por exemplo, depois que uma nova versão de um provedor de armazenamento de mensagem está instalada).</span><span class="sxs-lookup"><span data-stu-id="fc7b1-129">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier (for example, after a new version of a message store provider is installed).</span></span> 
  
<span data-ttu-id="fc7b1-130">Se **CompareEntryIDs** retornará um erro, não terão qualquer ação baseada no resultado da comparação.</span><span class="sxs-lookup"><span data-stu-id="fc7b1-130">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="fc7b1-131">Em vez disso, a abordagem mais conservadora levar possíveis.</span><span class="sxs-lookup"><span data-stu-id="fc7b1-131">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="fc7b1-132">**CompareEntryIDs** pode falhar se, por exemplo, um ou ambos os identificadores de entrada contiver um inválido **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="fc7b1-132">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contains an invalid **MAPIUID**.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="fc7b1-133">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="fc7b1-133">MFCMAPI reference</span></span>

<span data-ttu-id="fc7b1-134">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="fc7b1-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fc7b1-135">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="fc7b1-135">**File**</span></span>|<span data-ttu-id="fc7b1-136">**Function**</span><span class="sxs-lookup"><span data-stu-id="fc7b1-136">**Function**</span></span>|<span data-ttu-id="fc7b1-137">**Comment**</span><span class="sxs-lookup"><span data-stu-id="fc7b1-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fc7b1-138">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="fc7b1-138">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="fc7b1-139">CBaseDialog::OnCompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="fc7b1-139">CBaseDialog::OnCompareEntryIDs</span></span>  <br/> |<span data-ttu-id="fc7b1-140">MFCMAPI usa o método **IMsgStore::CompareEntryIDs** para comparar as identificações de entrada.</span><span class="sxs-lookup"><span data-stu-id="fc7b1-140">MFCMAPI uses the **IMsgStore::CompareEntryIDs** method to compare entry IDs.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fc7b1-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc7b1-141">See also</span></span>



[<span data-ttu-id="fc7b1-142">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="fc7b1-142">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="fc7b1-143">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="fc7b1-143">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="fc7b1-144">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="fc7b1-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

