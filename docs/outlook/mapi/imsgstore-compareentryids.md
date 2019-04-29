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
ms.openlocfilehash: 2a2439bae79b497f018391983e2c4b03a35eee70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424249"
---
# <a name="imsgstorecompareentryids"></a><span data-ttu-id="ea524-103">IMsgStore::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="ea524-103">IMsgStore::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="ea524-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ea524-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ea524-105">Compara dois identificadores de entrada para determinar se eles se referem à mesma entrada em um repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ea524-105">Compares two entry identifiers to determine whether they refer to the same entry in a message store.</span></span> <span data-ttu-id="ea524-106">O MAPI passa essa chamada para um provedor de serviços somente se os UIDs (identificadores exclusivos) nos dois identificadores de entrada a serem comparados são tratados por esse provedor.</span><span class="sxs-lookup"><span data-stu-id="ea524-106">MAPI passes this call to a service provider only if the unique identifiers (UIDs) in both entry identifiers to be compared are handled by that provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="ea524-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea524-107">Parameters</span></span>

 <span data-ttu-id="ea524-108">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="ea524-108">_cbEntryID1_</span></span>
  
> <span data-ttu-id="ea524-109">no A contagem de bytes no identificador de entrada apontado pelo __ parâmetro lpEntryID1 _._</span><span class="sxs-lookup"><span data-stu-id="ea524-109">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="ea524-110">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="ea524-110">_lpEntryID1_</span></span>
  
> <span data-ttu-id="ea524-111">no Um ponteiro para o primeiro identificador de entrada a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="ea524-111">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="ea524-112">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="ea524-112">_cbEntryID2_</span></span>
  
> <span data-ttu-id="ea524-113">no A contagem de bytes no identificador de entrada apontado pelo __ parâmetro lpEntryID2 _._</span><span class="sxs-lookup"><span data-stu-id="ea524-113">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="ea524-114">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="ea524-114">_lpEntryID2_</span></span>
  
> <span data-ttu-id="ea524-115">no Um ponteiro para o segundo identificador de entrada ser comparado.</span><span class="sxs-lookup"><span data-stu-id="ea524-115">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="ea524-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ea524-116">_ulFlags_</span></span>
  
> <span data-ttu-id="ea524-117">no Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ea524-117">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="ea524-118">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="ea524-118">_lpulResult_</span></span>
  
> <span data-ttu-id="ea524-119">bota Um ponteiro para o resultado da comparação.</span><span class="sxs-lookup"><span data-stu-id="ea524-119">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="ea524-120">TRUE se os dois identificadores de entrada se referem ao mesmo objeto; caso contrário, FALSE.</span><span class="sxs-lookup"><span data-stu-id="ea524-120">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ea524-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ea524-121">Return value</span></span>

<span data-ttu-id="ea524-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="ea524-122">S_OK</span></span> 
  
> <span data-ttu-id="ea524-123">A comparação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ea524-123">The comparison was successful.</span></span>
    
<span data-ttu-id="ea524-124">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="ea524-124">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="ea524-125">Um ou ambos os identificadores de entrada especificados como parâmetros não se referem a objetos, possivelmente porque os objetos correspondentes estão desabertos e indisponíveis no momento.</span><span class="sxs-lookup"><span data-stu-id="ea524-125">One or both of the entry identifiers specified as parameters do not refer to objects, possibly because the corresponding objects are unopened and unavailable at present.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ea524-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea524-126">Remarks</span></span>

<span data-ttu-id="ea524-127">O método **IMsgStore:: CompareEntryIDs** compara dois identificadores de entrada que pertencem ao repositório de mensagens para determinar se eles se referem ao mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="ea524-127">The **IMsgStore::CompareEntryIDs** method compares two entry identifiers that belong to the message store to determine whether they refer to the same object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ea524-128">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="ea524-128">Notes to callers</span></span>

 <span data-ttu-id="ea524-129">**CompareEntryIDs** é útil porque um objeto pode ter mais de um identificador de entrada válido (por exemplo, depois que uma nova versão de um provedor de repositório de mensagens é instalada).</span><span class="sxs-lookup"><span data-stu-id="ea524-129">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier (for example, after a new version of a message store provider is installed).</span></span> 
  
<span data-ttu-id="ea524-130">Se **CompareEntryIDs** retornar um erro, não realize nenhuma ação com base no resultado da comparação.</span><span class="sxs-lookup"><span data-stu-id="ea524-130">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="ea524-131">Em vez disso, considere a abordagem mais conservadora possível.</span><span class="sxs-lookup"><span data-stu-id="ea524-131">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="ea524-132">**CompareEntryIDs** pode falhar se, por exemplo, um ou ambos os identificadores de entrada contiverem um **MAPIUID**inválido.</span><span class="sxs-lookup"><span data-stu-id="ea524-132">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contains an invalid **MAPIUID**.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ea524-133">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ea524-133">MFCMAPI reference</span></span>

<span data-ttu-id="ea524-134">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ea524-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ea524-135">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="ea524-135">**File**</span></span>|<span data-ttu-id="ea524-136">**Função**</span><span class="sxs-lookup"><span data-stu-id="ea524-136">**Function**</span></span>|<span data-ttu-id="ea524-137">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="ea524-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ea524-138">BaseDialog. cpp</span><span class="sxs-lookup"><span data-stu-id="ea524-138">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="ea524-139">CBaseDialog:: OnCompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="ea524-139">CBaseDialog::OnCompareEntryIDs</span></span>  <br/> |<span data-ttu-id="ea524-140">MFCMAPI usa o método **IMsgStore:: CompareEntryIDs** para comparar IDs de entrada.</span><span class="sxs-lookup"><span data-stu-id="ea524-140">MFCMAPI uses the **IMsgStore::CompareEntryIDs** method to compare entry IDs.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ea524-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea524-141">See also</span></span>



[<span data-ttu-id="ea524-142">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="ea524-142">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="ea524-143">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ea524-143">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="ea524-144">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="ea524-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

