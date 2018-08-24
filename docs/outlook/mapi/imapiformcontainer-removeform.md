---
title: IMAPIFormContainerRemoveForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.RemoveForm
api_type:
- COM
ms.assetid: 7f851ce8-bd01-4ea5-86e0-e44323cc0aab
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1a1d11db538d9b5368d80962e44b9eab38b490d2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575648"
---
# <a name="imapiformcontainerremoveform"></a><span data-ttu-id="4c74f-103">IMAPIFormContainer::RemoveForm</span><span class="sxs-lookup"><span data-stu-id="4c74f-103">IMAPIFormContainer::RemoveForm</span></span>

  
  
<span data-ttu-id="4c74f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c74f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c74f-105">Remove um determinado formulário de um contêiner de formulário.</span><span class="sxs-lookup"><span data-stu-id="4c74f-105">Removes a particular form from a form container.</span></span>
  
```cpp
HRESULT RemoveForm(
  LPCSTR szMessageClass
);
```

## <a name="parameters"></a><span data-ttu-id="4c74f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c74f-106">Parameters</span></span>

 <span data-ttu-id="4c74f-107">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="4c74f-107">_szMessageClass_</span></span>
  
> <span data-ttu-id="4c74f-108">[in] Uma cadeia de caracteres que nomeia a classe de mensagem do formulário a ser removido do contêiner do formulário.</span><span class="sxs-lookup"><span data-stu-id="4c74f-108">[in] A string that names the message class of the form to be removed from the form container.</span></span> <span data-ttu-id="4c74f-109">Nomes de classe de mensagem são sempre cadeias de caracteres ANSI, Unicode nunca.</span><span class="sxs-lookup"><span data-stu-id="4c74f-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4c74f-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4c74f-110">Return value</span></span>

<span data-ttu-id="4c74f-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="4c74f-111">S_OK</span></span> 
  
> <span data-ttu-id="4c74f-112">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="4c74f-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="4c74f-113">E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="4c74f-113">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="4c74f-114">A classe de mensagem passada no parâmetro _szMessageClass_ não coincide com a classe de mensagem de qualquer formulário no contêiner do formulário.</span><span class="sxs-lookup"><span data-stu-id="4c74f-114">The message class passed in the  _szMessageClass_ parameter does not match the message class of any form in the form container.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="4c74f-115">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="4c74f-115">MFCMAPI reference</span></span>

<span data-ttu-id="4c74f-116">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4c74f-116">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4c74f-117">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="4c74f-117">**File**</span></span>|<span data-ttu-id="4c74f-118">**Function**</span><span class="sxs-lookup"><span data-stu-id="4c74f-118">**Function**</span></span>|<span data-ttu-id="4c74f-119">**Comment**</span><span class="sxs-lookup"><span data-stu-id="4c74f-119">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4c74f-120">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="4c74f-120">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="4c74f-121">CFormContainerDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="4c74f-121">CFormContainerDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="4c74f-122">MFCMAPI usa o método **IMAPIFormContainer::RemoveForm** para excluir um formulário de um contêiner de formulário.</span><span class="sxs-lookup"><span data-stu-id="4c74f-122">MFCMAPI uses the **IMAPIFormContainer::RemoveForm** method to delete a form from a form container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4c74f-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c74f-123">See also</span></span>



[<span data-ttu-id="4c74f-124">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4c74f-124">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="4c74f-125">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="4c74f-125">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

