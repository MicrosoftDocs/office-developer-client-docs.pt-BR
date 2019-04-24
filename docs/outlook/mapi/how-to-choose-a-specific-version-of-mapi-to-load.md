---
title: Escolher uma versão MAPI específica para carregar
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 85539a7f-74b6-4267-86ea-00da2c900c34
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d353eba55e33b8ab48b3c47d2f31f1b5e0973b58
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344517"
---
# <a name="choose-a-specific-version-of-mapi-to-load"></a><span data-ttu-id="2e22a-103">Escolher uma versão MAPI específica para carregar</span><span class="sxs-lookup"><span data-stu-id="2e22a-103">Choose a specific version of MAPI to load</span></span>

<span data-ttu-id="2e22a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e22a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e22a-105">Ao vincular explicitamente a uma implementação de MAPI, você deve selecionar cuidadosamente a implementação a ser carregada.</span><span class="sxs-lookup"><span data-stu-id="2e22a-105">When linking explicitly to an implementation of MAPI, you must carefully select which implementation to load.</span></span> 
  
<span data-ttu-id="2e22a-106">Há dois métodos para vincular explicitamente a uma implementação de MAPI.</span><span class="sxs-lookup"><span data-stu-id="2e22a-106">There are two methods to link explicitly to an implementation of MAPI.</span></span> 
  
1. <span data-ttu-id="2e22a-107">Você pode carregar a biblioteca de stub MAPI e especificar no registro uma DLL personalizada para carregar e distribuir as chamadas MAPI para.</span><span class="sxs-lookup"><span data-stu-id="2e22a-107">You can load the MAPI stub library, and specify in the registry a custom DLL to load and dispatch MAPI calls to.</span></span>
    
2. <span data-ttu-id="2e22a-108">Você pode implementar o algoritmo de pesquisa de cliente MAPI para pesquisar a versão de MAPI usada pelo cliente de email padrão e carregá-lo.</span><span class="sxs-lookup"><span data-stu-id="2e22a-108">You can implement the MAPI client lookup algorithm to look up the version of MAPI used by the default mail client and load it.</span></span>
    
<span data-ttu-id="2e22a-109">Como você pode alterar as [configurações do registro stub de Mapi32. dll](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx) para direcionar seu aplicativo para usar qualquer implementação de MAPI, recomendamos que você direcione seu aplicativo para usar uma implementação de MAPI que você testou com.</span><span class="sxs-lookup"><span data-stu-id="2e22a-109">Because you can change the [Mapi32.dll Stub Registry Settings](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx) to direct your application to use any implementation of MAPI, we recommend that you direct your application to use an implementation of MAPI that you have tested with.</span></span> <span data-ttu-id="2e22a-110">O procedimento a seguir descreve os dois métodos de vinculação explícita.</span><span class="sxs-lookup"><span data-stu-id="2e22a-110">The following describes both methods of linking explicitly.</span></span> 
  
## <a name="reading-from-the-registry"></a><span data-ttu-id="2e22a-111">Leitura do registro</span><span class="sxs-lookup"><span data-stu-id="2e22a-111">Reading from the registry</span></span>

### <a name="to-read-mapi-implementation-information-from-the-registry"></a><span data-ttu-id="2e22a-112">Para ler as informações de implementação de MAPI do registro</span><span class="sxs-lookup"><span data-stu-id="2e22a-112">To read MAPI implementation information from the registry</span></span>

1. <span data-ttu-id="2e22a-113">As chaves do registro que indicam uma DLL personalizada para um cliente de email estão localizadas na `HKLM\Software\Clients\Mail` chave do cliente de email.</span><span class="sxs-lookup"><span data-stu-id="2e22a-113">The registry keys that indicate a custom DLL for a mail client are located under the  `HKLM\Software\Clients\Mail` key of the mail client.</span></span> 
    
   <span data-ttu-id="2e22a-114">A tabela a seguir descreve estas chaves:</span><span class="sxs-lookup"><span data-stu-id="2e22a-114">The following table describes these keys:</span></span>
    
   |<span data-ttu-id="2e22a-115">**Tecla**</span><span class="sxs-lookup"><span data-stu-id="2e22a-115">**Key**</span></span>|<span data-ttu-id="2e22a-116">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2e22a-116">**Description**</span></span>|
   |:-----|:-----|
   |<span data-ttu-id="2e22a-117">MSIComponentID</span><span class="sxs-lookup"><span data-stu-id="2e22a-117">MSIComponentID</span></span>  <br/> |<span data-ttu-id="2e22a-118">Uma ID de categoria (GUID) PublishComponent do Windows Installer que identifica a DLL que exporta as chamadas simples de MAPI ou MAPI.</span><span class="sxs-lookup"><span data-stu-id="2e22a-118">A Windows Installer PublishComponent category ID (GUID) that identifies the DLL that exports simple MAPI or MAPI calls.</span></span> <span data-ttu-id="2e22a-119">Se definido, esta tecla tem precedência sobre a chave **DLLPath** ou **DLLPathEx** .</span><span class="sxs-lookup"><span data-stu-id="2e22a-119">If set, this key takes precedence over the **DLLPath** or **DLLPathEx** key.</span></span>  <br/> |
   |<span data-ttu-id="2e22a-120">MSIApplicationLCID</span><span class="sxs-lookup"><span data-stu-id="2e22a-120">MSIApplicationLCID</span></span>  <br/> |<span data-ttu-id="2e22a-121">Identificador de localidade (LCID) do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2e22a-121">Locale identifier (LCID) for your application.</span></span> <span data-ttu-id="2e22a-122">O primeiro valor de cadeia de caracteres identifica uma subchave de e os valores de cadeia de `HKLM\Software` caracteres subsequentes identificam os valores do registro sob esta chave que contêm informações de localidade.</span><span class="sxs-lookup"><span data-stu-id="2e22a-122">The first string value identifies a sub-key from  `HKLM\Software` and subsequent string values identify registry values underneath this key that contain locale information.</span></span>  <br/> |
   |<span data-ttu-id="2e22a-123">MSIOfficeLCID</span><span class="sxs-lookup"><span data-stu-id="2e22a-123">MSIOfficeLCID</span></span>  <br/> |<span data-ttu-id="2e22a-124">LCIDs do Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="2e22a-124">LCIDs for Microsoft Office.</span></span> <span data-ttu-id="2e22a-125">O primeiro valor de cadeia de caracteres identifica uma subchave de e os valores de cadeia de `HKLM\Software` caracteres subsequentes identificam os valores do registro sob essa chave.</span><span class="sxs-lookup"><span data-stu-id="2e22a-125">The first string value identifies a sub-key from  `HKLM\Software` and subsequent string values identify registry values underneath this key.</span></span>  <br/> |
   
   <span data-ttu-id="2e22a-126">Obtenha as informações dessas chaves.</span><span class="sxs-lookup"><span data-stu-id="2e22a-126">Obtain the information from these keys.</span></span>
    
2. <span data-ttu-id="2e22a-127">Passe os valores obtidos da etapa anterior para a função [FGetComponentPath](fgetcomponentpath.md) .</span><span class="sxs-lookup"><span data-stu-id="2e22a-127">Pass the values that you obtained from the previous step to the [FGetComponentPath](fgetcomponentpath.md) function.</span></span> <span data-ttu-id="2e22a-128">**FGetComponentPath** é uma função que é exportada pela biblioteca de stub de MAPI MAPISTUB. dll.</span><span class="sxs-lookup"><span data-stu-id="2e22a-128">**FGetComponentPath** is a function that is exported by the MAPI stub library Mapistub.dll.</span></span> <span data-ttu-id="2e22a-129">Ele retorna o caminho da versão personalizada de MAPI.</span><span class="sxs-lookup"><span data-stu-id="2e22a-129">It returns the path of the custom version of MAPI.</span></span> 


### <a name="to-load-the-implementation-of-mapi-marked-as-default"></a><span data-ttu-id="2e22a-130">Para carregar a implementação de MAPI marcada como padrão</span><span class="sxs-lookup"><span data-stu-id="2e22a-130">To load the implementation of MAPI marked as default</span></span>

1. <span data-ttu-id="2e22a-131">Leia o `HKLM\Software\Clients\Mail::(default)` valor do registro.</span><span class="sxs-lookup"><span data-stu-id="2e22a-131">Read the  `HKLM\Software\Clients\Mail::(default)` registry value.</span></span> 
    
2. <span data-ttu-id="2e22a-132">Procure as informações para o cliente indicado, conforme descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="2e22a-132">Look up the information for the indicated client as described earlier.</span></span>
    
> [!NOTE]
> <span data-ttu-id="2e22a-133">Observe que o cliente de email padrão pode não implementar o MAPI estendido.</span><span class="sxs-lookup"><span data-stu-id="2e22a-133">Note that the default mail client might not implement Extended MAPI.</span></span> 
  
#### <a name="example"></a><span data-ttu-id="2e22a-134">Exemplo</span><span class="sxs-lookup"><span data-stu-id="2e22a-134">Example</span></span>

<span data-ttu-id="2e22a-135">Para carregar MAPI conforme implementado pelo Outlook, procure as chaves do registro em `HKLM\Software\Clients\Mail\Microsoft Outlook` e passe-as para o **FGetComponentPath**.</span><span class="sxs-lookup"><span data-stu-id="2e22a-135">To load MAPI as implemented by Outlook, look up the registry keys under  `HKLM\Software\Clients\Mail\Microsoft Outlook` and pass them to **FGetComponentPath**.</span></span> <span data-ttu-id="2e22a-136">**FGetComponentPath** retornará o caminho para a implementação de MAPI do Outlook.</span><span class="sxs-lookup"><span data-stu-id="2e22a-136">**FGetComponentPath** will return the path for Outlook's implementation of MAPI.</span></span> 
  
<span data-ttu-id="2e22a-137">Se as chaves **MSIComponentID**, **MSIApplicationLCID**e **MSIOfficeLCID** não estiverem definidas, verifique o valor do registro **DLLPathEx** .</span><span class="sxs-lookup"><span data-stu-id="2e22a-137">If the keys **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID** are not set, check the **DLLPathEx** registry value.</span></span> <span data-ttu-id="2e22a-138">Se as chaves estiverem definidas, **FGetComponentPath** fornecerá o caminho da implementação de MAPI do cliente.</span><span class="sxs-lookup"><span data-stu-id="2e22a-138">If the keys are set, **FGetComponentPath** gives the path of the client's implementation of MAPI.</span></span> 
  
## <a name="implementing-the-mapi-client-lookup-algorithm"></a><span data-ttu-id="2e22a-139">Implementar o algoritmo de pesquisa de cliente MAPI</span><span class="sxs-lookup"><span data-stu-id="2e22a-139">Implementing the MAPI Client Lookup algorithm</span></span>

<span data-ttu-id="2e22a-140">A tabela a seguir lista as quatro funções do MFCMAPI que são usadas para pesquisar o caminho de uma implementação personalizada de MAPI:</span><span class="sxs-lookup"><span data-stu-id="2e22a-140">The following table lists the four functions from MFCMAPI that are used to look up the path for a custom implementation of MAPI:</span></span>
  
|<span data-ttu-id="2e22a-141">**Function**</span><span class="sxs-lookup"><span data-stu-id="2e22a-141">**Function**</span></span>|<span data-ttu-id="2e22a-142">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2e22a-142">**Description**</span></span>|
|:-----|:-----|
| `GetMAPIPath` <br/> |<span data-ttu-id="2e22a-143">Obtém o caminho da biblioteca MAPI.</span><span class="sxs-lookup"><span data-stu-id="2e22a-143">Gets the MAPI library path.</span></span>  <br/> |
| `GetMailKey` <br/> |<span data-ttu-id="2e22a-144">Obtém a chave de registro de email MAPI.</span><span class="sxs-lookup"><span data-stu-id="2e22a-144">Gets the MAPI mail registry key.</span></span>  <br/> |
| `GetMapiMsiIds` <br/> |<span data-ttu-id="2e22a-145">Obtém o identificador do Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2e22a-145">Gets the Windows Installer identifier.</span></span>  <br/> |
| `GetComponentPath` <br/> |<span data-ttu-id="2e22a-146">Obtém o caminho do componente usando [FGetComponentPath](fgetcomponentpath.md).</span><span class="sxs-lookup"><span data-stu-id="2e22a-146">Gets the component path using [FGetComponentPath](fgetcomponentpath.md).</span></span>  <br/> |
   
<span data-ttu-id="2e22a-147">Como o MFCMAPI carrega a implementação padrão de MAPI por padrão, se você quiser usar uma implementação diferente de MAPI, é necessário direcioná-lo explicitamente para isso.</span><span class="sxs-lookup"><span data-stu-id="2e22a-147">Because MFCMAPI loads the default implementation of MAPI by default, if you want to use a different implementation of MAPI, you must explicitly direct it to do so.</span></span> <span data-ttu-id="2e22a-148">Isso é feito usando a rotina **MAPI Session\Load** .</span><span class="sxs-lookup"><span data-stu-id="2e22a-148">This is performed by using the **Session\Load MAPI** routine.</span></span> 
  
### <a name="how-these-functions-work"></a><span data-ttu-id="2e22a-149">Como essas funções funcionam</span><span class="sxs-lookup"><span data-stu-id="2e22a-149">How these functions work</span></span>

1. <span data-ttu-id="2e22a-150">Chamadas `GetMAPIPath`MFCMAPI, passando NULL para o parâmetro Client, para carregar a implementação MAPI padrão.</span><span class="sxs-lookup"><span data-stu-id="2e22a-150">MFCMAPI calls  `GetMAPIPath`, passing NULL for the client parameter, to load the default MAPI implementation.</span></span>
    
2.  <span data-ttu-id="2e22a-151">`GetMAPIPath`chamadas `GetMapiMsiIds` para ler os valores de **MSIComponentID**, **MSIApplicationLCID**e **MSIOfficeLCID**.</span><span class="sxs-lookup"><span data-stu-id="2e22a-151">`GetMAPIPath` calls  `GetMapiMsiIds` to read the values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**.</span></span>
    
3.  <span data-ttu-id="2e22a-152">`GetMapiMsiIds`chamadas `GetMailKey` para abrir a chave do registro para o cliente de email padrão.</span><span class="sxs-lookup"><span data-stu-id="2e22a-152">`GetMapiMsiIds` calls  `GetMailKey` to open the registry key for the default mail client.</span></span> 
    
4.  <span data-ttu-id="2e22a-153">`GetMapiMsiIds`usa o identificador do registro retornado `GetMailKey` por para pesquisar valores de **MSIComponentID**, **MSIApplicationLCID**e **MSIOfficeLCID**.</span><span class="sxs-lookup"><span data-stu-id="2e22a-153">`GetMapiMsiIds` uses the registry handle returned by  `GetMailKey` to look up values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**.</span></span>
    
5. <span data-ttu-id="2e22a-154">Os valores de **MSIComponentID**, **MSIApplicationLCID**e **MSIOfficeLCID**são retornados para `GetMAPIPath`.</span><span class="sxs-lookup"><span data-stu-id="2e22a-154">The values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**, are returned to  `GetMAPIPath`.</span></span>  <span data-ttu-id="2e22a-155">`GetMAPIPath`em seguida, passa `GetComponentPath`-os para o.</span><span class="sxs-lookup"><span data-stu-id="2e22a-155">`GetMAPIPath` then passes them to  `GetComponentPath`.</span></span>
    
6.  <span data-ttu-id="2e22a-156">`GetComponentPath`carrega a biblioteca de stub MAPI, Mapi32. dll, do diretório do sistema.</span><span class="sxs-lookup"><span data-stu-id="2e22a-156">`GetComponentPath` loads the MAPI stub library, Mapi32.dll, from the system directory.</span></span> 
    
7.  <span data-ttu-id="2e22a-157">`GetComponentPath`em seguida, recupera o endereço da função **FGetComponentPath** de Mapi32. dll, supondo que Mapi32. dll exporta **FGetComponentPath**.</span><span class="sxs-lookup"><span data-stu-id="2e22a-157">`GetComponentPath` then retrieves the address of the **FGetComponentPath** function from Mapi32.dll, assuming that Mapi32.dll exports **FGetComponentPath**.</span></span>
    
8. <span data-ttu-id="2e22a-158">Se a obter o endereço de **FGetComponentPath** de Mapi32. dll falhar `GetComponentPath` , o recuperará o endereço de MAPISTUB. dll.</span><span class="sxs-lookup"><span data-stu-id="2e22a-158">If getting the address of **FGetComponentPath** from Mapi32.dll fails,  `GetComponentPath` retrieves the address from Mapistub.dll.</span></span> 
    
9.  <span data-ttu-id="2e22a-159">`GetComponentPath`em seguida, chama **FGetComponentPath**, obtendo o caminho da versão padrão do MAPI.</span><span class="sxs-lookup"><span data-stu-id="2e22a-159">`GetComponentPath` then calls **FGetComponentPath**, obtaining the path of the default version of MAPI.</span></span>
    
10.  <span data-ttu-id="2e22a-160">`GetMAPIPath`em seguida, retorna esse caminho para o chamador, que carrega o MAPI e explicitamente os links para ele, conforme descrito em [link to MAPI Functions](how-to-link-to-mapi-functions.md).</span><span class="sxs-lookup"><span data-stu-id="2e22a-160">`GetMAPIPath` then returns this path to the caller, which then loads MAPI and explicitly links to it as described in [Link to MAPI Functions](how-to-link-to-mapi-functions.md).</span></span>
    
> [!NOTE] 
> - <span data-ttu-id="2e22a-161">Para dar suporte a cópias localizadas de MAPI para localidades do inglês e `GetMAPIPath` que não sejam do inglês, lê os valores das subchaves **MSIApplicationLCID** e **MSIOfficeLCID** .</span><span class="sxs-lookup"><span data-stu-id="2e22a-161">To support localized copies of MAPI for English and non-English locales,  `GetMAPIPath` reads the values for the **MSIApplicationLCID** and **MSIOfficeLCID** subkeys.</span></span>  <span data-ttu-id="2e22a-162">`GetMAPIPath`em seguida, chama **FGetComponentPath**, primeiro especificando **MSIApplicationLCID** como **szQualifier**e, novamente, especificando **MSIOfficeLCID** como **szQualifier**.</span><span class="sxs-lookup"><span data-stu-id="2e22a-162">`GetMAPIPath` then calls **FGetComponentPath**, first specifying **MSIApplicationLCID** as **szQualifier**, and again specifying **MSIOfficeLCID** as **szQualifier**.</span></span> <span data-ttu-id="2e22a-163">Para obter mais informações sobre chaves do registro para clientes de email que oferecem suporte a idiomas que não são do inglês, confira conFigurando [as chaves msi para sua dll MAPI](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="2e22a-163">For more information about registry keys for mail clients that support non-English languages, see [Setting Up the MSI Keys for Your MAPI DLL](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx).</span></span>   
> - <span data-ttu-id="2e22a-164">Se o MFCMAPI não receber um caminho para MAPI usando `GetMAPIPath`o, ele carregará a biblioteca de stub MAPI do diretório do sistema.</span><span class="sxs-lookup"><span data-stu-id="2e22a-164">If MFCMAPI does not receive a path for MAPI using  `GetMAPIPath`, it loads the MAPI stub library from the system directory.</span></span>
> - <span data-ttu-id="2e22a-165">O valor do registro **MSMapiApps** discutido em [mapeamento explicitamente de chamadas MAPI para DLLs MAPI](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx) só se aplica quando a biblioteca stub MAPI é usada.</span><span class="sxs-lookup"><span data-stu-id="2e22a-165">The **MSMapiApps** registry value discussed in [Explicitly Mapping MAPI Calls to MAPI DLLs](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx) only applies when the MAPI Stub library is used.</span></span> <span data-ttu-id="2e22a-166">Os aplicativos que carregam uma implementação específica de MAPI ou carregam a implementação padrão não precisam definir a chave do registro **MSMapiApps** .</span><span class="sxs-lookup"><span data-stu-id="2e22a-166">Applications that load a specific implementation of MAPI or load the default implementation do not have to set the **MSMapiApps** registry key.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="2e22a-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e22a-167">See also</span></span>

- [<span data-ttu-id="2e22a-168">FGetComponentPath</span><span class="sxs-lookup"><span data-stu-id="2e22a-168">FGetComponentPath</span></span>](fgetcomponentpath.md)
- [<span data-ttu-id="2e22a-169">Visão geral da programação MAPI</span><span class="sxs-lookup"><span data-stu-id="2e22a-169">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
- [<span data-ttu-id="2e22a-170">Link para funções MAPI</span><span class="sxs-lookup"><span data-stu-id="2e22a-170">Link to MAPI Functions</span></span>](how-to-link-to-mapi-functions.md)
- [<span data-ttu-id="2e22a-171">Configurações do registro stub Mapi32. dll</span><span class="sxs-lookup"><span data-stu-id="2e22a-171">Mapi32.dll Stub Registry Settings</span></span>](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx)
- [<span data-ttu-id="2e22a-172">ConFigurando as chaves MSI para sua DLL MAPI</span><span class="sxs-lookup"><span data-stu-id="2e22a-172">Setting Up the MSI Keys for Your MAPI DLL</span></span>](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)
- [<span data-ttu-id="2e22a-173">Mapear explicitamente as chamadas MAPI para DLLs MAPI</span><span class="sxs-lookup"><span data-stu-id="2e22a-173">Explicitly Mapping MAPI Calls to MAPI DLLs</span></span>](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx)

