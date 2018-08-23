---
title: IMAPIFormInfoSaveForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.SaveForm
api_type:
- COM
ms.assetid: 18a10f14-0795-4d4d-b590-f4cef4f2902a
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 7fec6b6236d26789a3ec9abee7d2ae1c620f89b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593470"
---
# <a name="imapiforminfosaveform"></a><span data-ttu-id="47d44-103">IMAPIFormInfo::SaveForm</span><span class="sxs-lookup"><span data-stu-id="47d44-103">IMAPIFormInfo::SaveForm</span></span>

  
  
<span data-ttu-id="47d44-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47d44-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47d44-105">Salva uma descrição de um determinado formulário em um arquivo de configuração.</span><span class="sxs-lookup"><span data-stu-id="47d44-105">Saves a description of a particular form in a configuration file.</span></span>
  
```cpp
HRESULT SaveForm(
  LPCSTR szFileName
);
```

## <a name="parameters"></a><span data-ttu-id="47d44-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47d44-106">Parameters</span></span>

 <span data-ttu-id="47d44-107">_szFileName_</span><span class="sxs-lookup"><span data-stu-id="47d44-107">_szFileName_</span></span>
  
> <span data-ttu-id="47d44-108">[in] Uma cadeia de caracteres que nomeia o arquivo de mensagem de descrição do formulário onde a respectiva descrição é salva.</span><span class="sxs-lookup"><span data-stu-id="47d44-108">[in] A string that names the form's description message file where its description is saved.</span></span> <span data-ttu-id="47d44-109">Este nome de arquivo deve ter a extensão .fdm.</span><span class="sxs-lookup"><span data-stu-id="47d44-109">This file name must have the .fdm extension.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="47d44-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="47d44-110">Return value</span></span>

<span data-ttu-id="47d44-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="47d44-111">S_OK</span></span> 
  
> <span data-ttu-id="47d44-112">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="47d44-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="47d44-113">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="47d44-113">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="47d44-114">Não foi possível gravar o arquivo de configuração.</span><span class="sxs-lookup"><span data-stu-id="47d44-114">The configuration file could not be written.</span></span> <span data-ttu-id="47d44-115">Para obter a estrutura [MAPIERROR](mapierror.md) que está associada com o erro, chame o método [IMAPIProp::GetLastError](imapiprop-getlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="47d44-115">To get the [MAPIERROR](mapierror.md) structure that is associated with the error, call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="47d44-116">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="47d44-116">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="47d44-117">**SaveForm** provavelmente foi chamado para salvar um formulário no contêiner local do formulário.</span><span class="sxs-lookup"><span data-stu-id="47d44-117">**SaveForm** was probably called to save a form in the local form container.</span></span> <span data-ttu-id="47d44-118">**SaveForm** não é suportado no contêiner do local do formulário.</span><span class="sxs-lookup"><span data-stu-id="47d44-118">**SaveForm** is not supported on the local form container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="47d44-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="47d44-119">Remarks</span></span>

<span data-ttu-id="47d44-120">Aplicativos cliente chamam o método de **IMAPIFormInfo::SaveForm** para salvar uma descrição do formulário atual no arquivo que tenha o nome de arquivo fornecido.</span><span class="sxs-lookup"><span data-stu-id="47d44-120">Client applications call the **IMAPIFormInfo::SaveForm** method to save a description of the current form in the file that has the given file name.</span></span> <span data-ttu-id="47d44-121">**SaveForm** cria um arquivo de configuração.</span><span class="sxs-lookup"><span data-stu-id="47d44-121">**SaveForm** creates a configuration file.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="47d44-122">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="47d44-122">Notes to callers</span></span>

<span data-ttu-id="47d44-123">Você pode reinstalar formulários selecionando-os em uma lista de mensagens descritor de formulário em uma caixa de diálogo que compõem a exibição de provedores de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="47d44-123">You can reinstall forms by selecting them from a list of form descriptor messages in a dialog box that form library providers display.</span></span> <span data-ttu-id="47d44-124">A extensão recomendada para mensagens de descritor de formulário é .fdm.</span><span class="sxs-lookup"><span data-stu-id="47d44-124">The recommended extension for form descriptor messages is .fdm.</span></span>
  
<span data-ttu-id="47d44-125">Chamar o método [IMAPIProp::GetLastError](imapiprop-getlasterror.md) se **SaveForm** retorna MAPI_E_EXTENDED_ERROR e verificar a estrutura **MAPIERROR** retornada para determinar a condição que causou o erro.</span><span class="sxs-lookup"><span data-stu-id="47d44-125">Call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method if **SaveForm** returns MAPI_E_EXTENDED_ERROR, and check the returned **MAPIERROR** structure to determine the condition that caused the error.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="47d44-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="47d44-126">See also</span></span>



[<span data-ttu-id="47d44-127">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="47d44-127">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="47d44-128">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="47d44-128">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="47d44-129">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="47d44-129">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

