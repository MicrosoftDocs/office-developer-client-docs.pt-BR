---
title: Integrar aplicativos de capacidade de gerenciamento com o instalador de click-to-run do Office 365
manager: kelbow
ms.date: 10/22/2017
ms.audience: ITPro
localization_priority: Normal
ms.assetid: c0fa8fed-1585-4566-a9be-ef6d6d1b4ce8
description: Saiba como integrar o instalador do Office 365 Click-to-Run com uma solução de gerenciamento de software.
ms.openlocfilehash: abe941e3e3818eed1f18108f1678e46e8156b08c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771189"
---
# <a name="integrating-manageability-applications-with-office-365-click-to-run-installer"></a><span data-ttu-id="b0b47-103">Integrar aplicativos de capacidade de gerenciamento com o instalador de click-to-run do Office 365</span><span class="sxs-lookup"><span data-stu-id="b0b47-103">Integrating manageability applications with Office 365 click-to-run installer</span></span>

<span data-ttu-id="b0b47-104">Saiba como integrar o instalador do Office 365 Click-to-Run com uma solução de gerenciamento de software.</span><span class="sxs-lookup"><span data-stu-id="b0b47-104">Learn how to integrate the Office 365 Click-to-Run installer with a software management solution.</span></span>
  
<span data-ttu-id="b0b47-105">O instalador do Click-to-Run do Office 365 fornece uma interface COM que permite que os profissionais de TI e soluções de gerenciamento de software controle programático sobre gerenciamento de atualizações.</span><span class="sxs-lookup"><span data-stu-id="b0b47-105">The Office 365 Click-to-Run installer provides a COM interface that allows IT Professionals and software management solutions programmatic control over update management.</span></span> <span data-ttu-id="b0b47-106">Esta interface oferece recursos de gerenciamento adicionais além do que é fornecido pela ferramenta de implantação do Office.</span><span class="sxs-lookup"><span data-stu-id="b0b47-106">This interface provides additional management capabilities beyond what is provided by the Office Deployment Tool.</span></span>
  
> [!NOTE]
> <span data-ttu-id="b0b47-107">Este artigo se aplica ao Office 2016 e posterior, Office 365.</span><span class="sxs-lookup"><span data-stu-id="b0b47-107">This article applies to Office 2016 and later, Office 365.</span></span> 
  
## <a name="integrating-with-the-click-to-run"></a><span data-ttu-id="b0b47-108">Integrando com o Click-to-Run</span><span class="sxs-lookup"><span data-stu-id="b0b47-108">Integrating with the Click-to-Run</span></span>

<span data-ttu-id="b0b47-109">Para usar essa interface, um aplicativo de gerenciabilidade invoca a interface COM e chamadas expostos APIs que se comunicam diretamente com o serviço de instalação Click-to-Run.</span><span class="sxs-lookup"><span data-stu-id="b0b47-109">To use this interface, a manageability application invokes the COM interface and calls exposed APIs that communicate directly with the Click-to-Run installation service.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b0b47-110">O instalador do Office Click-to-Run pode ser executado na linha de comando com os parâmetros que podem controlar o comportamento, conforme documentado no [Office Deployment Tool for Click-to-Run](https://www.microsoft.com/en-us/download/details.aspx?id=49117).</span><span class="sxs-lookup"><span data-stu-id="b0b47-110">The Office Click-to-Run installer can be run from the command-line with parameters that can control the behavior, as documented in [Office Deployment Tool for Click-to-Run](https://www.microsoft.com/en-us/download/details.aspx?id=49117).</span></span> 
  
<span data-ttu-id="b0b47-111">**A seguir é um diagrama conceitual da interface COM**</span><span class="sxs-lookup"><span data-stu-id="b0b47-111">**Following is a conceptual diagram of the COM interface**</span></span>

<span data-ttu-id="b0b47-112">![Um diagrama de usar a interface COM no installer Office Click-To-Run.] (media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Um diagrama de usar a interface COM no installer Click-To-Run do Office")</span><span class="sxs-lookup"><span data-stu-id="b0b47-112">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "A diagram of using the COM interface on  the Office Click-To-Run installer")</span></span>
  
<span data-ttu-id="b0b47-113">A interface do Office 365 Click-to-Run installer implementa um baseado em COM, **IUpdateNotify** registrado para CLSID **CLSID_UpdateNotifyObject**.</span><span class="sxs-lookup"><span data-stu-id="b0b47-113">The Office 365 Click-to-Run installer implements a COM-based interface, **IUpdateNotify** registered to CLSID **CLSID_UpdateNotifyObject**.</span></span>
  
<span data-ttu-id="b0b47-114">Essa interface pode ser invocado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="b0b47-114">This interface can be invoked as follows:</span></span>
  
```cpp
hr = CoCreateInstance(CLSID_UpdateNotifyObject, NULL, CLSCTX_ALL,
       IID_IUpdateNotify, 
      (void **)&p); 
```

<span data-ttu-id="b0b47-115">A chamada só será bem-sucedida se o chamador está sendo executado em privilégios elevados, como o programa de instalação Click-to-Run deve ser executado com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="b0b47-115">The call will only succeed if the caller is running under elevated privileges, as the Click-to-Run installation program must be run with elevated privileges.</span></span>
  
<span data-ttu-id="b0b47-116">A interface **IUpdateNotify** COM expõe três funções assíncronas responsáveis para validar os comandos e parâmetros e agendar a execução com o serviço de instalação Click-to-Run.</span><span class="sxs-lookup"><span data-stu-id="b0b47-116">The **IUpdateNotify** COM interface exposes three asynchronous functions responsible for validating the commands and parameters and scheduling execution with the Click-to-Run installation service.</span></span> 
  
```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
HRESULT Cancel() // Cancel the download action.

```

<span data-ttu-id="b0b47-117">A outro método, o **Status**, pode ser usado para obter mais informações sobre o status do último comando executado ou o status do comando atualmente em execução (ou seja, êxito, falha, códigos de erro detalhadas).</span><span class="sxs-lookup"><span data-stu-id="b0b47-117">A forth method, **Status**, can be used to get information about the status of the last executed command or the status of the currently executing command (i.e. success, failure, detailed error codes).</span></span>
  
```cpp
HRESULT status([out] _UPDATE_STATUS_REPORT* pUpdateStatusReport) // Get status of current action. 
typedef struct _UPDATE_STATUS_REPORT  
{  
UPDATE_STATUS status;  
UINT error; 
BSTR contentid;  
} UPDATE_STATUS_REPORT;

```

<span data-ttu-id="b0b47-118">Existem quatro estados de que o serviço de instalação Click-to-Run pode estar em durante o ciclo de vida, durante o qual os métodos **IUpdateNotify** poderão ser convocados; Reinicializar, ociosa, baixando e aplicação.</span><span class="sxs-lookup"><span data-stu-id="b0b47-118">There are four states that the Click-to-Run installation service may be in during its lifecycle, during which **IUpdateNotify** methods may be called; Rebooting, Idle, Downloading and Applying.</span></span> 
  
<span data-ttu-id="b0b47-119">**A seguir é o diagrama de máquina de estado de Interface COM**</span><span class="sxs-lookup"><span data-stu-id="b0b47-119">**Following is the COM Interface State Machine diagram**</span></span>

<span data-ttu-id="b0b47-120">![Um diagrama de estado para a interface COM.] (media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "Um diagrama de estado para a interface COM")</span><span class="sxs-lookup"><span data-stu-id="b0b47-120">![A state diagram for the COM interface.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "A state diagram for the COM interface")</span></span>
  
> [!NOTE]
> <span data-ttu-id="b0b47-121">**Rebooting**: quando o computador está inicializando há um período de tempo quando o serviço do installer Click-to-Run não está disponível.</span><span class="sxs-lookup"><span data-stu-id="b0b47-121">**Rebooting**: When the machine is booting there is a period of time when the Click-to-Run installer service is not available.</span></span> <span data-ttu-id="b0b47-122">Uma chamada bem sucedida para o método de Status após uma reinicialização retornará eUPDATE_UNKNOWN.</span><span class="sxs-lookup"><span data-stu-id="b0b47-122">A successful call to the Status method after a reboot will return eUPDATE_UNKNOWN.</span></span> 
  
<span data-ttu-id="b0b47-123">**Ocioso:** Quando o instalador Click-to-Run está no estado ocioso, você pode chamar:</span><span class="sxs-lookup"><span data-stu-id="b0b47-123">**Idle:** When the Click-to-Run installer is in the idle state, you can call:</span></span> 
  
- <span data-ttu-id="b0b47-124">**Aplicar**: Install conteúdo baixado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b0b47-124">**Apply**: Install previously downloaded content.</span></span>
    
- <span data-ttu-id="b0b47-125">**Cancelar**: retorna `0x800000e`, "um método foi chamado num momento inesperado".</span><span class="sxs-lookup"><span data-stu-id="b0b47-125">**Cancel**: Returns  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="b0b47-126">**Download**: baixa o novo conteúdo para o cliente para instalação posterior.</span><span class="sxs-lookup"><span data-stu-id="b0b47-126">**Download**: Downloads new content to the client for later installation.</span></span>
    
- <span data-ttu-id="b0b47-127">**Status**: retorna o resultado de uma mensagem de erro ou a última ação concluída se a ação é encerrada em falha.</span><span class="sxs-lookup"><span data-stu-id="b0b47-127">**Status**: Returns the result of the last completed action, or an error message if the action ended in failure.</span></span> <span data-ttu-id="b0b47-128">Se não houver nenhuma ação anterior, o **Status** retorna `eUPDATE_UNKNOWN`.</span><span class="sxs-lookup"><span data-stu-id="b0b47-128">If there is no previous action, **Status** returns  `eUPDATE_UNKNOWN`.</span></span>
    
<span data-ttu-id="b0b47-129">**Baixando:** Quando o instalador Click-to-Run está no estado de download, você pode chamar:</span><span class="sxs-lookup"><span data-stu-id="b0b47-129">**Downloading:** When the Click-to-Run installer is in the downloading state, you can call:</span></span> 
  
- <span data-ttu-id="b0b47-130">**Aplicar**: retorna um **HRESULT** com o valor `0x800000e`, "um método foi chamado num momento inesperado".</span><span class="sxs-lookup"><span data-stu-id="b0b47-130">**Apply**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="b0b47-131">**Cancelar**: interrompe o download e remove o conteúdo baixado parcialmente.</span><span class="sxs-lookup"><span data-stu-id="b0b47-131">**Cancel**: Stops the download and removes the partially downloaded content.</span></span>
    
- <span data-ttu-id="b0b47-132">**Download**: retorna um **HRESULT** com o valor `0x800000e`, "um método foi chamado num momento inesperado".</span><span class="sxs-lookup"><span data-stu-id="b0b47-132">**Download**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span> 
    
- <span data-ttu-id="b0b47-133">**Status**: retorna **DOWNLOAD_WIP** para indicar que o trabalho de download está em andamento.</span><span class="sxs-lookup"><span data-stu-id="b0b47-133">**Status**: Returns **DOWNLOAD_WIP** to indicate that download work is in progress.</span></span> 
    
<span data-ttu-id="b0b47-134">**Aplicação:** Quando o instalador do Click-to-Run está no processo de instalação anteriormente Baixe conteúdo:</span><span class="sxs-lookup"><span data-stu-id="b0b47-134">**Applying:** When the Click-to-Run installer is in the process of installing previously download content:</span></span> 
  
- <span data-ttu-id="b0b47-135">**Aplicar**: retorna um **HRESULT** com o valor `0x800000e`, "um método foi chamado num momento inesperado".</span><span class="sxs-lookup"><span data-stu-id="b0b47-135">**Apply**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="b0b47-136">**Cancelar**: retorna `0x800000e`, a ação de aplicar não pode ser cancelada.</span><span class="sxs-lookup"><span data-stu-id="b0b47-136">**Cancel**: Returns  `0x800000e`, the Apply action cannot be canceled.</span></span>
    
- <span data-ttu-id="b0b47-137">**Download**: retorna um **HRESULT** com o valor `0x800000e`, "um método foi chamado num momento inesperado".</span><span class="sxs-lookup"><span data-stu-id="b0b47-137">**Download**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span> 
    
- <span data-ttu-id="b0b47-138">**Status**: retorna **APPLY_WIP** para indicar que se aplicam a trabalho estiver em andamento.</span><span class="sxs-lookup"><span data-stu-id="b0b47-138">**Status**: Returns **APPLY_WIP** to indicate that apply work is in progress.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="b0b47-139">Como OfficeC2RCOM é um serviço COM + e é carregado dinamicamente, você precisará chamar **CoCreateInstance** toda vez que você chama um método nessa classe para garantir que você obtenha o resultado esperado.</span><span class="sxs-lookup"><span data-stu-id="b0b47-139">Since OfficeC2RCOM is a COM+ service and is dynamically loaded, you need to call **CoCreateInstance** every time you call a method on this class to ensure that you get the expected result.</span></span> <span data-ttu-id="b0b47-140">O serviço COM + manipulará criando uma nova instância, se necessário.</span><span class="sxs-lookup"><span data-stu-id="b0b47-140">The COM+ service will handle creating a new instance if necessary.</span></span> <span data-ttu-id="b0b47-141">Quando um dos métodos é chamado pela primeira vez, COM + carregará o objeto **IUpdateNotify** e executá-lo dentro de uma das instâncias dllhost.exe.</span><span class="sxs-lookup"><span data-stu-id="b0b47-141">When one of the methods is called for the first time, COM+ will load the **IUpdateNotify** object and run it within one of the dllhost.exe instances.</span></span> <span data-ttu-id="b0b47-142">O novo objeto ficará ativo por cerca de 3 minutos em ocioso.</span><span class="sxs-lookup"><span data-stu-id="b0b47-142">The new object will stay active for about 3 minutes in idle.</span></span> <span data-ttu-id="b0b47-143">Se for feita uma chamada de subsequente em três minutos da última chamada, o objeto **IUpdateNotify** permanecerá carregado e uma nova instância não é criada.</span><span class="sxs-lookup"><span data-stu-id="b0b47-143">If a subsequent call is made within three minutes of the last call, the **IUpdateNotify** object will remain loaded and a new instance is not created.</span></span> <span data-ttu-id="b0b47-144">Se nenhuma chamada for feita em três minutos, o objeto IUpdateNotify será descarregado e será criado um novo objeto **IUpdateNotify** quando a próxima chamada é feita.</span><span class="sxs-lookup"><span data-stu-id="b0b47-144">If no call is made within three minutes, the IUpdateNotify object will be unloaded and a new **IUpdateNotify** object will be created when the next call is made.</span></span> 
  
## <a name="click-to-run-installer-com-api-reference-guide"></a><span data-ttu-id="b0b47-145">Guia de referência de API COM instalador Click-to-Run</span><span class="sxs-lookup"><span data-stu-id="b0b47-145">Click-to-Run installer COM API reference guide</span></span>

<span data-ttu-id="b0b47-146">Na seguinte documentação de referência de API:</span><span class="sxs-lookup"><span data-stu-id="b0b47-146">In the following API reference documentation:</span></span>
  
- <span data-ttu-id="b0b47-147">Parâmetros estão em um formato de par de chave/valor separado por um espaço.</span><span class="sxs-lookup"><span data-stu-id="b0b47-147">Parameters are in a key/value pair format separated by a space.</span></span>
    
- <span data-ttu-id="b0b47-148">Os parâmetros não diferenciam maiusculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b0b47-148">The parameters are not case-sensitive.</span></span>
    
- <span data-ttu-id="b0b47-149">Há uma [lista de parâmetros](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) com a documentação disponível.</span><span class="sxs-lookup"><span data-stu-id="b0b47-149">There is a [list of parameters](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) with documentation available.</span></span> 
    
- <span data-ttu-id="b0b47-150">Resumo das IUpdateNotify2 interface agora é incluído.</span><span class="sxs-lookup"><span data-stu-id="b0b47-150">Summary of IUpdateNotify2 interface is now included.</span></span>
    
### <a name="apply"></a><span data-ttu-id="b0b47-151">Aplicar</span><span class="sxs-lookup"><span data-stu-id="b0b47-151">Apply</span></span>

```cpp
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
```

#### <a name="parameters"></a><span data-ttu-id="b0b47-152">Par�metros</span><span class="sxs-lookup"><span data-stu-id="b0b47-152">Parameters</span></span>

-  <span data-ttu-id="b0b47-153">_displaylevel_: **true** para mostrar o status de instalação, incluindo erros, durante o processo de atualização; **false** para ocultar o status de instalação, incluindo erros, durante o processo de atualização.</span><span class="sxs-lookup"><span data-stu-id="b0b47-153">_displaylevel_: **true** to show the installation status, including errors, during the update process; **false** to hide the installation status, including errors, during the update process.</span></span> <span data-ttu-id="b0b47-154">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="b0b47-154">The default is **false**.</span></span>
    
-  <span data-ttu-id="b0b47-155">_forceappshutdown_: **true** para forçar os aplicativos do Office para serem desligados imediatamente quando a ação de **Aplicar** for disparada; **false** falhe se quaisquer aplicativos do Office estão sendo executados.</span><span class="sxs-lookup"><span data-stu-id="b0b47-155">_forceappshutdown_: **true** to force Office applications to shut down immediately when the **Apply** action is triggered; **false** to fail if any Office applications are running.</span></span> <span data-ttu-id="b0b47-156">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="b0b47-156">The default is **false**.</span></span> <span data-ttu-id="b0b47-157">Consulte [comentários](#bk_ApplyRemark) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="b0b47-157">See [Remarks](#bk_ApplyRemark) for more information.</span></span> 
    
  <span data-ttu-id="b0b47-158">Se qualquer aplicativo do Office estiver em execução quando a ação de **Aplicar** é acionada, a ação de **Aplicar** geralmente falhará.</span><span class="sxs-lookup"><span data-stu-id="b0b47-158">If any Office application is running when the **Apply** action is triggered, the **Apply** action will usually fail.</span></span> <span data-ttu-id="b0b47-159">Passando `forceappshutdown=true` para **Aplicar** o método causará o serviço **OfficeClickToRun** imediatamente desligar os aplicativos e aplicar a atualização.</span><span class="sxs-lookup"><span data-stu-id="b0b47-159">Passing  `forceappshutdown=true` to the **Apply** method will cause the **OfficeClickToRun** service to immediately shut down the applications and apply the update.</span></span> <span data-ttu-id="b0b47-160">Nesse caso, o usuário pode enfrentar perda de dados.</span><span class="sxs-lookup"><span data-stu-id="b0b47-160">The user may experience data loss in this case.</span></span> 
    
#### <a name="return-results"></a><span data-ttu-id="b0b47-161">Retornar resultados</span><span class="sxs-lookup"><span data-stu-id="b0b47-161">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b0b47-162">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="b0b47-162">**S_OK**</span></span> <br/> |<span data-ttu-id="b0b47-163">Ação foi enviada com êxito para o serviço de Click-To-Run para execução.</span><span class="sxs-lookup"><span data-stu-id="b0b47-163">Action was successfully submitted to the Click-To-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="b0b47-164">**E_ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="b0b47-164">**E_ACCESSDENIED**</span></span> <br/> |<span data-ttu-id="b0b47-165">O chamador não está sendo executado com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="b0b47-165">The caller is not running with elevated privileges.</span></span>  <br/> |
|<span data-ttu-id="b0b47-166">**E_INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="b0b47-166">**E_INVALIDARG**</span></span> <br/> |<span data-ttu-id="b0b47-167">Parâmetros inválidos foram passados.</span><span class="sxs-lookup"><span data-stu-id="b0b47-167">Invalid parameters were passed.</span></span>  <br/> |
|<span data-ttu-id="b0b47-168">**E_ILLEGAL_METHOD_CALL**</span><span class="sxs-lookup"><span data-stu-id="b0b47-168">**E_ILLEGAL_METHOD_CALL**</span></span> <br/> |<span data-ttu-id="b0b47-169">Ação não é permitida neste momento.</span><span class="sxs-lookup"><span data-stu-id="b0b47-169">Action is not allowed at this time.</span></span> <span data-ttu-id="b0b47-170">Consulte [comentários](#bk_ApplyRemark) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="b0b47-170">See [Remarks](#bk_ApplyRemark) for more information.</span></span>  <br/> |

<a name="bk_ApplyRemark"></a>

#### <a name="remarks"></a><span data-ttu-id="b0b47-171">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="b0b47-171">Remarks</span></span>

- <span data-ttu-id="b0b47-172">Se qualquer aplicativo do Office estiver em execução quando a ação de **Aplicar** é acionada, a ação de **Aplicar** falhará.</span><span class="sxs-lookup"><span data-stu-id="b0b47-172">If any Office application is running when the **Apply** action is triggered, the **Apply** action will fail.</span></span> <span data-ttu-id="b0b47-173">Passando `forceappshutdown=true` para **Aplicar** o método causará o serviço **OfficeClickToRun** para serem desligados imediatamente quaisquer aplicativos do Office que estão funcionando e aplicam a atualização.</span><span class="sxs-lookup"><span data-stu-id="b0b47-173">Passing  `forceappshutdown=true` to the **Apply** method will cause the **OfficeClickToRun** service to immediately shut down any Office applications that are running and apply the update.</span></span> <span data-ttu-id="b0b47-174">O usuário perceba dados conforme eles não serão solicitados a salvar as alterações para abrir documentos do..</span><span class="sxs-lookup"><span data-stu-id="b0b47-174">The user may experience data as they are not prompted to save changes to open documents..</span></span> 
    
- <span data-ttu-id="b0b47-175">Essa ação só pode ser acionada quando o status de COM é um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="b0b47-175">This action can only be triggered when the COM status is one of the following:</span></span> 
    
  - <span data-ttu-id="b0b47-176">**eUPDATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="b0b47-176">**eUPDATE_UNKNOWN**</span></span>
    
  - <span data-ttu-id="b0b47-177">**eDOWNLOAD_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="b0b47-177">**eDOWNLOAD_CANCELLED**</span></span>
    
  - <span data-ttu-id="b0b47-178">**eDOWNLOAD_FAILED**</span><span class="sxs-lookup"><span data-stu-id="b0b47-178">**eDOWNLOAD_FAILED**</span></span>
    
  - <span data-ttu-id="b0b47-179">**eDOWNLOAD_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="b0b47-179">**eDOWNLOAD_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="b0b47-180">**eAPPLY_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="b0b47-180">**eAPPLY_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="b0b47-181">**eAPPLY_FAILED**</span><span class="sxs-lookup"><span data-stu-id="b0b47-181">**eAPPLY_FAILED**</span></span>
    
- <span data-ttu-id="b0b47-182">Se você chamar o método **Apply** sem fazer o download de conteúdo anteriormente, o método **Apply** informará **Succeeded** como ela detectada nada a aplicar e o processo de **Aplicar** for concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="b0b47-182">If you call the **Apply** method without previously downloading content, the **Apply** method will report **Succeeded** as it detected nothing to apply and completed the **Apply** process successfully.</span></span> 
    
### <a name="cancel"></a><span data-ttu-id="b0b47-183">Cancelar</span><span class="sxs-lookup"><span data-stu-id="b0b47-183">Cancel</span></span>

```cpp
HRESULT Cancel() // Cancel the download action.
```

#### <a name="return-results"></a><span data-ttu-id="b0b47-184">Retornar resultados</span><span class="sxs-lookup"><span data-stu-id="b0b47-184">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b0b47-185">S_OK</span><span class="sxs-lookup"><span data-stu-id="b0b47-185">S_OK</span></span>  <br/> |<span data-ttu-id="b0b47-186">Ação foi enviada com êxito para o serviço de Click-to-Run para execução.</span><span class="sxs-lookup"><span data-stu-id="b0b47-186">Action was successfully submitted to the Click-to-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="b0b47-187">E_ILLEGAL_METHOD_CALL</span><span class="sxs-lookup"><span data-stu-id="b0b47-187">E_ILLEGAL_METHOD_CALL</span></span>  <br/> |<span data-ttu-id="b0b47-188">Ação não é permitida neste momento.</span><span class="sxs-lookup"><span data-stu-id="b0b47-188">Action is not allowed at this time.</span></span> <span data-ttu-id="b0b47-189">Consulte a seção [comentários](#bk_CancelRemarks) para obter mais informações</span><span class="sxs-lookup"><span data-stu-id="b0b47-189">See the [Remarks](#bk_CancelRemarks) section for more information</span></span>  <br/> |

<a name="bk_CancelRemarks"></a>

#### <a name="remarks"></a><span data-ttu-id="b0b47-190">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="b0b47-190">Remarks</span></span>

- <span data-ttu-id="b0b47-191">Este método só pode ser acionado quando o de id de status COM **eDOWNLOAD_WIP**.</span><span class="sxs-lookup"><span data-stu-id="b0b47-191">This method can only be triggered when the COM status id **eDOWNLOAD_WIP**.</span></span> <span data-ttu-id="b0b47-192">Ele tentará cancelar a ação de download atual.</span><span class="sxs-lookup"><span data-stu-id="b0b47-192">It will attempt to cancel the current download action.</span></span> <span data-ttu-id="b0b47-193">O status de COM será altere para **eDOWNLOAD_CANCELLING** e eventualmente para **eDOWNLOAD_CANCELED**.</span><span class="sxs-lookup"><span data-stu-id="b0b47-193">The COM status will change to **eDOWNLOAD_CANCELLING** and eventually change to **eDOWNLOAD_CANCELED**.</span></span> <span data-ttu-id="b0b47-194">O status COM retornará **E_ILLEGAL_METHOD_CALL** se disparado em qualquer outro momento.</span><span class="sxs-lookup"><span data-stu-id="b0b47-194">The COM status will return **E_ILLEGAL_METHOD_CALL** if triggered at any other time.</span></span> 
    
### <a name="download"></a><span data-ttu-id="b0b47-195">Baixar</span><span class="sxs-lookup"><span data-stu-id="b0b47-195">Download</span></span>

```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
```

#### <a name="parameters"></a><span data-ttu-id="b0b47-196">Par�metros</span><span class="sxs-lookup"><span data-stu-id="b0b47-196">Parameters</span></span>

-  <span data-ttu-id="b0b47-197">_displaylevel_: **true** para mostrar o status de instalação, incluindo erros, durante o processo de atualização; **false** para ocultar o status de instalação, incluindo erros, durante o processo de atualização.</span><span class="sxs-lookup"><span data-stu-id="b0b47-197">_displaylevel_: **true** to show the installation status, including errors, during the update process; **false** to hide the installation status, including errors, during the update process.</span></span> <span data-ttu-id="b0b47-198">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="b0b47-198">The default is **false**.</span></span>
    
-  <span data-ttu-id="b0b47-199">_updatebaseurl_: URL para a fonte de download alternativo.</span><span class="sxs-lookup"><span data-stu-id="b0b47-199">_updatebaseurl_: URL to the alternate download source.</span></span>
    
-  <span data-ttu-id="b0b47-200">_updatetoversion_: A versão para atualizar o Office.</span><span class="sxs-lookup"><span data-stu-id="b0b47-200">_updatetoversion_: The version to update Office to.</span></span> <span data-ttu-id="b0b47-201">Defina esse parâmetro se você deseja atualizar para uma versão mais antiga do que a versão está instalada no momento.</span><span class="sxs-lookup"><span data-stu-id="b0b47-201">Define this parameter if you want to update to an older version than the version that is currently installed.</span></span>
    
-  <span data-ttu-id="b0b47-202">_downloadsource_: CLSID da implementação **IBackgroundCopyManager** personalizada (Gerenciador de BITS).</span><span class="sxs-lookup"><span data-stu-id="b0b47-202">_downloadsource_: CLSID of the customized **IBackgroundCopyManager** implementation (BITS manager).</span></span> 
    
-  <span data-ttu-id="b0b47-203">_contentid_: identifica o conteúdo para download do servidor de conteúdo por meio do Gerenciador de BITS personalizado.</span><span class="sxs-lookup"><span data-stu-id="b0b47-203">_contentid_: Identifies the content to download from the content server through the customized BITS manager.</span></span> <span data-ttu-id="b0b47-204">Esse valor é passado por meio da interface de BITS para interpretação.</span><span class="sxs-lookup"><span data-stu-id="b0b47-204">This value is passed through the BITS interface for interpretation.</span></span>
    
#### <a name="return-results"></a><span data-ttu-id="b0b47-205">Retornar resultados</span><span class="sxs-lookup"><span data-stu-id="b0b47-205">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b0b47-206">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="b0b47-206">**S_OK**</span></span> <br/> |<span data-ttu-id="b0b47-207">Ação foi enviada com êxito para o serviço de Click-To-Run para execução.</span><span class="sxs-lookup"><span data-stu-id="b0b47-207">Action was successfully submitted to the Click-To-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="b0b47-208">**E_ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="b0b47-208">**E_ACCESSDENIED**</span></span> <br/> |<span data-ttu-id="b0b47-209">O chamador não está sendo executado com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="b0b47-209">The caller is not running with elevated privileges.</span></span>  <br/> |
|<span data-ttu-id="b0b47-210">**E_INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="b0b47-210">**E_INVALIDARG**</span></span> <br/> |<span data-ttu-id="b0b47-211">Parâmetros inválidos foram passados.</span><span class="sxs-lookup"><span data-stu-id="b0b47-211">Invalid parameters were passed.</span></span>  <br/> |
|<span data-ttu-id="b0b47-212">**E_ILLEGAL_METHOD_CALL**</span><span class="sxs-lookup"><span data-stu-id="b0b47-212">**E_ILLEGAL_METHOD_CALL**</span></span> <br/> |<span data-ttu-id="b0b47-213">Ação não é permitida neste momento.</span><span class="sxs-lookup"><span data-stu-id="b0b47-213">Action is not allowed at this time.</span></span> <span data-ttu-id="b0b47-214">Consulte [comentários](#bk_DownloadRemark) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="b0b47-214">See [Remarks](#bk_DownloadRemark) for more information.</span></span>  <br/> |

<a name="bk_DownloadRemark"></a>

#### <a name="remarks"></a><span data-ttu-id="b0b47-215">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="b0b47-215">Remarks</span></span>

- <span data-ttu-id="b0b47-216">Você deve especificar _downloadsource_ e _contentid_ como um par.</span><span class="sxs-lookup"><span data-stu-id="b0b47-216">You must specify  _downloadsource_ and  _contentid_ as a pair.</span></span> <span data-ttu-id="b0b47-217">Caso contrário, o método **Baixar** retornará um erro **E_INVALIDARG** .</span><span class="sxs-lookup"><span data-stu-id="b0b47-217">If not, the **Download** method will return an **E_INVALIDARG** error.</span></span> 
    
- <span data-ttu-id="b0b47-218">Se forem fornecidos _downloadsource_, _contentid_e _updatebaseurl_ , _updatebaseurl_ será ignorado.</span><span class="sxs-lookup"><span data-stu-id="b0b47-218">If  _downloadsource_,  _contentid_, and  _updatebaseurl_ are provided,  _updatebaseurl_ will be ignored.</span></span> 
    
- <span data-ttu-id="b0b47-219">Essa ação só pode ser acionada quando o status de COM é um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="b0b47-219">This action can only be triggered when the COM status is one of the following:</span></span> 
    
  - <span data-ttu-id="b0b47-220">**eUPDATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="b0b47-220">**eUPDATE_UNKNOWN**</span></span>
    
  - <span data-ttu-id="b0b47-221">**eDOWNLOAD_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="b0b47-221">**eDOWNLOAD_CANCELLED**</span></span>
    
  - <span data-ttu-id="b0b47-222">**eDOWNLOAD_FAILED**</span><span class="sxs-lookup"><span data-stu-id="b0b47-222">**eDOWNLOAD_FAILED**</span></span>
    
  - <span data-ttu-id="b0b47-223">**eDOWNLOAD_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="b0b47-223">**eDOWNLOAD_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="b0b47-224">**eAPPLY_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="b0b47-224">**eAPPLY_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="b0b47-225">**eAPPLY_FAILED**</span><span class="sxs-lookup"><span data-stu-id="b0b47-225">**eAPPLY_FAILED**</span></span>
    
- <span data-ttu-id="b0b47-226">Se você chamar o método **Apply** sem conteúdo baixado anteriormente, o método **Apply** informará **Succeeded** como ela detectada nada a aplicar e o processo de **Aplicar** for concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="b0b47-226">If you call the **Apply** method without previously downloaded content, the **Apply** method will report **Succeeded** as it detected nothing to apply and completed the **Apply** process successfully.</span></span> 
    
#### <a name="examples"></a><span data-ttu-id="b0b47-227">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b0b47-227">Examples</span></span>

- <span data-ttu-id="b0b47-228">Para baixar o conteúdo do Gerenciador de BITS personalizado: chamar a função de **download ()** , passando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="b0b47-228">To download the content from the customized BITS manager: Call the **download()** function passing the following parameters:</span></span> 
    
  ```cpp
  "downloadsource=CLSIDofBITSInterface contentid=BITSServerContentIdentifier"
  ```

- <span data-ttu-id="b0b47-229">Para baixar o conteúdo da Microsoft CDN: chamar a função de **download ()** sem especificar os parâmetros _downloadsource_, _contentid_ou _updatebaseurl_ .</span><span class="sxs-lookup"><span data-stu-id="b0b47-229">To download the content from the Microsoft CDN: Call the **download()** function without specifying the  _downloadsource_,  _contentid_, or  _updatebaseurl_ parameters.</span></span> 
    
- <span data-ttu-id="b0b47-230">Para baixar o conteúdo de um local personalizado: chamar a função de **download ()** , passando o parâmetro a seguir:</span><span class="sxs-lookup"><span data-stu-id="b0b47-230">To download the content from a customized location: Call the **download()** function passing the following parameter:</span></span> 
    
  ```cpp
  "updatebaseurl=yourcontentserverurl"
  ```

### <a name="status"></a><span data-ttu-id="b0b47-231">Status</span><span class="sxs-lookup"><span data-stu-id="b0b47-231">Status</span></span>

```cpp
typdef struct _UPDATE_STATUS_REPORT
{
    UPDATE_STATUS status;
    UINT error;
    LPCWSTR contentid;
}UPDATE_STATUS_REPORT;
HRESULT status([out] _UPDATE_STATUS_REPORT& pUpdateStatusReport) // Get status of current action
```

#### <a name="parameters"></a><span data-ttu-id="b0b47-232">Par�metros</span><span class="sxs-lookup"><span data-stu-id="b0b47-232">Parameters</span></span>

|||
|:-----|:-----|
| <span data-ttu-id="b0b47-233">_pUpdateStatusReport_</span><span class="sxs-lookup"><span data-stu-id="b0b47-233">_pUpdateStatusReport_</span></span> <br/> |<span data-ttu-id="b0b47-234">Ponteiro para uma estrutura UPDATE_STATUS_REPORT.</span><span class="sxs-lookup"><span data-stu-id="b0b47-234">Pointer to an UPDATE_STATUS_REPORT structure.</span></span>  <br/> |
   
#### <a name="return-results"></a><span data-ttu-id="b0b47-235">Retornar resultados</span><span class="sxs-lookup"><span data-stu-id="b0b47-235">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b0b47-236">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="b0b47-236">**S_OK**</span></span> <br/> |<span data-ttu-id="b0b47-237">O método **Status** sempre retorna este resultado.</span><span class="sxs-lookup"><span data-stu-id="b0b47-237">The **Status** method always returns this result.</span></span> <span data-ttu-id="b0b47-238">Inspecione o `UPDATE_STATUS_RESULT` estrutura para o status da ação atual.</span><span class="sxs-lookup"><span data-stu-id="b0b47-238">Inspect the  `UPDATE_STATUS_RESULT` structure for the status of the current action.</span></span>  <br/> |
   
#### <a name="remarks"></a><span data-ttu-id="b0b47-239">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="b0b47-239">Remarks</span></span>

- <span data-ttu-id="b0b47-240">O campo status do `UPDATE_STATUS_REPORT` contém o status da ação atual.</span><span class="sxs-lookup"><span data-stu-id="b0b47-240">The status field of the  `UPDATE_STATUS_REPORT` contains the status of the current action.</span></span> <span data-ttu-id="b0b47-241">Um dos seguintes valores de status é retornado:</span><span class="sxs-lookup"><span data-stu-id="b0b47-241">One of the following status values is returned:</span></span> 
    
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

- <span data-ttu-id="b0b47-242">Se o último comando resultou em um erro, o campo de erro do `UPDATE_STATUS_REPORT` contém informações detalhadas sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="b0b47-242">If the last command resulted in an error, the error field of the  `UPDATE_STATUS_REPORT` contains detailed information about the error.</span></span> <span data-ttu-id="b0b47-243">Dois tipos de códigos de erro são retornados pelo método **Status** .</span><span class="sxs-lookup"><span data-stu-id="b0b47-243">Two types of error codes are returned from the **Status** method.</span></span> 
    
- <span data-ttu-id="b0b47-244">Se o erro menor que `UDPATE_ERROR_CODE::eUNKNOWN`, o erro é um dos seguintes códigos de erro predefinidas:</span><span class="sxs-lookup"><span data-stu-id="b0b47-244">If the error less than  `UDPATE_ERROR_CODE::eUNKNOWN`, the error is one of the following pre-defined error codes:</span></span>
    
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

  <span data-ttu-id="b0b47-245">Se o código de erro de retorno for maior que `UDPATE_ERROR_CODE::eUNKNOWN` é o **HRESULT** de uma chamada de função com falha.</span><span class="sxs-lookup"><span data-stu-id="b0b47-245">If the return error code is larger than  `UDPATE_ERROR_CODE::eUNKNOWN` it is the **HRESULT** of a failed function call.</span></span> <span data-ttu-id="b0b47-246">Para extrair o HRESULT subtrair `UDPATE_ERROR_CODE::eUNKNOWN` do valor retornado no campo de erro o `UPDATE_STATUS_REPORT`.</span><span class="sxs-lookup"><span data-stu-id="b0b47-246">To extract the HRESULT subtract  `UDPATE_ERROR_CODE::eUNKNOWN` from the value returned in the error field of the  `UPDATE_STATUS_REPORT`.</span></span>
    
  <span data-ttu-id="b0b47-247">A lista completa dos valores de status e de erro pode ser exibida por meio da biblioteca de tipos do **IUpdateNotify** incorporada OfficeC2RCom.dll inspeção.</span><span class="sxs-lookup"><span data-stu-id="b0b47-247">The complete list of status and error values can be viewed by inspecting the **IUpdateNotify** type library embedded in OfficeC2RCom.dll.</span></span> 
    
- <span data-ttu-id="b0b47-248">O campo contentid é usado nas chamadas ao **Status** depois que **Baixar** iniciou e retorna contentid que foi passado para a chamada de **Download** .</span><span class="sxs-lookup"><span data-stu-id="b0b47-248">The contentid field is used for calls to **Status** after **Download** has initiated and returns the contentid that was passed in to the **Download** call.</span></span> <span data-ttu-id="b0b47-249">É uma prática recomendada para inicializar este campo como **Nulo** antes de chamar o método de **Status** e verifique se o valor depois que o **Status** foi retornado.</span><span class="sxs-lookup"><span data-stu-id="b0b47-249">It is a best practice to initialize this field to **null** before you call the **Status** method and then check the value after **Status** has been returned.</span></span> <span data-ttu-id="b0b47-250">Se o valor ainda for **nula**, isso significa que não há nenhuma contentid para retornar.</span><span class="sxs-lookup"><span data-stu-id="b0b47-250">If the value is still **null**, that means there is no contentid to return.</span></span> <span data-ttu-id="b0b47-251">Se o valor não for **nula**, você precisará liberá-la com uma chamada para **SysFreeString()**.</span><span class="sxs-lookup"><span data-stu-id="b0b47-251">If the value is not **null**, you need to free it with a call to **SysFreeString()**.</span></span> <span data-ttu-id="b0b47-252">Aqui está um trecho de código de como chamar **Status** após **Baixar**.</span><span class="sxs-lookup"><span data-stu-id="b0b47-252">Here is a code snippet of how to call **Status** after **Download**.</span></span>
    
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

### <a name="summary-of-iupdatenotify2-interface"></a><span data-ttu-id="b0b47-253">Resumo da interface IUpdateNotify2</span><span class="sxs-lookup"><span data-stu-id="b0b47-253">Summary of IUpdateNotify2 interface</span></span>

> [!NOTE]
> <span data-ttu-id="b0b47-254">Esse resumo é fornecido como um info complemento aos [aplicativos de capacidade de gerenciamento de integração com o instalador de clique para executar do Office 365](https://msdn.microsoft.com/pt-br/library/office/mt608768.aspx).</span><span class="sxs-lookup"><span data-stu-id="b0b47-254">This summary is provided as a compliment info to [Integrating manageability applications with the Office 365 click-to-run installer](https://msdn.microsoft.com/pt-br/library/office/mt608768.aspx).</span></span> <span data-ttu-id="b0b47-255">Depois que o doc pública for atualizada, este doc pode ser considerado como obsoleta.</span><span class="sxs-lookup"><span data-stu-id="b0b47-255">Once the public doc is updated, this doc can be considered as obsolete.</span></span> 
  
<span data-ttu-id="b0b47-256">De C2RTenant [16.0.8208.6352](http://oloop/BuildGroup/Details/tenantc2rclient#3519/1255278) (primeira compilação publicamente disponível deve ser a compilação de bifurcação junho – 8326.\*) adicionamos uma nova interface **IUpdateNotify2** .</span><span class="sxs-lookup"><span data-stu-id="b0b47-256">From C2RTenant [16.0.8208.6352](http://oloop/BuildGroup/Details/tenantc2rclient#3519/1255278) (First publicly available build should be June fork build -- 8326.\*) we have added a new **IUpdateNotify2** interface.</span></span> <span data-ttu-id="b0b47-257">Eis algumas informações básicas sobre essa interface:</span><span class="sxs-lookup"><span data-stu-id="b0b47-257">Here is some basic info about this interface:</span></span> 
  
- <span data-ttu-id="b0b47-258">CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}</span><span class="sxs-lookup"><span data-stu-id="b0b47-258">CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}</span></span>
    
- <span data-ttu-id="b0b47-259">Essa interface também hospedado a interface IUpdateNotify original para fornecer compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="b0b47-259">This interface also hosted the original IUpdateNotify interface to provide backward compatibility.</span></span> <span data-ttu-id="b0b47-260">O que significa que se você usar essa interface, você tem acesso a todos os métodos fornecidas na interface **UpdateNotifyObject** .</span><span class="sxs-lookup"><span data-stu-id="b0b47-260">Which means if you use this interface, you have access to all the methods provided in **UpdateNotifyObject** interface.</span></span> 
    
- <span data-ttu-id="b0b47-261">Novos métodos são adicionados ao IUpdateNotify2:</span><span class="sxs-lookup"><span data-stu-id="b0b47-261">New methods added to IUpdateNotify2:</span></span>
    
  - <span data-ttu-id="b0b47-262">**HRESULT** GetBlockingApps (BSTR [out] \* AppsList).</span><span class="sxs-lookup"><span data-stu-id="b0b47-262">**HRESULT** GetBlockingApps([out] BSTR \* AppsList).</span></span> <span data-ttu-id="b0b47-263">Obtenha atualizações bloqueando a lista de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="b0b47-263">Get updates blocking apps list.</span></span> <span data-ttu-id="b0b47-264">Essa chamada retornará executando aplicativos do Office que bloqueiam o processo de atualização de prosseguir.</span><span class="sxs-lookup"><span data-stu-id="b0b47-264">This call will return running Office apps which will block the update process from proceeding.</span></span> 
    
  - <span data-ttu-id="b0b47-265">**HRESULT** GetOfficeDeploymentData (dataType int, pcwszName **LPCWSTR** , BSTR [out] [in] [in] \* OfficeData).</span><span class="sxs-lookup"><span data-stu-id="b0b47-265">**HRESULT** GetOfficeDeploymentData([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR \* OfficeData).</span></span> <span data-ttu-id="b0b47-266">Obtenha os dados de implantação do Office.</span><span class="sxs-lookup"><span data-stu-id="b0b47-266">Get Office deployment Data.</span></span> 
    
- <span data-ttu-id="b0b47-267">Se desejar usar os métodos de novos, você precisa certificar-se:</span><span class="sxs-lookup"><span data-stu-id="b0b47-267">If you want to use the new methods, you need to make sure:</span></span>
    
  - <span data-ttu-id="b0b47-268">Sua versão C2R é mais recente que a compilação acima (\>= compilação de bifurcação de junho).</span><span class="sxs-lookup"><span data-stu-id="b0b47-268">Your C2R version is newer than the above build (\>= June fork build).</span></span>
    
  - <span data-ttu-id="b0b47-269">Use UpdateNotifyObject2, em vez de **UpdateNotifyObject** para chamar **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="b0b47-269">Use UpdateNotifyObject2, instead of **UpdateNotifyObject** to call **CoCreateInstance**.</span></span>
    
<span data-ttu-id="b0b47-270">Se você não usar qualquer um dos métodos novos, você não precisará alterar nada.</span><span class="sxs-lookup"><span data-stu-id="b0b47-270">If you don't use any of the new methods, you don't need to change anything.</span></span> <span data-ttu-id="b0b47-271">Todos os métodos existentes funcionará como exato da mesma maneira que antes.</span><span class="sxs-lookup"><span data-stu-id="b0b47-271">All the existing methods will work as exact the same way as before.</span></span>
  
## <a name="implementing-the-bits-interface"></a><span data-ttu-id="b0b47-272">Implementando a interface de BITS</span><span class="sxs-lookup"><span data-stu-id="b0b47-272">Implementing the BITS interface</span></span>

<span data-ttu-id="b0b47-273">O [Serviço de transferência inteligente de plano de fundo](https://msdn.microsoft.com/pt-br/library/bb968799(v=vs.85).aspx) (BITS) é um serviço oferecido pela Microsoft para transferir arquivos entre um cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="b0b47-273">The [Background Intelligent Transfer Service](https://msdn.microsoft.com/pt-br/library/bb968799(v=vs.85).aspx) (BITS) is a service provided by Microsoft to transfer files between a client and server.</span></span> <span data-ttu-id="b0b47-274">BITS é um dos canais que instalador Click-To-Run do Office pode usar para baixar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="b0b47-274">BITS is one of the channels that Office Click-To-Run installer can use to download content.</span></span> <span data-ttu-id="b0b47-275">Por padrão, o Office Click-To-Run instalador usa as janelas criada na implementação de BITS para baixar o conteúdo da CDN.</span><span class="sxs-lookup"><span data-stu-id="b0b47-275">By default, the Office Click-To-Run installer uses the Windows' built in implementation of BITS to download the content from the CDN.</span></span> 
  
<span data-ttu-id="b0b47-276">Fornecendo uma implementação personalizada de BITS para o método **download ()** da interface **IUpdateNotify** , seu software gerenciabilidade pode controlar onde e como o cliente baixa o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="b0b47-276">By providing a customized BITS implementation to the **download()** method of the **IUpdateNotify** interface, your manageability software can control where and how the client downloads the content.</span></span> <span data-ttu-id="b0b47-277">Uma interface de BITS personalizada é útil quando fornecendo um canal de distribuição de conteúdo personalizados que não seja os canais internos Click-to-Run, como a CDN do Office, servidores do IIS, ou compartilhamentos de arquivos.</span><span class="sxs-lookup"><span data-stu-id="b0b47-277">A customized BITS interface is useful when providing a custom content distribution channel other than the Click-to-Run built-in channels, such as the Office CDN, IIS servers, or file shares.</span></span> 
  
<span data-ttu-id="b0b47-278">O requisito mínimo para uma interface de BITS personalizada funcionar com o serviço Office C2R é:</span><span class="sxs-lookup"><span data-stu-id="b0b47-278">The minimum requirement for a customized BITS interface to work with Office C2R service is:</span></span>
  
- <span data-ttu-id="b0b47-279">Para **IBackgroundCopyManager**:</span><span class="sxs-lookup"><span data-stu-id="b0b47-279">For **IBackgroundCopyManager**:</span></span>
    
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

- <span data-ttu-id="b0b47-280">Para **IBackgroundCopyJob**:</span><span class="sxs-lookup"><span data-stu-id="b0b47-280">For **IBackgroundCopyJob**:</span></span>
    
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

- <span data-ttu-id="b0b47-281">Para **IBackgroundCopyJob3**:</span><span class="sxs-lookup"><span data-stu-id="b0b47-281">For **IBackgroundCopyJob3**:</span></span>
    
  ```cpp
  HRESULT _stdcall AddFileWithRanges(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName,
                      [in] DWORD RangeCount,
                      [in] BG_FILE_RANGE Ranges[])
  
  ```

- <span data-ttu-id="b0b47-282">Para o `Addfile` e `AddFileWithRanges` funções, a URL remota está no seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="b0b47-282">For the  `Addfile` and  `AddFileWithRanges` functions, the remote URL is in the following format:</span></span> 
    
  ```cpp
  cmbits://<contentid>/<relative path to target file>
  ```

  - <span data-ttu-id="b0b47-283">cmbits é codificada e significa BITS personalizadas.</span><span class="sxs-lookup"><span data-stu-id="b0b47-283">cmbits is hard coded, and stands for customized BITS.</span></span>
    
  -  <span data-ttu-id="b0b47-284">_ \<contentid\> _ é o parâmetro _contentid_ o método **download ()** .</span><span class="sxs-lookup"><span data-stu-id="b0b47-284">_\<contentid\>_ is the  _contentid_ parameter for the **Download()** method.</span></span> 
    
  -  <span data-ttu-id="b0b47-285">_ \<caminho relativo para o arquivo de destino\> _ fornece o local e o nome do arquivo para baixar.</span><span class="sxs-lookup"><span data-stu-id="b0b47-285">_\<relative path to target file\>_ provides the location and file name of the file to download.</span></span> 
    
    <span data-ttu-id="b0b47-286">Por exemplo, se você tiver fornecido um _contentid_ de `f732af58-5d86-4299-abe9-7595c35136ef` para o **download ()** quiser baixar o arquivo cab de versão, tais como método e Office C2R `v32.cab` arquivo, ele chamará **AddFile()** com as seguintes `RemoteUrl`:</span><span class="sxs-lookup"><span data-stu-id="b0b47-286">For example, if you have provided a  _contentid_ of  `f732af58-5d86-4299-abe9-7595c35136ef` to the **Download()** method, and Office C2R wants to download the version cab file, such as  `v32.cab` file, it will call **AddFile()** with the following  `RemoteUrl`:</span></span>
    
  ```cpp
  cmbits://f732af58-5d86-4299-abe9-7595c35136ef/Office/Data/V32.cab
  ```

- <span data-ttu-id="b0b47-287">Para **IBackgroundCopyError**:</span><span class="sxs-lookup"><span data-stu-id="b0b47-287">For **IBackgroundCopyError**:</span></span>
    
  ```cpp
  HRESULT _stdcall GetErrorDescription(
        [in]  DWORD  LanguageId,
        [out] LPWSTR *ppErrorDescription);
  
  ```

- <span data-ttu-id="b0b47-288">Para **IBackgroundCopyFile**:</span><span class="sxs-lookup"><span data-stu-id="b0b47-288">For **IBackgroundCopyFile**:</span></span>
    
  ```cpp
  HRESULT _stdcall GetLocalName([out] LPWSTR *ppName); 
  HRESULT _stdcall GetRemoteName([out] LPWSTR *ppName);
  
  ```

<!--## Automating content staging

IT administrators can choose to have desktop clients enabled to automatically receive updates when they are available directly from the Microsoft Content Delivery Network (CDN) or they can choose to control the deployment of updates available from the [update channels](https://support.office.com/pt-br/article/Overview-of-update-channels-for-Office-365-ProPlus-9ccf0f13-28ff-4975-9bd2-7e4ea2fefef4?ui=en-US&rs=en-US&ad=US) using the [Office 2016 Deployment Tool](https://www.microsoft.com/en-us/download/details.aspx?id=49117) or [System Center Configuration Manager](https://support.office.com/pt-br/article/Manage-updates-to-Office-365-ProPlus-with-System-Center-Configuration-Manager-b4a17328-fcfe-40bf-9202-58d7cbf1cede).
  
The service supports the ability for management tools to recognize and automate the download of the content when updates are made available.
  
**Following is a diagram showing the overview of downloading a custom image**

![An overview of downloading Office updates from the CDN.](media/9afac230-6b22-4526-a800-0562708cc436.png "An overview of downloading Office updates from the CDN")
  
In the above diagram you see that a new Office 365 ProPlus image is available on the Office Content Distribution Network (CDN). Along with the Office 365 ProPlus image, an XML-formatted file list is also available which has the information needed to enable manageability software to directly create customized images replacing the need for using the Office Deployment Tool.
  
An enterprise configures their WSUS to sync the Office 365 Client Updates. These updates do not contain the actual image payload but does allow the manageability software to recognize when new content is available. The manageability software can then read the Client Update metadata to understand what version of Office the update applies to.
  
If the update is applicable, the manageability software can use the CDN content and the file list to create the custom image and store it onto the file share location that it is configured to use.
  
### Format of the XML file list

There are two file lists available in a cab file on the CDN. One lists the files for the 32-bit version of Office and one for the 64-bit version of Office. The URL of the location of the Office File List (OFL.CAB) file is [http://officecdn.microsoft.com/pr/wsus/ofl.cab](http://officecdn.microsoft.com/pr/wsus/ofl.cab). The two file lists are called:
  
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
baseURL branch="Monthly" URL="http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60" /
```

- The following is a language neutral file needed for all languages. The name of the file is v64_16.0.4229.1004.cab and it should be copied from http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/v64_16.0.4229.1004.cab and renamed to …/office/data/v64.cab.
    
  ```cpp
  baseURL branch="Business" URL="http://officecdn.microsoft.com/pr/7ffbc6bf-bc32-4f92-8982-f9dd17fd3114" /
  File name="v64_%version%.cab" rename="v64.cab" relativePath="/office/data/" language="0"/
  
  ```

- The following is a file to be included in the en-US image as designated by the language LCID=1033. The name of the file is s641033.cab and it should be copied from http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641033.cab and not renamed.
    
  ```cpp
  File name="s641033.cab" relativePath="/office/data/%version%/" language="1033" /
  ```

### Hash verification of data files

Image creation tools may verify the integrity of the downloaded .dat files by comparing a computed HASH value with the supplied HASH value associated with each of the .dat files. Below is an example of a .dat file from the Monthly channel with build version 16.0.4229.1004 and language set to Bulgarian.
  
```cpp
File name="stream.x64.bg-bg.dat" hashLocation="s641026.cab/stream.x64.bg-bg.hash" hashAlgo="Sha256" relativePath="/office/data/%version%/" language="1026"
```

- The  _hashLocation_ attribute specifies the relative path location of the stream.x64.bg-bg.hash for the stream.x64.bg-bg.dat file. Construct the hash file location by concatenating URL + relativePath + hashLocation. In this example the stream.x64.bg-bg.hash location would be http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
    
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
http://officecdn.microsoft.com/pr/wsus/ofl.cab is the location of the XML file lists for this update, specifically the O365Client_32bit.xml from within the OFL.CAB.
http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.8326.2096&Branch=Current&Arch=64&XMLVer=1.4&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml 

```
THE ABOVE SECTION APPEARS TO BE A DUPLICATE OF THE FOLLOWING SECTION; TEMPORARILY COMMENTING IT OUT.-->

## <a name="automating-content-staging"></a><span data-ttu-id="b0b47-289">Automatizando o preparo de conteúdo</span><span class="sxs-lookup"><span data-stu-id="b0b47-289">Automating content staging</span></span>

<span data-ttu-id="b0b47-290">Os administradores de TI podem optar por ter habilitados para receber automaticamente atualizações quando eles estão disponíveis diretamente da Microsoft conteúdo entrega rede (CDN) ou eles podem escolher para controlar a implantação das atualizações disponíveis da atualização de clientes de desktop canais usando a ferramenta de implantação do Office ou o System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="b0b47-290">IT administrators can choose to have desktop clients enabled to automatically receive updates when they are available directly from the Microsoft Content Delivery Network (CDN) or they can choose to control the deployment of updates available from the update channels using the Office Deployment Tool or System Center Configuration Manager.</span></span>
  
<span data-ttu-id="b0b47-291">O serviço suporta a capacidade de ferramentas de gerenciamento reconhecer e automatizar o download do conteúdo quando atualizações são disponibilizadas.</span><span class="sxs-lookup"><span data-stu-id="b0b47-291">The service supports the ability for management tools to recognize and automate the download of the content when updates are made available.</span></span>
  
<span data-ttu-id="b0b47-292">**A imagem a seguir está uma visão geral de download de uma imagem personalizada**</span><span class="sxs-lookup"><span data-stu-id="b0b47-292">**The following image is an overview of downloading a custom image**</span></span>

<span data-ttu-id="b0b47-293">![Um diagrama de usar a interface COM no installer Office Click-To-Run.] (media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Um diagrama de usar a interface COM no installer Click-To-Run do Office")</span><span class="sxs-lookup"><span data-stu-id="b0b47-293">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "A diagram of using the COM interface on  the Office Click-To-Run installer")</span></span>
  
### <a name="overview-of-downloading-a-custom-image"></a><span data-ttu-id="b0b47-294">Visão geral de download de uma imagem personalizada</span><span class="sxs-lookup"><span data-stu-id="b0b47-294">Overview of downloading a custom image</span></span>
  
<span data-ttu-id="b0b47-295">No diagrama anterior, você vê que uma nova imagem do Office 365 ProPlus está disponível na rede de distribuição conteúdo do Office (CDN).</span><span class="sxs-lookup"><span data-stu-id="b0b47-295">In the previous diagram, you see that a new Office 365 ProPlus image is available on the Office Content Distribution Network (CDN).</span></span> <span data-ttu-id="b0b47-296">Junto com a imagem do Office 365 ProPlus, uma lista de arquivo no formato XML também está disponível que tem as informações necessárias para habilitar o software de capacidade de gerenciamento criar diretamente imagens personalizadas, substituindo a necessidade de usando a ferramenta de implantação do Office.</span><span class="sxs-lookup"><span data-stu-id="b0b47-296">Along with the Office 365 ProPlus image, an XML-formatted file list is also available which has the information needed to enable manageability software to directly create customized images replacing the need for using the Office Deployment Tool.</span></span>
  
<span data-ttu-id="b0b47-297">Uma empresa configura seu WSUS para sincronizar as atualizações do cliente do Office 365.</span><span class="sxs-lookup"><span data-stu-id="b0b47-297">An enterprise configures their WSUS to sync the Office 365 Client Updates.</span></span> <span data-ttu-id="b0b47-298">Essas atualizações não contêm a carga de imagem real, mas permitir que o software de gerenciabilidade reconhecer quando o conteúdo novo está disponível.</span><span class="sxs-lookup"><span data-stu-id="b0b47-298">These updates do not contain the actual image payload but does allow the manageability software to recognize when new content is available.</span></span> <span data-ttu-id="b0b47-299">O software de capacidade de gerenciamento, em seguida, pode ler os metadados de atualização do cliente para entender qual versão do Office que a atualização se aplica ao.</span><span class="sxs-lookup"><span data-stu-id="b0b47-299">The manageability software can then read the Client Update metadata to understand what version of Office the update applies to.</span></span>
  
<span data-ttu-id="b0b47-300">Se a atualização for aplicável, o software de capacidade de gerenciamento pode usar o conteúdo CDN e a lista de arquivos para criar a imagem personalizada e armazená-lo para o local de compartilhamento de arquivo que ele está configurado para usar.</span><span class="sxs-lookup"><span data-stu-id="b0b47-300">If the update is applicable, the manageability software can use the CDN content and the file list to create the custom image and store it onto the file share location that it is configured to use.</span></span>
  
### <a name="format-of-the-xml-file-list"></a><span data-ttu-id="b0b47-301">Formato da lista de arquivo XML</span><span class="sxs-lookup"><span data-stu-id="b0b47-301">Format of the XML file list</span></span>

<span data-ttu-id="b0b47-302">Há duas listas de arquivos disponíveis em um arquivo cab na CDN.</span><span class="sxs-lookup"><span data-stu-id="b0b47-302">There are two file lists available in a cab file on the CDN.</span></span> <span data-ttu-id="b0b47-303">Uma lista os arquivos para a versão de 32 bits do Office e outro para a versão de 64 bits do Office.</span><span class="sxs-lookup"><span data-stu-id="b0b47-303">One lists the files for the 32-bit version of Office and one for the 64-bit version of Office.</span></span> <span data-ttu-id="b0b47-304">A URL do local da lista de arquivos Office (OFL. Arquivo CAB) é [http://officecdn.microsoft.com/pr/wsus/ofl.cab](http://officecdn.microsoft.com/pr/wsus/ofl.cab).</span><span class="sxs-lookup"><span data-stu-id="b0b47-304">The URL of the location of the Office File List (OFL.CAB) file is [http://officecdn.microsoft.com/pr/wsus/ofl.cab](http://officecdn.microsoft.com/pr/wsus/ofl.cab).</span></span> <span data-ttu-id="b0b47-305">As listas de dois arquivos são chamadas:</span><span class="sxs-lookup"><span data-stu-id="b0b47-305">The two file lists are called:</span></span>
  
- <span data-ttu-id="b0b47-306">O365Client_32bit.XML</span><span class="sxs-lookup"><span data-stu-id="b0b47-306">O365Client_32bit.xml</span></span>
    
- <span data-ttu-id="b0b47-307">O365Client_64bit.XML</span><span class="sxs-lookup"><span data-stu-id="b0b47-307">O365Client_64bit.xml</span></span>
    
<span data-ttu-id="b0b47-308">Dentro do XML para cada do arquivo listas é um <UpdateFiles> nó que contém um atributo version.</span><span class="sxs-lookup"><span data-stu-id="b0b47-308">Within the XML for each of the file lists is an <UpdateFiles> node which contains a version attribute.</span></span>  <span data-ttu-id="b0b47-309">`<UpdateFiles version="1.4">`.</span><span class="sxs-lookup"><span data-stu-id="b0b47-309"></span></span> <span data-ttu-id="b0b47-310">Esta versão é incrementada se alterações forem feitas para as listas de arquivos.</span><span class="sxs-lookup"><span data-stu-id="b0b47-310">This version is incremented if changes are made to the file lists.</span></span>
  
<span data-ttu-id="b0b47-311">Há dois parâmetros que precisam ser combinado com o XML para tornar uma imagem personalizada:</span><span class="sxs-lookup"><span data-stu-id="b0b47-311">There are two parameters that need to be combined with the XML to make a custom image:</span></span> 
  
- <span data-ttu-id="b0b47-312">Substitua *% % de versão* a versão de compilação do Office.</span><span class="sxs-lookup"><span data-stu-id="b0b47-312">Replace  *%version%*  with the build version of Office.</span></span> <span data-ttu-id="b0b47-313">Isso pode ser derivado dos metadados de atualização do cliente (explicado na próxima seção).</span><span class="sxs-lookup"><span data-stu-id="b0b47-313">This can be derived from the Client Update metadata (explained in the next section).</span></span> 
    
- <span data-ttu-id="b0b47-314">Defina *baseURL* usando-se o valor da URL associado a ramificação que a imagem está sendo criada para.</span><span class="sxs-lookup"><span data-stu-id="b0b47-314">Define  *baseURL*  by using the URL value associated with the branch the image is being created for.</span></span> <span data-ttu-id="b0b47-315">Isso é derivado dos metadados de atualização do cliente, explicado na seção a seguir.</span><span class="sxs-lookup"><span data-stu-id="b0b47-315">This is derived from the Client Update metadata, explained in the following section.</span></span> 
    
<span data-ttu-id="b0b47-316">As etapas para a criação de uma imagem são:</span><span class="sxs-lookup"><span data-stu-id="b0b47-316">The steps for creating an image are:</span></span>
  
1. <span data-ttu-id="b0b47-317">Abra a lista de arquivo XML.</span><span class="sxs-lookup"><span data-stu-id="b0b47-317">Open the XML file list.</span></span>
    
2. <span data-ttu-id="b0b47-318">Substitua ocorrências de *% versão %* com a versão de compilação do Office aplicável.</span><span class="sxs-lookup"><span data-stu-id="b0b47-318">Replace occurrences of  *%version%*  with the applicable Office build version.</span></span> <span data-ttu-id="b0b47-319">A versão de compilação pode ser adquirida no releasehistory.xml, conforme descrito neste artigo.</span><span class="sxs-lookup"><span data-stu-id="b0b47-319">The build version can be acquired from releasehistory.xml as described later in this article.</span></span> 
    
3. <span data-ttu-id="b0b47-320">Leia o atributo de URL para a ramificação de destino.</span><span class="sxs-lookup"><span data-stu-id="b0b47-320">Read the URL attribute for the target branch.</span></span>
    
4. <span data-ttu-id="b0b47-321">Remova nós de idioma para qualquer idiomas não obrigatório a imagem personalizada.</span><span class="sxs-lookup"><span data-stu-id="b0b47-321">Remove language nodes for any languages not required in the custom image.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="b0b47-322">Nós com idioma = '0' são de idioma neutro e deve ser incluído na imagem.</span><span class="sxs-lookup"><span data-stu-id="b0b47-322">Nodes with language='0' are language neutral and must be included in the image.</span></span> 
  
5. <span data-ttu-id="b0b47-323">Construa uma imagem de local da CDN iteração entre a lista de arquivos XML e copiando os arquivos CDN, ao criar a estrutura de pasta, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="b0b47-323">Construct a local image of the CDN by iterating through the XML file list and copying the CDN files, while creating the folder structure as needed.</span></span> 
    
   - <span data-ttu-id="b0b47-324">Se o atributo *Renomear* for fornecido, em seguida, o arquivo copiado para o valor *Renomear* fornecidos no atributo renomear.</span><span class="sxs-lookup"><span data-stu-id="b0b47-324">If the  *rename*  attribute is provided, then  *rename*  the copied file to the value provided in the rename attribute.</span></span> <span data-ttu-id="b0b47-325">Isso é usado para criar o padrão de nível superior arquivos v64.cab e v32.cab.</span><span class="sxs-lookup"><span data-stu-id="b0b47-325">This is used to create the top-level default v64.cab and v32.cab files.</span></span> <span data-ttu-id="b0b47-326">Estas são as versões renomeadas do arquivo cab de compilação de nível superior e são usadas como a versão de instalação padrão, se a versão não for especificada.</span><span class="sxs-lookup"><span data-stu-id="b0b47-326">These are the renamed versions of the top-level build cab file and are used as the default installation version if the version is not specified.</span></span> 
    
   - <span data-ttu-id="b0b47-327">Use URL + relativePath + filename para construir o local CDN.</span><span class="sxs-lookup"><span data-stu-id="b0b47-327">Use URL + relativePath + filename to construct the CDN location.</span></span>
    
<span data-ttu-id="b0b47-328">A seguir estão exemplos que usam o canal mensal (conforme definido pelo `<baseURL>` nó) e versão 16.0.4229.1004 do releasehistory.xml de compilação.</span><span class="sxs-lookup"><span data-stu-id="b0b47-328">The following are examples that use the Monthly channel (as defined by the  `<baseURL>` node) and build version 16.0.4229.1004 from releasehistory.xml.</span></span> 
  
```xml
<baseURL branch="Monthly" URL="http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60" />
```

- <span data-ttu-id="b0b47-329">A seguir está um arquivo de idioma neutro necessário para todos os idiomas.</span><span class="sxs-lookup"><span data-stu-id="b0b47-329">The following is a language neutral file needed for all languages.</span></span> <span data-ttu-id="b0b47-330">O nome do arquivo é v64_16.0.4229.1004.cab e ele deve ser copiado de `http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/v64_16.0.4229.1004.cab` e renomeado para `…/office/data/v64.cab`.</span><span class="sxs-lookup"><span data-stu-id="b0b47-330">The name of the file is v64_16.0.4229.1004.cab and it should be copied from `http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/v64_16.0.4229.1004.cab` and renamed to `…/office/data/v64.cab`.</span></span> 
    
  ```xml
  <File name="v64_%version%.cab" rename="v64.cab" relativePath="/office/data/" language="0"/>
  
  ```

- <span data-ttu-id="b0b47-331">A seguir é um arquivo a ser incluído na imagem en-US designado pelo LCID do idioma = 1033.</span><span class="sxs-lookup"><span data-stu-id="b0b47-331">The following is a file to be included in the en-US image as designated by the language LCID=1033.</span></span> <span data-ttu-id="b0b47-332">O nome do arquivo é s641033.cab e ele deve ser copiado de `http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641033.cab` e não foi renomeado.</span><span class="sxs-lookup"><span data-stu-id="b0b47-332">The name of the file is s641033.cab and it should be copied from `http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641033.cab` and not renamed.</span></span>
    
  ```xml
  <File name="s641033.cab" relativePath="/office/data/%version%/" language="1033" />
  ```

### <a name="hash-verification-of-dat-files"></a><span data-ttu-id="b0b47-333">Verificação de hash dos arquivos. dat</span><span class="sxs-lookup"><span data-stu-id="b0b47-333">Hash verification of .dat files</span></span>

<span data-ttu-id="b0b47-334">Ferramentas de criação de imagem podem verificar a integridade dos arquivos. dat baixado comparando um valor HASH calculado com o valor HASH fornecido associado a cada um dos arquivos. dat.</span><span class="sxs-lookup"><span data-stu-id="b0b47-334">Image creation tools may verify the integrity of the downloaded .dat files by comparing a computed HASH value with the supplied HASH value associated with each of the .dat files.</span></span> <span data-ttu-id="b0b47-335">A seguir está um exemplo de um arquivo. dat do canal mensal com a versão de compilação 16.0.4229.1004 e idioma definido como búlgaro:</span><span class="sxs-lookup"><span data-stu-id="b0b47-335">Following is an example of a .dat file from the Monthly channel with build version 16.0.4229.1004 and language set to Bulgarian:</span></span>
  
```xml
<File name="stream.x64.bg-bg.dat" hashLocation="s641026.cab/stream.x64.bg-bg.hash" hashAlgo="Sha256" relativePath="/office/data/%version%/" language="1026"/>
```

- <span data-ttu-id="b0b47-336">O atributo **hashLocation** Especifica o local de caminho relativo da stream.x64.bg-bg.hash para o arquivo stream.x64.bg-bg.dat.</span><span class="sxs-lookup"><span data-stu-id="b0b47-336">The **hashLocation** attribute specifies the relative path location of the stream.x64.bg-bg.hash for the stream.x64.bg-bg.dat file.</span></span> <span data-ttu-id="b0b47-337">Construa o local do arquivo de hash concatenando a URL + relativePath + hashLocation.</span><span class="sxs-lookup"><span data-stu-id="b0b47-337">Construct the hash file location by concatenating URL + relativePath + hashLocation.</span></span> <span data-ttu-id="b0b47-338">No exemplo a seguir, o local de stream.x64.bg-bg.hash seria:</span><span class="sxs-lookup"><span data-stu-id="b0b47-338">In the following example, the stream.x64.bg-bg.hash location would be:</span></span> 
    
  ```http
  http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
  ```

- <span data-ttu-id="b0b47-339">O atributo **hashAlgo** Especifica qual algoritmo de hash foi usado.</span><span class="sxs-lookup"><span data-stu-id="b0b47-339">The **hashAlgo** attribute specifies what hashing algorithm was used.</span></span> <span data-ttu-id="b0b47-340">Nesse caso, Sha256 foi usada.</span><span class="sxs-lookup"><span data-stu-id="b0b47-340">In this case Sha256 was used.</span></span> 
    
  <span data-ttu-id="b0b47-341">Para validar a integridade do arquivo stream.x64.bg-bg.dat, abra o stream.x64.bg-bg.hash e ler o valor HASH que é a primeira linha do texto no arquivo de hash.</span><span class="sxs-lookup"><span data-stu-id="b0b47-341">To validate the integrity of the stream.x64.bg-bg.dat file, open the stream.x64.bg-bg.hash and read the HASH value which is the first line of text in the hash file.</span></span> <span data-ttu-id="b0b47-342">Compare com o valor de hash computados (usando o algoritmo de hash especificado) para verificar a integridade do arquivo. dat baixado.</span><span class="sxs-lookup"><span data-stu-id="b0b47-342">Compare this to the computed hash value (using the specified hashing algorithm) to verify the integrity of the downloaded .dat file.</span></span>
    
  <span data-ttu-id="b0b47-343">O exemplo a seguir mostra o código c# para ler o hash.</span><span class="sxs-lookup"><span data-stu-id="b0b47-343">The following example shows the C# code to read the hash.</span></span>
    
  ```cs
    string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
    string readHash = readHashes.First();
  ```

### <a name="office-365-client-updates"></a><span data-ttu-id="b0b47-344">Atualizações de cliente do Office 365</span><span class="sxs-lookup"><span data-stu-id="b0b47-344">Office 365 Client Updates</span></span>

<span data-ttu-id="b0b47-345">Todas as atualizações de cliente do Office 365 são publicadas para o [Catálogo do Microsoft Update](http://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).</span><span class="sxs-lookup"><span data-stu-id="b0b47-345">All Office 365 Client Updates are published to the [Microsoft Update Catalog](http://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).</span></span>
  
<span data-ttu-id="b0b47-346">Atualizações de cliente do Office 365 habilitar software gerenciabilidade tratar as atualizações do cliente do Office 365, de maneira muito semelhante a qualquer outra atualização WU com uma exceção; as atualizações do cliente não contêm uma carga real.</span><span class="sxs-lookup"><span data-stu-id="b0b47-346">Office 365 Client Updates enable manageability software to treat the Office 365 Client Updates in a manner very similar to any other WU update with one exception; the client updates do not contain an actual payload.</span></span> <span data-ttu-id="b0b47-347">As atualizações do cliente do Office 365 não deve ser instaladas em todos os clientes mas preferência seja usadas para acionar os fluxos de trabalho com o software de capacidade de gerenciamento, substituindo o comando de instalação com o COM base em mecanismo de instalação mostrado acima.</span><span class="sxs-lookup"><span data-stu-id="b0b47-347">The Office 365 Client Updates should not be installed on any clients but rather used to trigger the workflows with the manageability software replacing the installation command with the COM based installation mechanism shown above.</span></span> 
  
<span data-ttu-id="b0b47-348">**A figura a seguir mostra um diagrama do fluxo de trabalho de atualização de cliente do Office 365.**</span><span class="sxs-lookup"><span data-stu-id="b0b47-348">**The following figure shows a diagram of the Office 365 Client Update workflow.**</span></span>

<span data-ttu-id="b0b47-349">![Diagrama de fluxo de trabalho para atualizações do cliente O365PP.] (media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Diagrama de fluxo de trabalho para atualizações do cliente O365PP")</span><span class="sxs-lookup"><span data-stu-id="b0b47-349">![Workflow diagram for O365PP client updates.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Workflow diagram for O365PP client updates")</span></span>
  
<span data-ttu-id="b0b47-350">Cada Office 365 cliente atualização publicado inclui metadados sobre a atualização.</span><span class="sxs-lookup"><span data-stu-id="b0b47-350">Each Office 365 Client Update that is published includes metadata about the update.</span></span> <span data-ttu-id="b0b47-351">Esses metadados incluem um parâmetro chamado *MoreInfoUrl* que pode ser usado para derivar as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="b0b47-351">This metadata includes a parameter called  *MoreInfoUrl*  which can be used to derive the following information:</span></span> 
  
-  <span data-ttu-id="b0b47-352">*Ver*: identifica a versão do Office associada com essa atualização.</span><span class="sxs-lookup"><span data-stu-id="b0b47-352">*Ver*: Identifies the Office version associated with this update.</span></span> 
    
-  <span data-ttu-id="b0b47-353">*Filial*: identifica o canal de atualização para essa atualização.</span><span class="sxs-lookup"><span data-stu-id="b0b47-353">*Branch*: Identifies the Update Channel for this update.</span></span> <span data-ttu-id="b0b47-354">Os valores incluem InsiderFast, internas, mensalmente, multidifusão, amplos.</span><span class="sxs-lookup"><span data-stu-id="b0b47-354">Values include InsiderFast, Insiders, Monthly, Targeted, Broad.</span></span> <span data-ttu-id="b0b47-355">Valores adicionais podem ser adicionados no futuro.</span><span class="sxs-lookup"><span data-stu-id="b0b47-355">Additional values may be added in the future.</span></span> 
    
-  <span data-ttu-id="b0b47-356">*Forma arco*: identifica a arquitetura de processador associada a essa atualização.</span><span class="sxs-lookup"><span data-stu-id="b0b47-356">*Arch*: Identifies the processor architecture associated with this update.</span></span> 
    
-  <span data-ttu-id="b0b47-357">*xmlVer*: A versão das listas de arquivo XML que deve ser usado para construir a imagem base para esta atualização.</span><span class="sxs-lookup"><span data-stu-id="b0b47-357">*xmlVer*: The version of the XML file lists that should be used to construct the base image for this update.</span></span> 
    
-  <span data-ttu-id="b0b47-358">*xmlPath*: caminho para o OFL. Lista de arquivo CAB que contém o arquivo XML.</span><span class="sxs-lookup"><span data-stu-id="b0b47-358">*xmlPath*: Path to the OFL.CAB file which contains the XML file lists.</span></span> 
    
-  <span data-ttu-id="b0b47-359">*mlFile*: O nome da lista de arquivos que deve ser usado para esta atualização.</span><span class="sxs-lookup"><span data-stu-id="b0b47-359">*mlFile*: The name of the file list that should be used for this update.</span></span> <span data-ttu-id="b0b47-360">O valor será O365Client_32bit ou O365Client_64bit e isso coincidirá com a forma de arco.</span><span class="sxs-lookup"><span data-stu-id="b0b47-360">The value will be O365Client_32bit or O365Client_64bit and will match the Arch.</span></span> 
    
<span data-ttu-id="b0b47-361">A URL a seguir está um exemplo do parâmetro *MoreInfoURL* que refere-se para as versões de atualização de cliente do Office 365 para a versão de 32 bits do Office com a versão de compilação do 16.0.2342.2343 no canal atual.</span><span class="sxs-lookup"><span data-stu-id="b0b47-361">The following URL is an example of the  *MoreInfoURL*  parameter which refers to the Office 365 client update releases for the 32-bit version of Office with build version of 16.0.2342.2343 on the Current channel.</span></span> 
  
<span data-ttu-id="b0b47-362">http://officecdn.microsoft.com/pr/wsus/ofl.cabé o local das listas de arquivo XML para essa atualização, especificamente o O365Client_32bit.xml de dentro do OFL. CAB.</span><span class="sxs-lookup"><span data-stu-id="b0b47-362">http://officecdn.microsoft.com/pr/wsus/ofl.cab is the location of the XML file lists for this update, specifically the O365Client_32bit.xml from within the OFL.CAB.</span></span>
  
[<span data-ttu-id="b0b47-363">Liberações de canal de atualização de cliente Office 365</span><span class="sxs-lookup"><span data-stu-id="b0b47-363">Office 365 client update channel releases</span></span>](http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.8326.2096&Branch=Current&Arch=64&XMLVer=1.4&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml)
  
### <a name="additional-metadata-for-automating-content-staging"></a><span data-ttu-id="b0b47-364">Metadados adicionais para automatizar a preparação de conteúdo</span><span class="sxs-lookup"><span data-stu-id="b0b47-364">Additional metadata for automating content staging</span></span>

<span data-ttu-id="b0b47-365">Além de metadados que é publicado que define lá também são arquivos adicionais do XML publicados para o CDN que pode ajudar a fornecer informações adicionais sobre os clientes do Office 365 estão disponíveis a partir do CDN do Office.</span><span class="sxs-lookup"><span data-stu-id="b0b47-365">In addition to the metadata that is published which defines there are also additional XML files published to the CDN that can help provide additional information about the Office 365 clients that are available from the Office CDN.</span></span>
  
<span data-ttu-id="b0b47-366">**SKUS. XML**</span><span class="sxs-lookup"><span data-stu-id="b0b47-366">**SKUS.XML**</span></span>
  
<span data-ttu-id="b0b47-367">Este arquivo XML contido em um CAB assinado e publicado para o CDN Office na seguinte URL: [http://officecdn.microsoft.com/pr/wsus/skus.cab](http://officecdn.microsoft.com/pr/wsus/skus.cab).</span><span class="sxs-lookup"><span data-stu-id="b0b47-367">This XML file is contained within a signed CAB and published to the Office CDN at the following URL: [http://officecdn.microsoft.com/pr/wsus/skus.cab](http://officecdn.microsoft.com/pr/wsus/skus.cab).</span></span>
  
<span data-ttu-id="b0b47-368">Os metadados publicado nesse arquivo XML são útil para determinar quais produtos estão disponíveis para implantação e manutenção da CDN Office junto com várias opções para cada um.</span><span class="sxs-lookup"><span data-stu-id="b0b47-368">The metadata published in this XML file is useful for determining which products are available for deployment and servicing from the Office CDN along with various options for each.</span></span> 
  
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

<span data-ttu-id="b0b47-369">** \<ReleaseInfo\> ** nó raiz contém o atributo de PublishedDate que identifica a data em que este arquivo foi publicado.</span><span class="sxs-lookup"><span data-stu-id="b0b47-369">**\<ReleaseInfo\>** root node contains the PublishedDate attribute which identifies the date which this file was published.</span></span> 
  
<span data-ttu-id="b0b47-370">** \<SKU\> ** nó identifica um SKU individual.</span><span class="sxs-lookup"><span data-stu-id="b0b47-370">**\<SKU\>** node identifies an individual SKU.</span></span> 
  
- <span data-ttu-id="b0b47-371">O atributo *ProductID* identifica a ID que é passada como atributo ID no Configuration se estiver usando a ODT.</span><span class="sxs-lookup"><span data-stu-id="b0b47-371">The  *ProductID*  attribute identifies the ID that is passed as the ID attribute in the configuration.xml if using the ODT.</span></span> <span data-ttu-id="b0b47-372">Por exemplo, `<Product ID="O365ProPlusRetail">`.</span><span class="sxs-lookup"><span data-stu-id="b0b47-372">For example, `<Product ID="O365ProPlusRetail">`.</span></span> 
    
- <span data-ttu-id="b0b47-373">O *padrão* de atributo, se definido como verdadeiro, identifica a SKU recomendada.</span><span class="sxs-lookup"><span data-stu-id="b0b47-373">The  *Default*  attribute, if set to True, identifies the recommended SKU.</span></span> 
    
<span data-ttu-id="b0b47-374">** \<App\> ** nós são usados para definir os aplicativos individuais do Office que ofereça suporte a cada SKU.</span><span class="sxs-lookup"><span data-stu-id="b0b47-374">**\<App\>** nodes are used to define the individual Office apps that each SKU supports.</span></span> 
  
- <span data-ttu-id="b0b47-375">O atributo *Name* é o nome do aplicativo exibido.</span><span class="sxs-lookup"><span data-stu-id="b0b47-375">The  *Name*  attribute is the displayed application name.</span></span> 
    
- <span data-ttu-id="b0b47-376">O *AppID* é o atributo ID passado do Configuration. XML para o ** \<ExcludeApp\> ** nó se estiver usando a ODT.</span><span class="sxs-lookup"><span data-stu-id="b0b47-376">The  *AppID*  attribute is the ID attribute passed in the configuration.xml for the **\<ExcludeApp\>** node if using the ODT.</span></span> <span data-ttu-id="b0b47-377">Por exemplo, `<ExcludeApp ID="Publisher" />`.</span><span class="sxs-lookup"><span data-stu-id="b0b47-377">For example, `<ExcludeApp ID="Publisher" />`.</span></span> 
    
<span data-ttu-id="b0b47-378">**RELEASEHISTORY. XML**</span><span class="sxs-lookup"><span data-stu-id="b0b47-378">**RELEASEHISTORY.XML**</span></span>
  
<span data-ttu-id="b0b47-379">Este arquivo XML contido em um CAB assinado e publicado para o CDN do Office no seguinte local: [http://officecdn.microsoft.com/pr/wsus/releasehistory.cab](http://officecdn.microsoft.com/pr/wsus/releasehistory.cab).</span><span class="sxs-lookup"><span data-stu-id="b0b47-379">This XML file is contained within a signed CAB and published to the Office CDN at the following location: [http://officecdn.microsoft.com/pr/wsus/releasehistory.cab](http://officecdn.microsoft.com/pr/wsus/releasehistory.cab).</span></span> 
  
<span data-ttu-id="b0b47-380">Os metadados publicado nesse arquivo XML são útil para determinar quais canais são suportados para a manutenção de atualizações de CDN do Office, juntamente com informações sobre o histórico de compilação para cada um dos canais com suporte.</span><span class="sxs-lookup"><span data-stu-id="b0b47-380">The metadata published in this XML file is useful for determining which channels are supported for servicing updates from the Office CDN along with information about the build history for each of the supported channels.</span></span>
  
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

<span data-ttu-id="b0b47-381">O ** \<ReleaseHistory\> ** nó raiz contém o atributo de PublishedDate que identifica a data em que este arquivo foi publicado.</span><span class="sxs-lookup"><span data-stu-id="b0b47-381">The **\<ReleaseHistory\>** root node contains the PublishedDate attribute which identifies the date which this file was published.</span></span> 
  
<span data-ttu-id="b0b47-382">O ** \<UpdateChannel\> ** nó define um canal com suporte.</span><span class="sxs-lookup"><span data-stu-id="b0b47-382">The **\<UpdateChannel\>** node defines a supported channel.</span></span> 
  
- <span data-ttu-id="b0b47-383">*Nome* do atributo define a ID do canal que é utilizada para passar para a ODT no Configuration como o atributo de canal.</span><span class="sxs-lookup"><span data-stu-id="b0b47-383">The  *Name*  attribute defines the channel ID which is used to pass to the ODT in the configuration.xml as the Channel attribute.</span></span> 
    
  <span data-ttu-id="b0b47-384">Exemplo: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Current">`</span><span class="sxs-lookup"><span data-stu-id="b0b47-384">Example: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Current">`</span></span> 
    
  > [!NOTE] 
  > <span data-ttu-id="b0b47-385">Este atributo foi preterido e é usado apenas para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="b0b47-385">This attribute has been deprecated and is used for backward compatibility only.</span></span> <span data-ttu-id="b0b47-386">Use o atributo ID no lugar do atributo Name.</span><span class="sxs-lookup"><span data-stu-id="b0b47-386">Use the ID attribute in place of the Name attribute.</span></span> 
    
- <span data-ttu-id="b0b47-387">O atributo *ID* define a ID do canal que é utilizada para passar para a ODT no Configuration como o atributo de canal.</span><span class="sxs-lookup"><span data-stu-id="b0b47-387">The  *ID*  attribute defines the channel ID which is used to pass to the ODT in the configuration.xml as the Channel attribute.</span></span> 
    
  <span data-ttu-id="b0b47-388">Exemplo: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Deferred">`</span><span class="sxs-lookup"><span data-stu-id="b0b47-388">Example: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Deferred">`</span></span> 
    
- <span data-ttu-id="b0b47-389">O atributo **DisplayName** é usado como o nome para exibição.</span><span class="sxs-lookup"><span data-stu-id="b0b47-389">The **DisplayName**  attribute is used as the display name.</span></span> 
    
<span data-ttu-id="b0b47-390">O ** \<atualizar\> ** nó é usado para definir cada atualização que tenha sido publicada para o canal em particular.</span><span class="sxs-lookup"><span data-stu-id="b0b47-390">The **\<Update\>** node is used to define each update that has been published for that particular channel.</span></span> 
  
- <span data-ttu-id="b0b47-391">Atributo o **mais recente** , se definido como verdadeiro, define a versão que é a versão mais recente para esse canal.</span><span class="sxs-lookup"><span data-stu-id="b0b47-391">The **Latest**  attribute, if set to True, defines the release that is the latest release for that channel.</span></span> 
    
- <span data-ttu-id="b0b47-392">O atributo **Version** define o número de versão para essa atualização específica.</span><span class="sxs-lookup"><span data-stu-id="b0b47-392">The **Version** attribute defines the version number for this particular update.</span></span> 
    
- <span data-ttu-id="b0b47-393">O atributo **LegacyVersion** define o número de versão completa para essa atualização específica.</span><span class="sxs-lookup"><span data-stu-id="b0b47-393">The **LegacyVersion** attribute defines the full version number for this particular update.</span></span> 
    
- <span data-ttu-id="b0b47-394">O atributo **Construir** define o número de compilação para essa atualização específica.</span><span class="sxs-lookup"><span data-stu-id="b0b47-394">The **Build** attribute defines the build number for this particular update.</span></span> 
    
- <span data-ttu-id="b0b47-395">O atributo **PubTime** define a data e hora em que essa atualização foi publicada para o CDN do Office.</span><span class="sxs-lookup"><span data-stu-id="b0b47-395">The **PubTime** attribute defines the date and time at which this update was published to the Office CDN.</span></span> 
    

