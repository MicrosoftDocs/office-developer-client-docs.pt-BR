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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 994041d050df56fd3fa3c0e599542e05a202ad65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416129"
---
# <a name="imapiformcontainergetdisplay"></a><span data-ttu-id="771d6-103">IMAPIFormContainer::GetDisplay</span><span class="sxs-lookup"><span data-stu-id="771d6-103">IMAPIFormContainer::GetDisplay</span></span>

  
  
<span data-ttu-id="771d6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="771d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="771d6-105">Retorna o nome de exibição de um contêiner de formulário.</span><span class="sxs-lookup"><span data-stu-id="771d6-105">Returns the display name of a form container.</span></span>
  
```cpp
HRESULT GetDisplay(
  ULONG ulFlags,
  LPSTR FAR * pszDisplayName
);
```

## <a name="parameters"></a><span data-ttu-id="771d6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="771d6-106">Parameters</span></span>

 <span data-ttu-id="771d6-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="771d6-107">_ulFlags_</span></span>
  
> <span data-ttu-id="771d6-108">[in] Uma máscara de bits de sinalizadores que controla o tipo da cadeia de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="771d6-108">[in] A bitmask of flags that controls the type of the returned string.</span></span> <span data-ttu-id="771d6-109">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="771d6-109">The following flag can be set:</span></span>
    
<span data-ttu-id="771d6-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="771d6-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="771d6-111">A cadeia de caracteres retornada está no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="771d6-111">The returned string is in Unicode format.</span></span> <span data-ttu-id="771d6-112">Se o MAPI_UNICODE não estiver definido, a cadeia de caracteres está no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="771d6-112">If the MAPI_UNICODE flag is not set, the string is in ANSI format.</span></span>
    
 <span data-ttu-id="771d6-113">_pszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="771d6-113">_pszDisplayName_</span></span>
  
> <span data-ttu-id="771d6-114">[out] Um ponteiro para uma cadeia de caracteres que contém o nome de exibição do contêiner de formulário.</span><span class="sxs-lookup"><span data-stu-id="771d6-114">[out] A pointer to a string that contains the display name of the form container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="771d6-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="771d6-115">Return value</span></span>

<span data-ttu-id="771d6-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="771d6-116">S_OK</span></span> 
  
> <span data-ttu-id="771d6-117">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="771d6-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="771d6-118">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="771d6-118">MFCMAPI reference</span></span>

<span data-ttu-id="771d6-119">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="771d6-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="771d6-120">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="771d6-120">**File**</span></span>|<span data-ttu-id="771d6-121">**Função**</span><span class="sxs-lookup"><span data-stu-id="771d6-121">**Function**</span></span>|<span data-ttu-id="771d6-122">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="771d6-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="771d6-123">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="771d6-123">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="771d6-124">CFormContainerDlg::CFormContainerDlg</span><span class="sxs-lookup"><span data-stu-id="771d6-124">CFormContainerDlg::CFormContainerDlg</span></span>  <br/> |<span data-ttu-id="771d6-125">MFCMAPI uses the **IMAPIFormContainer::GetDisplay** method to get the name of the form container when it renders CFormContainerDlg.</span><span class="sxs-lookup"><span data-stu-id="771d6-125">MFCMAPI uses the **IMAPIFormContainer::GetDisplay** method to get the name of the form container when it renders CFormContainerDlg.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="771d6-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="771d6-126">See also</span></span>



[<span data-ttu-id="771d6-127">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="771d6-127">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="771d6-128">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="771d6-128">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

