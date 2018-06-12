---
title: IMAPIFormContainerGetDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.GetDisplay
api_type:
- COM
ms.assetid: 6829e273-4a75-4278-b58a-ae7543e075ac
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 0f9826dab72968055604c5bb9f8f537facc5618e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767029"
---
# <a name="imapiformcontainergetdisplay"></a><span data-ttu-id="e0fb9-103">IMAPIFormContainer::GetDisplay</span><span class="sxs-lookup"><span data-stu-id="e0fb9-103">IMAPIFormContainer::GetDisplay</span></span>

  
  
<span data-ttu-id="e0fb9-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e0fb9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e0fb9-105">Retorna o nome de exibição de um contêiner de formulário.</span><span class="sxs-lookup"><span data-stu-id="e0fb9-105">Returns the display name of a form container.</span></span>
  
```cpp
HRESULT GetDisplay(
  ULONG ulFlags,
  LPSTR FAR * pszDisplayName
);
```

## <a name="parameters"></a><span data-ttu-id="e0fb9-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="e0fb9-106">Parameters</span></span>

 <span data-ttu-id="e0fb9-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e0fb9-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e0fb9-108">[in] Uma bitmask dos sinalizadores que controla o tipo de cadeia de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="e0fb9-108">[in] A bitmask of flags that controls the type of the returned string.</span></span> <span data-ttu-id="e0fb9-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="e0fb9-109">The following flag can be set:</span></span>
    
<span data-ttu-id="e0fb9-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e0fb9-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e0fb9-111">A cadeia de caracteres retornada está no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="e0fb9-111">The returned string is in Unicode format.</span></span> <span data-ttu-id="e0fb9-112">Se o sinalizador MAPI_UNICODE não estiver definido, a cadeia de caracteres é no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="e0fb9-112">If the MAPI_UNICODE flag is not set, the string is in ANSI format.</span></span>
    
 <span data-ttu-id="e0fb9-113">_pszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="e0fb9-113">_pszDisplayName_</span></span>
  
> <span data-ttu-id="e0fb9-114">[out] Um ponteiro para uma cadeia de caracteres que contém o nome de exibição do contêiner do formulário.</span><span class="sxs-lookup"><span data-stu-id="e0fb9-114">[out] A pointer to a string that contains the display name of the form container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e0fb9-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e0fb9-115">Return value</span></span>

<span data-ttu-id="e0fb9-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="e0fb9-116">S_OK</span></span> 
  
> <span data-ttu-id="e0fb9-117">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="e0fb9-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="e0fb9-118">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e0fb9-118">MFCMAPI reference</span></span>

<span data-ttu-id="e0fb9-119">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e0fb9-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e0fb9-120">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="e0fb9-120">**File**</span></span>|<span data-ttu-id="e0fb9-121">**Function**</span><span class="sxs-lookup"><span data-stu-id="e0fb9-121">**Function**</span></span>|<span data-ttu-id="e0fb9-122">**Comment**</span><span class="sxs-lookup"><span data-stu-id="e0fb9-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e0fb9-123">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="e0fb9-123">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="e0fb9-124">CFormContainerDlg::CFormContainerDlg</span><span class="sxs-lookup"><span data-stu-id="e0fb9-124">CFormContainerDlg::CFormContainerDlg</span></span>  <br/> |<span data-ttu-id="e0fb9-125">MFCMAPI usa o método **IMAPIFormContainer::GetDisplay** para obter o nome do contêiner formulário quando ele for processada CFormContainerDlg.</span><span class="sxs-lookup"><span data-stu-id="e0fb9-125">MFCMAPI uses the **IMAPIFormContainer::GetDisplay** method to get the name of the form container when it renders CFormContainerDlg.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e0fb9-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0fb9-126">See also</span></span>



[<span data-ttu-id="e0fb9-127">IMAPIFormContainer: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e0fb9-127">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="e0fb9-128">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="e0fb9-128">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

