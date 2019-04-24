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
ms.openlocfilehash: 4dfde82aa843072168288f4e0b0084dfccd5cd2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338455"
---
# <a name="imapisessioncompareentryids"></a><span data-ttu-id="43b66-103">IMAPISession::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="43b66-103">IMAPISession::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="43b66-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43b66-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43b66-105">Compara dois identificadores de entrada para determinar se eles se referem ao mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="43b66-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="43b66-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43b66-106">Parameters</span></span>

 <span data-ttu-id="43b66-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="43b66-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="43b66-108">no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID1_ .</span><span class="sxs-lookup"><span data-stu-id="43b66-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="43b66-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="43b66-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="43b66-110">no Um ponteiro para o primeiro identificador de entrada a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="43b66-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="43b66-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="43b66-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="43b66-112">no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID2_ .</span><span class="sxs-lookup"><span data-stu-id="43b66-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="43b66-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="43b66-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="43b66-114">no Um ponteiro para o segundo identificador de entrada ser comparado.</span><span class="sxs-lookup"><span data-stu-id="43b66-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="43b66-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="43b66-115">_ulFlags_</span></span>
  
> <span data-ttu-id="43b66-116">no Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="43b66-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="43b66-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="43b66-117">_lpulResult_</span></span>
  
> <span data-ttu-id="43b66-118">bota Um ponteiro para o resultado da comparação.</span><span class="sxs-lookup"><span data-stu-id="43b66-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="43b66-119">TRUE se os dois identificadores de entrada se referem ao mesmo objeto; caso contrário, FALSE.</span><span class="sxs-lookup"><span data-stu-id="43b66-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="43b66-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="43b66-120">Return value</span></span>

<span data-ttu-id="43b66-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="43b66-121">S_OK</span></span> 
  
> <span data-ttu-id="43b66-122">A comparação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="43b66-122">The comparison was successful.</span></span>
    
<span data-ttu-id="43b66-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="43b66-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="43b66-124">Um ou ambos os identificadores de entrada especificados como parâmetros não se referem a objetos, possivelmente porque esses objetos estão atualmente não abertos e disponíveis.</span><span class="sxs-lookup"><span data-stu-id="43b66-124">One or both of the entry identifiers specified as parameters do not refer to objects, possibly because these objects are currently unopened and unavailable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="43b66-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="43b66-125">Remarks</span></span>

<span data-ttu-id="43b66-126">O método **IMAPISession:: CompareEntryIDs** compara dois identificadores de entrada que pertencem a um único provedor de serviços para determinar se eles se referem ao mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="43b66-126">The **IMAPISession::CompareEntryIDs** method compares two entry identifiers that belong to a single service provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="43b66-127">O MAPI extrai a parte [MAPIUID](mapiuid.md) dos identificadores de entrada para determinar o provedor de serviços responsável pelos objetos e, em seguida, chama o método **CompareEntryIDs** do objeto de logon para executar a comparação.</span><span class="sxs-lookup"><span data-stu-id="43b66-127">MAPI extracts the [MAPIUID](mapiuid.md) portion from the entry identifiers to determine the service provider responsible for the objects and then calls its logon object's **CompareEntryIDs** method to perform the comparison.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="43b66-128">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="43b66-128">Notes to callers</span></span>

<span data-ttu-id="43b66-129">O método **CompareEntryIDs** é útil porque um objeto pode ter mais de um identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="43b66-129">The **CompareEntryIDs** method is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="43b66-130">Essa situação pode ocorrer, por exemplo, após a instalação de uma nova versão de um provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="43b66-130">This situation can occur, for example, after a new version of a service provider is installed.</span></span> 
  
<span data-ttu-id="43b66-131">Se **CompareEntryIDs** retornar um erro, não realize nenhuma ação com base no resultado da comparação.</span><span class="sxs-lookup"><span data-stu-id="43b66-131">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="43b66-132">Em vez disso, considere a abordagem mais conservadora possível.</span><span class="sxs-lookup"><span data-stu-id="43b66-132">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="43b66-133">**CompareEntryIDs** pode falhar se, por exemplo, um ou ambos os identificadores de entrada contiverem um **MAPIUID**inválido.</span><span class="sxs-lookup"><span data-stu-id="43b66-133">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contain an invalid **MAPIUID**.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="43b66-134">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="43b66-134">MFCMAPI reference</span></span>

<span data-ttu-id="43b66-135">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="43b66-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="43b66-136">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="43b66-136">**File**</span></span>|<span data-ttu-id="43b66-137">**Função**</span><span class="sxs-lookup"><span data-stu-id="43b66-137">**Function**</span></span>|<span data-ttu-id="43b66-138">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="43b66-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="43b66-139">BaseDialog. cpp</span><span class="sxs-lookup"><span data-stu-id="43b66-139">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="43b66-140">CbaseDialog:: OnCompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="43b66-140">CbaseDialog::OnCompareEntryIDs</span></span>  <br/> |<span data-ttu-id="43b66-141">MFCMAPI usa o método **IMAPISession:: CompareEntryIDs** para comparar duas identificações de entrada inseridas por um usuário.</span><span class="sxs-lookup"><span data-stu-id="43b66-141">MFCMAPI uses the **IMAPISession::CompareEntryIDs** method to compare two entry IDs that a user enters.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="43b66-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="43b66-142">See also</span></span>



[<span data-ttu-id="43b66-143">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="43b66-143">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="43b66-144">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="43b66-144">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="43b66-145">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="43b66-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

