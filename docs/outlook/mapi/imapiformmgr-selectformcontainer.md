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
ms.openlocfilehash: f66d0fb1fc9d252ff8b6985c4a54de79313266d1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577923"
---
# <a name="imapiformmgrselectformcontainer"></a><span data-ttu-id="fca94-103">IMAPIFormMgr::SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="fca94-103">IMAPIFormMgr::SelectFormContainer</span></span>

  
  
<span data-ttu-id="fca94-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fca94-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fca94-105">Apresenta uma caixa de diálogo que permite que o usuário selecione um contêiner de formulário e retorna uma interface para o objeto de contêiner do usuário selecionado.</span><span class="sxs-lookup"><span data-stu-id="fca94-105">Presents a dialog box that enables the user to select a form container, and returns an interface for the container object the user selected.</span></span>
  
```cpp
HRESULT SelectFormContainer(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="fca94-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fca94-106">Parameters</span></span>

 <span data-ttu-id="fca94-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="fca94-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="fca94-108">[in] Uma alça para a janela pai da caixa de diálogo exibida.</span><span class="sxs-lookup"><span data-stu-id="fca94-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="fca94-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fca94-109">_ulFlags_</span></span>
  
> <span data-ttu-id="fca94-110">[in] Uma bitmask dos sinalizadores que controla como a biblioteca de formulários está selecionada (ou seja, como o contêiner de formulário estiver selecionado).</span><span class="sxs-lookup"><span data-stu-id="fca94-110">[in] A bitmask of flags that controls how the form library is selected (that is, how the form container is selected).</span></span> <span data-ttu-id="fca94-111">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="fca94-111">The following flags can be set:</span></span>
    
<span data-ttu-id="fca94-112">MAPIFORM_SELECT_ALL_REGISTRIES</span><span class="sxs-lookup"><span data-stu-id="fca94-112">MAPIFORM_SELECT_ALL_REGISTRIES</span></span> 
  
> <span data-ttu-id="fca94-113">Pode ser feita a seleção de todos os contêineres.</span><span class="sxs-lookup"><span data-stu-id="fca94-113">Selection can be made from all containers.</span></span> <span data-ttu-id="fca94-114">Este é o tipo de seleção padrão.</span><span class="sxs-lookup"><span data-stu-id="fca94-114">This is the default selection type.</span></span> 
    
<span data-ttu-id="fca94-115">MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY</span><span class="sxs-lookup"><span data-stu-id="fca94-115">MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="fca94-116">Seleção pode ser feita apenas dos contêineres de pasta.</span><span class="sxs-lookup"><span data-stu-id="fca94-116">Selection can be made only from folder containers.</span></span>
    
<span data-ttu-id="fca94-117">MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY</span><span class="sxs-lookup"><span data-stu-id="fca94-117">MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="fca94-118">Seleção pode ser feita apenas dos contêineres que não estão associados a pastas.</span><span class="sxs-lookup"><span data-stu-id="fca94-118">Selection can be made only from containers that are not associated with folders.</span></span>
    
 <span data-ttu-id="fca94-119">_lppfcnt_</span><span class="sxs-lookup"><span data-stu-id="fca94-119">_lppfcnt_</span></span>
  
> <span data-ttu-id="fca94-120">[out] Um ponteiro para um ponteiro para a interface retornada.</span><span class="sxs-lookup"><span data-stu-id="fca94-120">[out] A pointer to a pointer to the returned interface.</span></span> <span data-ttu-id="fca94-121">Esta interface é para o objeto de contêiner que está selecionado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="fca94-121">This interface is for the container object that is selected by the user.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fca94-122">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="fca94-122">Return value</span></span>

<span data-ttu-id="fca94-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="fca94-123">S_OK</span></span> 
  
> <span data-ttu-id="fca94-124">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="fca94-124">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fca94-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="fca94-125">Remarks</span></span>

<span data-ttu-id="fca94-126">Visualizadores de formulário normalmente chame o método de **IMAPIFormMgr::SelectFormContainer** para selecionar um recipiente de formulário em que um formulário está instalado.</span><span class="sxs-lookup"><span data-stu-id="fca94-126">Form viewers typically call the **IMAPIFormMgr::SelectFormContainer** method to select a form container into which a form is installed.</span></span> <span data-ttu-id="fca94-127">**SelectFormContainer** não pode ser usado para selecionar o contêiner de formulário local, que tem o valor HFRMREG_LOCAL.</span><span class="sxs-lookup"><span data-stu-id="fca94-127">**SelectFormContainer** cannot be used to select the local form container, which has the value HFRMREG_LOCAL.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="fca94-128">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="fca94-128">MFCMAPI reference</span></span>

<span data-ttu-id="fca94-129">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="fca94-129">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fca94-130">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="fca94-130">**File**</span></span>|<span data-ttu-id="fca94-131">**Function**</span><span class="sxs-lookup"><span data-stu-id="fca94-131">**Function**</span></span>|<span data-ttu-id="fca94-132">**Comment**</span><span class="sxs-lookup"><span data-stu-id="fca94-132">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fca94-133">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="fca94-133">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="fca94-134">CMainDlg::OnSelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="fca94-134">CMainDlg::OnSelectFormContainer</span></span>  <br/> |<span data-ttu-id="fca94-135">MFCMAPI usa o método **IMAPIFormMgr::SelectFormContainer** para selecionar um contêiner de formulário antes de renderizar seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="fca94-135">MFCMAPI uses the **IMAPIFormMgr::SelectFormContainer** method to select a form container before rendering its contents.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fca94-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="fca94-136">See also</span></span>



[<span data-ttu-id="fca94-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fca94-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="fca94-138">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="fca94-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

