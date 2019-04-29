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
ms.openlocfilehash: e3b238129e55e03da33ef3af75ecce7e73fbad03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425593"
---
# <a name="iabcontainerdeleteentries"></a><span data-ttu-id="186ed-103">IABContainer::DeleteEntries</span><span class="sxs-lookup"><span data-stu-id="186ed-103">IABContainer::DeleteEntries</span></span>

  
  
<span data-ttu-id="186ed-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="186ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="186ed-105">Remove uma ou mais entradas, tipicamente usuários de mensagens, listas de distribuição ou outros contêineres.</span><span class="sxs-lookup"><span data-stu-id="186ed-105">Removes one or more entries, typically messaging users, distribution lists, or other containers.</span></span>
  
```cpp
HRESULT DeleteEntries(
  LPENTRYLIST lpEntries,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="186ed-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="186ed-106">Parameters</span></span>

 <span data-ttu-id="186ed-107">_lpEntries_</span><span class="sxs-lookup"><span data-stu-id="186ed-107">_lpEntries_</span></span>
  
> <span data-ttu-id="186ed-108">no Um ponteiro para uma matriz de [](entrylist.md) estruturas ENTRYLIST que contêm identificadores de entrada que representam as entradas sendo excluídas.</span><span class="sxs-lookup"><span data-stu-id="186ed-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that contain entry identifiers that represent the entries being deleted.</span></span> 
    
 <span data-ttu-id="186ed-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="186ed-109">_ulFlags_</span></span>
  
> <span data-ttu-id="186ed-110">no Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="186ed-110">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="186ed-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="186ed-111">Return value</span></span>

<span data-ttu-id="186ed-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="186ed-112">S_OK</span></span> 
  
> <span data-ttu-id="186ed-113">As entradas especificadas foram excluídas com êxito.</span><span class="sxs-lookup"><span data-stu-id="186ed-113">The specified entries have been successfully deleted.</span></span> 
    
<span data-ttu-id="186ed-114">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="186ed-114">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="186ed-115">A chamada teve êxito, mas uma ou mais entradas não puderam ser excluídas.</span><span class="sxs-lookup"><span data-stu-id="186ed-115">The call succeeded, but one or more of the entries could not be deleted.</span></span> <span data-ttu-id="186ed-116">Quando esse valor é retornado, a chamada deve ser tratada como bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="186ed-116">When this value is returned, the call should be handled as successful.</span></span> <span data-ttu-id="186ed-117">Para testar esse valor, use a macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="186ed-117">To test for this value, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="186ed-118">Para obter mais informações, consulte [usando macros para tratamento de erros](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="186ed-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="186ed-119">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="186ed-119">MFCMAPI reference</span></span>

<span data-ttu-id="186ed-120">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="186ed-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="186ed-121">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="186ed-121">**File**</span></span>|<span data-ttu-id="186ed-122">**Função**</span><span class="sxs-lookup"><span data-stu-id="186ed-122">**Function**</span></span>|<span data-ttu-id="186ed-123">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="186ed-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="186ed-124">Abdlg. cpp</span><span class="sxs-lookup"><span data-stu-id="186ed-124">Abdlg.cpp</span></span>  <br/> |<span data-ttu-id="186ed-125">CabDlg:: OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="186ed-125">CabDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="186ed-126">MFCMAPI usa o método **DeleteEntries** para excluir uma entrada específica de um contêiner de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="186ed-126">MFCMAPI uses the **DeleteEntries** method to delete a specific entry from an address book container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="186ed-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="186ed-127">See also</span></span>



[<span data-ttu-id="186ed-128">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="186ed-128">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)


[<span data-ttu-id="186ed-129">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="186ed-129">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

