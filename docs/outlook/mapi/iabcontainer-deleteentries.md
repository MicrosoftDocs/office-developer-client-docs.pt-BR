---
title: IABContainerDeleteEntries
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.DeleteEntries
api_type:
- COM
ms.assetid: 70a24811-0c41-4b44-8c63-7ef807bc9051
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c744407790fecde6b6d89dff669ea4db07ce7701
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766822"
---
# <a name="iabcontainerdeleteentries"></a><span data-ttu-id="486c4-103">IABContainer::DeleteEntries</span><span class="sxs-lookup"><span data-stu-id="486c4-103">IABContainer::DeleteEntries</span></span>

  
  
<span data-ttu-id="486c4-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="486c4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="486c4-105">Remove uma ou mais entradas, normalmente mensagens outros contêineres, listas de distribuição ou os usuários.</span><span class="sxs-lookup"><span data-stu-id="486c4-105">Removes one or more entries, typically messaging users, distribution lists, or other containers.</span></span>
  
```cpp
HRESULT DeleteEntries(
  LPENTRYLIST lpEntries,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="486c4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="486c4-106">Parameters</span></span>

 <span data-ttu-id="486c4-107">_lpEntries_</span><span class="sxs-lookup"><span data-stu-id="486c4-107">_lpEntries_</span></span>
  
> <span data-ttu-id="486c4-108">[in] Um ponteiro para uma matriz de estruturas [ENTRYLIST](entrylist.md) que contêm os identificadores de entrada que representam as entradas que está sendo excluídas.</span><span class="sxs-lookup"><span data-stu-id="486c4-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that contain entry identifiers that represent the entries being deleted.</span></span> 
    
 <span data-ttu-id="486c4-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="486c4-109">_ulFlags_</span></span>
  
> <span data-ttu-id="486c4-110">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="486c4-110">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="486c4-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="486c4-111">Return value</span></span>

<span data-ttu-id="486c4-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="486c4-112">S_OK</span></span> 
  
> <span data-ttu-id="486c4-113">As entradas especificadas tenham sido excluídas com êxito.</span><span class="sxs-lookup"><span data-stu-id="486c4-113">The specified entries have been successfully deleted.</span></span> 
    
<span data-ttu-id="486c4-114">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="486c4-114">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="486c4-115">A chamada foi bem-sucedida, mas um ou mais das entradas não pôde ser excluída.</span><span class="sxs-lookup"><span data-stu-id="486c4-115">The call succeeded, but one or more of the entries could not be deleted.</span></span> <span data-ttu-id="486c4-116">Quando este valor é retornado, a chamada deve ser manipulada com êxito.</span><span class="sxs-lookup"><span data-stu-id="486c4-116">When this value is returned, the call should be handled as successful.</span></span> <span data-ttu-id="486c4-117">Para testar esse valor, use a macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="486c4-117">To test for this value, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="486c4-118">Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="486c4-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="486c4-119">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="486c4-119">MFCMAPI reference</span></span>

<span data-ttu-id="486c4-120">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="486c4-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="486c4-121">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="486c4-121">**File**</span></span>|<span data-ttu-id="486c4-122">**Function**</span><span class="sxs-lookup"><span data-stu-id="486c4-122">**Function**</span></span>|<span data-ttu-id="486c4-123">**Comment**</span><span class="sxs-lookup"><span data-stu-id="486c4-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="486c4-124">Abdlg.cpp</span><span class="sxs-lookup"><span data-stu-id="486c4-124">Abdlg.cpp</span></span>  <br/> |<span data-ttu-id="486c4-125">CabDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="486c4-125">CabDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="486c4-126">MFCMAPI usa o método **DeleteEntries** para excluir uma entrada específica de um contêiner de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="486c4-126">MFCMAPI uses the **DeleteEntries** method to delete a specific entry from an address book container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="486c4-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="486c4-127">See also</span></span>



[<span data-ttu-id="486c4-128">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="486c4-128">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)


[<span data-ttu-id="486c4-129">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="486c4-129">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

