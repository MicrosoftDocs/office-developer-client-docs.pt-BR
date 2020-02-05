---
title: Como integrar aplicativos de capacidade de gerenciamento ao instalador clique para executar do Office 365
manager: lindalu
ms.date: 10/22/2017
ms.audience: ITPro
localization_priority: Normal
ms.assetid: c0fa8fed-1585-4566-a9be-ef6d6d1b4ce8
description: Aprenda a integrar o instalador Clique para Executar do Office 365 a uma solução de gerenciamento de software.
ms.openlocfilehash: 0c695d538a0a906bce19719c2735cb39740ff6a2
ms.sourcegitcommit: 31b0a7373ff74fe1d6383c30bc67d7675b73d283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2020
ms.locfileid: "41773733"
---
# <a name="integrating-manageability-applications-with-office-365-click-to-run-installer"></a><span data-ttu-id="19c67-103">Como integrar aplicativos de capacidade de gerenciamento ao instalador clique para executar do Office 365</span><span class="sxs-lookup"><span data-stu-id="19c67-103">Integrating manageability applications with Office 365 click-to-run installer</span></span>

<span data-ttu-id="19c67-104">Aprenda a integrar o instalador Clique para Executar do Office 365 a uma solução de gerenciamento de software.</span><span class="sxs-lookup"><span data-stu-id="19c67-104">Learn how to integrate the Office 365 Click-to-Run installer with a software management solution.</span></span>
  
<span data-ttu-id="19c67-105">O instalador Clique para Executar do Office 365 fornece uma interface COM que permite aos Profissionais de TI e soluções de gerenciamento de software controle programático sobre o gerenciamento de atualizações.</span><span class="sxs-lookup"><span data-stu-id="19c67-105">The Office 365 Click-to-Run installer provides a COM interface that allows IT Professionals and software management solutions programmatic control over update management.</span></span> <span data-ttu-id="19c67-106">Essa interface tem recursos adicionais de gerenciamento além do que é fornecido pela Ferramenta de Implantação do Office.</span><span class="sxs-lookup"><span data-stu-id="19c67-106">This interface provides additional management capabilities beyond what is provided by the Office Deployment Tool.</span></span>
  
> [!NOTE]
> <span data-ttu-id="19c67-107">Este artigo aplica-se ao Office 2016 e posterior, bem como ao Office 365.</span><span class="sxs-lookup"><span data-stu-id="19c67-107">This article applies to Office 2016 and later, Office 365.</span></span> 
  
## <a name="integrating-with-the-click-to-run"></a><span data-ttu-id="19c67-108">Integração ao Clique para Executar</span><span class="sxs-lookup"><span data-stu-id="19c67-108">Integrating with the Click-to-Run</span></span>

<span data-ttu-id="19c67-109">Para usar essa interface, um aplicativo de capacidade de gerenciamento invoca a interface COM e chama APIs expostas que se comunicam diretamente com o serviço de instalação Clique para Executar.</span><span class="sxs-lookup"><span data-stu-id="19c67-109">To use this interface, a manageability application invokes the COM interface and calls exposed APIs that communicate directly with the Click-to-Run installation service.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="19c67-110">O instalador Clique para Executar do Office pode ser executado na linha de comando com parâmetros que podem controlar o comportamento, conforme documentado em [Ferramenta de Implantação do Office para Clique para Executar](https://www.microsoft.com/download/details.aspx?id=49117).</span><span class="sxs-lookup"><span data-stu-id="19c67-110">The Office Click-to-Run installer can be run from the command-line with parameters that can control the behavior, as documented in [Office Deployment Tool for Click-to-Run](https://www.microsoft.com/download/details.aspx?id=49117).</span></span> 
  
<span data-ttu-id="19c67-111">**Veja a seguir um diagrama conceitual da interface COM**</span><span class="sxs-lookup"><span data-stu-id="19c67-111">**Following is a conceptual diagram of the COM interface**</span></span>

<span data-ttu-id="19c67-112">![Um diagrama usando a interface COM no instalador Clique para Executar do Office.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Um diagrama de usar a interface COM no instalador clique para executar do Office")</span><span class="sxs-lookup"><span data-stu-id="19c67-112">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "A diagram of using the COM interface on  the Office Click-To-Run installer")</span></span>
  
<span data-ttu-id="19c67-113">O instalador Clique para Executar do Office 365 implementa uma interface baseada em COM, **IUpdateNotify**, registrada na CLSID **CLSID_UpdateNotifyObject**.</span><span class="sxs-lookup"><span data-stu-id="19c67-113">The Office 365 Click-to-Run installer implements a COM-based interface, **IUpdateNotify** registered to CLSID **CLSID_UpdateNotifyObject**.</span></span>
  
<span data-ttu-id="19c67-114">Essa interface pode ser invocada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="19c67-114">This interface can be invoked as follows:</span></span>
  
```cpp
hr = CoCreateInstance(CLSID_UpdateNotifyObject, NULL, CLSCTX_ALL,
       IID_IUpdateNotify, 
      (void **)&p); 
```

<span data-ttu-id="19c67-115">A chamada será bem-sucedida se o autor da chamada estiver em execução sob privilégios elevados, pois o programa de instalação Clique para Executar deve ser executado com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="19c67-115">The call will only succeed if the caller is running under elevated privileges, as the Click-to-Run installation program must be run with elevated privileges.</span></span>
  
<span data-ttu-id="19c67-116">A interface COM **IUpdateNotify** expõe três funções assíncronas responsáveis por validar os comandos e parâmetros, bem como agendar a execução com o serviço de instalação Clique para Executar.</span><span class="sxs-lookup"><span data-stu-id="19c67-116">The **IUpdateNotify** COM interface exposes three asynchronous functions responsible for validating the commands and parameters and scheduling execution with the Click-to-Run installation service.</span></span> 
  
```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
HRESULT Cancel() // Cancel the download action.

```

<span data-ttu-id="19c67-117">Um quarto método, **Status**, pode ser usado para obter informações sobre o status do último comando executado ou o status do comando em execução no momento (isto é, êxito, falha, códigos de erro detalhados).</span><span class="sxs-lookup"><span data-stu-id="19c67-117">A forth method, **Status**, can be used to get information about the status of the last executed command or the status of the currently executing command (i.e. success, failure, detailed error codes).</span></span>
  
```cpp
HRESULT status([out] _UPDATE_STATUS_REPORT* pUpdateStatusReport) // Get status of current action. 
typedef struct _UPDATE_STATUS_REPORT  
{  
UPDATE_STATUS status;  
UINT error; 
BSTR contentid;  
} UPDATE_STATUS_REPORT;

```

<span data-ttu-id="19c67-118">Há quatro estados em que o serviço de instalação Clique para Executar pode estar durante o seu ciclo de vida, durante o qual os métodos **IUpdateNotify** podem ser chamados; Reinicializando, Ocioso, Baixando e Aplicando.</span><span class="sxs-lookup"><span data-stu-id="19c67-118">There are four states that the Click-to-Run installation service may be in during its lifecycle, during which **IUpdateNotify** methods may be called; Rebooting, Idle, Downloading and Applying.</span></span> 
  
<span data-ttu-id="19c67-119">**Veja a seguir o diagrama de Máquina de Estado da interface COM**</span><span class="sxs-lookup"><span data-stu-id="19c67-119">**Following is the COM Interface State Machine diagram**</span></span>

<span data-ttu-id="19c67-120">![Um diagrama de estado da interface COM.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "Um diagrama de estado para a interface COM")</span><span class="sxs-lookup"><span data-stu-id="19c67-120">![A state diagram for the COM interface.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "A state diagram for the COM interface")</span></span>
  
> [!NOTE]
> <span data-ttu-id="19c67-121">**Reinicializando**: quando o computador está sendo inicializado, há um período em que o serviço instalador Clique para Executar fica indisponível.</span><span class="sxs-lookup"><span data-stu-id="19c67-121">**Rebooting**: When the machine is booting there is a period of time when the Click-to-Run installer service is not available.</span></span> <span data-ttu-id="19c67-122">Uma chamada bem-sucedida ao método Status após uma reinicialização retornará eUPDATE_UNKNOWN.</span><span class="sxs-lookup"><span data-stu-id="19c67-122">A successful call to the Status method after a reboot will return eUPDATE_UNKNOWN.</span></span> 
  
<span data-ttu-id="19c67-123">**Ocioso:** quando o instalador Clique para Executar estiver no estado ocioso, você poderá chamar:</span><span class="sxs-lookup"><span data-stu-id="19c67-123">**Idle:** When the Click-to-Run installer is in the idle state, you can call:</span></span> 
  
- <span data-ttu-id="19c67-124">**Aplicar**: instala o conteúdo anteriormente baixado.</span><span class="sxs-lookup"><span data-stu-id="19c67-124">**Apply**: Install previously downloaded content.</span></span>
    
- <span data-ttu-id="19c67-125">**Cancelar**: retorna `0x800000e`, "Um método foi chamado em um momento inesperado".</span><span class="sxs-lookup"><span data-stu-id="19c67-125">**Cancel**: Returns  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="19c67-126">**Baixar**: baixa novo conteúdo no cliente para instalação posterior.</span><span class="sxs-lookup"><span data-stu-id="19c67-126">**Download**: Downloads new content to the client for later installation.</span></span>
    
- <span data-ttu-id="19c67-127">**Status**: retorna o resultado da última ação concluída ou uma mensagem de erro se a ação terminou em falha.</span><span class="sxs-lookup"><span data-stu-id="19c67-127">**Status**: Returns the result of the last completed action, or an error message if the action ended in failure.</span></span> <span data-ttu-id="19c67-128">Se não houver ação anterior, **Status** retornará `eUPDATE_UNKNOWN`.</span><span class="sxs-lookup"><span data-stu-id="19c67-128">If there is no previous action, **Status** returns  `eUPDATE_UNKNOWN`.</span></span>
    
<span data-ttu-id="19c67-129">**Baixando:** quando o instalador Clique para Executar estiver no estado baixando, você poderá chamar:</span><span class="sxs-lookup"><span data-stu-id="19c67-129">**Downloading:** When the Click-to-Run installer is in the downloading state, you can call:</span></span> 
  
- <span data-ttu-id="19c67-130">**Aplicar**: retorna **HRESULT** com o valor `0x800000e`, "Um método foi chamado em um momento inesperado".</span><span class="sxs-lookup"><span data-stu-id="19c67-130">**Apply**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="19c67-131">**Cancelar**: interrompe o download e remove o conteúdo parcialmente baixado.</span><span class="sxs-lookup"><span data-stu-id="19c67-131">**Cancel**: Stops the download and removes the partially downloaded content.</span></span>
    
- <span data-ttu-id="19c67-132">**Baixar**: retorna **HRESULT** com o valor `0x800000e`, "Um método foi chamado em um momento inesperado".</span><span class="sxs-lookup"><span data-stu-id="19c67-132">**Download**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span> 
    
- <span data-ttu-id="19c67-133">**Status**: retorna **DOWNLOAD_WIP** para indicar que o trabalho de download está em andamento.</span><span class="sxs-lookup"><span data-stu-id="19c67-133">**Status**: Returns **DOWNLOAD_WIP** to indicate that download work is in progress.</span></span> 
    
<span data-ttu-id="19c67-134">**Aplicando:** quando o instalador Clique para Executar estiver no processo de instalação do conteúdo anteriormente baixado:</span><span class="sxs-lookup"><span data-stu-id="19c67-134">**Applying:** When the Click-to-Run installer is in the process of installing previously download content:</span></span> 
  
- <span data-ttu-id="19c67-135">**Aplicar**: retorna **HRESULT** com o valor `0x800000e`, "Um método foi chamado em um momento inesperado".</span><span class="sxs-lookup"><span data-stu-id="19c67-135">**Apply**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="19c67-136">**Cancelar**: retorna `0x800000e`, a ação Aplicar não pode ser cancelada.</span><span class="sxs-lookup"><span data-stu-id="19c67-136">**Cancel**: Returns  `0x800000e`, the Apply action cannot be canceled.</span></span>
    
- <span data-ttu-id="19c67-137">**Baixar**: retorna **HRESULT** com o valor `0x800000e`, "Um método foi chamado em um momento inesperado".</span><span class="sxs-lookup"><span data-stu-id="19c67-137">**Download**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span> 
    
- <span data-ttu-id="19c67-138">**Status**: retorna **APPLY_WIP** para indicar que o trabalho de aplicação está em andamento.</span><span class="sxs-lookup"><span data-stu-id="19c67-138">**Status**: Returns **APPLY_WIP** to indicate that apply work is in progress.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="19c67-139">Uma vez que OfficeC2RCOM é um serviço COM+ e foi dinamicamente carregado, é preciso chamar **CoCreateInstance** toda vez que você chama um método nessa classe, a fim de garantir a obtenção do resultado esperado.</span><span class="sxs-lookup"><span data-stu-id="19c67-139">Since OfficeC2RCOM is a COM+ service and is dynamically loaded, you need to call **CoCreateInstance** every time you call a method on this class to ensure that you get the expected result.</span></span> <span data-ttu-id="19c67-140">O serviço COM+ tratará de criar uma nova instância, se necessário.</span><span class="sxs-lookup"><span data-stu-id="19c67-140">The COM+ service will handle creating a new instance if necessary.</span></span> <span data-ttu-id="19c67-141">Quando um dos métodos é chamado pela primeira vez, COM+ carregará o objeto **IUpdateNotify** e o executará em uma das instâncias de dllhost.exe.</span><span class="sxs-lookup"><span data-stu-id="19c67-141">When one of the methods is called for the first time, COM+ will load the **IUpdateNotify** object and run it within one of the dllhost.exe instances.</span></span> <span data-ttu-id="19c67-142">O novo objeto permanecerá ativo por aproximadamente 3 minutos em estado ocioso.</span><span class="sxs-lookup"><span data-stu-id="19c67-142">The new object will stay active for about 3 minutes in idle.</span></span> <span data-ttu-id="19c67-143">Se uma chamada subsequente for feita dentro de três minutos, a contar da última chamada, o objeto **IUpdateNotify** permanecerá carregado e não será criada uma nova instância.</span><span class="sxs-lookup"><span data-stu-id="19c67-143">If a subsequent call is made within three minutes of the last call, the **IUpdateNotify** object will remain loaded and a new instance is not created.</span></span> <span data-ttu-id="19c67-144">Se nenhuma chamada for feita em três minutos, o objeto IUpdateNotify será descarregado e um novo objeto **IUpdateNotify** será criado quando a próxima chamada for feita.</span><span class="sxs-lookup"><span data-stu-id="19c67-144">If no call is made within three minutes, the IUpdateNotify object will be unloaded and a new **IUpdateNotify** object will be created when the next call is made.</span></span> 
  
## <a name="click-to-run-installer-com-api-reference-guide"></a><span data-ttu-id="19c67-145">Guia de referência da API COM do instalador Clique para Executar</span><span class="sxs-lookup"><span data-stu-id="19c67-145">Click-to-Run installer COM API reference guide</span></span>

<span data-ttu-id="19c67-146">Na seguinte documentação de referência de API:</span><span class="sxs-lookup"><span data-stu-id="19c67-146">In the following API reference documentation:</span></span>
  
- <span data-ttu-id="19c67-147">Os parâmetros estão em um formato de par chave/valor separados por um espaço.</span><span class="sxs-lookup"><span data-stu-id="19c67-147">Parameters are in a key/value pair format separated by a space.</span></span>
    
- <span data-ttu-id="19c67-148">Os parâmetros não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="19c67-148">The parameters are not case-sensitive.</span></span>
    
- <span data-ttu-id="19c67-149">Há uma [lista de parâmetros](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) com documentação disponível.</span><span class="sxs-lookup"><span data-stu-id="19c67-149">There is a [list of parameters](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) with documentation available.</span></span> 
    
- <span data-ttu-id="19c67-150">Agora, o resumo da interface IUpdateNotify2 está incluído.</span><span class="sxs-lookup"><span data-stu-id="19c67-150">Summary of IUpdateNotify2 interface is now included.</span></span>
    
### <a name="apply"></a><span data-ttu-id="19c67-151">Aplicar</span><span class="sxs-lookup"><span data-stu-id="19c67-151">Apply</span></span>

```cpp
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
```

#### <a name="parameters"></a><span data-ttu-id="19c67-152">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="19c67-152">Parameters</span></span>

-  <span data-ttu-id="19c67-153">_displaylevel_: **true** para mostrar o status da instalação, incluindo erros, durante o processo de atualização; **false** para ocultar o status da instalação, incluindo erros, durante o processo de atualização.</span><span class="sxs-lookup"><span data-stu-id="19c67-153">_displaylevel_: **true** to show the installation status, including errors, during the update process; **false** to hide the installation status, including errors, during the update process.</span></span> <span data-ttu-id="19c67-154">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="19c67-154">The default is **false**.</span></span>
    
-  <span data-ttu-id="19c67-155">_forceappshutdown_: **true** para forçar os aplicativos do Office a desligarem imediatamente quando a ação **Aplicar** for disparada; **false** para falha, se algum aplicativo do Office estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="19c67-155">_forceappshutdown_: **true** to force Office applications to shut down immediately when the **Apply** action is triggered; **false** to fail if any Office applications are running.</span></span> <span data-ttu-id="19c67-156">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="19c67-156">The default is **false**.</span></span> <span data-ttu-id="19c67-157">Veja [Comentários](#bk_ApplyRemark) para saber mais.</span><span class="sxs-lookup"><span data-stu-id="19c67-157">See [Remarks](#bk_ApplyRemark) for more information.</span></span> 
    
  <span data-ttu-id="19c67-158">Se algum aplicativo do Office estiver em execução quando a ação **Aplicar** for disparada, a ação **Aplicar** normalmente falha.</span><span class="sxs-lookup"><span data-stu-id="19c67-158">If any Office application is running when the **Apply** action is triggered, the **Apply** action will usually fail.</span></span> <span data-ttu-id="19c67-159">Passar `forceappshutdown=true` ao método **Aplicar** fará com que o serviço **OfficeClickToRun** desligue imediatamente os aplicativos e aplique a atualização.</span><span class="sxs-lookup"><span data-stu-id="19c67-159">Passing  `forceappshutdown=true` to the **Apply** method will cause the **OfficeClickToRun** service to immediately shut down the applications and apply the update.</span></span> <span data-ttu-id="19c67-160">O usuário poderá enfrentar perda de dados nesse caso.</span><span class="sxs-lookup"><span data-stu-id="19c67-160">The user may experience data loss in this case.</span></span> 
    
#### <a name="return-results"></a><span data-ttu-id="19c67-161">Retornar resultados</span><span class="sxs-lookup"><span data-stu-id="19c67-161">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19c67-162">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="19c67-162">**S_OK**</span></span> <br/> |<span data-ttu-id="19c67-163">A ação foi enviada com êxito ao serviço Clique para Executar para execução.</span><span class="sxs-lookup"><span data-stu-id="19c67-163">Action was successfully submitted to the Click-To-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="19c67-164">**E_ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="19c67-164">**E_ACCESSDENIED**</span></span> <br/> |<span data-ttu-id="19c67-165">O autor da chamada não está em execução com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="19c67-165">The caller is not running with elevated privileges.</span></span>  <br/> |
|<span data-ttu-id="19c67-166">**E_INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="19c67-166">**E_INVALIDARG**</span></span> <br/> |<span data-ttu-id="19c67-167">Parâmetros inválidos foram passados.</span><span class="sxs-lookup"><span data-stu-id="19c67-167">Invalid parameters were passed.</span></span>  <br/> |
|<span data-ttu-id="19c67-168">**E_ILLEGAL_METHOD_CALL**</span><span class="sxs-lookup"><span data-stu-id="19c67-168">**E_ILLEGAL_METHOD_CALL**</span></span> <br/> |<span data-ttu-id="19c67-169">A ação não é permitida neste momento.</span><span class="sxs-lookup"><span data-stu-id="19c67-169">Action is not allowed at this time.</span></span> <span data-ttu-id="19c67-170">Veja [Comentários](#bk_ApplyRemark) para saber mais.</span><span class="sxs-lookup"><span data-stu-id="19c67-170">See [Remarks](#bk_ApplyRemark) for more information.</span></span>  <br/> |

<a name="bk_ApplyRemark"></a>

#### <a name="remarks"></a><span data-ttu-id="19c67-171">Comentários</span><span class="sxs-lookup"><span data-stu-id="19c67-171">Remarks</span></span>

- <span data-ttu-id="19c67-172">Se algum aplicativo do Office estiver em execução quando a ação **Aplicar** for disparada, a ação **Aplicar** falhará.</span><span class="sxs-lookup"><span data-stu-id="19c67-172">If any Office application is running when the **Apply** action is triggered, the **Apply** action will fail.</span></span> <span data-ttu-id="19c67-173">Passar `forceappshutdown=true` ao método **Aplicar** fará com que o serviço **OfficeClickToRun** desligue imediatamente qualquer aplicativo do Office que esteja em execução e aplique a atualização.</span><span class="sxs-lookup"><span data-stu-id="19c67-173">Passing  `forceappshutdown=true` to the **Apply** method will cause the **OfficeClickToRun** service to immediately shut down any Office applications that are running and apply the update.</span></span> <span data-ttu-id="19c67-174">O usuário pode sofrer perda de dados, uma vez que não é solicitado que salve as alterações em documentos abertos.</span><span class="sxs-lookup"><span data-stu-id="19c67-174">The user may experience data as they are not prompted to save changes to open documents..</span></span> 
    
- <span data-ttu-id="19c67-175">Essa ação poderá ser disparada somente quando o status COM for um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="19c67-175">This action can only be triggered when the COM status is one of the following:</span></span> 
    
  - <span data-ttu-id="19c67-176">**eUPDATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="19c67-176">**eUPDATE_UNKNOWN**</span></span>
    
  - <span data-ttu-id="19c67-177">**eDOWNLOAD_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="19c67-177">**eDOWNLOAD_CANCELLED**</span></span>
    
  - <span data-ttu-id="19c67-178">**eDOWNLOAD_FAILED**</span><span class="sxs-lookup"><span data-stu-id="19c67-178">**eDOWNLOAD_FAILED**</span></span>
    
  - <span data-ttu-id="19c67-179">**eDOWNLOAD_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="19c67-179">**eDOWNLOAD_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="19c67-180">**eAPPLY_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="19c67-180">**eAPPLY_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="19c67-181">**eAPPLY_FAILED**</span><span class="sxs-lookup"><span data-stu-id="19c67-181">**eAPPLY_FAILED**</span></span>
    
- <span data-ttu-id="19c67-182">Se você chamar o método **Apply** sem baixar o conteúdo antes, o método **Apply** indicará **Êxito**, pois ele não detectou nada a ser aplicado e concluiu o processo **Apply** com êxito.</span><span class="sxs-lookup"><span data-stu-id="19c67-182">If you call the **Apply** method without previously downloading content, the **Apply** method will report **Succeeded** as it detected nothing to apply and completed the **Apply** process successfully.</span></span> 
    
### <a name="cancel"></a><span data-ttu-id="19c67-183">Cancelar</span><span class="sxs-lookup"><span data-stu-id="19c67-183">Cancel</span></span>

```cpp
HRESULT Cancel() // Cancel the download action.
```

#### <a name="return-results"></a><span data-ttu-id="19c67-184">Retornar resultados</span><span class="sxs-lookup"><span data-stu-id="19c67-184">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19c67-185">S_OK</span><span class="sxs-lookup"><span data-stu-id="19c67-185">S_OK</span></span>  <br/> |<span data-ttu-id="19c67-186">A ação foi enviada com êxito ao serviço Clique para Executar para execução.</span><span class="sxs-lookup"><span data-stu-id="19c67-186">Action was successfully submitted to the Click-to-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="19c67-187">E_ILLEGAL_METHOD_CALL</span><span class="sxs-lookup"><span data-stu-id="19c67-187">E_ILLEGAL_METHOD_CALL</span></span>  <br/> |<span data-ttu-id="19c67-188">A ação não é permitida neste momento.</span><span class="sxs-lookup"><span data-stu-id="19c67-188">Action is not allowed at this time.</span></span> <span data-ttu-id="19c67-189">Consulte a seção [Comentários](#bk_CancelRemarks) para obter mais informações</span><span class="sxs-lookup"><span data-stu-id="19c67-189">See the [Remarks](#bk_CancelRemarks) section for more information</span></span>  <br/> |

<a name="bk_CancelRemarks"></a>

#### <a name="remarks"></a><span data-ttu-id="19c67-190">Comentários</span><span class="sxs-lookup"><span data-stu-id="19c67-190">Remarks</span></span>

- <span data-ttu-id="19c67-191">Esse método poderá ser disparado somente quando o status COM for **eDOWNLOAD_WIP**.</span><span class="sxs-lookup"><span data-stu-id="19c67-191">This method can only be triggered when the COM status id **eDOWNLOAD_WIP**.</span></span> <span data-ttu-id="19c67-192">Ele tentará cancelar a ação de download atual.</span><span class="sxs-lookup"><span data-stu-id="19c67-192">It will attempt to cancel the current download action.</span></span> <span data-ttu-id="19c67-193">O status COM será alterado para **eDOWNLOAD_CANCELLING** e, por fim, para **eDOWNLOAD_CANCELED**.</span><span class="sxs-lookup"><span data-stu-id="19c67-193">The COM status will change to **eDOWNLOAD_CANCELLING** and eventually change to **eDOWNLOAD_CANCELED**.</span></span> <span data-ttu-id="19c67-194">O status COM retornará **E_ILLEGAL_METHOD_CALL** se disparado em qualquer outro momento.</span><span class="sxs-lookup"><span data-stu-id="19c67-194">The COM status will return **E_ILLEGAL_METHOD_CALL** if triggered at any other time.</span></span> 
    
### <a name="download"></a><span data-ttu-id="19c67-195">Baixar</span><span class="sxs-lookup"><span data-stu-id="19c67-195">Download</span></span>

```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
```

#### <a name="parameters"></a><span data-ttu-id="19c67-196">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="19c67-196">Parameters</span></span>

-  <span data-ttu-id="19c67-197">_displaylevel_: **true** para mostrar o status da instalação, incluindo erros, durante o processo de atualização; **false** para ocultar o status da instalação, incluindo erros, durante o processo de atualização.</span><span class="sxs-lookup"><span data-stu-id="19c67-197">_displaylevel_: **true** to show the installation status, including errors, during the update process; **false** to hide the installation status, including errors, during the update process.</span></span> <span data-ttu-id="19c67-198">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="19c67-198">The default is **false**.</span></span>
    
-  <span data-ttu-id="19c67-199">_updatebaseurl_: URL para a fonte alternativa de download.</span><span class="sxs-lookup"><span data-stu-id="19c67-199">_updatebaseurl_: URL to the alternate download source.</span></span>
    
-  <span data-ttu-id="19c67-200">_updatetoversion_: a versão para a qual atualizar o Office.</span><span class="sxs-lookup"><span data-stu-id="19c67-200">_updatetoversion_: The version to update Office to.</span></span> <span data-ttu-id="19c67-201">Defina esse parâmetro se desejar atualizar para um versão mais antiga do que a versão que está atualmente instalada.</span><span class="sxs-lookup"><span data-stu-id="19c67-201">Define this parameter if you want to update to an older version than the version that is currently installed.</span></span>
    
-  <span data-ttu-id="19c67-202">_downloadsource_: CLSID da implementação **IBackgroundCopyManager** personalizada (gerenciador do BITS).</span><span class="sxs-lookup"><span data-stu-id="19c67-202">_downloadsource_: CLSID of the customized **IBackgroundCopyManager** implementation (BITS manager).</span></span> 
    
-  <span data-ttu-id="19c67-203">_contentid_: identifica o conteúdo a ser baixado do servidor de conteúdo por meio do gerenciador do BITS personalizado.</span><span class="sxs-lookup"><span data-stu-id="19c67-203">_contentid_: Identifies the content to download from the content server through the customized BITS manager.</span></span> <span data-ttu-id="19c67-204">Esse valor é passado pela interface do BITS para interpretação.</span><span class="sxs-lookup"><span data-stu-id="19c67-204">This value is passed through the BITS interface for interpretation.</span></span>
    
#### <a name="return-results"></a><span data-ttu-id="19c67-205">Retornar resultados</span><span class="sxs-lookup"><span data-stu-id="19c67-205">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19c67-206">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="19c67-206">**S_OK**</span></span> <br/> |<span data-ttu-id="19c67-207">A ação foi enviada com êxito ao serviço Clique para Executar para execução.</span><span class="sxs-lookup"><span data-stu-id="19c67-207">Action was successfully submitted to the Click-To-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="19c67-208">**E_ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="19c67-208">**E_ACCESSDENIED**</span></span> <br/> |<span data-ttu-id="19c67-209">O autor da chamada não está em execução com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="19c67-209">The caller is not running with elevated privileges.</span></span>  <br/> |
|<span data-ttu-id="19c67-210">**E_INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="19c67-210">**E_INVALIDARG**</span></span> <br/> |<span data-ttu-id="19c67-211">Parâmetros inválidos foram passados.</span><span class="sxs-lookup"><span data-stu-id="19c67-211">Invalid parameters were passed.</span></span>  <br/> |
|<span data-ttu-id="19c67-212">**E_ILLEGAL_METHOD_CALL**</span><span class="sxs-lookup"><span data-stu-id="19c67-212">**E_ILLEGAL_METHOD_CALL**</span></span> <br/> |<span data-ttu-id="19c67-213">A ação não é permitida neste momento.</span><span class="sxs-lookup"><span data-stu-id="19c67-213">Action is not allowed at this time.</span></span> <span data-ttu-id="19c67-214">Veja [Comentários](#bk_DownloadRemark) para saber mais.</span><span class="sxs-lookup"><span data-stu-id="19c67-214">See [Remarks](#bk_DownloadRemark) for more information.</span></span>  <br/> |

<a name="bk_DownloadRemark"></a>

#### <a name="remarks"></a><span data-ttu-id="19c67-215">Comentários</span><span class="sxs-lookup"><span data-stu-id="19c67-215">Remarks</span></span>

- <span data-ttu-id="19c67-216">Você deve especificar _downloadsource_ e _contentid_ como um par.</span><span class="sxs-lookup"><span data-stu-id="19c67-216">You must specify  _downloadsource_ and  _contentid_ as a pair.</span></span> <span data-ttu-id="19c67-217">Caso contrário, o método **Baixar** retornará um erro **E_INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="19c67-217">If not, the **Download** method will return an **E_INVALIDARG** error.</span></span> 
    
- <span data-ttu-id="19c67-218">Se _downloadsource_, _contentid_ e _updatebaseurl_ forem fornecidos, _updatebaseurl_ será ignorado.</span><span class="sxs-lookup"><span data-stu-id="19c67-218">If  _downloadsource_,  _contentid_, and  _updatebaseurl_ are provided,  _updatebaseurl_ will be ignored.</span></span> 
    
- <span data-ttu-id="19c67-219">Essa ação poderá ser disparada somente quando o status COM for um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="19c67-219">This action can only be triggered when the COM status is one of the following:</span></span> 
    
  - <span data-ttu-id="19c67-220">**eUPDATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="19c67-220">**eUPDATE_UNKNOWN**</span></span>
    
  - <span data-ttu-id="19c67-221">**eDOWNLOAD_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="19c67-221">**eDOWNLOAD_CANCELLED**</span></span>
    
  - <span data-ttu-id="19c67-222">**eDOWNLOAD_FAILED**</span><span class="sxs-lookup"><span data-stu-id="19c67-222">**eDOWNLOAD_FAILED**</span></span>
    
  - <span data-ttu-id="19c67-223">**eDOWNLOAD_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="19c67-223">**eDOWNLOAD_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="19c67-224">**eAPPLY_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="19c67-224">**eAPPLY_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="19c67-225">**eAPPLY_FAILED**</span><span class="sxs-lookup"><span data-stu-id="19c67-225">**eAPPLY_FAILED**</span></span>
    
- <span data-ttu-id="19c67-226">Se você chamar o método **Apply** sem o conteúdo baixado anteriormente, o método **Apply** indicará **Êxito**, pois ele não detectou nada a ser aplicado e concluiu o processo **Apply** com êxito.</span><span class="sxs-lookup"><span data-stu-id="19c67-226">If you call the **Apply** method without previously downloaded content, the **Apply** method will report **Succeeded** as it detected nothing to apply and completed the **Apply** process successfully.</span></span> 
    
#### <a name="examples"></a><span data-ttu-id="19c67-227">Exemplos</span><span class="sxs-lookup"><span data-stu-id="19c67-227">Examples</span></span>

- <span data-ttu-id="19c67-228">Para baixar o conteúdo do gerenciador do BITS personalizado: chame a função **download()** passando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="19c67-228">To download the content from the customized BITS manager: Call the **download()** function passing the following parameters:</span></span> 
    
  ```cpp
  "downloadsource=CLSIDofBITSInterface contentid=BITSServerContentIdentifier"
  ```

- <span data-ttu-id="19c67-229">Para baixar o conteúdo CDN da Microsoft: chame a função **download()** sem especificar os parâmetros _downloadsource_, _contentid_ ou _ updatebaseurl_.</span><span class="sxs-lookup"><span data-stu-id="19c67-229">To download the content from the Microsoft CDN: Call the **download()** function without specifying the  _downloadsource_,  _contentid_, or  _updatebaseurl_ parameters.</span></span> 
    
- <span data-ttu-id="19c67-230">Para baixar o conteúdo de um local personalizado: chame a função **download()** passando o seguinte parâmetro:</span><span class="sxs-lookup"><span data-stu-id="19c67-230">To download the content from a customized location: Call the **download()** function passing the following parameter:</span></span> 
    
  ```cpp
  "updatebaseurl=yourcontentserverurl"
  ```

### <a name="status"></a><span data-ttu-id="19c67-231">Status</span><span class="sxs-lookup"><span data-stu-id="19c67-231">Status</span></span>

```cpp
typdef struct _UPDATE_STATUS_REPORT
{
    UPDATE_STATUS status;
    UINT error;
    LPCWSTR contentid;
}UPDATE_STATUS_REPORT;
HRESULT status([out] _UPDATE_STATUS_REPORT& pUpdateStatusReport) // Get status of current action
```

#### <a name="parameters"></a><span data-ttu-id="19c67-232">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="19c67-232">Parameters</span></span>

|||
|:-----|:-----|
| <span data-ttu-id="19c67-233">_pUpdateStatusReport_</span><span class="sxs-lookup"><span data-stu-id="19c67-233">_pUpdateStatusReport_</span></span> <br/> |<span data-ttu-id="19c67-234">Ponteiro para uma estrutura UPDATE_STATUS_REPORT.</span><span class="sxs-lookup"><span data-stu-id="19c67-234">Pointer to an UPDATE_STATUS_REPORT structure.</span></span>  <br/> |
   
#### <a name="return-results"></a><span data-ttu-id="19c67-235">Retornar resultados</span><span class="sxs-lookup"><span data-stu-id="19c67-235">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19c67-236">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="19c67-236">**S_OK**</span></span> <br/> |<span data-ttu-id="19c67-237">O método **Status** sempre retorna esse resultado.</span><span class="sxs-lookup"><span data-stu-id="19c67-237">The **Status** method always returns this result.</span></span> <span data-ttu-id="19c67-238">Inspecione a estrutura `UPDATE_STATUS_RESULT` para ver o status atual ação.</span><span class="sxs-lookup"><span data-stu-id="19c67-238">Inspect the  `UPDATE_STATUS_RESULT` structure for the status of the current action.</span></span>  <br/> |
   
#### <a name="remarks"></a><span data-ttu-id="19c67-239">Comentários</span><span class="sxs-lookup"><span data-stu-id="19c67-239">Remarks</span></span>

- <span data-ttu-id="19c67-240">O campo de status de `UPDATE_STATUS_REPORT` contém o status de ação atual.</span><span class="sxs-lookup"><span data-stu-id="19c67-240">The status field of the  `UPDATE_STATUS_REPORT` contains the status of the current action.</span></span> <span data-ttu-id="19c67-241">Um dos seguintes valores de status é retornado:</span><span class="sxs-lookup"><span data-stu-id="19c67-241">One of the following status values is returned:</span></span> 
    
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

- <span data-ttu-id="19c67-242">Se o último comando resultou em um erro, o campo de erro de `UPDATE_STATUS_REPORT` conterá informações detalhadas sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="19c67-242">If the last command resulted in an error, the error field of the  `UPDATE_STATUS_REPORT` contains detailed information about the error.</span></span> <span data-ttu-id="19c67-243">Dois tipos de código de erro são retornados do método **Status**.</span><span class="sxs-lookup"><span data-stu-id="19c67-243">Two types of error codes are returned from the **Status** method.</span></span> 
    
- <span data-ttu-id="19c67-244">Se o erro for inferior a `UPDATE_ERROR_CODE::eUNKNOWN`, o erro será um dos seguintes códigos de erro predefinidos:</span><span class="sxs-lookup"><span data-stu-id="19c67-244">If the error less than  `UPDATE_ERROR_CODE::eUNKNOWN`, the error is one of the following pre-defined error codes:</span></span>
    
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

  <span data-ttu-id="19c67-245">Se um código de erro de retorno for superior a `UPDATE_ERROR_CODE::eUNKNOWN`, trata-se do **HRESULT** de uma chamada de função com falha.</span><span class="sxs-lookup"><span data-stu-id="19c67-245">If the return error code is larger than  `UPDATE_ERROR_CODE::eUNKNOWN` it is the **HRESULT** of a failed function call.</span></span> <span data-ttu-id="19c67-246">Para extrair o HRESULT, subtraia `UPDATE_ERROR_CODE::eUNKNOWN` do valor retornado no campo de erro de `UPDATE_STATUS_REPORT`.</span><span class="sxs-lookup"><span data-stu-id="19c67-246">To extract the HRESULT subtract  `UPDATE_ERROR_CODE::eUNKNOWN` from the value returned in the error field of the  `UPDATE_STATUS_REPORT`.</span></span>
    
  <span data-ttu-id="19c67-247">A lista completa de valores de status e erro pode ser exibida inspecionando a biblioteca de tipos **IUpdateNotify** inserida em OfficeC2RCom.dll.</span><span class="sxs-lookup"><span data-stu-id="19c67-247">The complete list of status and error values can be viewed by inspecting the **IUpdateNotify** type library embedded in OfficeC2RCom.dll.</span></span> 
    
- <span data-ttu-id="19c67-248">O campo contentid é usado para chamadas a **Status** depois que **Baixar** tiver sido iniciado e retornar o contentid que foi passado à chamada **Baixar**.</span><span class="sxs-lookup"><span data-stu-id="19c67-248">The contentid field is used for calls to **Status** after **Download** has initiated and returns the contentid that was passed in to the **Download** call.</span></span> <span data-ttu-id="19c67-249">É uma prática recomendada inicializar esse campo como **nulo** antes chamar o método **Status** e, em seguida, verificar o valor depois que **Status** tiver sido retornado.</span><span class="sxs-lookup"><span data-stu-id="19c67-249">It is a best practice to initialize this field to **null** before you call the **Status** method and then check the value after **Status** has been returned.</span></span> <span data-ttu-id="19c67-250">Se o valor ainda for **null**, isso significa que não há contentid a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="19c67-250">If the value is still **null**, that means there is no contentid to return.</span></span> <span data-ttu-id="19c67-251">Se o valor não for **null**, você precisará liberá-lo com um chamada a **SysFreeString()**.</span><span class="sxs-lookup"><span data-stu-id="19c67-251">If the value is not **null**, you need to free it with a call to **SysFreeString()**.</span></span> <span data-ttu-id="19c67-252">Veja um trecho de código de como chamar **Status** após **Baixar**.</span><span class="sxs-lookup"><span data-stu-id="19c67-252">Here is a code snippet of how to call **Status** after **Download**.</span></span>
    
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

### <a name="summary-of-iupdatenotify2-interface"></a><span data-ttu-id="19c67-253">Resumo da interface IUpdateNotify2</span><span class="sxs-lookup"><span data-stu-id="19c67-253">Summary of IUpdateNotify2 interface</span></span>

> [!NOTE]
> <span data-ttu-id="19c67-254">Esse resumo é fornecido como informações complementares de [Integrando aplicativos de capacidade de gerenciamento ao instalador Clique para Executar do Office 365](https://docs.microsoft.com/office/client-developer/shared/manageability-applications-with-the-office-365-click-to-run-installer).</span><span class="sxs-lookup"><span data-stu-id="19c67-254">This summary is provided as a compliment info to [Integrating manageability applications with the Office 365 click-to-run installer](https://docs.microsoft.com/office/client-developer/shared/manageability-applications-with-the-office-365-click-to-run-installer).</span></span> <span data-ttu-id="19c67-255">Assim que o documento público for atualizado, esse documento poderá ser considerado obsoleto.</span><span class="sxs-lookup"><span data-stu-id="19c67-255">Once the public doc is updated, this doc can be considered as obsolete.</span></span> 
  
<span data-ttu-id="19c67-256">No C2RTenant [16.0.8208.6352](https://oloop/BuildGroup/Details/tenantc2rclient#3519/1255278) (Primeiro build publicamente disponível deve ser o build fork de junho-- 8326.\*), adicionamos uma nova interface **IUpdateNotify2**.</span><span class="sxs-lookup"><span data-stu-id="19c67-256">From C2RTenant [16.0.8208.6352](https://oloop/BuildGroup/Details/tenantc2rclient#3519/1255278) (First publicly available build should be June fork build -- 8326.\*) we have added a new **IUpdateNotify2** interface.</span></span> <span data-ttu-id="19c67-257">Veja algumas informações básicas sobre essa interface:</span><span class="sxs-lookup"><span data-stu-id="19c67-257">Here is some basic info about this interface:</span></span> 
  
- <span data-ttu-id="19c67-258">CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}</span><span class="sxs-lookup"><span data-stu-id="19c67-258">CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}</span></span>
    
- <span data-ttu-id="19c67-259">Essa interface também hospedava a interface IUpdateNotify original para fornecer compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="19c67-259">This interface also hosted the original IUpdateNotify interface to provide backward compatibility.</span></span> <span data-ttu-id="19c67-260">Isso significa que, ao usar essa interface, você terá acesso a todos os métodos fornecidos na interface **UpdateNotifyObject**.</span><span class="sxs-lookup"><span data-stu-id="19c67-260">Which means if you use this interface, you have access to all the methods provided in **UpdateNotifyObject** interface.</span></span> 
    
- <span data-ttu-id="19c67-261">Novos métodos adicionados a IUpdateNotify2:</span><span class="sxs-lookup"><span data-stu-id="19c67-261">New methods added to IUpdateNotify2:</span></span>
    
  - <span data-ttu-id="19c67-262">**HRESULT** GetBlockingApps([out] BSTR \* AppsList).</span><span class="sxs-lookup"><span data-stu-id="19c67-262">**HRESULT** GetBlockingApps([out] BSTR \* AppsList).</span></span> <span data-ttu-id="19c67-263">Obtenha a lista de aplicativos de bloqueio de atualizações.</span><span class="sxs-lookup"><span data-stu-id="19c67-263">Get updates blocking apps list.</span></span> <span data-ttu-id="19c67-264">Essa chamada retornará os aplicativos do Office em execução que impedirão o processo de atualização de prosseguir.</span><span class="sxs-lookup"><span data-stu-id="19c67-264">This call will return running Office apps which will block the update process from proceeding.</span></span> 
    
  - <span data-ttu-id="19c67-265">**HRESULT** GetOfficeDeploymentData([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR \* OfficeData).</span><span class="sxs-lookup"><span data-stu-id="19c67-265">**HRESULT** GetOfficeDeploymentData([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR \* OfficeData).</span></span> <span data-ttu-id="19c67-266">Obtenha os dados de implantação do Office.</span><span class="sxs-lookup"><span data-stu-id="19c67-266">Get Office deployment Data.</span></span> 
    
- <span data-ttu-id="19c67-267">Se desejar usar os novos métodos, você precisará garantir:</span><span class="sxs-lookup"><span data-stu-id="19c67-267">If you want to use the new methods, you need to make sure:</span></span>
    
  - <span data-ttu-id="19c67-268">Que a sua versão C2R seja mais nova do que o build acima (\> = build fork de junho).</span><span class="sxs-lookup"><span data-stu-id="19c67-268">Your C2R version is newer than the above build (\>= June fork build).</span></span>
    
  - <span data-ttu-id="19c67-269">O uso de UpdateNotifyObject2, em vez de **UpdateNotifyObject** para chamar **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="19c67-269">Use UpdateNotifyObject2, instead of **UpdateNotifyObject** to call **CoCreateInstance**.</span></span>
    
<span data-ttu-id="19c67-270">Se você não usar qualquer um dos métodos novos, não será necessário alterar nada.</span><span class="sxs-lookup"><span data-stu-id="19c67-270">If you don't use any of the new methods, you don't need to change anything.</span></span> <span data-ttu-id="19c67-271">Todos os métodos existentes funcionarão exatamente da mesma maneira que antes.</span><span class="sxs-lookup"><span data-stu-id="19c67-271">All the existing methods will work as exact the same way as before.</span></span>
  
## <a name="implementing-the-bits-interface"></a><span data-ttu-id="19c67-272">Como implantar a interface do BITS</span><span class="sxs-lookup"><span data-stu-id="19c67-272">Implementing the BITS interface</span></span>

<span data-ttu-id="19c67-273">O BITS ([Serviço de Transferência Inteligente em Segundo Plano](https://docs.microsoft.com/windows/win32/bits/background-intelligent-transfer-service-portal)) é um serviço fornecido pela Microsoft para transferir arquivos entre um cliente e um servidor.</span><span class="sxs-lookup"><span data-stu-id="19c67-273">The [Background Intelligent Transfer Service](https://docs.microsoft.com/windows/win32/bits/background-intelligent-transfer-service-portal) (BITS) is a service provided by Microsoft to transfer files between a client and server.</span></span> <span data-ttu-id="19c67-274">O BITS é um dos canais que o instalador Clique para Executar do Office pode usar para baixar conteúdo.</span><span class="sxs-lookup"><span data-stu-id="19c67-274">BITS is one of the channels that Office Click-To-Run installer can use to download content.</span></span> <span data-ttu-id="19c67-275">Por padrão, o instalador Clique para Executar do Office usa a implementação interna do BITS do Windows para baixar o conteúdo da CDN.</span><span class="sxs-lookup"><span data-stu-id="19c67-275">By default, the Office Click-To-Run installer uses the Windows' built in implementation of BITS to download the content from the CDN.</span></span> 
  
<span data-ttu-id="19c67-276">Ao fornecer uma implementação do BITS personalizado ao método **download()** da interface **IUpdateNotify**, seu software de capacidade de gerenciamento pode controlar onde e como o cliente baixa o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="19c67-276">By providing a customized BITS implementation to the **download()** method of the **IUpdateNotify** interface, your manageability software can control where and how the client downloads the content.</span></span> <span data-ttu-id="19c67-277">Uma interface do BITS personalizado é útil ao fornecer um canal de distribuição de conteúdo personalizado diferente dos canais internos de Clique para Executar, como CDN do Office, servidores IIS ou compartilhamentos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="19c67-277">A customized BITS interface is useful when providing a custom content distribution channel other than the Click-to-Run built-in channels, such as the Office CDN, IIS servers, or file shares.</span></span> 
  
<span data-ttu-id="19c67-278">O requisito mínimo para uma interface do BITS personalizado trabalhar com o serviço C2R do Office é:</span><span class="sxs-lookup"><span data-stu-id="19c67-278">The minimum requirement for a customized BITS interface to work with Office C2R service is:</span></span>
  
- <span data-ttu-id="19c67-279">Para **IBackgroundCopyManager**:</span><span class="sxs-lookup"><span data-stu-id="19c67-279">For **IBackgroundCopyManager**:</span></span>
    
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

- <span data-ttu-id="19c67-280">Para **IBackgroundCopyJob**:</span><span class="sxs-lookup"><span data-stu-id="19c67-280">For **IBackgroundCopyJob**:</span></span>
    
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

- <span data-ttu-id="19c67-281">Para **IBackgroundCopyJob3**:</span><span class="sxs-lookup"><span data-stu-id="19c67-281">For **IBackgroundCopyJob3**:</span></span>
    
  ```cpp
  HRESULT _stdcall AddFileWithRanges(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName,
                      [in] DWORD RangeCount,
                      [in] BG_FILE_RANGE Ranges[])
  
  ```

- <span data-ttu-id="19c67-282">Para as funções `Addfile` e `AddFileWithRanges`, a URL remota está no seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="19c67-282">For the  `Addfile` and  `AddFileWithRanges` functions, the remote URL is in the following format:</span></span> 
    
  ```cpp
  cmbits://<contentid>/<relative path to target file>
  ```

  - <span data-ttu-id="19c67-283">cmbits é embutido em código e significa o BITS personalizado.</span><span class="sxs-lookup"><span data-stu-id="19c67-283">cmbits is hard coded, and stands for customized BITS.</span></span>
    
  -  <span data-ttu-id="19c67-284">_\<contentid\>_ é o parâmetro _contentid_ para o método **Download()**.</span><span class="sxs-lookup"><span data-stu-id="19c67-284">_\<contentid\>_ is the  _contentid_ parameter for the **Download()** method.</span></span> 
    
  -  <span data-ttu-id="19c67-285">_\<caminho relativo para arquivo de destino\>_ fornece o local e o nome do arquivo para download.</span><span class="sxs-lookup"><span data-stu-id="19c67-285">_\<relative path to target file\>_ provides the location and file name of the file to download.</span></span> 
    
    <span data-ttu-id="19c67-286">Por exemplo, se você tiver fornecido um _contentid_ de `f732af58-5d86-4299-abe9-7595c35136ef` ao método **Download()** e o C2R do Office quiser baixar o arquivo cab da versão, como o arquivo `v32.cab`, ele chamará **AddFile()** com o seguinte `RemoteUrl`:</span><span class="sxs-lookup"><span data-stu-id="19c67-286">For example, if you have provided a  _contentid_ of  `f732af58-5d86-4299-abe9-7595c35136ef` to the **Download()** method, and Office C2R wants to download the version cab file, such as  `v32.cab` file, it will call **AddFile()** with the following  `RemoteUrl`:</span></span>
    
  ```cpp
  cmbits://f732af58-5d86-4299-abe9-7595c35136ef/Office/Data/V32.cab
  ```

- <span data-ttu-id="19c67-287">Para **IBackgroundCopyError**:</span><span class="sxs-lookup"><span data-stu-id="19c67-287">For **IBackgroundCopyError**:</span></span>
    
  ```cpp
  HRESULT _stdcall GetErrorDescription(
        [in]  DWORD  LanguageId,
        [out] LPWSTR *ppErrorDescription);
  
  ```

- <span data-ttu-id="19c67-288">Para **IBackgroundCopyFile**:</span><span class="sxs-lookup"><span data-stu-id="19c67-288">For **IBackgroundCopyFile**:</span></span>
    
  ```cpp
  HRESULT _stdcall GetLocalName([out] LPWSTR *ppName); 
  HRESULT _stdcall GetRemoteName([out] LPWSTR *ppName);
  
  ```

<!--## Automating content staging

IT administrators can choose to have desktop clients enabled to automatically receive updates when they are available directly from the Microsoft Content Delivery Network (CDN) or they can choose to control the deployment of updates available from the [update channels](https://docs.microsoft.com/DeployOffice/overview-of-update-channels-for-office-365-proplus) using the [Office 2016 Deployment Tool](https://www.microsoft.com/download/details.aspx?id=49117) or [System Center Configuration Manager](https://docs.microsoft.com/deployoffice/manage-office-365-proplus-updates-with-configuration-manager).
  
The service supports the ability for management tools to recognize and automate the download of the content when updates are made available.
  
**Following is a diagram showing the overview of downloading a custom image**

![An overview of downloading Office updates from the CDN.](media/9afac230-6b22-4526-a800-0562708cc436.png "An overview of downloading Office updates from the CDN")
  
In the above diagram you see that a new Office 365 ProPlus image is available on the Office Content Distribution Network (CDN). Along with the Office 365 ProPlus image, an XML-formatted file list is also available which has the information needed to enable manageability software to directly create customized images replacing the need for using the Office Deployment Tool.
  
An enterprise configures their WSUS to sync the Office 365 Client Updates. These updates do not contain the actual image payload but does allow the manageability software to recognize when new content is available. The manageability software can then read the Client Update metadata to understand what version of Office the update applies to.
  
If the update is applicable, the manageability software can use the CDN content and the file list to create the custom image and store it onto the file share location that it is configured to use.
  
### Format of the XML file list

There are two file lists available in a cab file on the CDN. One lists the files for the 32-bit version of Office and one for the 64-bit version of Office. The URL of the location of the Office File List (OFL.CAB) file is [https://officecdn.microsoft.com/pr/wsus/ofl.cab](https://officecdn.microsoft.com/pr/wsus/ofl.cab). The two file lists are called:
  
- O365Client_32bit.xml
    
- O365Client_64bit.xml
    
Within the XML for each of the file lists is an  `UpdateFiles` node which contains a version attribute.  `UpdateFiles version="1.4"`.
  
This version is incremented if changes are made to the file lists.
  
There are two parameters that need to be combined with the XML to make a custom image: 
  
- Replace  _%version%_ with the build version of Office. This can be derived from the Client Update metadata  `MoreInfoURL` field, see below. 
    
- Define  _baseURL_ by using the URL value associated with the branch the image is being created for. This can be derived from the Client Update metadata, see below. 
    
The steps for creating an image are:
  
1. Open the XML file list.
    
2. Replace occurrences of  _%version%_ with the applicable Office build version. The build version can be acquired from releasehistory.xml as described later in this article. 
    
3. Read the URL attribute for the target branch.
    
4. Remove language nodes for any languages not required in the custom image.
    
   > [!NOTE]
   > Nodes with language='0' are language neutral and must be included in the image. 
  
5. Construct a local image of the CDN by iterating through the XML file list and copying the CDN files, while creating the folder structure as needed. 
    
   - If the  _rename_ attribute is provided, then rename the copied file to the value provided in the  _rename_ attribute. This used to create the top-level default v64.cab and v32.cab files. These are the renamed versions of the top-level build cab file and are used as the default installation version if the version is not specified. 
    
   - Use URL + relativePath + filename to construct the CDN location.
    
The following examples use the Monthly channel (as defined by the  `baseURL` node) and build version 16.0.4229.1004 from releasehistory.xml. 
  
```cpp
baseURL branch="Monthly" URL="https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60" /
```

- The following is a language neutral file needed for all languages. The name of the file is v64_16.0.4229.1004.cab and it should be copied from https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/v64_16.0.4229.1004.cab and renamed to …/office/data/v64.cab.
    
  ```cpp
  baseURL branch="Business" URL="https://officecdn.microsoft.com/pr/7ffbc6bf-bc32-4f92-8982-f9dd17fd3114" /
  File name="v64_%version%.cab" rename="v64.cab" relativePath="/office/data/" language="0"/
  
  ```

- The following is a file to be included in the en-US image as designated by the language LCID=1033. The name of the file is s641033.cab and it should be copied from https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641033.cab and not renamed.
    
  ```cpp
  File name="s641033.cab" relativePath="/office/data/%version%/" language="1033" /
  ```

### Hash verification of data files

Image creation tools may verify the integrity of the downloaded .dat files by comparing a computed HASH value with the supplied HASH value associated with each of the .dat files. Below is an example of a .dat file from the Monthly channel with build version 16.0.4229.1004 and language set to Bulgarian.
  
```cpp
File name="stream.x64.bg-bg.dat" hashLocation="s641026.cab/stream.x64.bg-bg.hash" hashAlgo="Sha256" relativePath="/office/data/%version%/" language="1026"
```

- The  _hashLocation_ attribute specifies the relative path location of the stream.x64.bg-bg.hash for the stream.x64.bg-bg.dat file. Construct the hash file location by concatenating URL + relativePath + hashLocation. In this example the stream.x64.bg-bg.hash location would be https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
    
- The  _hashAlgo_ attribute specifies what hashing algorithm was used. In this case the Sha256 algorithm was used. 
    
To validate the integrity of the stream.x64.bg-bg.dat file, open the stream.x64.bg-bg.hash and read the hash value from the first line of text in the hash file. Compare this to the has value that you computed using the specified hashing algorithm to verify that the values match. Use the following C# code to read the hash.
  
```cs
string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
string readHash = readHashes.First();

```

### Office 365 Client Updates

Office 365 Client Updates enable manageability software to treat the Office 365 Client Updates in a manner very similar to any other WU update with one exception; the client updates do not contain an actual payload. The Office 365 Client Updates should not be installed on any clients but rather used to trigger the workflows with the manageability software replacing the installation command with the COM based installation mechanism shown above.
  
**Office 365 Client Update workflow**

![Workflow diagram for O365PP client updates.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Workflow diagram for O365PP client updates")
  
Each Office 365 Client Update that is published includes metadata about the update. This metadata includes a parameter called  _MoreInfoUrl_ which can be used to derive the following information: 
  
-  _Ver_: Identifies the Office version associated with this update. For example 16.0.4229.1004.
    
-  _Branch_: Identifies the Update Channel for this update. Values include InsiderFast, Insiders, Monthly, Targeted, Broad. Additional values may be added in the future.
    
-  _Arch_: Identifies the processor architecture associated with this update.
    
-  _xmlVer_: Identifies the version of the XML file lists to use to construct the base image for this update.
    
-  _xmlPath_: Path to the OFL.CAB file that contains the XML file lists.
    
-  _xmlFile_: The name of the file list that should be used for this update. The value will be  `O365Client_32bit` or  `O365Client_64bit` and will match the value in  _Arch_.
    
The following is an example of the  _MoreInfoURL_ parameter which refers to the Office 365 Client Update for the 32-bit version of Office with build version of 16.0.2342.2343 on the Current channel. 
  
```http
https://officecdn.microsoft.com/pr/wsus/ofl.cab is the location of the XML file lists for this update, specifically the O365Client_32bit.xml from within the OFL.CAB.
https://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.8326.2096&Branch=Current&Arch=64&XMLVer=1.4&xmlPath=https://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml 

```
THE ABOVE SECTION APPEARS TO BE A DUPLICATE OF THE FOLLOWING SECTION; TEMPORARILY COMMENTING IT OUT.-->

## <a name="automating-content-staging"></a><span data-ttu-id="19c67-289">Como automatizar o preparo do conteúdo</span><span class="sxs-lookup"><span data-stu-id="19c67-289">Automating content staging</span></span>

<span data-ttu-id="19c67-290">Os administradores podem optar por terem clientes de desktop habilitados a receber automaticamente atualizações quando estiverem disponíveis diretamente da CDN (Rede de Distribuição de Conteúdo) da Microsoft ou eles podem optar por controlar a implantação de atualizações disponíveis nos canais de atualização usando a Ferramenta de Implantação do Office ou o System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="19c67-290">IT administrators can choose to have desktop clients enabled to automatically receive updates when they are available directly from the Microsoft Content Delivery Network (CDN) or they can choose to control the deployment of updates available from the update channels using the Office Deployment Tool or System Center Configuration Manager.</span></span>
  
<span data-ttu-id="19c67-291">O serviço dá suporte à capacidade das ferramentas de gerenciamento de reconhecer e automatizar o download do conteúdo quando as atualizações são disponibilizadas.</span><span class="sxs-lookup"><span data-stu-id="19c67-291">The service supports the ability for management tools to recognize and automate the download of the content when updates are made available.</span></span>
  
<span data-ttu-id="19c67-292">**A imagem a seguir é uma visão geral de como baixar uma imagem personalizada**</span><span class="sxs-lookup"><span data-stu-id="19c67-292">**The following image is an overview of downloading a custom image**</span></span>

<span data-ttu-id="19c67-293">![Um diagrama usando a interface COM no instalador Clique para Executar do Office.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Um diagrama de usar a interface COM no instalador clique para executar do Office")</span><span class="sxs-lookup"><span data-stu-id="19c67-293">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "A diagram of using the COM interface on  the Office Click-To-Run installer")</span></span>
  
### <a name="overview-of-downloading-a-custom-image"></a><span data-ttu-id="19c67-294">Visão geral de como baixar uma imagem personalizada</span><span class="sxs-lookup"><span data-stu-id="19c67-294">Overview of downloading a custom image</span></span>
  
<span data-ttu-id="19c67-295">No diagrama anterior, você vê que uma nova imagem do Office 365 ProPlus está disponível na CDN (Rede de Distribuição de Conteúdo) do Office.</span><span class="sxs-lookup"><span data-stu-id="19c67-295">In the previous diagram, you see that a new Office 365 ProPlus image is available on the Office Content Distribution Network (CDN).</span></span> <span data-ttu-id="19c67-296">Com a imagem do Office 365 ProPlus, também está disponível uma lista de arquivos formatados em XML, que têm as informações necessárias para habilitar o software de capacidade de gerenciamento para criar diretamente imagens personalizadas, substituindo a necessidade de usar a Ferramenta de Implantação do Office.</span><span class="sxs-lookup"><span data-stu-id="19c67-296">Along with the Office 365 ProPlus image, an XML-formatted file list is also available which has the information needed to enable manageability software to directly create customized images replacing the need for using the Office Deployment Tool.</span></span>
  
<span data-ttu-id="19c67-297">Uma empresa configura o seu WSUS para sincronizar as Atualizações de Cliente do Office 365.</span><span class="sxs-lookup"><span data-stu-id="19c67-297">An enterprise configures their WSUS to sync the Office 365 Client Updates.</span></span> <span data-ttu-id="19c67-298">Essas atualizações não contêm a carga real da imagem, mas permitem que o software de capacidade de gerenciamento reconheça quando conteúdo novo está disponível.</span><span class="sxs-lookup"><span data-stu-id="19c67-298">These updates do not contain the actual image payload but does allow the manageability software to recognize when new content is available.</span></span> <span data-ttu-id="19c67-299">O software de capacidade de gerenciamento pode ler os metadados da Atualização do Cliente para entender à qual versão do Office a atualização se aplica.</span><span class="sxs-lookup"><span data-stu-id="19c67-299">The manageability software can then read the Client Update metadata to understand what version of Office the update applies to.</span></span>
  
<span data-ttu-id="19c67-300">Se a atualização for aplicável, o software de capacidade de gerenciamento pode usar o conteúdo da CDN e a lista de arquivos para criar a imagem personalizada e armazená-la no local do compartilhamento de arquivos que ele está configurado para usar.</span><span class="sxs-lookup"><span data-stu-id="19c67-300">If the update is applicable, the manageability software can use the CDN content and the file list to create the custom image and store it onto the file share location that it is configured to use.</span></span>
  
### <a name="format-of-the-xml-file-list"></a><span data-ttu-id="19c67-301">Formato da lista de arquivos XML</span><span class="sxs-lookup"><span data-stu-id="19c67-301">Format of the XML file list</span></span>

<span data-ttu-id="19c67-302">Há duas listas de arquivos disponíveis em um arquivo cab na CDN.</span><span class="sxs-lookup"><span data-stu-id="19c67-302">There are two file lists available in a cab file on the CDN.</span></span> <span data-ttu-id="19c67-303">Uma relaciona os arquivos para a versão de 32 bits do Office e a outra para a versão de 64 bits do Office.</span><span class="sxs-lookup"><span data-stu-id="19c67-303">One lists the files for the 32-bit version of Office and one for the 64-bit version of Office.</span></span> <span data-ttu-id="19c67-304">A URL do local do arquivo Lista de Arquivos do Office (OFL.CAB) é [https://officecdn.microsoft.com/pr/wsus/ofl.cab](https://officecdn.microsoft.com/pr/wsus/ofl.cab).</span><span class="sxs-lookup"><span data-stu-id="19c67-304">The URL of the location of the Office File List (OFL.CAB) file is [https://officecdn.microsoft.com/pr/wsus/ofl.cab](https://officecdn.microsoft.com/pr/wsus/ofl.cab).</span></span> <span data-ttu-id="19c67-305">As duas listas de arquivos são chamadas de:</span><span class="sxs-lookup"><span data-stu-id="19c67-305">The two file lists are called:</span></span>
  
- <span data-ttu-id="19c67-306">O365Client_32bit.xml</span><span class="sxs-lookup"><span data-stu-id="19c67-306">O365Client_32bit.xml</span></span>
    
- <span data-ttu-id="19c67-307">O365Client_64bit.xml</span><span class="sxs-lookup"><span data-stu-id="19c67-307">O365Client_64bit.xml</span></span>
    
<span data-ttu-id="19c67-308">No XML para cada uma das listas de arquivos, há um nó <UpdateFiles> que contém um atributo de versão.</span><span class="sxs-lookup"><span data-stu-id="19c67-308">Within the XML for each of the file lists is an <UpdateFiles> node which contains a version attribute.</span></span>  <span data-ttu-id="19c67-309">`<UpdateFiles version="1.4">`.</span><span class="sxs-lookup"><span data-stu-id="19c67-309">`<UpdateFiles version="1.4">`.</span></span> <span data-ttu-id="19c67-310">Essa versão será incrementada se alterações forem feitas nas listas de arquivos.</span><span class="sxs-lookup"><span data-stu-id="19c67-310">This version is incremented if changes are made to the file lists.</span></span>
  
<span data-ttu-id="19c67-311">Há dois parâmetros que precisam ser combinados com o XML para criar uma imagem personalizada:</span><span class="sxs-lookup"><span data-stu-id="19c67-311">There are two parameters that need to be combined with the XML to make a custom image:</span></span> 
  
- <span data-ttu-id="19c67-312">Substitua *%version%* pela versão do build do Office.</span><span class="sxs-lookup"><span data-stu-id="19c67-312">Replace  *%version%*  with the build version of Office.</span></span> <span data-ttu-id="19c67-313">Esse valor pode ser derivado dos metadados da Atualização do Cliente (explicado na próxima seção).</span><span class="sxs-lookup"><span data-stu-id="19c67-313">This can be derived from the Client Update metadata (explained in the next section).</span></span> 
    
- <span data-ttu-id="19c67-314">Defina *baseURL* usando o valor de URL associado à ramificação para a qual a imagem está sendo criada.</span><span class="sxs-lookup"><span data-stu-id="19c67-314">Define  *baseURL*  by using the URL value associated with the branch the image is being created for.</span></span> <span data-ttu-id="19c67-315">Esse valor é derivado dos metadados da Atualização do Cliente, explicado na seção a seguir.</span><span class="sxs-lookup"><span data-stu-id="19c67-315">This is derived from the Client Update metadata, explained in the following section.</span></span> 
    
<span data-ttu-id="19c67-316">As etapas para criar uma imagem são:</span><span class="sxs-lookup"><span data-stu-id="19c67-316">The steps for creating an image are:</span></span>
  
1. <span data-ttu-id="19c67-317">Abra a lista de arquivos XML.</span><span class="sxs-lookup"><span data-stu-id="19c67-317">Open the XML file list.</span></span>
    
2. <span data-ttu-id="19c67-318">Substitua as ocorrências de *%version%* pela versão aplicável do build do Office.</span><span class="sxs-lookup"><span data-stu-id="19c67-318">Replace occurrences of  *%version%*  with the applicable Office build version.</span></span> <span data-ttu-id="19c67-319">A versão do build pode ser adquirida em releasehistory.xml, conforme descrito mais adiante neste artigo.</span><span class="sxs-lookup"><span data-stu-id="19c67-319">The build version can be acquired from releasehistory.xml as described later in this article.</span></span> 
    
3. <span data-ttu-id="19c67-320">Leia o atributo URL para a ramificação de destino.</span><span class="sxs-lookup"><span data-stu-id="19c67-320">Read the URL attribute for the target branch.</span></span>
    
4. <span data-ttu-id="19c67-321">Remova os nós de idioma de todos os idiomas desnecessários na imagem personalizada.</span><span class="sxs-lookup"><span data-stu-id="19c67-321">Remove language nodes for any languages not required in the custom image.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="19c67-322">Os nós com idioma='0' têm neutralidade de idioma e devem ser incluídos na imagem.</span><span class="sxs-lookup"><span data-stu-id="19c67-322">Nodes with language='0' are language neutral and must be included in the image.</span></span> 
  
5. <span data-ttu-id="19c67-323">Crie uma imagem local da CDN iterando pela lista de arquivos XML e copiando os arquivos da CDN, enquanto cria a estrutura de pasta conforme a necessidade.</span><span class="sxs-lookup"><span data-stu-id="19c67-323">Construct a local image of the CDN by iterating through the XML file list and copying the CDN files, while creating the folder structure as needed.</span></span> 
    
   - <span data-ttu-id="19c67-324">Se o atributo *rename* for fornecido, isso significa que *rename* copiou o arquivo para o valor fornecido no atributo rename.</span><span class="sxs-lookup"><span data-stu-id="19c67-324">If the  *rename*  attribute is provided, then  *rename*  the copied file to the value provided in the rename attribute.</span></span> <span data-ttu-id="19c67-325">Isso é usado para criar os arquivos padrão de nível superior v64.cab e v32.cab.</span><span class="sxs-lookup"><span data-stu-id="19c67-325">This is used to create the top-level default v64.cab and v32.cab files.</span></span> <span data-ttu-id="19c67-326">Essas são as versões renomeadas do arquivo cab do build de nível superior e serão usadas como a versão de instalação padrão se a versão não for especificada.</span><span class="sxs-lookup"><span data-stu-id="19c67-326">These are the renamed versions of the top-level build cab file and are used as the default installation version if the version is not specified.</span></span> 
    
   - <span data-ttu-id="19c67-327">Use URL + relativePath + nome do arquivo para criar o local da CDN.</span><span class="sxs-lookup"><span data-stu-id="19c67-327">Use URL + relativePath + filename to construct the CDN location.</span></span>
    
<span data-ttu-id="19c67-328">Veja a seguir os exemplos que usam o canal Monthly (conforme definido pelo nó `<baseURL>`) e versão do build 16.0.4229.1004 em releasehistory.xml.</span><span class="sxs-lookup"><span data-stu-id="19c67-328">The following are examples that use the Monthly channel (as defined by the  `<baseURL>` node) and build version 16.0.4229.1004 from releasehistory.xml.</span></span> 
  
```xml
<baseURL branch="Monthly" URL="https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60" />
```

- <span data-ttu-id="19c67-329">Veja a seguir um arquivo com neutralidade de idioma necessário para todos os idiomas.</span><span class="sxs-lookup"><span data-stu-id="19c67-329">The following is a language neutral file needed for all languages.</span></span> <span data-ttu-id="19c67-330">O nome do arquivo é v64_16.0.4229.1004.cab e ele deve ser copiado de `https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/v64_16.0.4229.1004.cab` e renomeado para `…/office/data/v64.cab`.</span><span class="sxs-lookup"><span data-stu-id="19c67-330">The name of the file is v64_16.0.4229.1004.cab and it should be copied from `https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/v64_16.0.4229.1004.cab` and renamed to `…/office/data/v64.cab`.</span></span> 
    
  ```xml
  <File name="v64_%version%.cab" rename="v64.cab" relativePath="/office/data/" language="0"/>
  
  ```

- <span data-ttu-id="19c67-331">Veja a seguir um arquivo a ser incluído na imagem en-US como designado pela LCID = 1033 do idioma.</span><span class="sxs-lookup"><span data-stu-id="19c67-331">The following is a file to be included in the en-US image as designated by the language LCID=1033.</span></span> <span data-ttu-id="19c67-332">O nome do arquivo é s641033.cab e ele deve ser copiado de `https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641033.cab` e não deve ser renomeado.</span><span class="sxs-lookup"><span data-stu-id="19c67-332">The name of the file is s641033.cab and it should be copied from `https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641033.cab` and not renamed.</span></span>
    
  ```xml
  <File name="s641033.cab" relativePath="/office/data/%version%/" language="1033" />
  ```

### <a name="hash-verification-of-dat-files"></a><span data-ttu-id="19c67-333">Verificação de hash de arquivos .dat</span><span class="sxs-lookup"><span data-stu-id="19c67-333">Hash verification of .dat files</span></span>

<span data-ttu-id="19c67-334">As ferramentas de criação de imagens podem verificar a integridade dos arquivos .dat baixados comparando um valor de HASH calculado com o valor de HASH fornecido associado a cada um dos arquivos .dat.</span><span class="sxs-lookup"><span data-stu-id="19c67-334">Image creation tools may verify the integrity of the downloaded .dat files by comparing a computed HASH value with the supplied HASH value associated with each of the .dat files.</span></span> <span data-ttu-id="19c67-335">Veja a seguir um exemplo de arquivo .dat do canal Monthly com o build versão 16.0.4229.1004 e idioma definido como búlgaro:</span><span class="sxs-lookup"><span data-stu-id="19c67-335">Following is an example of a .dat file from the Monthly channel with build version 16.0.4229.1004 and language set to Bulgarian:</span></span>
  
```xml
<File name="stream.x64.bg-bg.dat" hashLocation="s641026.cab/stream.x64.bg-bg.hash" hashAlgo="Sha256" relativePath="/office/data/%version%/" language="1026"/>
```

- <span data-ttu-id="19c67-336">O atributo **hashLocation** especifica o local do caminho relativo de stream.x64.bg-bg.hash para o arquivo stream.x64.bg-bg.dat.</span><span class="sxs-lookup"><span data-stu-id="19c67-336">The **hashLocation** attribute specifies the relative path location of the stream.x64.bg-bg.hash for the stream.x64.bg-bg.dat file.</span></span> <span data-ttu-id="19c67-337">Crie o local do arquivo hash concatenando a URL + relativePath + hashLocation.</span><span class="sxs-lookup"><span data-stu-id="19c67-337">Construct the hash file location by concatenating URL + relativePath + hashLocation.</span></span> <span data-ttu-id="19c67-338">No seguinte exemplo, o local stream.x64.bg-bg.hash seria:</span><span class="sxs-lookup"><span data-stu-id="19c67-338">In the following example, the stream.x64.bg-bg.hash location would be:</span></span> 
    
  ```http
  https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
  ```

- <span data-ttu-id="19c67-339">O atributo **hashAlgo** especifica qual algoritmo de hash foi usado.</span><span class="sxs-lookup"><span data-stu-id="19c67-339">The **hashAlgo** attribute specifies what hashing algorithm was used.</span></span> <span data-ttu-id="19c67-340">Nesse caso, foi usado Sha256.</span><span class="sxs-lookup"><span data-stu-id="19c67-340">In this case Sha256 was used.</span></span> 
    
  <span data-ttu-id="19c67-341">Para validar a integridade do arquivo stream.x64.bg-bg.dat, abra o stream.x64.bg-bg.hash e leia o valor do HASH, que é a primeira linha do texto no arquivo de hash.</span><span class="sxs-lookup"><span data-stu-id="19c67-341">To validate the integrity of the stream.x64.bg-bg.dat file, open the stream.x64.bg-bg.hash and read the HASH value which is the first line of text in the hash file.</span></span> <span data-ttu-id="19c67-342">Compare-o com o valor do hash calculado (usando o algoritmo de hash especificado) para verificar a integridade do arquivo .dat baixado.</span><span class="sxs-lookup"><span data-stu-id="19c67-342">Compare this to the computed hash value (using the specified hashing algorithm) to verify the integrity of the downloaded .dat file.</span></span>
    
  <span data-ttu-id="19c67-343">O exemplo a seguir mostra o código C# para leitura do hash.</span><span class="sxs-lookup"><span data-stu-id="19c67-343">The following example shows the C# code to read the hash.</span></span>
    
  ```cs
    string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
    string readHash = readHashes.First();
  ```

### <a name="office-365-client-updates"></a><span data-ttu-id="19c67-344">Atualizações de cliente do Office 365</span><span class="sxs-lookup"><span data-stu-id="19c67-344">Office 365 Client Updates</span></span>

<span data-ttu-id="19c67-345">Todas as Atualizações de Cliente do Office 365 são publicadas no [Catálogo do Microsoft Update](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).</span><span class="sxs-lookup"><span data-stu-id="19c67-345">All Office 365 Client Updates are published to the [Microsoft Update Catalog](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).</span></span>
  
<span data-ttu-id="19c67-346">As Atualizações de Cliente do Office 365 permitem que o software de capacidade de gerenciamento trate as Atualizações de Cliente do Office 365 de maneira muito semelhante a qualquer outra atualização do WU, com uma única exceção: as atualizações de cliente não contêm uma carga real.</span><span class="sxs-lookup"><span data-stu-id="19c67-346">Office 365 Client Updates enable manageability software to treat the Office 365 Client Updates in a manner very similar to any other WU update with one exception; the client updates do not contain an actual payload.</span></span> <span data-ttu-id="19c67-347">As Atualizações de Cliente do Office 365 não devem ser instaladas em qualquer cliente, mas usadas para disparar os fluxos de trabalho com o software de capacidade de gerenciamento substituindo o comando de instalação pelo mecanismo de instalação baseado em COM mostrado acima.</span><span class="sxs-lookup"><span data-stu-id="19c67-347">The Office 365 Client Updates should not be installed on any clients but rather used to trigger the workflows with the manageability software replacing the installation command with the COM based installation mechanism shown above.</span></span> 
  
<span data-ttu-id="19c67-348">**A figura a seguir mostra um diagrama do fluxo de trabalho da Atualização de Cliente do Office 365.**</span><span class="sxs-lookup"><span data-stu-id="19c67-348">**The following figure shows a diagram of the Office 365 Client Update workflow.**</span></span>

<span data-ttu-id="19c67-349">![Diagrama de fluxo de trabalho de atualizações do cliente O365PP .](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Diagrama de fluxo de trabalho para atualizações do cliente O365PP")</span><span class="sxs-lookup"><span data-stu-id="19c67-349">![Workflow diagram for O365PP client updates.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Workflow diagram for O365PP client updates")</span></span>
  
<span data-ttu-id="19c67-350">Cada Atualização de Cliente do Office 365 que é publicada inclui metadados sobre a atualização.</span><span class="sxs-lookup"><span data-stu-id="19c67-350">Each Office 365 Client Update that is published includes metadata about the update.</span></span> <span data-ttu-id="19c67-351">Esses metadados incluem um parâmetro chamado *MoreInfoUrl*, que pode ser usado para derivar as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="19c67-351">This metadata includes a parameter called  *MoreInfoUrl*  which can be used to derive the following information:</span></span> 
  
-  <span data-ttu-id="19c67-352">*Ver*: identifica a versão do Office associada a essa atualização.</span><span class="sxs-lookup"><span data-stu-id="19c67-352">*Ver*: Identifies the Office version associated with this update.</span></span> 
    
-  <span data-ttu-id="19c67-353">*Branch*: identifica o Canal de Atualizações para essa atualização.</span><span class="sxs-lookup"><span data-stu-id="19c67-353">*Branch*: Identifies the Update Channel for this update.</span></span> <span data-ttu-id="19c67-354">Os valores incluem InsiderFast, Insiders, Monthly, Targeted, Broad.</span><span class="sxs-lookup"><span data-stu-id="19c67-354">Values include InsiderFast, Insiders, Monthly, Targeted, Broad.</span></span> <span data-ttu-id="19c67-355">Outros valores podem ser adicionados no futuro.</span><span class="sxs-lookup"><span data-stu-id="19c67-355">Additional values may be added in the future.</span></span> 
    
-  <span data-ttu-id="19c67-356">*Arch*: identifica a arquitetura do processador associada a essa atualização.</span><span class="sxs-lookup"><span data-stu-id="19c67-356">*Arch*: Identifies the processor architecture associated with this update.</span></span> 
    
-  <span data-ttu-id="19c67-357">*xmlVer*: a versão das listas de arquivos XML que deve ser usada para criar a imagem base dessa atualização.</span><span class="sxs-lookup"><span data-stu-id="19c67-357">*xmlVer*: The version of the XML file lists that should be used to construct the base image for this update.</span></span> 
    
-  <span data-ttu-id="19c67-358">*xmlPath*: caminho para o arquivo OFL.CAB, que contém as listas de arquivos XML.</span><span class="sxs-lookup"><span data-stu-id="19c67-358">*xmlPath*: Path to the OFL.CAB file which contains the XML file lists.</span></span> 
    
-  <span data-ttu-id="19c67-359">*mlFile*: o nome da lista de arquivos que deve ser usada para essa atualização.</span><span class="sxs-lookup"><span data-stu-id="19c67-359">*mlFile*: The name of the file list that should be used for this update.</span></span> <span data-ttu-id="19c67-360">O valor será O365Client_32bit ou O365Client_64bit e corresponderá ao valor de Arch.</span><span class="sxs-lookup"><span data-stu-id="19c67-360">The value will be O365Client_32bit or O365Client_64bit and will match the Arch.</span></span> 
    
<span data-ttu-id="19c67-361">A URL a seguir é um exemplo do parâmetro *MoreInfoURL* que se refere às liberações de atualização de cliente do Office 365 para a versão de 32 bits do Office com a versão de build 16.0.2342.2343 no Canal Atual.</span><span class="sxs-lookup"><span data-stu-id="19c67-361">The following URL is an example of the  *MoreInfoURL*  parameter which refers to the Office 365 client update releases for the 32-bit version of Office with build version of 16.0.2342.2343 on the Current channel.</span></span> 
  
<span data-ttu-id="19c67-362">https://officecdn.microsoft.com/pr/wsus/ofl.cab é o local das listas de arquivos XML para essa atualização, especificamente o O365Client_32bit.xml de dentro de OFL.CAB.</span><span class="sxs-lookup"><span data-stu-id="19c67-362">https://officecdn.microsoft.com/pr/wsus/ofl.cab is the location of the XML file lists for this update, specifically the O365Client_32bit.xml from within the OFL.CAB.</span></span>
  
[<span data-ttu-id="19c67-363">Lançamentos do canal de atualização de cliente do Office 365</span><span class="sxs-lookup"><span data-stu-id="19c67-363">Office 365 client update channel releases</span></span>](https://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.8326.2096&Branch=Current&Arch=64&XMLVer=1.4&xmlPath=https://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml)
  
### <a name="additional-metadata-for-automating-content-staging"></a><span data-ttu-id="19c67-364">Metadados adicionais para automatização do preparo de conteúdo</span><span class="sxs-lookup"><span data-stu-id="19c67-364">Additional metadata for automating content staging</span></span>

<span data-ttu-id="19c67-365">Além dos metadados que são publicados, também há arquivos XML adicionais publicados na CDN que podem ajudar a fornecer informações adicionais sobre os clientes do Office 365 que estão disponível na CDN do Office.</span><span class="sxs-lookup"><span data-stu-id="19c67-365">In addition to the metadata that is published which defines there are also additional XML files published to the CDN that can help provide additional information about the Office 365 clients that are available from the Office CDN.</span></span>
  
<span data-ttu-id="19c67-366">**SKUS.XML**</span><span class="sxs-lookup"><span data-stu-id="19c67-366">**SKUS.XML**</span></span>
  
<span data-ttu-id="19c67-367">Esse arquivo XML está contido em um CAB assinado e é publicado na CDN do Office na seguinte URL: [https://officecdn.microsoft.com/pr/wsus/skus.cab](https://officecdn.microsoft.com/pr/wsus/skus.cab).</span><span class="sxs-lookup"><span data-stu-id="19c67-367">This XML file is contained within a signed CAB and published to the Office CDN at the following URL: [https://officecdn.microsoft.com/pr/wsus/skus.cab](https://officecdn.microsoft.com/pr/wsus/skus.cab).</span></span>
  
<span data-ttu-id="19c67-368">Os metadados publicados nesse arquivo XML são úteis para determinar quais produtos estão disponíveis para implantação e manutenção na CDN do Office com várias opções para cada um.</span><span class="sxs-lookup"><span data-stu-id="19c67-368">The metadata published in this XML file is useful for determining which products are available for deployment and servicing from the Office CDN along with various options for each.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<ReleaseInfo PublishedDate="08/07/2017 16:34">
  <!-- Suite / App catalog -->
  <Suite>
    <SKU Name="Office 365 ProPlus" ProductID="O365ProPlusRetail" Default="True">
      <Apps>
        <App Name="Access" AppID="Access" />
        <App Name="Excel" AppID="Excel" />
        <App Name="OneDrive for Business (Groove)" AppID="Groove" />
        <App Name="OneDrive for Business (Next Gen Sync Client)" AppID="OneDrive" />
        <App Name="OneNote" AppID="OneNote" />
        <App Name="Outlook" AppID="Outlook" />
        <App Name="PowerPoint" AppID="PowerPoint" />
        <App Name="Publisher" AppID="Publisher" />
        <App Name="Skype for Business" AppID="Lync" />
        <App Name="Word" AppID="Word" />
      </Apps>
      <Channels>
        <Channel ID="Monthly"/>
        <Channel ID="Insiders"/>
        <Channel ID="Targeted"/>
        <Channel ID="Broad"/>
      </Channels>
    </SKU>
```

<span data-ttu-id="19c67-369">O nó raiz **\<ReleaseInfo\>** contém o atributo PublishedDate que identifica a data em que esse arquivo foi publicado.</span><span class="sxs-lookup"><span data-stu-id="19c67-369">**\<ReleaseInfo\>** root node contains the PublishedDate attribute which identifies the date which this file was published.</span></span> 
  
<span data-ttu-id="19c67-370">O nó **\<SKU\>** identifica um SKU individual.</span><span class="sxs-lookup"><span data-stu-id="19c67-370">**\<SKU\>** node identifies an individual SKU.</span></span> 
  
- <span data-ttu-id="19c67-371">O atributo *ProductID* identifica a ID que é passada como o atributo ID no arquivo configuration.xml no caso de uso do ODT.</span><span class="sxs-lookup"><span data-stu-id="19c67-371">The  *ProductID*  attribute identifies the ID that is passed as the ID attribute in the configuration.xml if using the ODT.</span></span> <span data-ttu-id="19c67-372">Por exemplo, `<Product ID="O365ProPlusRetail">`.</span><span class="sxs-lookup"><span data-stu-id="19c67-372">For example, `<Product ID="O365ProPlusRetail">`.</span></span> 
    
- <span data-ttu-id="19c67-373">O atributo *Default*, se definido como True, identifica o SKU recomendado.</span><span class="sxs-lookup"><span data-stu-id="19c67-373">The  *Default*  attribute, if set to True, identifies the recommended SKU.</span></span> 
    
<span data-ttu-id="19c67-374">Os nós **\<App\>** são usados para definir os aplicativos individuais do Office aos quais cada SKU dá suporte.</span><span class="sxs-lookup"><span data-stu-id="19c67-374">**\<App\>** nodes are used to define the individual Office apps that each SKU supports.</span></span> 
  
- <span data-ttu-id="19c67-375">O atributo *Name* é o nome do aplicativo exibido.</span><span class="sxs-lookup"><span data-stu-id="19c67-375">The  *Name*  attribute is the displayed application name.</span></span> 
    
- <span data-ttu-id="19c67-376">O atributo *AppID* é o atributo ID passado no arquivo configuration.xml para o nó **\<ExcludeApp\>** no caso de uso do ODT.</span><span class="sxs-lookup"><span data-stu-id="19c67-376">The  *AppID*  attribute is the ID attribute passed in the configuration.xml for the **\<ExcludeApp\>** node if using the ODT.</span></span> <span data-ttu-id="19c67-377">Por exemplo, `<ExcludeApp ID="Publisher" />`.</span><span class="sxs-lookup"><span data-stu-id="19c67-377">For example, `<ExcludeApp ID="Publisher" />`.</span></span> 
    
<span data-ttu-id="19c67-378">**RELEASEHISTORY.XML**</span><span class="sxs-lookup"><span data-stu-id="19c67-378">**RELEASEHISTORY.XML**</span></span>
  
<span data-ttu-id="19c67-379">Esse arquivo XML está contido em um CAB assinado e é publicado na CDN do Office no seguinte local: [https://officecdn.microsoft.com/pr/wsus/releasehistory.cab](https://officecdn.microsoft.com/pr/wsus/releasehistory.cab).</span><span class="sxs-lookup"><span data-stu-id="19c67-379">This XML file is contained within a signed CAB and published to the Office CDN at the following location: [https://officecdn.microsoft.com/pr/wsus/releasehistory.cab](https://officecdn.microsoft.com/pr/wsus/releasehistory.cab).</span></span> 
  
<span data-ttu-id="19c67-380">Os metadados publicados nesse arquivo XML são úteis para determinar quais canais têm suporte para atualizações de manutenção da CDN do Office com informações sobre o histórico do build para cada um dos canais com suporte.</span><span class="sxs-lookup"><span data-stu-id="19c67-380">The metadata published in this XML file is useful for determining which channels are supported for servicing updates from the Office CDN along with information about the build history for each of the supported channels.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<ReleaseHistory PublishedDate="10/22/2017 00:48">
  <UpdateChannel Name="Current" ID="Monthly" DisplayName="Monthly Channel">
    <Update Latest="True" Version="1709" LegacyVersion="16.0.8528.2139" Build="8528.2139" PubTime="2017-10-16T19:45:50.743Z" />
    <Update Latest="False" Version="1708" LegacyVersion="16.0.8431.2107" Build="8431.2107" PubTime="2017-10-11T01:52:33.793Z" />
    <Update Latest="False" Version="1708" LegacyVersion="16.0.8431.2079" Build="8431.2079" PubTime="2017-09-18T22:26:13.673Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2107" Build="8326.2107" PubTime="2017-09-12T18:56:53.657Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2096" Build="8326.2096" PubTime="2017-08-30T00:10:25.253Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2076" Build="8326.2076" PubTime="2017-08-19T00:13:01.787Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2073" Build="8326.2073" PubTime="2017-08-11T19:35:42.173Z" />
  </UpdateChannel>
```

<span data-ttu-id="19c67-381">O nó raiz **\<ReleaseHistory\>** contém o atributo PublishedDate, que identifica a data em que esse arquivo foi publicado.</span><span class="sxs-lookup"><span data-stu-id="19c67-381">The **\<ReleaseHistory\>** root node contains the PublishedDate attribute which identifies the date which this file was published.</span></span> 
  
<span data-ttu-id="19c67-382">O nó **\<UpdateChannel\>** define um canal com suporte.</span><span class="sxs-lookup"><span data-stu-id="19c67-382">The **\<UpdateChannel\>** node defines a supported channel.</span></span> 
  
- <span data-ttu-id="19c67-383">O atributo *Name* define a ID do canal que é usada na passagem para o ODT no arquivo configuration.xml como o atributo Channel.</span><span class="sxs-lookup"><span data-stu-id="19c67-383">The  *Name*  attribute defines the channel ID which is used to pass to the ODT in the configuration.xml as the Channel attribute.</span></span> 
    
  <span data-ttu-id="19c67-384">Exemplo: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Current">`</span><span class="sxs-lookup"><span data-stu-id="19c67-384">Example: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Current">`</span></span> 
    
  > [!NOTE] 
  > <span data-ttu-id="19c67-385">Esse atributo foi preterido e é usado apenas para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="19c67-385">This attribute has been deprecated and is used for backward compatibility only.</span></span> <span data-ttu-id="19c67-386">Use o atributo ID no lugar do atributo Name.</span><span class="sxs-lookup"><span data-stu-id="19c67-386">Use the ID attribute in place of the Name attribute.</span></span> 
    
- <span data-ttu-id="19c67-387">O atributo *ID* define a ID do canal que é usada na passagem para o ODT no arquivo configuration.xml como o atributo Channel.</span><span class="sxs-lookup"><span data-stu-id="19c67-387">The  *ID*  attribute defines the channel ID which is used to pass to the ODT in the configuration.xml as the Channel attribute.</span></span> 
    
  <span data-ttu-id="19c67-388">Exemplo: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Deferred">`</span><span class="sxs-lookup"><span data-stu-id="19c67-388">Example: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Deferred">`</span></span> 
    
- <span data-ttu-id="19c67-389">O atributo **DisplayName** é usado como o nome de exibição.</span><span class="sxs-lookup"><span data-stu-id="19c67-389">The **DisplayName**  attribute is used as the display name.</span></span> 
    
<span data-ttu-id="19c67-390">O nó **\<Update\>** é usado para definir cada atualização que foi publicada para esse canal particular.</span><span class="sxs-lookup"><span data-stu-id="19c67-390">The **\<Update\>** node is used to define each update that has been published for that particular channel.</span></span> 
  
- <span data-ttu-id="19c67-391">O atributo **Latest**, se definido como True, determina o lançamento mais recente para esse canal.</span><span class="sxs-lookup"><span data-stu-id="19c67-391">The **Latest**  attribute, if set to True, defines the release that is the latest release for that channel.</span></span> 
    
- <span data-ttu-id="19c67-392">O atributo **Version** define o número de versão para essa atualização específica.</span><span class="sxs-lookup"><span data-stu-id="19c67-392">The **Version** attribute defines the version number for this particular update.</span></span> 
    
- <span data-ttu-id="19c67-393">O atributo **LegacyVersion** define o número da versão completa para essa atualização específica.</span><span class="sxs-lookup"><span data-stu-id="19c67-393">The **LegacyVersion** attribute defines the full version number for this particular update.</span></span> 
    
- <span data-ttu-id="19c67-394">O atributo **Build** define o número do build para essa atualização específica.</span><span class="sxs-lookup"><span data-stu-id="19c67-394">The **Build** attribute defines the build number for this particular update.</span></span> 
    
- <span data-ttu-id="19c67-395">O atributo **PubTime** define a data e a hora em que essa atualização foi publicada na CDN do Office.</span><span class="sxs-lookup"><span data-stu-id="19c67-395">The **PubTime** attribute defines the date and time at which this update was published to the Office CDN.</span></span> 
    

