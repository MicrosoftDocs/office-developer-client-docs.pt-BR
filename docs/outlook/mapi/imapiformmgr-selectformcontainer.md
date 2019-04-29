---
title: IMAPIFormMgrSelectFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyMessages
api_type:
- COM
ms.assetid: c33daad6-52c4-4968-ac56-415178c9bf12
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bfddc24e6a9c7cf8bdeae1e5ea730ecdb116f564
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428589"
---
# <a name="imapiformmgrselectformcontainer"></a><span data-ttu-id="a6804-103">IMAPIFormMgr::SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="a6804-103">IMAPIFormMgr::SelectFormContainer</span></span>

  
  
<span data-ttu-id="a6804-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6804-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6804-105">Apresenta uma caixa de diálogo que permite ao usuário selecionar um contêiner de formulários e retorna uma interface para o objeto Container que o usuário selecionou.</span><span class="sxs-lookup"><span data-stu-id="a6804-105">Presents a dialog box that enables the user to select a form container, and returns an interface for the container object the user selected.</span></span>
  
```cpp
HRESULT SelectFormContainer(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="a6804-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6804-106">Parameters</span></span>

 <span data-ttu-id="a6804-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a6804-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="a6804-108">no Uma alça para a janela pai da caixa de diálogo exibida.</span><span class="sxs-lookup"><span data-stu-id="a6804-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="a6804-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a6804-109">_ulFlags_</span></span>
  
> <span data-ttu-id="a6804-110">no Uma bitmask de sinalizadores que controla como a biblioteca de formulários é selecionada (ou seja, como o contêiner de formulários é selecionado).</span><span class="sxs-lookup"><span data-stu-id="a6804-110">[in] A bitmask of flags that controls how the form library is selected (that is, how the form container is selected).</span></span> <span data-ttu-id="a6804-111">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="a6804-111">The following flags can be set:</span></span>
    
<span data-ttu-id="a6804-112">MAPIFORM_SELECT_ALL_REGISTRIES</span><span class="sxs-lookup"><span data-stu-id="a6804-112">MAPIFORM_SELECT_ALL_REGISTRIES</span></span> 
  
> <span data-ttu-id="a6804-113">A seleção pode ser feita de todos os contêineres.</span><span class="sxs-lookup"><span data-stu-id="a6804-113">Selection can be made from all containers.</span></span> <span data-ttu-id="a6804-114">Este é o tipo de seleção padrão.</span><span class="sxs-lookup"><span data-stu-id="a6804-114">This is the default selection type.</span></span> 
    
<span data-ttu-id="a6804-115">MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY</span><span class="sxs-lookup"><span data-stu-id="a6804-115">MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="a6804-116">A seleção pode ser feita somente a partir de contêineres de pasta.</span><span class="sxs-lookup"><span data-stu-id="a6804-116">Selection can be made only from folder containers.</span></span>
    
<span data-ttu-id="a6804-117">MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY</span><span class="sxs-lookup"><span data-stu-id="a6804-117">MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="a6804-118">A seleção pode ser feita apenas de contêineres que não estão associados a pastas.</span><span class="sxs-lookup"><span data-stu-id="a6804-118">Selection can be made only from containers that are not associated with folders.</span></span>
    
 <span data-ttu-id="a6804-119">_lppfcnt_</span><span class="sxs-lookup"><span data-stu-id="a6804-119">_lppfcnt_</span></span>
  
> <span data-ttu-id="a6804-120">bota Um ponteiro para um ponteiro para a interface retornada.</span><span class="sxs-lookup"><span data-stu-id="a6804-120">[out] A pointer to a pointer to the returned interface.</span></span> <span data-ttu-id="a6804-121">Essa interface é para o objeto Container selecionado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="a6804-121">This interface is for the container object that is selected by the user.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a6804-122">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a6804-122">Return value</span></span>

<span data-ttu-id="a6804-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="a6804-123">S_OK</span></span> 
  
> <span data-ttu-id="a6804-124">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="a6804-124">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a6804-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6804-125">Remarks</span></span>

<span data-ttu-id="a6804-126">Normalmente, os visualizadores de formulários chamam o método **IMAPIFormMgr:: SelectFormContainer** para selecionar um contêiner de formulários no qual um formulário está instalado.</span><span class="sxs-lookup"><span data-stu-id="a6804-126">Form viewers typically call the **IMAPIFormMgr::SelectFormContainer** method to select a form container into which a form is installed.</span></span> <span data-ttu-id="a6804-127">**SelectFormContainer** não pode ser usado para selecionar o contêiner de formulário local, que tem o valor HFRMREG_LOCAL.</span><span class="sxs-lookup"><span data-stu-id="a6804-127">**SelectFormContainer** cannot be used to select the local form container, which has the value HFRMREG_LOCAL.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a6804-128">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a6804-128">MFCMAPI reference</span></span>

<span data-ttu-id="a6804-129">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a6804-129">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a6804-130">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="a6804-130">**File**</span></span>|<span data-ttu-id="a6804-131">**Função**</span><span class="sxs-lookup"><span data-stu-id="a6804-131">**Function**</span></span>|<span data-ttu-id="a6804-132">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="a6804-132">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a6804-133">MainDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="a6804-133">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="a6804-134">CMainDlg:: OnSelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="a6804-134">CMainDlg::OnSelectFormContainer</span></span>  <br/> |<span data-ttu-id="a6804-135">MFCMAPI usa o método **IMAPIFormMgr:: SelectFormContainer** para selecionar um contêiner de formulário antes de renderizar seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="a6804-135">MFCMAPI uses the **IMAPIFormMgr::SelectFormContainer** method to select a form container before rendering its contents.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a6804-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6804-136">See also</span></span>



[<span data-ttu-id="a6804-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a6804-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="a6804-138">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="a6804-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

