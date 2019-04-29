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
# <a name="imapiformcontainergetdisplay"></a><span data-ttu-id="ea261-103">IMAPIFormContainer::GetDisplay</span><span class="sxs-lookup"><span data-stu-id="ea261-103">IMAPIFormContainer::GetDisplay</span></span>

  
  
<span data-ttu-id="ea261-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ea261-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ea261-105">Retorna o nome de exibição de um contêiner de formulários.</span><span class="sxs-lookup"><span data-stu-id="ea261-105">Returns the display name of a form container.</span></span>
  
```cpp
HRESULT GetDisplay(
  ULONG ulFlags,
  LPSTR FAR * pszDisplayName
);
```

## <a name="parameters"></a><span data-ttu-id="ea261-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea261-106">Parameters</span></span>

 <span data-ttu-id="ea261-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ea261-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ea261-108">no Uma bitmask de sinalizadores que controla o tipo da cadeia de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="ea261-108">[in] A bitmask of flags that controls the type of the returned string.</span></span> <span data-ttu-id="ea261-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="ea261-109">The following flag can be set:</span></span>
    
<span data-ttu-id="ea261-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ea261-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ea261-111">A cadeia de caracteres retornada está no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="ea261-111">The returned string is in Unicode format.</span></span> <span data-ttu-id="ea261-112">Se o sinalizador MAPI_UNICODE não estiver definido, a cadeia de caracteres estará no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="ea261-112">If the MAPI_UNICODE flag is not set, the string is in ANSI format.</span></span>
    
 <span data-ttu-id="ea261-113">_pszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="ea261-113">_pszDisplayName_</span></span>
  
> <span data-ttu-id="ea261-114">bota Um ponteiro para uma cadeia de caracteres que contém o nome de exibição do contêiner de formulários.</span><span class="sxs-lookup"><span data-stu-id="ea261-114">[out] A pointer to a string that contains the display name of the form container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ea261-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ea261-115">Return value</span></span>

<span data-ttu-id="ea261-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="ea261-116">S_OK</span></span> 
  
> <span data-ttu-id="ea261-117">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="ea261-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="ea261-118">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ea261-118">MFCMAPI reference</span></span>

<span data-ttu-id="ea261-119">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ea261-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ea261-120">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="ea261-120">**File**</span></span>|<span data-ttu-id="ea261-121">**Função**</span><span class="sxs-lookup"><span data-stu-id="ea261-121">**Function**</span></span>|<span data-ttu-id="ea261-122">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="ea261-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ea261-123">FormContainerDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="ea261-123">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="ea261-124">CFormContainerDlg:: CFormContainerDlg</span><span class="sxs-lookup"><span data-stu-id="ea261-124">CFormContainerDlg::CFormContainerDlg</span></span>  <br/> |<span data-ttu-id="ea261-125">MFCMAPI usa o método **IMAPIFormContainer:: getdisplay** para obter o nome do contêiner de formulário quando ele renderiza CFormContainerDlg.</span><span class="sxs-lookup"><span data-stu-id="ea261-125">MFCMAPI uses the **IMAPIFormContainer::GetDisplay** method to get the name of the form container when it renders CFormContainerDlg.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ea261-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea261-126">See also</span></span>



[<span data-ttu-id="ea261-127">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ea261-127">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="ea261-128">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="ea261-128">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

