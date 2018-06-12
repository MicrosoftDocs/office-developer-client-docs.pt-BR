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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: d329d3a14b6026d0bd62df9feba6ccff251e4151
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767016"
---
# <a name="imapiformcontainerinstallform"></a><span data-ttu-id="d5859-103">IMAPIFormContainer::InstallForm</span><span class="sxs-lookup"><span data-stu-id="d5859-103">IMAPIFormContainer::InstallForm</span></span>

  
  
<span data-ttu-id="d5859-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d5859-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d5859-105">Instala um formulário em uma biblioteca de formulários.</span><span class="sxs-lookup"><span data-stu-id="d5859-105">Installs a form into a form library.</span></span>
  
```cpp
HRESULT InstallForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR szCfgPathName
);
```

## <a name="parameters"></a><span data-ttu-id="d5859-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="d5859-106">Parameters</span></span>

 <span data-ttu-id="d5859-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="d5859-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="d5859-108">[in] Um identificador para a janela pai de todas as caixas de diálogo ou windows que esse método exibe.</span><span class="sxs-lookup"><span data-stu-id="d5859-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span> <span data-ttu-id="d5859-109">O parâmetro _ulUIParam_ é ignorado, a menos que o aplicativo cliente define o sinalizador MAPI_DIALOG no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="d5859-109">The  _ulUIParam_ parameter is ignored unless the client application sets the MAPI_DIALOG flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="d5859-110">O parâmetro _ulUIParam_ pode ser NULL se MAPI_DIALOG também não é passado.</span><span class="sxs-lookup"><span data-stu-id="d5859-110">The  _ulUIParam_ parameter can be NULL if MAPI_DIALOG is not also passed.</span></span> 
    
 <span data-ttu-id="d5859-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d5859-111">_ulFlags_</span></span>
  
> <span data-ttu-id="d5859-112">[in] Uma bitmask dos sinalizadores que controla a instalação do formulário.</span><span class="sxs-lookup"><span data-stu-id="d5859-112">[in] A bitmask of flags that controls the installation of the form.</span></span> <span data-ttu-id="d5859-113">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="d5859-113">The following flags can be set:</span></span>
    
<span data-ttu-id="d5859-114">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="d5859-114">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="d5859-115">Exibe uma caixa de diálogo para fornecer informações sobre o andamento ou solicita ao usuário para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="d5859-115">Displays a dialog box to provide progress information or prompt the user for more information.</span></span> <span data-ttu-id="d5859-116">Se esse sinalizador não estiver definida, nenhuma caixa de diálogo é exibida.</span><span class="sxs-lookup"><span data-stu-id="d5859-116">If this flag is not set, no dialog box is displayed.</span></span>
    
<span data-ttu-id="d5859-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d5859-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d5859-118">As cadeias de caracteres passada na estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="d5859-118">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="d5859-119">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="d5859-119">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="d5859-120">MAPIFORM_INSTALL_OVERWRITEONCONFLICT</span><span class="sxs-lookup"><span data-stu-id="d5859-120">MAPIFORM_INSTALL_OVERWRITEONCONFLICT</span></span> 
  
> <span data-ttu-id="d5859-121">Se outro formulário já existir que trata a classe de mensagem manipulada neste formulário, substitua o formulário existente por este.</span><span class="sxs-lookup"><span data-stu-id="d5859-121">If another form already exists that handles the message class handled by this form, replace the existing form with this one.</span></span> <span data-ttu-id="d5859-122">Esse sinalizador é ignorada se o sinalizador MAPI_DIALOG também está presente.</span><span class="sxs-lookup"><span data-stu-id="d5859-122">This flag is ignored if the MAPI_DIALOG flag is also present.</span></span> 
    
 <span data-ttu-id="d5859-123">_szCfgPathName_</span><span class="sxs-lookup"><span data-stu-id="d5859-123">_szCfgPathName_</span></span>
  
> <span data-ttu-id="d5859-124">[in] O caminho para o arquivo de configuração do formulário.</span><span class="sxs-lookup"><span data-stu-id="d5859-124">[in] The path to the form's configuration file.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d5859-125">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d5859-125">Return value</span></span>

<span data-ttu-id="d5859-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="d5859-126">S_OK</span></span> 
  
> <span data-ttu-id="d5859-127">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="d5859-127">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="d5859-128">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="d5859-128">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="d5859-129">Ocorreu um erro de implementação.</span><span class="sxs-lookup"><span data-stu-id="d5859-129">An implementation error occurred.</span></span> <span data-ttu-id="d5859-130">Para obter a estrutura [MAPIERROR](mapierror.md) que está associada com o erro, chame o método [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="d5859-130">To get the [MAPIERROR](mapierror.md) structure that is associated with the error, call the [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="d5859-131">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="d5859-131">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="d5859-132">O usuário cancelou a instalação do formulário, geralmente clicando no botão **Cancelar** em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d5859-132">The user canceled the installation of the form, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="d5859-133">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="d5859-133">Notes to implementers</span></span>

<span data-ttu-id="d5859-134">Provedores de biblioteca de formulário devem preencher uma estrutura **MAPIERROR** e retornar MAPI_E_EXTENDED_ERROR se qualquer uma das seguintes condições ocorrerem:</span><span class="sxs-lookup"><span data-stu-id="d5859-134">Form library providers should fill in a **MAPIERROR** structure and return MAPI_E_EXTENDED_ERROR if any of the following conditions occur:</span></span> 
  
- <span data-ttu-id="d5859-135">O arquivo de configuração não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="d5859-135">The configuration file is not found.</span></span>
    
- <span data-ttu-id="d5859-136">O arquivo de configuração não é legível.</span><span class="sxs-lookup"><span data-stu-id="d5859-136">The configuration file is not readable.</span></span>
    
- <span data-ttu-id="d5859-137">O arquivo de configuração é inválido.</span><span class="sxs-lookup"><span data-stu-id="d5859-137">The configuration file is invalid.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="d5859-138">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="d5859-138">Notes to callers</span></span>

<span data-ttu-id="d5859-139">Aplicativos cliente chamam o método de **IMAPIFormContainer::InstallForm** para instalar um formulário em um contêiner de formulário específico.</span><span class="sxs-lookup"><span data-stu-id="d5859-139">Client applications call the **IMAPIFormContainer::InstallForm** method to install a form into a specific form container.</span></span> <span data-ttu-id="d5859-140">O parâmetro _szCfgPathName_ deve conter o caminho de um arquivo de configuração de formulário (ou seja, um arquivo com a extensão. cfg que descreva o formulário e sua implementação).</span><span class="sxs-lookup"><span data-stu-id="d5859-140">The  _szCfgPathName_ parameter must contain the path of a form configuration file (that is, a file with the .cfg extension that describes the form and its implementation).</span></span> <span data-ttu-id="d5859-141">Os sinalizadores no parâmetro _ulFlags_ especificam o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d5859-141">The flags in the  _ulFlags_ parameter specify the following:</span></span> 
  
- <span data-ttu-id="d5859-142">Se o sinalizador MAPI_DIALOG estiver definido, uma interface do usuário é exibida, permitindo que o usuário que estiver instalando o formulário para especificar detalhes da instalação.</span><span class="sxs-lookup"><span data-stu-id="d5859-142">If the MAPI_DIALOG flag is set, a user interface is displayed, enabling the user who is installing the form to specify installation details.</span></span>
    
- <span data-ttu-id="d5859-143">Se o sinalizador MAPIFORM_INSTALL_OVERWRITEONCONFLICT estiver definido, qualquer formato anterior para a mesma classe de mensagem é substituído com o formulário está sendo instalado.</span><span class="sxs-lookup"><span data-stu-id="d5859-143">If the MAPIFORM_INSTALL_OVERWRITEONCONFLICT flag is set, any previous form for the same message class is replaced with the form being installed.</span></span> <span data-ttu-id="d5859-144">Caso contrário, a instalação do formulário é mesclada com a descrição do formulário atual, se houver uma.</span><span class="sxs-lookup"><span data-stu-id="d5859-144">Otherwise, the form installation is merged with the current form description, if one exists.</span></span>
    
- <span data-ttu-id="d5859-145">Se for definido MAPI_DIALOG, MAPIFORM_INSTALL_OVERWRITEONCONFLICT será ignorada.</span><span class="sxs-lookup"><span data-stu-id="d5859-145">If MAPI_DIALOG is set, MAPIFORM_INSTALL_OVERWRITEONCONFLICT is ignored.</span></span>
    
- <span data-ttu-id="d5859-146">A ausência de MAPIFORM_INSTALL_OVERWRITEONCONFLICT na sinalizar defina significa que uma mesclagem será feita.</span><span class="sxs-lookup"><span data-stu-id="d5859-146">The absence of MAPIFORM_INSTALL_OVERWRITEONCONFLICT in the flag set means that a merge will be done.</span></span> <span data-ttu-id="d5859-147">Quaisquer novas plataformas no arquivo. cfg que não estão presentes no momento na descrição do formulário serão instaladas e nenhuma outra alteração ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="d5859-147">Any new platforms in the .cfg file that are not currently present in the form description will be installed and no other changes will occur.</span></span>
    
- <span data-ttu-id="d5859-148">Se o sinalizador MAPI_UNICODE estiver definido, o caminho do arquivo de configuração de formulário é uma cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="d5859-148">If the MAPI_UNICODE flag is set, the path of the form configuration file is a Unicode string.</span></span> 
    
<span data-ttu-id="d5859-149">Clientes devem chamar [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) se **InstallForm** retorna MAPI_E_EXTENDED_ERROR, e eles devem verificar a estrutura [MAPIERROR](mapierror.md) retornada para determinar a condição que gerou o erro.</span><span class="sxs-lookup"><span data-stu-id="d5859-149">Clients should call [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) if **InstallForm** returns MAPI_E_EXTENDED_ERROR, and they should check the returned [MAPIERROR](mapierror.md) structure to determine the condition that raised the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d5859-150">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d5859-150">MFCMAPI reference</span></span>

<span data-ttu-id="d5859-151">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d5859-151">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d5859-152">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="d5859-152">**File**</span></span>|<span data-ttu-id="d5859-153">**Function**</span><span class="sxs-lookup"><span data-stu-id="d5859-153">**Function**</span></span>|<span data-ttu-id="d5859-154">**Comment**</span><span class="sxs-lookup"><span data-stu-id="d5859-154">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d5859-155">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="d5859-155">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="d5859-156">CFormContainerDlg::OnInstallForm</span><span class="sxs-lookup"><span data-stu-id="d5859-156">CFormContainerDlg::OnInstallForm</span></span>  <br/> |<span data-ttu-id="d5859-157">MFCMAPI usa o método **IMAPIFormContainer::InstallForm** para instalar um formulário em um contêiner de formulário.</span><span class="sxs-lookup"><span data-stu-id="d5859-157">MFCMAPI uses the **IMAPIFormContainer::InstallForm** method to install a form in a form container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d5859-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5859-158">See also</span></span>



[<span data-ttu-id="d5859-159">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="d5859-159">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="d5859-160">IMAPIFormContainer: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d5859-160">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="d5859-161">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="d5859-161">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

