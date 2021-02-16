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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 391ea3ef4f44db2a9d007241232f58db27647ba2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428743"
---
# <a name="imapiforminfosaveform"></a><span data-ttu-id="3ba53-103">IMAPIFormInfo::SaveForm</span><span class="sxs-lookup"><span data-stu-id="3ba53-103">IMAPIFormInfo::SaveForm</span></span>

  
  
<span data-ttu-id="3ba53-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ba53-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ba53-105">Salva uma descrição de um formulário específico em um arquivo de configuração.</span><span class="sxs-lookup"><span data-stu-id="3ba53-105">Saves a description of a particular form in a configuration file.</span></span>
  
```cpp
HRESULT SaveForm(
  LPCSTR szFileName
);
```

## <a name="parameters"></a><span data-ttu-id="3ba53-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ba53-106">Parameters</span></span>

 <span data-ttu-id="3ba53-107">_szFileName_</span><span class="sxs-lookup"><span data-stu-id="3ba53-107">_szFileName_</span></span>
  
> <span data-ttu-id="3ba53-108">[in] Uma cadeia de caracteres que nomeia o arquivo de mensagem de descrição do formulário onde sua descrição é salva.</span><span class="sxs-lookup"><span data-stu-id="3ba53-108">[in] A string that names the form's description message file where its description is saved.</span></span> <span data-ttu-id="3ba53-109">Esse nome de arquivo deve ter a extensão .fdm.</span><span class="sxs-lookup"><span data-stu-id="3ba53-109">This file name must have the .fdm extension.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3ba53-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3ba53-110">Return value</span></span>

<span data-ttu-id="3ba53-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="3ba53-111">S_OK</span></span> 
  
> <span data-ttu-id="3ba53-112">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="3ba53-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="3ba53-113">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="3ba53-113">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="3ba53-114">Não foi possível escrever o arquivo de configuração.</span><span class="sxs-lookup"><span data-stu-id="3ba53-114">The configuration file could not be written.</span></span> <span data-ttu-id="3ba53-115">Para obter a [estrutura MAPIERROR](mapierror.md) associada ao erro, chame o método [IMAPIProp::GetLastError.](imapiprop-getlasterror.md)</span><span class="sxs-lookup"><span data-stu-id="3ba53-115">To get the [MAPIERROR](mapierror.md) structure that is associated with the error, call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="3ba53-116">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="3ba53-116">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="3ba53-117">**SaveForm** provavelmente foi chamado para salvar um formulário no contêiner de formulário local.</span><span class="sxs-lookup"><span data-stu-id="3ba53-117">**SaveForm** was probably called to save a form in the local form container.</span></span> <span data-ttu-id="3ba53-118">**SaveForm** não é suportado no contêiner de formulário local.</span><span class="sxs-lookup"><span data-stu-id="3ba53-118">**SaveForm** is not supported on the local form container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3ba53-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ba53-119">Remarks</span></span>

<span data-ttu-id="3ba53-120">Os aplicativos cliente chamam o método **IMAPIFormInfo::SaveForm** para salvar uma descrição do formulário atual no arquivo que tem o nome de arquivo determinado.</span><span class="sxs-lookup"><span data-stu-id="3ba53-120">Client applications call the **IMAPIFormInfo::SaveForm** method to save a description of the current form in the file that has the given file name.</span></span> <span data-ttu-id="3ba53-121">**SaveForm** cria um arquivo de configuração.</span><span class="sxs-lookup"><span data-stu-id="3ba53-121">**SaveForm** creates a configuration file.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3ba53-122">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="3ba53-122">Notes to callers</span></span>

<span data-ttu-id="3ba53-123">Você pode reinstalar formulários selecionando-os em uma lista de mensagens de descritor de formulário em uma caixa de diálogo exibida pelos provedores de biblioteca de formulários.</span><span class="sxs-lookup"><span data-stu-id="3ba53-123">You can reinstall forms by selecting them from a list of form descriptor messages in a dialog box that form library providers display.</span></span> <span data-ttu-id="3ba53-124">A extensão recomendada para mensagens de descritor de formulário é .fdm.</span><span class="sxs-lookup"><span data-stu-id="3ba53-124">The recommended extension for form descriptor messages is .fdm.</span></span>
  
<span data-ttu-id="3ba53-125">Chame o [método IMAPIProp::GetLastError](imapiprop-getlasterror.md) se **SaveForm** retornar MAPI_E_EXTENDED_ERROR e verifique a estrutura **MAPIERROR** retornada para determinar a condição que causou o erro.</span><span class="sxs-lookup"><span data-stu-id="3ba53-125">Call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method if **SaveForm** returns MAPI_E_EXTENDED_ERROR, and check the returned **MAPIERROR** structure to determine the condition that caused the error.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3ba53-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ba53-126">See also</span></span>



[<span data-ttu-id="3ba53-127">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="3ba53-127">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="3ba53-128">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="3ba53-128">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="3ba53-129">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3ba53-129">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

