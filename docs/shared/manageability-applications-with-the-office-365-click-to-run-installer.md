---
title: Integração de aplicativos de capacidade de gerenciamento com o instalador clique para executar do Microsoft 365
manager: lindalu
ms.date: 09/28/2020
ms.audience: ITPro
localization_priority: Normal
ms.assetid: c0fa8fed-1585-4566-a9be-ef6d6d1b4ce8
description: Saiba como integrar o instalador de clique para executar do Microsoft 365 Apps com uma solução de gerenciamento de software.
ms.openlocfilehash: eccd634f7906acf25b521ed2deb456ca914f37da
ms.sourcegitcommit: c8c51bd3f51c0a59fe44c014c8e56f1ba7c7aa03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/28/2020
ms.locfileid: "48297311"
---
# <a name="integrating-manageability-applications-with-microsoft-365-apps-click-to-run-installer"></a><span data-ttu-id="53e8c-103">Integração de aplicativos de capacidade de gerenciamento com o instalador clique para executar do Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="53e8c-103">Integrating manageability applications with Microsoft 365 Apps Click-to-Run installer</span></span>

<span data-ttu-id="53e8c-104">Saiba como integrar o instalador de clique para executar do Microsoft 365 Apps com uma solução de gerenciamento de software.</span><span class="sxs-lookup"><span data-stu-id="53e8c-104">Learn how to integrate the Microsoft 365 Apps Click-to-Run installer with a software management solution.</span></span>
  
<span data-ttu-id="53e8c-105">O instalador de clique para executar do Microsoft 365 Apps fornece uma interface COM que permite aos profissionais de ti e soluções de gerenciamento de software controlar o gerenciamento de atualizações.</span><span class="sxs-lookup"><span data-stu-id="53e8c-105">The Microsoft 365 Apps Click-to-Run installer provides a COM interface that allows IT Professionals and software management solutions programmatic control over update management.</span></span> <span data-ttu-id="53e8c-106">Essa interface tem recursos adicionais de gerenciamento além do que é fornecido pela Ferramenta de Implantação do Office.</span><span class="sxs-lookup"><span data-stu-id="53e8c-106">This interface provides additional management capabilities beyond what is provided by the Office Deployment Tool.</span></span>
  
> [!NOTE]
> <span data-ttu-id="53e8c-107">Este artigo aplica-se aos aplicativos do Office que usam o instalador clique para executar.</span><span class="sxs-lookup"><span data-stu-id="53e8c-107">This article applies to Office apps that use the Click-to-Run installer.</span></span> 
  
## <a name="integrating-with-the-click-to-run"></a><span data-ttu-id="53e8c-108">Integração ao Clique para Executar</span><span class="sxs-lookup"><span data-stu-id="53e8c-108">Integrating with the Click-to-Run</span></span>

<span data-ttu-id="53e8c-109">Para usar essa interface, um aplicativo de capacidade de gerenciamento invoca a interface COM e chama APIs expostas que se comunicam diretamente com o serviço de instalação Clique para Executar.</span><span class="sxs-lookup"><span data-stu-id="53e8c-109">To use this interface, a manageability application invokes the COM interface and calls exposed APIs that communicate directly with the Click-to-Run installation service.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="53e8c-110">O instalador Clique para Executar do Office pode ser executado na linha de comando com parâmetros que podem controlar o comportamento, conforme documentado em [Ferramenta de Implantação do Office para Clique para Executar](https://docs.microsoft.com/DeployOffice/overview-office-deployment-tool).</span><span class="sxs-lookup"><span data-stu-id="53e8c-110">The Office Click-to-Run installer can be run from the command-line with parameters that can control the behavior, as documented in [Office Deployment Tool for Click-to-Run](https://docs.microsoft.com/DeployOffice/overview-office-deployment-tool).</span></span> 
  
<span data-ttu-id="53e8c-111">**Veja a seguir um diagrama conceitual da interface COM**</span><span class="sxs-lookup"><span data-stu-id="53e8c-111">**Following is a conceptual diagram of the COM interface**</span></span>

<span data-ttu-id="53e8c-112">![Um diagrama usando a interface COM no instalador Clique para Executar do Office.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Um diagrama de usar a interface COM no instalador clique para executar do Office")</span><span class="sxs-lookup"><span data-stu-id="53e8c-112">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "A diagram of using the COM interface on  the Office Click-To-Run installer")</span></span>
  
<span data-ttu-id="53e8c-113">O instalador de clique para executar do Microsoft 365 apps implementa uma interface baseada em COM, **IUpdateNotify** registrado para CLSID **CLSID_UpdateNotifyObject**.</span><span class="sxs-lookup"><span data-stu-id="53e8c-113">The Microsoft 365 Apps Click-to-Run installer implements a COM-based interface, **IUpdateNotify** registered to CLSID **CLSID_UpdateNotifyObject**.</span></span>
  
<span data-ttu-id="53e8c-114">Essa interface pode ser invocada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="53e8c-114">This interface can be invoked as follows:</span></span>
  
```cpp
hr = CoCreateInstance(CLSID_UpdateNotifyObject, NULL, CLSCTX_ALL,
       IID_IUpdateNotify, 
      (void **)&p); 
```

<span data-ttu-id="53e8c-115">A chamada será bem-sucedida se o autor da chamada estiver em execução sob privilégios elevados, pois o programa de instalação Clique para Executar deve ser executado com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="53e8c-115">The call will only succeed if the caller is running under elevated privileges, as the Click-to-Run installation program must be run with elevated privileges.</span></span>
  
<span data-ttu-id="53e8c-116">A interface COM **IUpdateNotify** expõe três funções assíncronas responsáveis por validar os comandos e parâmetros, bem como agendar a execução com o serviço de instalação Clique para Executar.</span><span class="sxs-lookup"><span data-stu-id="53e8c-116">The **IUpdateNotify** COM interface exposes three asynchronous functions responsible for validating the commands and parameters and scheduling execution with the Click-to-Run installation service.</span></span> 
  
```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
HRESULT Cancel() // Cancel the download action.

```

<span data-ttu-id="53e8c-117">Um quarto método, **Status**, pode ser usado para obter informações sobre o status do último comando executado ou o status do comando em execução no momento (isto é, êxito, falha, códigos de erro detalhados).</span><span class="sxs-lookup"><span data-stu-id="53e8c-117">A forth method, **Status**, can be used to get information about the status of the last executed command or the status of the currently executing command (i.e. success, failure, detailed error codes).</span></span>
  
```cpp
HRESULT status([out] _UPDATE_STATUS_REPORT* pUpdateStatusReport) // Get status of current action. 
typedef struct _UPDATE_STATUS_REPORT  
{  
UPDATE_STATUS status;  
UINT error; 
BSTR contentid;  
} UPDATE_STATUS_REPORT;

```

<span data-ttu-id="53e8c-118">Há quatro estados em que o serviço de instalação Clique para Executar pode estar durante o seu ciclo de vida, durante o qual os métodos **IUpdateNotify** podem ser chamados; Reinicializando, Ocioso, Baixando e Aplicando.</span><span class="sxs-lookup"><span data-stu-id="53e8c-118">There are four states that the Click-to-Run installation service may be in during its lifecycle, during which **IUpdateNotify** methods may be called; Rebooting, Idle, Downloading and Applying.</span></span> 
  
<span data-ttu-id="53e8c-119">**Veja a seguir o diagrama de Máquina de Estado da interface COM**</span><span class="sxs-lookup"><span data-stu-id="53e8c-119">**Following is the COM Interface State Machine diagram**</span></span>

<span data-ttu-id="53e8c-120">![Um diagrama de estado da interface COM.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "Um diagrama de estado para a interface COM")</span><span class="sxs-lookup"><span data-stu-id="53e8c-120">![A state diagram for the COM interface.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "A state diagram for the COM interface")</span></span>
  
> [!NOTE]
> <span data-ttu-id="53e8c-121">**Reinicializando**: quando o computador está sendo inicializado, há um período em que o serviço instalador Clique para Executar fica indisponível.</span><span class="sxs-lookup"><span data-stu-id="53e8c-121">**Rebooting**: When the machine is booting there is a period of time when the Click-to-Run installer service is not available.</span></span> <span data-ttu-id="53e8c-122">Uma chamada bem-sucedida ao método Status após uma reinicialização retornará eUPDATE_UNKNOWN.</span><span class="sxs-lookup"><span data-stu-id="53e8c-122">A successful call to the Status method after a reboot will return eUPDATE_UNKNOWN.</span></span> 
  
<span data-ttu-id="53e8c-123">**Ocioso:** quando o instalador Clique para Executar estiver no estado ocioso, você poderá chamar:</span><span class="sxs-lookup"><span data-stu-id="53e8c-123">**Idle:** When the Click-to-Run installer is in the idle state, you can call:</span></span> 
  
- <span data-ttu-id="53e8c-124">**Aplicar**: instala o conteúdo anteriormente baixado.</span><span class="sxs-lookup"><span data-stu-id="53e8c-124">**Apply**: Install previously downloaded content.</span></span>
    
- <span data-ttu-id="53e8c-125">**Cancelar**: retorna `0x800000e`, "Um método foi chamado em um momento inesperado".</span><span class="sxs-lookup"><span data-stu-id="53e8c-125">**Cancel**: Returns  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="53e8c-126">**Baixar**: baixa novo conteúdo no cliente para instalação posterior.</span><span class="sxs-lookup"><span data-stu-id="53e8c-126">**Download**: Downloads new content to the client for later installation.</span></span>
    
- <span data-ttu-id="53e8c-127">**Status**: retorna o resultado da última ação concluída ou uma mensagem de erro se a ação terminou em falha.</span><span class="sxs-lookup"><span data-stu-id="53e8c-127">**Status**: Returns the result of the last completed action, or an error message if the action ended in failure.</span></span> <span data-ttu-id="53e8c-128">Se não houver ação anterior, **Status** retornará `eUPDATE_UNKNOWN`.</span><span class="sxs-lookup"><span data-stu-id="53e8c-128">If there is no previous action, **Status** returns  `eUPDATE_UNKNOWN`.</span></span>
    
<span data-ttu-id="53e8c-129">**Baixando:** quando o instalador Clique para Executar estiver no estado baixando, você poderá chamar:</span><span class="sxs-lookup"><span data-stu-id="53e8c-129">**Downloading:** When the Click-to-Run installer is in the downloading state, you can call:</span></span> 
  
- <span data-ttu-id="53e8c-130">**Aplicar**: retorna **HRESULT** com o valor `0x800000e`, "Um método foi chamado em um momento inesperado".</span><span class="sxs-lookup"><span data-stu-id="53e8c-130">**Apply**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="53e8c-131">**Cancelar**: interrompe o download e remove o conteúdo parcialmente baixado.</span><span class="sxs-lookup"><span data-stu-id="53e8c-131">**Cancel**: Stops the download and removes the partially downloaded content.</span></span>
    
- <span data-ttu-id="53e8c-132">**Baixar**: retorna **HRESULT** com o valor `0x800000e`, "Um método foi chamado em um momento inesperado".</span><span class="sxs-lookup"><span data-stu-id="53e8c-132">**Download**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span> 
    
- <span data-ttu-id="53e8c-133">**Status**: retorna **DOWNLOAD_WIP** para indicar que o trabalho de download está em andamento.</span><span class="sxs-lookup"><span data-stu-id="53e8c-133">**Status**: Returns **DOWNLOAD_WIP** to indicate that download work is in progress.</span></span> 
    
<span data-ttu-id="53e8c-134">**Aplicando:** quando o instalador Clique para Executar estiver no processo de instalação do conteúdo anteriormente baixado:</span><span class="sxs-lookup"><span data-stu-id="53e8c-134">**Applying:** When the Click-to-Run installer is in the process of installing previously download content:</span></span> 
  
- <span data-ttu-id="53e8c-135">**Aplicar**: retorna **HRESULT** com o valor `0x800000e`, "Um método foi chamado em um momento inesperado".</span><span class="sxs-lookup"><span data-stu-id="53e8c-135">**Apply**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="53e8c-136">**Cancelar**: retorna `0x800000e`, a ação Aplicar não pode ser cancelada.</span><span class="sxs-lookup"><span data-stu-id="53e8c-136">**Cancel**: Returns  `0x800000e`, the Apply action cannot be canceled.</span></span>
    
- <span data-ttu-id="53e8c-137">**Baixar**: retorna **HRESULT** com o valor `0x800000e`, "Um método foi chamado em um momento inesperado".</span><span class="sxs-lookup"><span data-stu-id="53e8c-137">**Download**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span> 
    
- <span data-ttu-id="53e8c-138">**Status**: retorna **APPLY_WIP** para indicar que o trabalho de aplicação está em andamento.</span><span class="sxs-lookup"><span data-stu-id="53e8c-138">**Status**: Returns **APPLY_WIP** to indicate that apply work is in progress.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="53e8c-139">Uma vez que OfficeC2RCOM é um serviço COM+ e foi dinamicamente carregado, é preciso chamar **CoCreateInstance** toda vez que você chama um método nessa classe, a fim de garantir a obtenção do resultado esperado.</span><span class="sxs-lookup"><span data-stu-id="53e8c-139">Since OfficeC2RCOM is a COM+ service and is dynamically loaded, you need to call **CoCreateInstance** every time you call a method on this class to ensure that you get the expected result.</span></span> <span data-ttu-id="53e8c-140">O serviço COM+ tratará de criar uma nova instância, se necessário.</span><span class="sxs-lookup"><span data-stu-id="53e8c-140">The COM+ service will handle creating a new instance if necessary.</span></span> <span data-ttu-id="53e8c-141">Quando um dos métodos é chamado pela primeira vez, COM+ carregará o objeto **IUpdateNotify** e o executará em uma das instâncias de dllhost.exe.</span><span class="sxs-lookup"><span data-stu-id="53e8c-141">When one of the methods is called for the first time, COM+ will load the **IUpdateNotify** object and run it within one of the dllhost.exe instances.</span></span> <span data-ttu-id="53e8c-142">O novo objeto permanecerá ativo por aproximadamente 3 minutos em estado ocioso.</span><span class="sxs-lookup"><span data-stu-id="53e8c-142">The new object will stay active for about 3 minutes in idle.</span></span> <span data-ttu-id="53e8c-143">Se uma chamada subsequente for feita dentro de três minutos, a contar da última chamada, o objeto **IUpdateNotify** permanecerá carregado e não será criada uma nova instância.</span><span class="sxs-lookup"><span data-stu-id="53e8c-143">If a subsequent call is made within three minutes of the last call, the **IUpdateNotify** object will remain loaded and a new instance is not created.</span></span> <span data-ttu-id="53e8c-144">Se nenhuma chamada for feita em três minutos, o objeto IUpdateNotify será descarregado e um novo objeto **IUpdateNotify** será criado quando a próxima chamada for feita.</span><span class="sxs-lookup"><span data-stu-id="53e8c-144">If no call is made within three minutes, the IUpdateNotify object will be unloaded and a new **IUpdateNotify** object will be created when the next call is made.</span></span> 
  
## <a name="click-to-run-installer-com-api-reference-guide"></a><span data-ttu-id="53e8c-145">Guia de referência da API COM do instalador Clique para Executar</span><span class="sxs-lookup"><span data-stu-id="53e8c-145">Click-to-Run installer COM API reference guide</span></span>

<span data-ttu-id="53e8c-146">Na seguinte documentação de referência de API:</span><span class="sxs-lookup"><span data-stu-id="53e8c-146">In the following API reference documentation:</span></span>
  
- <span data-ttu-id="53e8c-147">Os parâmetros estão em um formato de par chave/valor separados por um espaço.</span><span class="sxs-lookup"><span data-stu-id="53e8c-147">Parameters are in a key/value pair format separated by a space.</span></span>
    
- <span data-ttu-id="53e8c-148">Os parâmetros não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="53e8c-148">The parameters are not case-sensitive.</span></span>
    
- <span data-ttu-id="53e8c-149">Há uma [lista de parâmetros](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) com documentação disponível.</span><span class="sxs-lookup"><span data-stu-id="53e8c-149">There is a [list of parameters](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) with documentation available.</span></span> 
    
- <span data-ttu-id="53e8c-150">Agora, o resumo da interface IUpdateNotify2 está incluído.</span><span class="sxs-lookup"><span data-stu-id="53e8c-150">Summary of IUpdateNotify2 interface is now included.</span></span>
    
### <a name="apply"></a><span data-ttu-id="53e8c-151">Aplicar</span><span class="sxs-lookup"><span data-stu-id="53e8c-151">Apply</span></span>

```cpp
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
```

#### <a name="parameters"></a><span data-ttu-id="53e8c-152">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="53e8c-152">Parameters</span></span>

-  <span data-ttu-id="53e8c-153">_displaylevel_: **true** para mostrar o status da instalação, incluindo erros, durante o processo de atualização; **false** para ocultar o status da instalação, incluindo erros, durante o processo de atualização.</span><span class="sxs-lookup"><span data-stu-id="53e8c-153">_displaylevel_: **true** to show the installation status, including errors, during the update process; **false** to hide the installation status, including errors, during the update process.</span></span> <span data-ttu-id="53e8c-154">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="53e8c-154">The default is **false**.</span></span>
    
-  <span data-ttu-id="53e8c-155">_forceappshutdown_: **true** para forçar os aplicativos do Office a desligarem imediatamente quando a ação **Aplicar** for disparada; **false** para falha, se algum aplicativo do Office estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="53e8c-155">_forceappshutdown_: **true** to force Office applications to shut down immediately when the **Apply** action is triggered; **false** to fail if any Office applications are running.</span></span> <span data-ttu-id="53e8c-156">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="53e8c-156">The default is **false**.</span></span> <span data-ttu-id="53e8c-157">Veja [Comentários](#bk_ApplyRemark) para saber mais.</span><span class="sxs-lookup"><span data-stu-id="53e8c-157">See [Remarks](#bk_ApplyRemark) for more information.</span></span> 
    
  <span data-ttu-id="53e8c-158">Se algum aplicativo do Office estiver em execução quando a ação **Aplicar** for disparada, a ação **Aplicar** normalmente falha.</span><span class="sxs-lookup"><span data-stu-id="53e8c-158">If any Office application is running when the **Apply** action is triggered, the **Apply** action will usually fail.</span></span> <span data-ttu-id="53e8c-159">Passar `forceappshutdown=true` ao método **Aplicar** fará com que o serviço **OfficeClickToRun** desligue imediatamente os aplicativos e aplique a atualização.</span><span class="sxs-lookup"><span data-stu-id="53e8c-159">Passing  `forceappshutdown=true` to the **Apply** method will cause the **OfficeClickToRun** service to immediately shut down the applications and apply the update.</span></span> <span data-ttu-id="53e8c-160">O usuário poderá enfrentar perda de dados nesse caso.</span><span class="sxs-lookup"><span data-stu-id="53e8c-160">The user may experience data loss in this case.</span></span> 
    
#### <a name="return-results"></a><span data-ttu-id="53e8c-161">Retornar resultados</span><span class="sxs-lookup"><span data-stu-id="53e8c-161">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53e8c-162">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="53e8c-162">**S_OK**</span></span> <br/> |<span data-ttu-id="53e8c-163">A ação foi enviada com êxito ao serviço Clique para Executar para execução.</span><span class="sxs-lookup"><span data-stu-id="53e8c-163">Action was successfully submitted to the Click-To-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="53e8c-164">**E_ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="53e8c-164">**E_ACCESSDENIED**</span></span> <br/> |<span data-ttu-id="53e8c-165">O autor da chamada não está em execução com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="53e8c-165">The caller is not running with elevated privileges.</span></span>  <br/> |
|<span data-ttu-id="53e8c-166">**E_INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="53e8c-166">**E_INVALIDARG**</span></span> <br/> |<span data-ttu-id="53e8c-167">Parâmetros inválidos foram passados.</span><span class="sxs-lookup"><span data-stu-id="53e8c-167">Invalid parameters were passed.</span></span>  <br/> |
|<span data-ttu-id="53e8c-168">**E_ILLEGAL_METHOD_CALL**</span><span class="sxs-lookup"><span data-stu-id="53e8c-168">**E_ILLEGAL_METHOD_CALL**</span></span> <br/> |<span data-ttu-id="53e8c-169">A ação não é permitida neste momento.</span><span class="sxs-lookup"><span data-stu-id="53e8c-169">Action is not allowed at this time.</span></span> <span data-ttu-id="53e8c-170">Veja [Comentários](#bk_ApplyRemark) para saber mais.</span><span class="sxs-lookup"><span data-stu-id="53e8c-170">See [Remarks](#bk_ApplyRemark) for more information.</span></span>  <br/> |

<a name="bk_ApplyRemark"></a>

#### <a name="remarks"></a><span data-ttu-id="53e8c-171">Comentários</span><span class="sxs-lookup"><span data-stu-id="53e8c-171">Remarks</span></span>

- <span data-ttu-id="53e8c-172">Se algum aplicativo do Office estiver em execução quando a ação **Aplicar** for disparada, a ação **Aplicar** falhará.</span><span class="sxs-lookup"><span data-stu-id="53e8c-172">If any Office application is running when the **Apply** action is triggered, the **Apply** action will fail.</span></span> <span data-ttu-id="53e8c-173">Passar `forceappshutdown=true` ao método **Aplicar** fará com que o serviço **OfficeClickToRun** desligue imediatamente qualquer aplicativo do Office que esteja em execução e aplique a atualização.</span><span class="sxs-lookup"><span data-stu-id="53e8c-173">Passing  `forceappshutdown=true` to the **Apply** method will cause the **OfficeClickToRun** service to immediately shut down any Office applications that are running and apply the update.</span></span> <span data-ttu-id="53e8c-174">O usuário pode sofrer perda de dados, uma vez que não é solicitado que salve as alterações em documentos abertos.</span><span class="sxs-lookup"><span data-stu-id="53e8c-174">The user may experience data as they are not prompted to save changes to open documents..</span></span> 
    
- <span data-ttu-id="53e8c-175">Essa ação poderá ser disparada somente quando o status COM for um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="53e8c-175">This action can only be triggered when the COM status is one of the following:</span></span> 
    
  - <span data-ttu-id="53e8c-176">**eUPDATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="53e8c-176">**eUPDATE_UNKNOWN**</span></span>
    
  - <span data-ttu-id="53e8c-177">**eDOWNLOAD_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="53e8c-177">**eDOWNLOAD_CANCELLED**</span></span>
    
  - <span data-ttu-id="53e8c-178">**eDOWNLOAD_FAILED**</span><span class="sxs-lookup"><span data-stu-id="53e8c-178">**eDOWNLOAD_FAILED**</span></span>
    
  - <span data-ttu-id="53e8c-179">**eDOWNLOAD_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="53e8c-179">**eDOWNLOAD_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="53e8c-180">**eAPPLY_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="53e8c-180">**eAPPLY_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="53e8c-181">**eAPPLY_FAILED**</span><span class="sxs-lookup"><span data-stu-id="53e8c-181">**eAPPLY_FAILED**</span></span>
    
- <span data-ttu-id="53e8c-182">Se você chamar o método **Apply** sem baixar o conteúdo antes, o método **Apply** indicará **Êxito**, pois ele não detectou nada a ser aplicado e concluiu o processo **Apply** com êxito.</span><span class="sxs-lookup"><span data-stu-id="53e8c-182">If you call the **Apply** method without previously downloading content, the **Apply** method will report **Succeeded** as it detected nothing to apply and completed the **Apply** process successfully.</span></span> 
    
### <a name="cancel"></a><span data-ttu-id="53e8c-183">Cancelar</span><span class="sxs-lookup"><span data-stu-id="53e8c-183">Cancel</span></span>

```cpp
HRESULT Cancel() // Cancel the download action.
```

#### <a name="return-results"></a><span data-ttu-id="53e8c-184">Retornar resultados</span><span class="sxs-lookup"><span data-stu-id="53e8c-184">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53e8c-185">S_OK</span><span class="sxs-lookup"><span data-stu-id="53e8c-185">S_OK</span></span>  <br/> |<span data-ttu-id="53e8c-186">A ação foi enviada com êxito ao serviço Clique para Executar para execução.</span><span class="sxs-lookup"><span data-stu-id="53e8c-186">Action was successfully submitted to the Click-to-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="53e8c-187">E_ILLEGAL_METHOD_CALL</span><span class="sxs-lookup"><span data-stu-id="53e8c-187">E_ILLEGAL_METHOD_CALL</span></span>  <br/> |<span data-ttu-id="53e8c-188">A ação não é permitida neste momento.</span><span class="sxs-lookup"><span data-stu-id="53e8c-188">Action is not allowed at this time.</span></span> <span data-ttu-id="53e8c-189">Consulte a seção [Comentários](#bk_CancelRemarks) para obter mais informações</span><span class="sxs-lookup"><span data-stu-id="53e8c-189">See the [Remarks](#bk_CancelRemarks) section for more information</span></span>  <br/> |

<a name="bk_CancelRemarks"></a>

#### <a name="remarks"></a><span data-ttu-id="53e8c-190">Comentários</span><span class="sxs-lookup"><span data-stu-id="53e8c-190">Remarks</span></span>

- <span data-ttu-id="53e8c-191">Esse método poderá ser disparado somente quando o status COM for **eDOWNLOAD_WIP**.</span><span class="sxs-lookup"><span data-stu-id="53e8c-191">This method can only be triggered when the COM status id **eDOWNLOAD_WIP**.</span></span> <span data-ttu-id="53e8c-192">Ele tentará cancelar a ação de download atual.</span><span class="sxs-lookup"><span data-stu-id="53e8c-192">It will attempt to cancel the current download action.</span></span> <span data-ttu-id="53e8c-193">O status COM será alterado para **eDOWNLOAD_CANCELLING** e, por fim, para **eDOWNLOAD_CANCELED**.</span><span class="sxs-lookup"><span data-stu-id="53e8c-193">The COM status will change to **eDOWNLOAD_CANCELLING** and eventually change to **eDOWNLOAD_CANCELED**.</span></span> <span data-ttu-id="53e8c-194">O status COM retornará **E_ILLEGAL_METHOD_CALL** se disparado em qualquer outro momento.</span><span class="sxs-lookup"><span data-stu-id="53e8c-194">The COM status will return **E_ILLEGAL_METHOD_CALL** if triggered at any other time.</span></span> 
    
### <a name="download"></a><span data-ttu-id="53e8c-195">Baixar</span><span class="sxs-lookup"><span data-stu-id="53e8c-195">Download</span></span>

```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
```

#### <a name="parameters"></a><span data-ttu-id="53e8c-196">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="53e8c-196">Parameters</span></span>

-  <span data-ttu-id="53e8c-197">_displaylevel_: **true** para mostrar o status da instalação, incluindo erros, durante o processo de atualização; **false** para ocultar o status da instalação, incluindo erros, durante o processo de atualização.</span><span class="sxs-lookup"><span data-stu-id="53e8c-197">_displaylevel_: **true** to show the installation status, including errors, during the update process; **false** to hide the installation status, including errors, during the update process.</span></span> <span data-ttu-id="53e8c-198">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="53e8c-198">The default is **false**.</span></span>
    
-  <span data-ttu-id="53e8c-199">_updatebaseurl_: URL para a fonte alternativa de download.</span><span class="sxs-lookup"><span data-stu-id="53e8c-199">_updatebaseurl_: URL to the alternate download source.</span></span>
    
-  <span data-ttu-id="53e8c-200">_updatetoversion_: a versão para a qual atualizar o Office.</span><span class="sxs-lookup"><span data-stu-id="53e8c-200">_updatetoversion_: The version to update Office to.</span></span> <span data-ttu-id="53e8c-201">Defina esse parâmetro se desejar atualizar para um versão mais antiga do que a versão que está atualmente instalada.</span><span class="sxs-lookup"><span data-stu-id="53e8c-201">Define this parameter if you want to update to an older version than the version that is currently installed.</span></span>
    
-  <span data-ttu-id="53e8c-202">_downloadsource_: CLSID da implementação **IBackgroundCopyManager** personalizada (gerenciador do BITS).</span><span class="sxs-lookup"><span data-stu-id="53e8c-202">_downloadsource_: CLSID of the customized **IBackgroundCopyManager** implementation (BITS manager).</span></span> 
    
-  <span data-ttu-id="53e8c-203">_contentid_: identifica o conteúdo a ser baixado do servidor de conteúdo por meio do gerenciador do BITS personalizado.</span><span class="sxs-lookup"><span data-stu-id="53e8c-203">_contentid_: Identifies the content to download from the content server through the customized BITS manager.</span></span> <span data-ttu-id="53e8c-204">Esse valor é passado pela interface do BITS para interpretação.</span><span class="sxs-lookup"><span data-stu-id="53e8c-204">This value is passed through the BITS interface for interpretation.</span></span>
    
#### <a name="return-results"></a><span data-ttu-id="53e8c-205">Retornar resultados</span><span class="sxs-lookup"><span data-stu-id="53e8c-205">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53e8c-206">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="53e8c-206">**S_OK**</span></span> <br/> |<span data-ttu-id="53e8c-207">A ação foi enviada com êxito ao serviço Clique para Executar para execução.</span><span class="sxs-lookup"><span data-stu-id="53e8c-207">Action was successfully submitted to the Click-To-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="53e8c-208">**E_ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="53e8c-208">**E_ACCESSDENIED**</span></span> <br/> |<span data-ttu-id="53e8c-209">O autor da chamada não está em execução com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="53e8c-209">The caller is not running with elevated privileges.</span></span>  <br/> |
|<span data-ttu-id="53e8c-210">**E_INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="53e8c-210">**E_INVALIDARG**</span></span> <br/> |<span data-ttu-id="53e8c-211">Parâmetros inválidos foram passados.</span><span class="sxs-lookup"><span data-stu-id="53e8c-211">Invalid parameters were passed.</span></span>  <br/> |
|<span data-ttu-id="53e8c-212">**E_ILLEGAL_METHOD_CALL**</span><span class="sxs-lookup"><span data-stu-id="53e8c-212">**E_ILLEGAL_METHOD_CALL**</span></span> <br/> |<span data-ttu-id="53e8c-213">A ação não é permitida neste momento.</span><span class="sxs-lookup"><span data-stu-id="53e8c-213">Action is not allowed at this time.</span></span> <span data-ttu-id="53e8c-214">Veja [Comentários](#bk_DownloadRemark) para saber mais.</span><span class="sxs-lookup"><span data-stu-id="53e8c-214">See [Remarks](#bk_DownloadRemark) for more information.</span></span>  <br/> |

<a name="bk_DownloadRemark"></a>

#### <a name="remarks"></a><span data-ttu-id="53e8c-215">Comentários</span><span class="sxs-lookup"><span data-stu-id="53e8c-215">Remarks</span></span>

- <span data-ttu-id="53e8c-216">Você deve especificar _downloadsource_ e _contentid_ como um par.</span><span class="sxs-lookup"><span data-stu-id="53e8c-216">You must specify  _downloadsource_ and  _contentid_ as a pair.</span></span> <span data-ttu-id="53e8c-217">Caso contrário, o método **Baixar** retornará um erro **E_INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="53e8c-217">If not, the **Download** method will return an **E_INVALIDARG** error.</span></span> 
    
- <span data-ttu-id="53e8c-218">Se _downloadsource_, _contentid_ e _updatebaseurl_ forem fornecidos, _updatebaseurl_ será ignorado.</span><span class="sxs-lookup"><span data-stu-id="53e8c-218">If  _downloadsource_,  _contentid_, and  _updatebaseurl_ are provided,  _updatebaseurl_ will be ignored.</span></span> 
    
- <span data-ttu-id="53e8c-219">Essa ação poderá ser disparada somente quando o status COM for um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="53e8c-219">This action can only be triggered when the COM status is one of the following:</span></span> 
    
  - <span data-ttu-id="53e8c-220">**eUPDATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="53e8c-220">**eUPDATE_UNKNOWN**</span></span>
    
  - <span data-ttu-id="53e8c-221">**eDOWNLOAD_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="53e8c-221">**eDOWNLOAD_CANCELLED**</span></span>
    
  - <span data-ttu-id="53e8c-222">**eDOWNLOAD_FAILED**</span><span class="sxs-lookup"><span data-stu-id="53e8c-222">**eDOWNLOAD_FAILED**</span></span>
    
  - <span data-ttu-id="53e8c-223">**eDOWNLOAD_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="53e8c-223">**eDOWNLOAD_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="53e8c-224">**eAPPLY_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="53e8c-224">**eAPPLY_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="53e8c-225">**eAPPLY_FAILED**</span><span class="sxs-lookup"><span data-stu-id="53e8c-225">**eAPPLY_FAILED**</span></span>
    
- <span data-ttu-id="53e8c-226">Se você chamar o método **Apply** sem o conteúdo baixado anteriormente, o método **Apply** indicará **Êxito**, pois ele não detectou nada a ser aplicado e concluiu o processo **Apply** com êxito.</span><span class="sxs-lookup"><span data-stu-id="53e8c-226">If you call the **Apply** method without previously downloaded content, the **Apply** method will report **Succeeded** as it detected nothing to apply and completed the **Apply** process successfully.</span></span> 
    
#### <a name="examples"></a><span data-ttu-id="53e8c-227">Exemplos</span><span class="sxs-lookup"><span data-stu-id="53e8c-227">Examples</span></span>

- <span data-ttu-id="53e8c-228">Para baixar o conteúdo do gerenciador do BITS personalizado: chame a função **download()** passando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="53e8c-228">To download the content from the customized BITS manager: Call the **download()** function passing the following parameters:</span></span> 
    
  ```cpp
  "downloadsource=CLSIDofBITSInterface contentid=BITSServerContentIdentifier"
  ```

- <span data-ttu-id="53e8c-229">Para baixar o conteúdo da CDN (rede de distribuição de conteúdo) do Office: chame a função **Download ()** sem especificar os parâmetros de  _Download_,  _ContentId_ou  _updatebaseurl_ .</span><span class="sxs-lookup"><span data-stu-id="53e8c-229">To download the content from the Office Content Delivery Network (CDN): Call the **download()** function without specifying the  _downloadsource_,  _contentid_, or  _updatebaseurl_ parameters.</span></span> 
    
- <span data-ttu-id="53e8c-230">Para baixar o conteúdo de um local personalizado: chame a função **download()** passando o seguinte parâmetro:</span><span class="sxs-lookup"><span data-stu-id="53e8c-230">To download the content from a customized location: Call the **download()** function passing the following parameter:</span></span> 
    
  ```cpp
  "updatebaseurl=yourcontentserverurl"
  ```

### <a name="status"></a><span data-ttu-id="53e8c-231">Status</span><span class="sxs-lookup"><span data-stu-id="53e8c-231">Status</span></span>

```cpp
typdef struct _UPDATE_STATUS_REPORT
{
    UPDATE_STATUS status;
    UINT error;
    LPCWSTR contentid;
}UPDATE_STATUS_REPORT;
HRESULT status([out] _UPDATE_STATUS_REPORT& pUpdateStatusReport) // Get status of current action
```

#### <a name="parameters"></a><span data-ttu-id="53e8c-232">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="53e8c-232">Parameters</span></span>

|||
|:-----|:-----|
| <span data-ttu-id="53e8c-233">_pUpdateStatusReport_</span><span class="sxs-lookup"><span data-stu-id="53e8c-233">_pUpdateStatusReport_</span></span> <br/> |<span data-ttu-id="53e8c-234">Ponteiro para uma estrutura UPDATE_STATUS_REPORT.</span><span class="sxs-lookup"><span data-stu-id="53e8c-234">Pointer to an UPDATE_STATUS_REPORT structure.</span></span>  <br/> |
   
#### <a name="return-results"></a><span data-ttu-id="53e8c-235">Retornar resultados</span><span class="sxs-lookup"><span data-stu-id="53e8c-235">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53e8c-236">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="53e8c-236">**S_OK**</span></span> <br/> |<span data-ttu-id="53e8c-237">O método **Status** sempre retorna esse resultado.</span><span class="sxs-lookup"><span data-stu-id="53e8c-237">The **Status** method always returns this result.</span></span> <span data-ttu-id="53e8c-238">Inspecione a estrutura `UPDATE_STATUS_RESULT` para ver o status atual ação.</span><span class="sxs-lookup"><span data-stu-id="53e8c-238">Inspect the  `UPDATE_STATUS_RESULT` structure for the status of the current action.</span></span>  <br/> |
   
#### <a name="remarks"></a><span data-ttu-id="53e8c-239">Comentários</span><span class="sxs-lookup"><span data-stu-id="53e8c-239">Remarks</span></span>

- <span data-ttu-id="53e8c-240">O campo de status de `UPDATE_STATUS_REPORT` contém o status de ação atual.</span><span class="sxs-lookup"><span data-stu-id="53e8c-240">The status field of the  `UPDATE_STATUS_REPORT` contains the status of the current action.</span></span> <span data-ttu-id="53e8c-241">Um dos seguintes valores de status é retornado:</span><span class="sxs-lookup"><span data-stu-id="53e8c-241">One of the following status values is returned:</span></span> 
    
  ```cpp
  typedef enum _UPDATE_STATUS
  {
  eUPDATE_UNKNOWN = 0,
  eDOWNLOAD_PENDING,
  eDOWNLOAD_WIP,
  eDOWNLOAD_CANCELLING,
  eDOWNLOAD_CANCELLED,
  eDOWNLOAD_FAILED,
  eDOWNLOAD_SUCCEEDED,
  eAPPLY_PENDING,
  eAPPLY_WIP,
  eAPPLY_SUCCEEDED,
  eAPPLY_FAILED,
  } UPDATE_STATUS;
  
  ```

- <span data-ttu-id="53e8c-242">Se o último comando resultou em um erro, o campo de erro de `UPDATE_STATUS_REPORT` conterá informações detalhadas sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="53e8c-242">If the last command resulted in an error, the error field of the  `UPDATE_STATUS_REPORT` contains detailed information about the error.</span></span> <span data-ttu-id="53e8c-243">Dois tipos de código de erro são retornados do método **Status**.</span><span class="sxs-lookup"><span data-stu-id="53e8c-243">Two types of error codes are returned from the **Status** method.</span></span> 
    
- <span data-ttu-id="53e8c-244">Se o erro for inferior a `UPDATE_ERROR_CODE::eUNKNOWN`, o erro será um dos seguintes códigos de erro predefinidos:</span><span class="sxs-lookup"><span data-stu-id="53e8c-244">If the error less than  `UPDATE_ERROR_CODE::eUNKNOWN`, the error is one of the following pre-defined error codes:</span></span>
    
  ```cpp
  typedef enum _UPDATE_ERROR_CODE
  {
  eOK = 0,
  eFAILED_UNEXPECTED,
  eTRIGGER_DISABLED,
  ePIPELINE_IN_USE,
  eFAILED_STOP_C2RSERVICE,
  eFAILED_GET_CLIENTUPDATEFOLDER,
  eFAILED_LOCK_PACKAGE_TO_UPDATE,
  eFAILED_CREATE_STREAM_SESSION,
  eFAILED_PUBLISH_WORKING_CONFIGURATION,
  eFAILED_DOWNLOAD_UPGRADE_PACKAGE,
  eFAILED_APPLY_UPGRADE_PACKAGE,
  eFAILED_INITIALIZE_RSOD,
  eFAILED_PUBLISH_RSOD,
  // Keep this one as the last
  eUNKNOWN
  } UPDATE_ERROR_CODE;
  
  ```

  <span data-ttu-id="53e8c-245">Se um código de erro de retorno for superior a `UPDATE_ERROR_CODE::eUNKNOWN`, trata-se do **HRESULT** de uma chamada de função com falha.</span><span class="sxs-lookup"><span data-stu-id="53e8c-245">If the return error code is larger than  `UPDATE_ERROR_CODE::eUNKNOWN` it is the **HRESULT** of a failed function call.</span></span> <span data-ttu-id="53e8c-246">Para extrair o HRESULT, subtraia `UPDATE_ERROR_CODE::eUNKNOWN` do valor retornado no campo de erro de `UPDATE_STATUS_REPORT`.</span><span class="sxs-lookup"><span data-stu-id="53e8c-246">To extract the HRESULT subtract  `UPDATE_ERROR_CODE::eUNKNOWN` from the value returned in the error field of the  `UPDATE_STATUS_REPORT`.</span></span>
    
  <span data-ttu-id="53e8c-247">A lista completa de valores de status e erro pode ser exibida inspecionando a biblioteca de tipos **IUpdateNotify** inserida em OfficeC2RCom.dll.</span><span class="sxs-lookup"><span data-stu-id="53e8c-247">The complete list of status and error values can be viewed by inspecting the **IUpdateNotify** type library embedded in OfficeC2RCom.dll.</span></span> 
    
- <span data-ttu-id="53e8c-248">O campo contentid é usado para chamadas a **Status** depois que **Baixar** tiver sido iniciado e retornar o contentid que foi passado à chamada **Baixar**.</span><span class="sxs-lookup"><span data-stu-id="53e8c-248">The contentid field is used for calls to **Status** after **Download** has initiated and returns the contentid that was passed in to the **Download** call.</span></span> <span data-ttu-id="53e8c-249">É uma prática recomendada inicializar esse campo como **nulo** antes chamar o método **Status** e, em seguida, verificar o valor depois que **Status** tiver sido retornado.</span><span class="sxs-lookup"><span data-stu-id="53e8c-249">It is a best practice to initialize this field to **null** before you call the **Status** method and then check the value after **Status** has been returned.</span></span> <span data-ttu-id="53e8c-250">Se o valor ainda for **null**, isso significa que não há contentid a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="53e8c-250">If the value is still **null**, that means there is no contentid to return.</span></span> <span data-ttu-id="53e8c-251">Se o valor não for **null**, você precisará liberá-lo com um chamada a **SysFreeString()**.</span><span class="sxs-lookup"><span data-stu-id="53e8c-251">If the value is not **null**, you need to free it with a call to **SysFreeString()**.</span></span> <span data-ttu-id="53e8c-252">Veja um trecho de código de como chamar **Status** após **Baixar**.</span><span class="sxs-lookup"><span data-stu-id="53e8c-252">Here is a code snippet of how to call **Status** after **Download**.</span></span>
    
  ```cpp
  std::wstring contentID;
  UPDATE_STATUS_REPORT statusReport;
  statusReport.status = eUPDATE_UNKNOWN;
  statusReport.error = eOK;
  statusReport.contentid = NULL;
  hr = p->Status(&statusReport);
  if (statusReport.contentid != NULL)
  {
  contentID = statusReport.contentid;
  SysFreeString(statusReport.contentid);
  }
  wprintf(L"ContentID: %s, Status: %d, LastError: %d", contentID.c_str(), statusReport.status, statusReport.error);
  
  ```

### <a name="summary-of-iupdatenotify2-interface"></a><span data-ttu-id="53e8c-253">Resumo da interface IUpdateNotify2</span><span class="sxs-lookup"><span data-stu-id="53e8c-253">Summary of IUpdateNotify2 interface</span></span>

<span data-ttu-id="53e8c-254">Na versão [16.0.8208.6352] adicionamos uma nova interface **IUpdateNotify2** .</span><span class="sxs-lookup"><span data-stu-id="53e8c-254">From version [16.0.8208.6352] we have added a new **IUpdateNotify2** interface.</span></span> 
  
- <span data-ttu-id="53e8c-255">CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}</span><span class="sxs-lookup"><span data-stu-id="53e8c-255">CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}</span></span>
    
- <span data-ttu-id="53e8c-256">Essa interface também hospedava a interface IUpdateNotify original para fornecer compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="53e8c-256">This interface also hosted the original IUpdateNotify interface to provide backward compatibility.</span></span> <span data-ttu-id="53e8c-257">Isso significa que, ao usar essa interface, você terá acesso a todos os métodos fornecidos na interface **UpdateNotifyObject**.</span><span class="sxs-lookup"><span data-stu-id="53e8c-257">Which means if you use this interface, you have access to all the methods provided in **UpdateNotifyObject** interface.</span></span> 
    
- <span data-ttu-id="53e8c-258">Novos métodos adicionados a IUpdateNotify2:</span><span class="sxs-lookup"><span data-stu-id="53e8c-258">New methods added to IUpdateNotify2:</span></span>
    
  - <span data-ttu-id="53e8c-259">**HRESULT** GetBlockingApps([out] BSTR \* AppsList).</span><span class="sxs-lookup"><span data-stu-id="53e8c-259">**HRESULT** GetBlockingApps([out] BSTR \* AppsList).</span></span> <span data-ttu-id="53e8c-260">Obtenha a lista de aplicativos de bloqueio de atualizações.</span><span class="sxs-lookup"><span data-stu-id="53e8c-260">Get updates blocking apps list.</span></span> <span data-ttu-id="53e8c-261">Essa chamada retornará os aplicativos do Office em execução que impedirão o processo de atualização de prosseguir.</span><span class="sxs-lookup"><span data-stu-id="53e8c-261">This call will return running Office apps which will block the update process from proceeding.</span></span> 
    
  - <span data-ttu-id="53e8c-262">**HRESULT** GetOfficeDeploymentData([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR \* OfficeData).</span><span class="sxs-lookup"><span data-stu-id="53e8c-262">**HRESULT** GetOfficeDeploymentData([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR \* OfficeData).</span></span> <span data-ttu-id="53e8c-263">Obtenha os dados de implantação do Office.</span><span class="sxs-lookup"><span data-stu-id="53e8c-263">Get Office deployment Data.</span></span> 
    
- <span data-ttu-id="53e8c-264">Se desejar usar os novos métodos, você precisará garantir:</span><span class="sxs-lookup"><span data-stu-id="53e8c-264">If you want to use the new methods, you need to make sure:</span></span>
    
  - <span data-ttu-id="53e8c-265">Que a sua versão C2R seja mais nova do que o build acima (\> = build fork de junho).</span><span class="sxs-lookup"><span data-stu-id="53e8c-265">Your C2R version is newer than the above build (\>= June fork build).</span></span>
    
  - <span data-ttu-id="53e8c-266">O uso de UpdateNotifyObject2, em vez de **UpdateNotifyObject** para chamar **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="53e8c-266">Use UpdateNotifyObject2, instead of **UpdateNotifyObject** to call **CoCreateInstance**.</span></span>
    
<span data-ttu-id="53e8c-267">Se você não usar qualquer um dos métodos novos, não será necessário alterar nada.</span><span class="sxs-lookup"><span data-stu-id="53e8c-267">If you don't use any of the new methods, you don't need to change anything.</span></span> <span data-ttu-id="53e8c-268">Todos os métodos existentes funcionarão exatamente da mesma maneira que antes.</span><span class="sxs-lookup"><span data-stu-id="53e8c-268">All the existing methods will work as exact the same way as before.</span></span>
  
## <a name="implementing-the-bits-interface"></a><span data-ttu-id="53e8c-269">Como implantar a interface do BITS</span><span class="sxs-lookup"><span data-stu-id="53e8c-269">Implementing the BITS interface</span></span>

<span data-ttu-id="53e8c-270">O BITS ([Serviço de Transferência Inteligente em Segundo Plano](https://docs.microsoft.com/windows/win32/bits/background-intelligent-transfer-service-portal)) é um serviço fornecido pela Microsoft para transferir arquivos entre um cliente e um servidor.</span><span class="sxs-lookup"><span data-stu-id="53e8c-270">The [Background Intelligent Transfer Service](https://docs.microsoft.com/windows/win32/bits/background-intelligent-transfer-service-portal) (BITS) is a service provided by Microsoft to transfer files between a client and server.</span></span> <span data-ttu-id="53e8c-271">O BITS é um dos canais que o instalador Clique para Executar do Office pode usar para baixar conteúdo.</span><span class="sxs-lookup"><span data-stu-id="53e8c-271">BITS is one of the channels that Office Click-To-Run installer can use to download content.</span></span> <span data-ttu-id="53e8c-272">Por padrão, o instalador de clique para executar do Microsoft 365 aplicativos usa a implementação interna do BITS do Windows para baixar o conteúdo da CDN.</span><span class="sxs-lookup"><span data-stu-id="53e8c-272">By default, the Microsoft 365 Apps Click-To-Run installer uses the Windows' built in implementation of BITS to download the content from the CDN.</span></span> 
  
<span data-ttu-id="53e8c-273">Ao fornecer uma implementação do BITS personalizado ao método **download()** da interface **IUpdateNotify**, seu software de capacidade de gerenciamento pode controlar onde e como o cliente baixa o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="53e8c-273">By providing a customized BITS implementation to the **download()** method of the **IUpdateNotify** interface, your manageability software can control where and how the client downloads the content.</span></span> <span data-ttu-id="53e8c-274">Uma interface de BITS personalizada é útil ao fornecer um canal de distribuição de conteúdo personalizado que não seja o clique para executar canais internos, como a CDN, servidores IIS ou compartilhamentos de arquivos.</span><span class="sxs-lookup"><span data-stu-id="53e8c-274">A customized BITS interface is useful when providing a custom content distribution channel other than the Click-to-Run built-in channels, such as the CDN, IIS servers, or file shares.</span></span> 
  
<span data-ttu-id="53e8c-275">O requisito mínimo para uma interface do BITS personalizado trabalhar com o serviço C2R do Office é:</span><span class="sxs-lookup"><span data-stu-id="53e8c-275">The minimum requirement for a customized BITS interface to work with Office C2R service is:</span></span>
  
- <span data-ttu-id="53e8c-276">Para **IBackgroundCopyManager**:</span><span class="sxs-lookup"><span data-stu-id="53e8c-276">For **IBackgroundCopyManager**:</span></span>
    
  ```cpp
  HRESULT _stdcall CreateJob(
                      [in] LPWSTR DisplayName, 
                      [in] BG_JOB_TYPE Type, 
                      [out] GUID* pJobId, 
                      [out] IBackgroundCopyJob** ppJob)
  HRESULT _stdcall GetJob(
                      [in] GUID* jobID, 
                      [out] IBackgroundCopyJob** ppJob)
  HRESULT _stdcall EnumJobs(
                      [in] unsigned long dwFlags, 
                      [out] IEnumBackgroundCopyJobs** ppenum)
  
  ```

- <span data-ttu-id="53e8c-277">Para **IBackgroundCopyJob**:</span><span class="sxs-lookup"><span data-stu-id="53e8c-277">For **IBackgroundCopyJob**:</span></span>
    
  ```cpp
  HRESULT _stdcall AddFile(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName)
  HRESULT _stdcall Resume()
  HRESULT _stdcall Complete()
  HRESULT _stdcall Cancel();
  HRESULT _stdcall GetState([out] BG_JOB_STATE* pVal);
  HRESULT GetProgress( [out] BG_JOB_PROGRESS *pProgress);
  
  ```

- <span data-ttu-id="53e8c-278">Para **IBackgroundCopyJob3**:</span><span class="sxs-lookup"><span data-stu-id="53e8c-278">For **IBackgroundCopyJob3**:</span></span>
    
  ```cpp
  HRESULT _stdcall AddFileWithRanges(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName,
                      [in] DWORD RangeCount,
                      [in] BG_FILE_RANGE Ranges[])
  
  ```

- <span data-ttu-id="53e8c-279">Para as funções `Addfile` e `AddFileWithRanges`, a URL remota está no seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="53e8c-279">For the  `Addfile` and  `AddFileWithRanges` functions, the remote URL is in the following format:</span></span> 
    
  ```cpp
  cmbits://<contentid>/<relative path to target file>
  ```

  - <span data-ttu-id="53e8c-280">cmbits é embutido em código e significa o BITS personalizado.</span><span class="sxs-lookup"><span data-stu-id="53e8c-280">cmbits is hard coded, and stands for customized BITS.</span></span>
    
  -  <span data-ttu-id="53e8c-281">_\<contentid\>_ é o parâmetro  _ContentId_ para o método **Download ()** .</span><span class="sxs-lookup"><span data-stu-id="53e8c-281">_\<contentid\>_ is the  _contentid_ parameter for the **Download()** method.</span></span> 
    
  -  <span data-ttu-id="53e8c-282">_\<relative path to target file\>_ fornece o local e o nome do arquivo a ser baixado.</span><span class="sxs-lookup"><span data-stu-id="53e8c-282">_\<relative path to target file\>_ provides the location and file name of the file to download.</span></span> 
    
    <span data-ttu-id="53e8c-283">Por exemplo, se você tiver fornecido um _contentid_ de `f732af58-5d86-4299-abe9-7595c35136ef` ao método **Download()** e o C2R do Office quiser baixar o arquivo cab da versão, como o arquivo `v32.cab`, ele chamará **AddFile()** com o seguinte `RemoteUrl`:</span><span class="sxs-lookup"><span data-stu-id="53e8c-283">For example, if you have provided a  _contentid_ of  `f732af58-5d86-4299-abe9-7595c35136ef` to the **Download()** method, and Office C2R wants to download the version cab file, such as  `v32.cab` file, it will call **AddFile()** with the following  `RemoteUrl`:</span></span>
    
  ```cpp
  cmbits://f732af58-5d86-4299-abe9-7595c35136ef/Office/Data/V32.cab
  ```

- <span data-ttu-id="53e8c-284">Para **IBackgroundCopyError**:</span><span class="sxs-lookup"><span data-stu-id="53e8c-284">For **IBackgroundCopyError**:</span></span>
    
  ```cpp
  HRESULT _stdcall GetErrorDescription(
        [in]  DWORD  LanguageId,
        [out] LPWSTR *ppErrorDescription);
  
  ```

- <span data-ttu-id="53e8c-285">Para **IBackgroundCopyFile**:</span><span class="sxs-lookup"><span data-stu-id="53e8c-285">For **IBackgroundCopyFile**:</span></span>
    
  ```cpp
  HRESULT _stdcall GetLocalName([out] LPWSTR *ppName); 
  HRESULT _stdcall GetRemoteName([out] LPWSTR *ppName);
  
  ```
## <a name="automating-content-staging"></a><span data-ttu-id="53e8c-286">Como automatizar o preparo do conteúdo</span><span class="sxs-lookup"><span data-stu-id="53e8c-286">Automating content staging</span></span>

<span data-ttu-id="53e8c-287">Os administradores de ti podem optar por ter clientes de desktop habilitados para receber atualizações automaticamente quando estiverem disponíveis diretamente da CDN ou podem optar por controlar a implantação de atualizações disponíveis nos canais de atualização usando a ferramenta de implantação do Office ou o Microsoft Endpoint Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="53e8c-287">IT administrators can choose to have desktop clients enabled to automatically receive updates when they are available directly from the CDN or they can choose to control the deployment of updates available from the update channels using the Office Deployment Tool or Microsoft Endpoint Configuration Manager.</span></span>
  
<span data-ttu-id="53e8c-288">O serviço dá suporte à capacidade das ferramentas de gerenciamento de reconhecer e automatizar o download do conteúdo quando as atualizações são disponibilizadas.</span><span class="sxs-lookup"><span data-stu-id="53e8c-288">The service supports the ability for management tools to recognize and automate the download of the content when updates are made available.</span></span>
  
<span data-ttu-id="53e8c-289">**A imagem a seguir é uma visão geral de como baixar uma imagem personalizada**</span><span class="sxs-lookup"><span data-stu-id="53e8c-289">**The following image is an overview of downloading a custom image**</span></span>

<span data-ttu-id="53e8c-290">![Um diagrama usando a interface COM no instalador Clique para Executar do Office.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Um diagrama de usar a interface COM no instalador clique para executar do Office")</span><span class="sxs-lookup"><span data-stu-id="53e8c-290">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "A diagram of using the COM interface on the Office Click-To-Run installer")</span></span>
  
### <a name="overview-of-downloading-a-custom-image"></a><span data-ttu-id="53e8c-291">Visão geral de como baixar uma imagem personalizada</span><span class="sxs-lookup"><span data-stu-id="53e8c-291">Overview of downloading a custom image</span></span>
  
<span data-ttu-id="53e8c-292">No diagrama anterior, você vê que uma nova imagem do Microsoft 365 aplicativos está disponível na CDN.</span><span class="sxs-lookup"><span data-stu-id="53e8c-292">In the previous diagram, you see that a new Microsoft 365 Apps image is available on the CDN.</span></span> <span data-ttu-id="53e8c-293">Juntamente com a imagem de aplicativos do Microsoft 365, uma API está disponível, com as informações necessárias para habilitar o software de capacidade de criação para criar diretamente imagens personalizadas, substituindo a necessidade de usar a ferramenta de implantação do Office.</span><span class="sxs-lookup"><span data-stu-id="53e8c-293">Along with the Microsoft 365 Apps image, an API is available which has the information needed to enable manageability software to directly create customized images replacing the need for using the Office Deployment Tool.</span></span>

<span data-ttu-id="53e8c-294">Uma empresa configura o WSUS para sincronizar as atualizações do Microsoft 365 apps.</span><span class="sxs-lookup"><span data-stu-id="53e8c-294">An enterprise configures their WSUS to sync the Microsoft 365 Apps updates.</span></span> <span data-ttu-id="53e8c-295">Essas atualizações não contêm a carga real da imagem, mas permitem que o software de capacidade de gerenciamento reconheça quando conteúdo novo está disponível.</span><span class="sxs-lookup"><span data-stu-id="53e8c-295">These updates do not contain the actual image payload but does allow the manageability software to recognize when new content is available.</span></span> <span data-ttu-id="53e8c-296">O software de capacidade de gerenciamento pode ler os metadados de atualização de aplicativos do Microsoft 365 para entender a qual versão do Office a atualização se aplica.</span><span class="sxs-lookup"><span data-stu-id="53e8c-296">The manageability software can then read the Microsoft 365 Apps Update metadata to understand what version of Office the update applies to.</span></span>

<span data-ttu-id="53e8c-297">Se a atualização for aplicável, o software de capacidade de gerenciamento pode usar o conteúdo da CDN e a lista de arquivos para criar a imagem personalizada e armazená-la no local do compartilhamento de arquivos que ele está configurado para usar.</span><span class="sxs-lookup"><span data-stu-id="53e8c-297">If the update is applicable, the manageability software can use the CDN content and the file list to create the custom image and store it onto the file share location that it is configured to use.</span></span>
  
### <a name="using-the-microsoft-365-apps-file-list-api"></a><span data-ttu-id="53e8c-298">Usando a API de lista de arquivos de aplicativos do Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="53e8c-298">Using the Microsoft 365 Apps file list API</span></span>

<span data-ttu-id="53e8c-299">A API da lista de arquivos de aplicativos do Microsoft 365 é usada para recuperar os nomes dos arquivos necessários para uma atualização específica do Microsoft 365 apps.</span><span class="sxs-lookup"><span data-stu-id="53e8c-299">The Microsoft 365 Apps file list API is used to retrieve the names of the files needed for a particular Microsoft 365 Apps update.</span></span>

<span data-ttu-id="53e8c-300">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="53e8c-300">HTTP Request</span></span>

<span data-ttu-id="53e8c-301">GET https://config.office.com/api/filelist</span><span class="sxs-lookup"><span data-stu-id="53e8c-301">GET https://config.office.com/api/filelist</span></span>

<span data-ttu-id="53e8c-302">Não forneça um corpo de solicitação para esse método.</span><span class="sxs-lookup"><span data-stu-id="53e8c-302">Do not supply a request body for this method.</span></span>

<span data-ttu-id="53e8c-303">Nenhuma permissão é necessária para chamar esta API.</span><span class="sxs-lookup"><span data-stu-id="53e8c-303">No permissions are required to call this API.</span></span>

<span data-ttu-id="53e8c-304">Parâmetros de consulta opcionais</span><span class="sxs-lookup"><span data-stu-id="53e8c-304">Optional query parameters</span></span>

|<span data-ttu-id="53e8c-305">**Nome**</span><span class="sxs-lookup"><span data-stu-id="53e8c-305">**Name**</span></span>|<span data-ttu-id="53e8c-306">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="53e8c-306">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="53e8c-307">channel</span><span class="sxs-lookup"><span data-stu-id="53e8c-307">channel</span></span> <br/>| <span data-ttu-id="53e8c-308">Especifica o nome do canal</span><span class="sxs-lookup"><span data-stu-id="53e8c-308">Specifies the channel name</span></span>  <br/> <span data-ttu-id="53e8c-309">Opcional – padrão para ' semestral '</span><span class="sxs-lookup"><span data-stu-id="53e8c-309">Optional – default to ‘SemiAnnual’</span></span> <br/> <span data-ttu-id="53e8c-310">Valores com suporte https://docs.microsoft.com/DeployOffice/office-deployment-tool-configuration-options#channel-attribute-part-of-add-element</span><span class="sxs-lookup"><span data-stu-id="53e8c-310">Supported values https://docs.microsoft.com/DeployOffice/office-deployment-tool-configuration-options#channel-attribute-part-of-add-element</span></span> |
| <span data-ttu-id="53e8c-311">versão</span><span class="sxs-lookup"><span data-stu-id="53e8c-311">version</span></span> <br/>| <span data-ttu-id="53e8c-312">Especifica a versão de atualização</span><span class="sxs-lookup"><span data-stu-id="53e8c-312">Specifies the update version</span></span> <br/> <span data-ttu-id="53e8c-313">Opcional – o padrão é a versão mais recente disponível para o canal especificado</span><span class="sxs-lookup"><span data-stu-id="53e8c-313">Optional – defaults to the latest version available for the specified channel</span></span> |
| <span data-ttu-id="53e8c-314">arco</span><span class="sxs-lookup"><span data-stu-id="53e8c-314">arch</span></span> <br/>| <span data-ttu-id="53e8c-315">Especifica a arquitetura do cliente</span><span class="sxs-lookup"><span data-stu-id="53e8c-315">Specifies client architecture</span></span> <br/> <span data-ttu-id="53e8c-316">Opcional – o padrão é "x64"</span><span class="sxs-lookup"><span data-stu-id="53e8c-316">Optional – defaults to ‘x64’</span></span> <br/> <span data-ttu-id="53e8c-317">Valores com suporte: x64, x86</span><span class="sxs-lookup"><span data-stu-id="53e8c-317">Supported values: x64, x86</span></span> |
| <span data-ttu-id="53e8c-318">lid</span><span class="sxs-lookup"><span data-stu-id="53e8c-318">lid</span></span> <br/>| <span data-ttu-id="53e8c-319">Especifica os arquivos de idioma que serão incluídos</span><span class="sxs-lookup"><span data-stu-id="53e8c-319">Specifies the language files to include</span></span> <br/> <span data-ttu-id="53e8c-320">Opcional – padrão para nenhum</span><span class="sxs-lookup"><span data-stu-id="53e8c-320">Optional – defaults to none</span></span> <br/> <span data-ttu-id="53e8c-321">Para especificar vários idiomas, inclua um parâmetro de consulta tampa para cada idioma</span><span class="sxs-lookup"><span data-stu-id="53e8c-321">To specify multiple languages, include an lid query parameter for each language</span></span> <br/> <span data-ttu-id="53e8c-322">Use o formato de identificador de idioma, ex.</span><span class="sxs-lookup"><span data-stu-id="53e8c-322">Use the language identifier format, ex.</span></span> <span data-ttu-id="53e8c-323">"pt-br", "fr-fr"</span><span class="sxs-lookup"><span data-stu-id="53e8c-323">‘en-us’, ‘fr-fr’</span></span> |
| <span data-ttu-id="53e8c-324">idiomas</span><span class="sxs-lookup"><span data-stu-id="53e8c-324">alllanguages</span></span> <br/>| <span data-ttu-id="53e8c-325">Especifica a inclusão de todos os arquivos de idioma</span><span class="sxs-lookup"><span data-stu-id="53e8c-325">Specifies to include all language files</span></span> <br/> <span data-ttu-id="53e8c-326">Opcional – o padrão é false</span><span class="sxs-lookup"><span data-stu-id="53e8c-326">Optional – defaults to false</span></span> |

<span data-ttu-id="53e8c-327">Resposta HTTP</span><span class="sxs-lookup"><span data-stu-id="53e8c-327">HTTP Response</span></span>

<span data-ttu-id="53e8c-328">Se bem-sucedido, este método retorna um código de resposta de OK 200 e uma coleção de objetos File no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="53e8c-328">If successful, this method returns a 200 OK response code and collection of file objects in the response body.</span></span>

<span data-ttu-id="53e8c-329">Para criar uma imagem, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="53e8c-329">To create an image, follow these steps:</span></span>
1.  <span data-ttu-id="53e8c-330">Chame a API, fornecendo os parâmetros de consulta apropriados para o canal, a versão e a arquitetura da atualização em que você está interessado.</span><span class="sxs-lookup"><span data-stu-id="53e8c-330">Call the API, providing the appropriate query parameters for the channel, version and architecture of the update you are interested in.</span></span>
<span data-ttu-id="53e8c-331">Observação: objetos de arquivo com o atributo "LCID": "0" são arquivos neutros de idioma e devem ser incluídos na imagem.</span><span class="sxs-lookup"><span data-stu-id="53e8c-331">Note: File objects with the attribute "lcid": "0" are language neutral files and must be included in the image.</span></span>
2.  <span data-ttu-id="53e8c-332">Construa uma imagem local da CDN Iterando pelos objetos de arquivo e copiando os arquivos de CDN, enquanto cria a estrutura de pastas, conforme especificado pelo atributo "relativePath", definido para cada um dos objetos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="53e8c-332">Construct a local image of the CDN by iterating through the file objects and copying the CDN files, while creating the folder structure as specified by the “relativePath” attribute defined for each of the file objects.</span></span>

<span data-ttu-id="53e8c-333">O exemplo a seguir recupera a lista de arquivos para o canal atual e a versão 16.0.4229.1004 para 64 bits e inclui os arquivos de idioma francês e inglês:</span><span class="sxs-lookup"><span data-stu-id="53e8c-333">The following example retrieves the file list for the Current Channel and version 16.0.4229.1004 for 64bit and includes the French and English language files:</span></span>

```http
Get https://config.office.com/api/filelist?Channel=Current&Version=16.0.4229.1004&Arch=x64&Lid=fr-fr&Lid=en-US
```

### <a name="hash-verification-of-dat-files"></a><span data-ttu-id="53e8c-334">Verificação de hash de arquivos .dat</span><span class="sxs-lookup"><span data-stu-id="53e8c-334">Hash verification of .dat files</span></span>

<span data-ttu-id="53e8c-335">As ferramentas de criação de imagem podem verificar a integridade dos arquivos. dat baixados comparando um valor de hash calculado com o valor de hash fornecido associado a cada um dos arquivos. dat.</span><span class="sxs-lookup"><span data-stu-id="53e8c-335">Image creation tools may verify the integrity of the downloaded .dat files by comparing a computed hash value with the supplied hash value associated with each of the .dat files.</span></span> <span data-ttu-id="53e8c-336">Veja a seguir um exemplo de um objeto File que especifica os valores hashLocation e hashAlgorithm:</span><span class="sxs-lookup"><span data-stu-id="53e8c-336">Following is an example of a file object that specifies hashLocation and hashAlgorithm values:</span></span>
  
```xml
{
  "url": "https://officecdn.microsoft.com/pr/7ffbc6bf-bc32-4f92-8982-f9dd17fd3114/office/data/16.0.1234.1001/stream.x64.x-none.dat",
  "name": "stream.x64.x-none.dat",
  "relativePath": "/office/data/16.0.1234.1001/",
  "hashLocation": "s640.cab/stream.x64.x-none.hash",
  "hashAlgorithm": "Sha256",
  "lcid": "0"
},
```

- <span data-ttu-id="53e8c-337">O atributo **hashLocation** especifica o local do caminho relativo do arquivo. cab que contém o valor de hash.</span><span class="sxs-lookup"><span data-stu-id="53e8c-337">The **hashLocation** attribute specifies the relative path location of .cab file that contains the hash value.</span></span> <span data-ttu-id="53e8c-338">Crie o local do arquivo hash concatenando a URL + relativePath + hashLocation.</span><span class="sxs-lookup"><span data-stu-id="53e8c-338">Construct the hash file location by concatenating URL + relativePath + hashLocation.</span></span> <span data-ttu-id="53e8c-339">No seguinte exemplo, o local stream.x64.bg-bg.hash seria:</span><span class="sxs-lookup"><span data-stu-id="53e8c-339">In the following example, the stream.x64.bg-bg.hash location would be:</span></span> 
    
  ```http
  https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
  ```

- <span data-ttu-id="53e8c-340">O atributo **hashAlgorithm** especifica qual algoritmo de hash foi usado.</span><span class="sxs-lookup"><span data-stu-id="53e8c-340">The **hashAlgorithm** attribute specifies what hashing algorithm was used.</span></span> 
    
  <span data-ttu-id="53e8c-341">Para validar a integridade do arquivo stream.x64.bg-bg.dat, abra o stream.x64.bg-bg.hash e leia o valor do HASH, que é a primeira linha do texto no arquivo de hash.</span><span class="sxs-lookup"><span data-stu-id="53e8c-341">To validate the integrity of the stream.x64.bg-bg.dat file, open the stream.x64.bg-bg.hash and read the HASH value which is the first line of text in the hash file.</span></span> <span data-ttu-id="53e8c-342">Compare-o com o valor do hash calculado (usando o algoritmo de hash especificado) para verificar a integridade do arquivo .dat baixado.</span><span class="sxs-lookup"><span data-stu-id="53e8c-342">Compare this to the computed hash value (using the specified hashing algorithm) to verify the integrity of the downloaded .dat file.</span></span>
    
  <span data-ttu-id="53e8c-343">O exemplo a seguir mostra o código C# para leitura do hash.</span><span class="sxs-lookup"><span data-stu-id="53e8c-343">The following example shows the C# code to read the hash.</span></span>
    
  ```cs
    string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
    string readHash = readHashes.First();
  ```

### <a name="microsoft-365-apps-updates"></a><span data-ttu-id="53e8c-344">Atualizações de aplicativos do Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="53e8c-344">Microsoft 365 Apps Updates</span></span>

<span data-ttu-id="53e8c-345">Todas as atualizações de aplicativos do Microsoft 365 são publicadas no [catálogo do Microsoft Update](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).</span><span class="sxs-lookup"><span data-stu-id="53e8c-345">All Microsoft 365 Apps Updates are published to the [Microsoft Update Catalog](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).</span></span>
  
<span data-ttu-id="53e8c-346">As atualizações de aplicativos do Microsoft 365 permitem que o software de capacidade de gerenciamento trate as atualizações dos aplicativos da Microsoft 365 de uma maneira muito semelhante a qualquer outra atualização do WU, com uma exceção; as atualizações do cliente não contêm uma carga real.</span><span class="sxs-lookup"><span data-stu-id="53e8c-346">Microsoft 365 Apps Updates enable manageability software to treat Microsoft 365 Apps Updates in a manner very similar to any other WU update with one exception; the client updates do not contain an actual payload.</span></span> <span data-ttu-id="53e8c-347">As atualizações de aplicativos do 365 da Microsoft não devem ser instaladas em nenhum cliente, mas sim para disparar os fluxos de trabalho com o software de capacidade de gerenciamento que substitui o comando de instalação pelo mecanismo de instalação com base no COM, mostrado acima.</span><span class="sxs-lookup"><span data-stu-id="53e8c-347">The Microsoft 365 Apps Updates should not be installed on any clients but rather used to trigger the workflows with the manageability software replacing the installation command with the COM based installation mechanism shown above.</span></span>

<span data-ttu-id="53e8c-348">**A figura a seguir mostra um diagrama do fluxo de trabalho da Atualização de Cliente do Office 365.**</span><span class="sxs-lookup"><span data-stu-id="53e8c-348">**The following figure shows a diagram of the Office 365 Client Update workflow.**</span></span>

<span data-ttu-id="53e8c-349">![Diagrama de fluxo de trabalho de atualizações do cliente O365PP .](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Diagrama de fluxo de trabalho para atualizações do cliente O365PP")</span><span class="sxs-lookup"><span data-stu-id="53e8c-349">![Workflow diagram for O365PP client updates.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Workflow diagram for O365PP client updates")</span></span>
  
<span data-ttu-id="53e8c-350">Cada atualização de aplicativos do Microsoft 365 publicada inclui metadados sobre a atualização.</span><span class="sxs-lookup"><span data-stu-id="53e8c-350">Each Microsoft 365 Apps Update that is published includes metadata about the update.</span></span> <span data-ttu-id="53e8c-351">Estes metadados incluem um parâmetro chamado MoreInfoUrl que pode ser usado para derivar a chamada de API para a API da lista de arquivos para essa atualização específica.</span><span class="sxs-lookup"><span data-stu-id="53e8c-351">This metadata includes a parameter called MoreInfoUrl which can be used to derive the API call to the file list API for that specific update.</span></span>

<span data-ttu-id="53e8c-352">No exemplo a seguir, a API da lista de arquivos é incorporada no MoreInfoURL e começa com "InPath ="</span><span class="sxs-lookup"><span data-stu-id="53e8c-352">In the following example, the file list API is embedded in the MoreInfoURL and starts with “ServicePath=”</span></span>

<span data-ttu-id="53e8c-353">http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.12527.21104&Branch=Insiders&Arch=64&XMLVer=1.6&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml& Caminho do próprio =https://config.office.com/api/filelist?Channel=Insiders&Version=16.0.12527.21104&Arch=64&AllLanguages=True</span><span class="sxs-lookup"><span data-stu-id="53e8c-353">http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.12527.21104&Branch=Insiders&Arch=64&XMLVer=1.6&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml& ServicePath=https://config.office.com/api/filelist?Channel=Insiders&Version=16.0.12527.21104&Arch=64&AllLanguages=True</span></span>
  
### <a name="additional-metadata-for-automating-content-staging"></a><span data-ttu-id="53e8c-354">Metadados adicionais para automatização do preparo de conteúdo</span><span class="sxs-lookup"><span data-stu-id="53e8c-354">Additional metadata for automating content staging</span></span>

<span data-ttu-id="53e8c-355">**API de histórico de versão**</span><span class="sxs-lookup"><span data-stu-id="53e8c-355">**Release History API**</span></span>
  
<span data-ttu-id="53e8c-356">A API de histórico de lançamento do Microsoft 365 apps é usada para recuperar os detalhes de cada uma das atualizações publicadas na CDN junto com os nomes dos canais e outros atributos do canal.</span><span class="sxs-lookup"><span data-stu-id="53e8c-356">The Microsoft 365 Apps release history API is used to retrieve details for each of the updates published to the CDN along with the channel names and other channel attributes.</span></span>

<span data-ttu-id="53e8c-357">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="53e8c-357">HTTP Request</span></span>

```http
GET https://config.office.com/api/filelist/channels 
```

<span data-ttu-id="53e8c-358">Não forneça um corpo de solicitação para esse método.</span><span class="sxs-lookup"><span data-stu-id="53e8c-358">Do not supply a request body for this method.</span></span>

<span data-ttu-id="53e8c-359">Nenhuma permissão é necessária para chamar esta API.</span><span class="sxs-lookup"><span data-stu-id="53e8c-359">No permissions are required to call this API.</span></span>

<span data-ttu-id="53e8c-360">Resposta HTTP</span><span class="sxs-lookup"><span data-stu-id="53e8c-360">HTTP Response</span></span>

<span data-ttu-id="53e8c-361">Se bem-sucedido, este método retorna um código de resposta de OK 200 e uma coleção de objetos File no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="53e8c-361">If successful, this method returns a 200 OK response code and collection of file objects in the response body.</span></span>

<span data-ttu-id="53e8c-362">**API de SKUs**</span><span class="sxs-lookup"><span data-stu-id="53e8c-362">**SKUs API**</span></span>
  
<span data-ttu-id="53e8c-363">A API SKUs retorna informações que são úteis para determinar quais produtos estão disponíveis para implantação e manutenção da CDN do Office juntamente com várias opções para cada um deles.</span><span class="sxs-lookup"><span data-stu-id="53e8c-363">The SKUs API returns information that is useful for determining which products are available for deployment and servicing from the Office CDN along with various options for each.</span></span>

<span data-ttu-id="53e8c-364">Solicitação HTTP</span><span class="sxs-lookup"><span data-stu-id="53e8c-364">HTTP Request</span></span>

```http
GET https://config.office.com/api/filelist/skus 
```

<span data-ttu-id="53e8c-365">Não forneça um corpo de solicitação para esse método.</span><span class="sxs-lookup"><span data-stu-id="53e8c-365">Do not supply a request body for this method.</span></span>

<span data-ttu-id="53e8c-366">Nenhuma permissão é necessária para chamar esta API.</span><span class="sxs-lookup"><span data-stu-id="53e8c-366">No permissions are required to call this API.</span></span>

<span data-ttu-id="53e8c-367">Resposta HTTP</span><span class="sxs-lookup"><span data-stu-id="53e8c-367">HTTP Response</span></span>

<span data-ttu-id="53e8c-368">Se bem-sucedido, este método retorna um código de resposta de OK 200 e uma coleção de objetos File no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="53e8c-368">If successful, this method returns a 200 OK response code and collection of file objects in the response body.</span></span>
