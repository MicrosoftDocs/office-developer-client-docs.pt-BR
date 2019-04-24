---
title: IMAPIFormMgrSelectForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.SelectForm
api_type:
- COM
ms.assetid: c1cfe71b-01f3-429a-8b4c-73191a2ffea0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c25f352e7fa607a46741164574a4ba91d4026edf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321669"
---
# <a name="imapiformmgrselectform"></a><span data-ttu-id="7561b-103">IMAPIFormMgr::SelectForm</span><span class="sxs-lookup"><span data-stu-id="7561b-103">IMAPIFormMgr::SelectForm</span></span>

  
  
<span data-ttu-id="7561b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7561b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7561b-105">Apresenta uma caixa de diálogo que permite ao usuário selecionar um formulário e retorna um objeto de informações de formulário que descreve esse formulário.</span><span class="sxs-lookup"><span data-stu-id="7561b-105">Presents a dialog box that enables the user to select a form, and returns a form information object that describes that form.</span></span>
  
```cpp
HRESULT SelectForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR pszTitle,
  LPMAPIFOLDER pfld,
  LPMAPIFORMINFO FAR * ppfrminfoReturned
);
```

## <a name="parameters"></a><span data-ttu-id="7561b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7561b-106">Parameters</span></span>

 <span data-ttu-id="7561b-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="7561b-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="7561b-108">no Uma alça para a janela pai da caixa de diálogo exibida.</span><span class="sxs-lookup"><span data-stu-id="7561b-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="7561b-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7561b-109">_ulFlags_</span></span>
  
> <span data-ttu-id="7561b-110">no Uma máscara de bits de sinalizadores que controla o tipo das cadeias de caracteres passadas.</span><span class="sxs-lookup"><span data-stu-id="7561b-110">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="7561b-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="7561b-111">The following flag can be set:</span></span>
    
<span data-ttu-id="7561b-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7561b-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="7561b-113">As cadeias de caracteres passadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="7561b-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="7561b-114">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="7561b-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="7561b-115">_pszTitle_</span><span class="sxs-lookup"><span data-stu-id="7561b-115">_pszTitle_</span></span>
  
> <span data-ttu-id="7561b-116">no Um ponteiro para uma cadeia de caracteres que contém a legenda da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7561b-116">[in] A pointer to a string that contains the caption of the dialog box.</span></span> <span data-ttu-id="7561b-117">Se o parâmetro _pszTitle_ for NULL, o provedor de biblioteca de formulários fornecerá uma legenda padrão.</span><span class="sxs-lookup"><span data-stu-id="7561b-117">If the  _pszTitle_ parameter is NULL, the form library provider supplies a default caption.</span></span> 
    
 <span data-ttu-id="7561b-118">_pfld_</span><span class="sxs-lookup"><span data-stu-id="7561b-118">_pfld_</span></span>
  
> <span data-ttu-id="7561b-119">no Um ponteiro para a pasta na qual o formulário será selecionado.</span><span class="sxs-lookup"><span data-stu-id="7561b-119">[in] A pointer to the folder from which to select the form.</span></span> <span data-ttu-id="7561b-120">Se o parâmetro _pfld_ for NULL, o formulário pode ser selecionado do contêiner de formulários local, pessoal ou organização.</span><span class="sxs-lookup"><span data-stu-id="7561b-120">If the  _pfld_ parameter is NULL, the form can be selected from the local, personal, or organization form container.</span></span> 
    
 <span data-ttu-id="7561b-121">_ppfrminfoReturned_</span><span class="sxs-lookup"><span data-stu-id="7561b-121">_ppfrminfoReturned_</span></span>
  
> <span data-ttu-id="7561b-122">bota Um ponteiro para um ponteiro para o objeto de informações do formulário retornado.</span><span class="sxs-lookup"><span data-stu-id="7561b-122">[out] A pointer to a pointer to the returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7561b-123">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7561b-123">Return value</span></span>

<span data-ttu-id="7561b-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="7561b-124">S_OK</span></span> 
  
> <span data-ttu-id="7561b-125">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="7561b-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="7561b-126">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="7561b-126">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="7561b-127">O sinalizador MAPI_UNICODE foi definido e a implementação não tem suporte para Unicode ou o MAPI_UNICODE não foi definido e a implementação oferece suporte somente a Unicode.</span><span class="sxs-lookup"><span data-stu-id="7561b-127">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="7561b-128">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="7561b-128">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="7561b-129">O usuário cancelou a operação, geralmente clicando no botão **Cancelar** na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7561b-129">The user canceled the operation, typically by clicking the **Cancel** button in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7561b-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="7561b-130">Remarks</span></span>

<span data-ttu-id="7561b-131">Os visualizadores de formulários chamam o método **IMAPIFormMgr:: SelectForm** para primeiro apresentar uma caixa de diálogo que permite ao usuário selecionar um formulário e, em seguida, recuperar um objeto de informações de formulário que descreve o formulário selecionado.</span><span class="sxs-lookup"><span data-stu-id="7561b-131">Form viewers call the **IMAPIFormMgr::SelectForm** method to first present a dialog box that enables the user to select a form and then to retrieve a form information object that describes the selected form.</span></span> <span data-ttu-id="7561b-132">A caixa de diálogo restringe o usuário a selecionar um único Formulário.</span><span class="sxs-lookup"><span data-stu-id="7561b-132">The dialog box constrains the user to select a single form.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7561b-133">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="7561b-133">Notes to callers</span></span>

<span data-ttu-id="7561b-134">A caixa de diálogo **SelectForm** exibe somente formulários que não estão ocultos (ou seja, formulários que têm suas propriedades ocultas desmarcadas).</span><span class="sxs-lookup"><span data-stu-id="7561b-134">The **SelectForm** dialog box displays only forms that are not hidden (that is, forms that have their hidden properties clear).</span></span> <span data-ttu-id="7561b-135">Se um visualizador de formulários passar o sinalizador MAPI_UNICODE no parâmetro _parâmetroulflags_ , todas as cadeias de caracteres serão Unicode.</span><span class="sxs-lookup"><span data-stu-id="7561b-135">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings are Unicode.</span></span> <span data-ttu-id="7561b-136">Os provedores de biblioteca de formulários que não dão suporte a cadeias de caracteres Unicode devem retornar MAPI_E_BAD_CHARWIDTH se MAPI_UNICODE é passado.</span><span class="sxs-lookup"><span data-stu-id="7561b-136">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7561b-137">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7561b-137">MFCMAPI reference</span></span>

<span data-ttu-id="7561b-138">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="7561b-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7561b-139">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="7561b-139">**File**</span></span>|<span data-ttu-id="7561b-140">**Função**</span><span class="sxs-lookup"><span data-stu-id="7561b-140">**Function**</span></span>|<span data-ttu-id="7561b-141">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="7561b-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7561b-142">FolderDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="7561b-142">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="7561b-143">CFolderDlg:: OnSelectForm</span><span class="sxs-lookup"><span data-stu-id="7561b-143">CFolderDlg::OnSelectForm</span></span>  <br/> |<span data-ttu-id="7561b-144">MFCMAPI usa o método **IMAPIFormMgr:: SelectForm** para selecionar um formulário e enviar informações sobre o formulário para um ou mais logs.</span><span class="sxs-lookup"><span data-stu-id="7561b-144">MFCMAPI uses the **IMAPIFormMgr::SelectForm** method to select a form and send information about the form to one or more logs.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7561b-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="7561b-145">See also</span></span>



[<span data-ttu-id="7561b-146">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7561b-146">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="7561b-147">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="7561b-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

