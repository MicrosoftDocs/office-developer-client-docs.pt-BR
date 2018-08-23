---
title: IMAPIFormMgrSelectMultipleForms
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.SelectMultipleForms
api_type:
- COM
ms.assetid: 172f8f53-b837-4286-9236-3f72806d7f1f
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: b974b733c24e61cb256ac0cf7b377d5630966fdf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579288"
---
# <a name="imapiformmgrselectmultipleforms"></a><span data-ttu-id="7a860-103">IMAPIFormMgr::SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="7a860-103">IMAPIFormMgr::SelectMultipleForms</span></span>

  
  
<span data-ttu-id="7a860-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a860-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a860-105">Apresenta uma caixa de diálogo que permite ao usuário selecionar vários formulários e retorna uma matriz de formulário objetos de informações que descrevem esses formulários.</span><span class="sxs-lookup"><span data-stu-id="7a860-105">Presents a dialog box that enables the user to select multiple forms, and returns an array of form information objects that describe those forms.</span></span>
  
```cpp
HRESULT SelectMultipleForms(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR pszTitle,
  LPMAPIFOLDER pfld,
  LPMAPIFORMINFOARRAY pfrminfoarray,
  LPMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a><span data-ttu-id="7a860-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a860-106">Parameters</span></span>

 <span data-ttu-id="7a860-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="7a860-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="7a860-108">[in] Uma alça para a janela pai da caixa de diálogo exibida.</span><span class="sxs-lookup"><span data-stu-id="7a860-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="7a860-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7a860-109">_ulFlags_</span></span>
  
> <span data-ttu-id="7a860-110">[in] Uma bitmask dos sinalizadores que controla o tipo das cadeias de caracteres no passado.</span><span class="sxs-lookup"><span data-stu-id="7a860-110">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="7a860-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="7a860-111">The following flag can be set:</span></span>
    
<span data-ttu-id="7a860-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7a860-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="7a860-113">As cadeias de caracteres passada na estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="7a860-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="7a860-114">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="7a860-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="7a860-115">_pszTitle_</span><span class="sxs-lookup"><span data-stu-id="7a860-115">_pszTitle_</span></span>
  
> <span data-ttu-id="7a860-116">[in] Um ponteiro para uma cadeia de caracteres que contém a legenda da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7a860-116">[in] A pointer to a string that contains the caption of the dialog box.</span></span> <span data-ttu-id="7a860-117">Se o parâmetro _pszTitle_ for NULL, o provedor de biblioteca de formulário que fornece os formulários fornece uma legenda padrão.</span><span class="sxs-lookup"><span data-stu-id="7a860-117">If the  _pszTitle_ parameter is NULL, the form library provider that provides the forms supplies a default caption.</span></span> 
    
 <span data-ttu-id="7a860-118">_pfld_</span><span class="sxs-lookup"><span data-stu-id="7a860-118">_pfld_</span></span>
  
> <span data-ttu-id="7a860-119">[in] Um ponteiro para a pasta da qual selecionar os formulários.</span><span class="sxs-lookup"><span data-stu-id="7a860-119">[in] A pointer to the folder from which to select the forms.</span></span> <span data-ttu-id="7a860-120">Se o parâmetro _pfld_ for NULL, os formulários são selecionados do contêiner formulário local, pessoal ou organização.</span><span class="sxs-lookup"><span data-stu-id="7a860-120">If the  _pfld_ parameter is NULL, the forms are selected from the local, personal, or organization form container.</span></span> 
    
 <span data-ttu-id="7a860-121">_pfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="7a860-121">_pfrminfoarray_</span></span>
  
> <span data-ttu-id="7a860-122">[in] Um ponteiro para uma matriz de objetos de informações de formulário que são pré-selecionados para o usuário.</span><span class="sxs-lookup"><span data-stu-id="7a860-122">[in] A pointer to an array of form information objects that are preselected for the user.</span></span>
    
 <span data-ttu-id="7a860-123">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="7a860-123">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="7a860-124">[out] Um ponteiro para um ponteiro para a matriz retornada dos objetos de informações do formulário.</span><span class="sxs-lookup"><span data-stu-id="7a860-124">[out] A pointer to a pointer to the returned array of form information objects.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7a860-125">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="7a860-125">Return value</span></span>

<span data-ttu-id="7a860-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="7a860-126">S_OK</span></span> 
  
> <span data-ttu-id="7a860-127">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="7a860-127">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="7a860-128">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="7a860-128">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="7a860-129">Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação suporta somente Unicode.</span><span class="sxs-lookup"><span data-stu-id="7a860-129">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="7a860-130">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="7a860-130">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="7a860-131">O usuário cancelou a operação, geralmente clicando no botão **Cancelar** na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7a860-131">The user canceled the operation, typically by clicking the **Cancel** button in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7a860-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a860-132">Remarks</span></span>

<span data-ttu-id="7a860-133">Visualizadores de formulário chame o método de **IMAPIFormMgr::SelectMultipleForms** para apresentado antes de uma caixa de diálogo que permite ao usuário selecionar vários formulários e, em seguida, para recuperar uma matriz de formulário informações objetos que descrevem os formulários selecionados.</span><span class="sxs-lookup"><span data-stu-id="7a860-133">Form viewers call the **IMAPIFormMgr::SelectMultipleForms** method to first present a dialog box that enables the user to select multiple forms and then to retrieve an array of form information objects that describe the selected forms.</span></span> <span data-ttu-id="7a860-134">A caixa de diálogo **SelectMultipleForms** exibe todos os formulários, se ou não estão ocultos (ou seja, se ou não suas propriedades ocultas são criptografadas).</span><span class="sxs-lookup"><span data-stu-id="7a860-134">The **SelectMultipleForms** dialog box displays all forms, whether or not they are hidden (that is, whether or not their hidden properties are clear).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7a860-135">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="7a860-135">Notes to implementers</span></span>

<span data-ttu-id="7a860-136">Se um visualizador de formulário passa o sinalizador MAPI_UNICODE no parâmetro _ulFlags_ , todas as cadeias de caracteres são Unicode.</span><span class="sxs-lookup"><span data-stu-id="7a860-136">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings are Unicode.</span></span> <span data-ttu-id="7a860-137">Provedores de biblioteca de formulário que não oferecem suporte a cadeias de caracteres Unicode devem retornar MAPI_E_BAD_CHARWIDTH se MAPI_UNICODE é passado.</span><span class="sxs-lookup"><span data-stu-id="7a860-137">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7a860-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a860-138">See also</span></span>



[<span data-ttu-id="7a860-139">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7a860-139">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

