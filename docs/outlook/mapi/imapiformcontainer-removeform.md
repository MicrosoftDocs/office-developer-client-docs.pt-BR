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
ms.openlocfilehash: e53c0cbd9946ff04516594a7ce99fdc2daf4ff4d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432195"
---
# <a name="imapiformcontainerremoveform"></a><span data-ttu-id="3ee4a-103">IMAPIFormContainer::RemoveForm</span><span class="sxs-lookup"><span data-stu-id="3ee4a-103">IMAPIFormContainer::RemoveForm</span></span>

  
  
<span data-ttu-id="3ee4a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ee4a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ee4a-105">Remove um formulário específico de um contêiner de formulário.</span><span class="sxs-lookup"><span data-stu-id="3ee4a-105">Removes a particular form from a form container.</span></span>
  
```cpp
HRESULT RemoveForm(
  LPCSTR szMessageClass
);
```

## <a name="parameters"></a><span data-ttu-id="3ee4a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ee4a-106">Parameters</span></span>

 <span data-ttu-id="3ee4a-107">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="3ee4a-107">_szMessageClass_</span></span>
  
> <span data-ttu-id="3ee4a-108">[in] Uma cadeia de caracteres que nomeia a classe de mensagem do formulário a ser removida do contêiner de formulário.</span><span class="sxs-lookup"><span data-stu-id="3ee4a-108">[in] A string that names the message class of the form to be removed from the form container.</span></span> <span data-ttu-id="3ee4a-109">Os nomes de classe de mensagem são sempre cadeias de caracteres ANSI, nunca Unicode.</span><span class="sxs-lookup"><span data-stu-id="3ee4a-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3ee4a-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3ee4a-110">Return value</span></span>

<span data-ttu-id="3ee4a-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="3ee4a-111">S_OK</span></span> 
  
> <span data-ttu-id="3ee4a-112">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="3ee4a-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="3ee4a-113">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="3ee4a-113">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="3ee4a-114">A classe de mensagem passada no  _parâmetro szMessageClass_ não combina com a classe de mensagem de nenhum formulário no contêiner de formulário.</span><span class="sxs-lookup"><span data-stu-id="3ee4a-114">The message class passed in the  _szMessageClass_ parameter does not match the message class of any form in the form container.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="3ee4a-115">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3ee4a-115">MFCMAPI reference</span></span>

<span data-ttu-id="3ee4a-116">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="3ee4a-116">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3ee4a-117">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="3ee4a-117">**File**</span></span>|<span data-ttu-id="3ee4a-118">**Função**</span><span class="sxs-lookup"><span data-stu-id="3ee4a-118">**Function**</span></span>|<span data-ttu-id="3ee4a-119">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="3ee4a-119">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3ee4a-120">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="3ee4a-120">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="3ee4a-121">CFormContainerDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="3ee4a-121">CFormContainerDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="3ee4a-122">MFCMAPI usa o **método IMAPIFormContainer::RemoveForm** para excluir um formulário de um contêiner de formulário.</span><span class="sxs-lookup"><span data-stu-id="3ee4a-122">MFCMAPI uses the **IMAPIFormContainer::RemoveForm** method to delete a form from a form container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3ee4a-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ee4a-123">See also</span></span>



[<span data-ttu-id="3ee4a-124">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3ee4a-124">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="3ee4a-125">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="3ee4a-125">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

