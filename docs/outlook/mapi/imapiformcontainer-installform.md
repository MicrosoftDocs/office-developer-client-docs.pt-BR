---
title: IMAPIFormContainerInstallForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.InstallForm
api_type:
- COM
ms.assetid: b39ca52c-4dbe-41c0-9e1b-3998a9dc9742
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a0650033e4fea79046eac5757e3d0deb963c38e6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405083"
---
# <a name="imapiformcontainerinstallform"></a><span data-ttu-id="e4c45-103">IMAPIFormContainer::InstallForm</span><span class="sxs-lookup"><span data-stu-id="e4c45-103">IMAPIFormContainer::InstallForm</span></span>

  
  
<span data-ttu-id="e4c45-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4c45-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4c45-105">Instala um formulário em uma biblioteca de formulário.</span><span class="sxs-lookup"><span data-stu-id="e4c45-105">Installs a form into a form library.</span></span>
  
```cpp
HRESULT InstallForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR szCfgPathName
);
```

## <a name="parameters"></a><span data-ttu-id="e4c45-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4c45-106">Parameters</span></span>

 <span data-ttu-id="e4c45-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="e4c45-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="e4c45-108">[in] Um alça para a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe.</span><span class="sxs-lookup"><span data-stu-id="e4c45-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span> <span data-ttu-id="e4c45-109">O _parâmetro ulUIParam é_ ignorado, a menos que o aplicativo cliente defina o MAPI_DIALOG padrão no parâmetro _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="e4c45-109">The  _ulUIParam_ parameter is ignored unless the client application sets the MAPI_DIALOG flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="e4c45-110">O  _parâmetro ulUIParam_ poderá ser NULL se MAPI_DIALOG também for passado.</span><span class="sxs-lookup"><span data-stu-id="e4c45-110">The  _ulUIParam_ parameter can be NULL if MAPI_DIALOG is not also passed.</span></span> 
    
 <span data-ttu-id="e4c45-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e4c45-111">_ulFlags_</span></span>
  
> <span data-ttu-id="e4c45-112">[in] Uma máscara de bits de sinalizadores que controla a instalação do formulário.</span><span class="sxs-lookup"><span data-stu-id="e4c45-112">[in] A bitmask of flags that controls the installation of the form.</span></span> <span data-ttu-id="e4c45-113">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="e4c45-113">The following flags can be set:</span></span>
    
<span data-ttu-id="e4c45-114">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="e4c45-114">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="e4c45-115">Exibe uma caixa de diálogo para fornecer informações de progresso ou solicitar ao usuário mais informações.</span><span class="sxs-lookup"><span data-stu-id="e4c45-115">Displays a dialog box to provide progress information or prompt the user for more information.</span></span> <span data-ttu-id="e4c45-116">Se esse sinalizador não estiver definido, nenhuma caixa de diálogo será exibida.</span><span class="sxs-lookup"><span data-stu-id="e4c45-116">If this flag is not set, no dialog box is displayed.</span></span>
    
<span data-ttu-id="e4c45-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e4c45-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e4c45-118">As cadeias de caracteres passadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="e4c45-118">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="e4c45-119">Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="e4c45-119">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="e4c45-120">MAPIFORM_INSTALL_OVERWRITEONCONFLICT</span><span class="sxs-lookup"><span data-stu-id="e4c45-120">MAPIFORM_INSTALL_OVERWRITEONCONFLICT</span></span> 
  
> <span data-ttu-id="e4c45-121">If another form already exists that handles the message class handled by this form, replace the existing form with this one.</span><span class="sxs-lookup"><span data-stu-id="e4c45-121">If another form already exists that handles the message class handled by this form, replace the existing form with this one.</span></span> <span data-ttu-id="e4c45-122">Esse sinalizador será ignorado se o sinalizador MAPI_DIALOG também estiver presente.</span><span class="sxs-lookup"><span data-stu-id="e4c45-122">This flag is ignored if the MAPI_DIALOG flag is also present.</span></span> 
    
 <span data-ttu-id="e4c45-123">_szCfgPathName_</span><span class="sxs-lookup"><span data-stu-id="e4c45-123">_szCfgPathName_</span></span>
  
> <span data-ttu-id="e4c45-124">[in] O caminho para o arquivo de configuração do formulário.</span><span class="sxs-lookup"><span data-stu-id="e4c45-124">[in] The path to the form's configuration file.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e4c45-125">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e4c45-125">Return value</span></span>

<span data-ttu-id="e4c45-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="e4c45-126">S_OK</span></span> 
  
> <span data-ttu-id="e4c45-127">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="e4c45-127">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="e4c45-128">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="e4c45-128">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="e4c45-129">Ocorreu um erro de implementação.</span><span class="sxs-lookup"><span data-stu-id="e4c45-129">An implementation error occurred.</span></span> <span data-ttu-id="e4c45-130">Para obter a [estrutura MAPIERROR](mapierror.md) associada ao erro, chame o método [IMAPIFormContainer::GetLastError.](imapiformcontainer-getlasterror.md)</span><span class="sxs-lookup"><span data-stu-id="e4c45-130">To get the [MAPIERROR](mapierror.md) structure that is associated with the error, call the [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="e4c45-131">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="e4c45-131">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="e4c45-132">O usuário cancelou a instalação do formulário, normalmente clicando no botão **Cancelar** em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e4c45-132">The user canceled the installation of the form, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="e4c45-133">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="e4c45-133">Notes to implementers</span></span>

<span data-ttu-id="e4c45-134">Os provedores de biblioteca de formulário devem preencher uma estrutura **MAPIERROR** e retornar MAPI_E_EXTENDED_ERROR caso ocorra uma das seguintes condições:</span><span class="sxs-lookup"><span data-stu-id="e4c45-134">Form library providers should fill in a **MAPIERROR** structure and return MAPI_E_EXTENDED_ERROR if any of the following conditions occur:</span></span> 
  
- <span data-ttu-id="e4c45-135">O arquivo de configuração não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="e4c45-135">The configuration file is not found.</span></span>
    
- <span data-ttu-id="e4c45-136">O arquivo de configuração não pode ser lido.</span><span class="sxs-lookup"><span data-stu-id="e4c45-136">The configuration file is not readable.</span></span>
    
- <span data-ttu-id="e4c45-137">O arquivo de configuração é inválido.</span><span class="sxs-lookup"><span data-stu-id="e4c45-137">The configuration file is invalid.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="e4c45-138">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="e4c45-138">Notes to callers</span></span>

<span data-ttu-id="e4c45-139">Os aplicativos cliente chamam **o método IMAPIFormContainer::InstallForm** para instalar um formulário em um contêiner de formulário específico.</span><span class="sxs-lookup"><span data-stu-id="e4c45-139">Client applications call the **IMAPIFormContainer::InstallForm** method to install a form into a specific form container.</span></span> <span data-ttu-id="e4c45-140">O  _parâmetro szCfgPathName_ deve conter o caminho de um arquivo de configuração de formulário (ou seja, um arquivo com a extensão .cfg que descreve o formulário e sua implementação).</span><span class="sxs-lookup"><span data-stu-id="e4c45-140">The  _szCfgPathName_ parameter must contain the path of a form configuration file (that is, a file with the .cfg extension that describes the form and its implementation).</span></span> <span data-ttu-id="e4c45-141">Os sinalizadores no  _parâmetro ulFlags_ especificam o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e4c45-141">The flags in the  _ulFlags_ parameter specify the following:</span></span> 
  
- <span data-ttu-id="e4c45-142">Se o MAPI_DIALOG sinalizador estiver definido, uma interface do usuário será exibida, permitindo que o usuário que está instalando o formulário especifique detalhes de instalação.</span><span class="sxs-lookup"><span data-stu-id="e4c45-142">If the MAPI_DIALOG flag is set, a user interface is displayed, enabling the user who is installing the form to specify installation details.</span></span>
    
- <span data-ttu-id="e4c45-143">Se o MAPIFORM_INSTALL_OVERWRITEONCONFLICT sinalizador estiver definido, qualquer formulário anterior para a mesma classe de mensagem será substituído pelo formulário que está sendo instalado.</span><span class="sxs-lookup"><span data-stu-id="e4c45-143">If the MAPIFORM_INSTALL_OVERWRITEONCONFLICT flag is set, any previous form for the same message class is replaced with the form being installed.</span></span> <span data-ttu-id="e4c45-144">Caso contrário, a instalação do formulário será mesclada com a descrição do formulário atual, se houver uma.</span><span class="sxs-lookup"><span data-stu-id="e4c45-144">Otherwise, the form installation is merged with the current form description, if one exists.</span></span>
    
- <span data-ttu-id="e4c45-145">Se MAPI_DIALOG estiver definido, MAPIFORM_INSTALL_OVERWRITEONCONFLICT será ignorado.</span><span class="sxs-lookup"><span data-stu-id="e4c45-145">If MAPI_DIALOG is set, MAPIFORM_INSTALL_OVERWRITEONCONFLICT is ignored.</span></span>
    
- <span data-ttu-id="e4c45-146">A ausência de MAPIFORM_INSTALL_OVERWRITEONCONFLICT no conjunto de sinalizadores significa que uma mesclagem será feita.</span><span class="sxs-lookup"><span data-stu-id="e4c45-146">The absence of MAPIFORM_INSTALL_OVERWRITEONCONFLICT in the flag set means that a merge will be done.</span></span> <span data-ttu-id="e4c45-147">Todas as novas plataformas no arquivo .cfg que não estão presentes no momento na descrição do formulário serão instaladas e nenhuma outra alteração ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="e4c45-147">Any new platforms in the .cfg file that are not currently present in the form description will be installed and no other changes will occur.</span></span>
    
- <span data-ttu-id="e4c45-148">Se o MAPI_UNICODE padrão estiver definido, o caminho do arquivo de configuração de formulário será uma cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="e4c45-148">If the MAPI_UNICODE flag is set, the path of the form configuration file is a Unicode string.</span></span> 
    
<span data-ttu-id="e4c45-149">Os clientes devem chamar [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) se **InstallForm** retornar MAPI_E_EXTENDED_ERROR e eles devem verificar a estrutura [MAPIERROR](mapierror.md) retornada para determinar a condição que gerou o erro.</span><span class="sxs-lookup"><span data-stu-id="e4c45-149">Clients should call [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) if **InstallForm** returns MAPI_E_EXTENDED_ERROR, and they should check the returned [MAPIERROR](mapierror.md) structure to determine the condition that raised the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e4c45-150">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e4c45-150">MFCMAPI reference</span></span>

<span data-ttu-id="e4c45-151">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e4c45-151">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e4c45-152">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="e4c45-152">**File**</span></span>|<span data-ttu-id="e4c45-153">**Função**</span><span class="sxs-lookup"><span data-stu-id="e4c45-153">**Function**</span></span>|<span data-ttu-id="e4c45-154">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="e4c45-154">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e4c45-155">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="e4c45-155">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="e4c45-156">CFormContainerDlg::OnInstallForm</span><span class="sxs-lookup"><span data-stu-id="e4c45-156">CFormContainerDlg::OnInstallForm</span></span>  <br/> |<span data-ttu-id="e4c45-157">MFCMAPI usa o **método IMAPIFormContainer::InstallForm** para instalar um formulário em um contêiner de formulário.</span><span class="sxs-lookup"><span data-stu-id="e4c45-157">MFCMAPI uses the **IMAPIFormContainer::InstallForm** method to install a form in a form container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e4c45-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4c45-158">See also</span></span>



[<span data-ttu-id="e4c45-159">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="e4c45-159">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="e4c45-160">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e4c45-160">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="e4c45-161">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="e4c45-161">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

