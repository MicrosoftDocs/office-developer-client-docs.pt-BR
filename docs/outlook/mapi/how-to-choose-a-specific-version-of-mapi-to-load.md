---
title: Escolher uma versão específica de MAPI para carregar
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 85539a7f-74b6-4267-86ea-00da2c900c34
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: d0bce7b3a12f259b7ac5f28219c8a92dd2200f07
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19766705"
---
# <a name="choose-a-specific-version-of-mapi-to-load"></a><span data-ttu-id="10b33-103">Escolher uma versão específica de MAPI para carregar</span><span class="sxs-lookup"><span data-stu-id="10b33-103">Choose a specific version of MAPI to load</span></span>

<span data-ttu-id="10b33-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="10b33-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="10b33-105">Quando vincular explicitamente a implementação de MAPI, você deve selecionar cuidadosamente qual implementação para carregar.</span><span class="sxs-lookup"><span data-stu-id="10b33-105">When linking explicitly to an implementation of MAPI, you must carefully select which implementation to load.</span></span> 
  
<span data-ttu-id="10b33-106">Há dois métodos para vincular explicitamente a implementação de MAPI.</span><span class="sxs-lookup"><span data-stu-id="10b33-106">There are two methods to link explicitly to an implementation of MAPI.</span></span> 
  
1. <span data-ttu-id="10b33-107">Você pode carregar a biblioteca de stub MAPI e especificar no registro de uma DLL personalizada para carregar e expedir MAPI chamadas para.</span><span class="sxs-lookup"><span data-stu-id="10b33-107">You can load the MAPI stub library, and specify in the registry a custom DLL to load and dispatch MAPI calls to.</span></span>
    
2. <span data-ttu-id="10b33-108">Você pode implementar o algoritmo de pesquisa do cliente MAPI para pesquisar a versão do MAPI usado pelo cliente de email padrão e carregá-la.</span><span class="sxs-lookup"><span data-stu-id="10b33-108">You can implement the MAPI client lookup algorithm to look up the version of MAPI used by the default mail client and load it.</span></span>
    
<span data-ttu-id="10b33-109">Como você pode alterar as [Configurações de registro de Stub Mapi32](http://msdn.microsoft.com/en-us/library/ms531218%28EXCHG.10%29.aspx) para direcionar o seu aplicativo para usar qualquer implementação de MAPI, recomendamos que você direcione o seu aplicativo para usar uma implementação do MAPI que você testadas com.</span><span class="sxs-lookup"><span data-stu-id="10b33-109">Because you can change the [Mapi32.dll Stub Registry Settings](http://msdn.microsoft.com/en-us/library/ms531218%28EXCHG.10%29.aspx) to direct your application to use any implementation of MAPI, we recommend that you direct your application to use an implementation of MAPI that you have tested with.</span></span> <span data-ttu-id="10b33-110">A seguir descreve os dois métodos de vínculo explicitamente.</span><span class="sxs-lookup"><span data-stu-id="10b33-110">The following describes both methods of linking explicitly.</span></span> 
  
## <a name="reading-from-the-registry"></a><span data-ttu-id="10b33-111">Leitura do registro</span><span class="sxs-lookup"><span data-stu-id="10b33-111">Reading from the registry</span></span>

### <a name="to-read-mapi-implementation-information-from-the-registry"></a><span data-ttu-id="10b33-112">Para ler informações de implementação do MAPI do registro</span><span class="sxs-lookup"><span data-stu-id="10b33-112">To read MAPI implementation information from the registry</span></span>

1. <span data-ttu-id="10b33-113">As chaves do registro que indicam uma DLL personalizada para um cliente de email estão localizadas no `HKLM\Software\Clients\Mail` chave do cliente de email.</span><span class="sxs-lookup"><span data-stu-id="10b33-113">The registry keys that indicate a custom DLL for a mail client are located under the  `HKLM\Software\Clients\Mail` key of the mail client.</span></span> 
    
   <span data-ttu-id="10b33-114">A tabela a seguir descreve essas chaves:</span><span class="sxs-lookup"><span data-stu-id="10b33-114">The following table describes these keys:</span></span>
    
   |<span data-ttu-id="10b33-115">**Key**</span><span class="sxs-lookup"><span data-stu-id="10b33-115">**Key**</span></span>|<span data-ttu-id="10b33-116">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="10b33-116">**Description**</span></span>|
   |:-----|:-----|
   |<span data-ttu-id="10b33-117">MSIComponentID</span><span class="sxs-lookup"><span data-stu-id="10b33-117">MSIComponentID</span></span>  <br/> |<span data-ttu-id="10b33-118">Chama a uma categoria do Windows Installer PublishComponent ID (GUID) que identifica a DLL que exporta o simple MAPI ou MAPI.</span><span class="sxs-lookup"><span data-stu-id="10b33-118">A Windows Installer PublishComponent category ID (GUID) that identifies the DLL that exports simple MAPI or MAPI calls.</span></span> <span data-ttu-id="10b33-119">Se definido, esta tecla tem precedência sobre a tecla **DLLPath** ou **DLLPathEx** .</span><span class="sxs-lookup"><span data-stu-id="10b33-119">If set, this key takes precedence over the **DLLPath** or **DLLPathEx** key.</span></span>  <br/> |
   |<span data-ttu-id="10b33-120">MSIApplicationLCID</span><span class="sxs-lookup"><span data-stu-id="10b33-120">MSIApplicationLCID</span></span>  <br/> |<span data-ttu-id="10b33-121">Identificador de localidade (LCID) para o seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="10b33-121">Locale identifier (LCID) for your application.</span></span> <span data-ttu-id="10b33-122">A primeira sequência de valor identifica uma chave sub-recurso de `HKLM\Software` e valores de cadeia de caracteres subsequentes identificam os valores do registro sob essa chave que contêm informações de localidade.</span><span class="sxs-lookup"><span data-stu-id="10b33-122">The first string value identifies a sub-key from  `HKLM\Software` and subsequent string values identify registry values underneath this key that contain locale information.</span></span>  <br/> |
   |<span data-ttu-id="10b33-123">MSIOfficeLCID</span><span class="sxs-lookup"><span data-stu-id="10b33-123">MSIOfficeLCID</span></span>  <br/> |<span data-ttu-id="10b33-124">LCIDs para Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="10b33-124">LCIDs for Microsoft Office.</span></span> <span data-ttu-id="10b33-125">A primeira sequência de valor identifica uma chave sub-recurso de `HKLM\Software` e valores de cadeia de caracteres subsequentes identificam valores sob essa chave de registro.</span><span class="sxs-lookup"><span data-stu-id="10b33-125">The first string value identifies a sub-key from  `HKLM\Software` and subsequent string values identify registry values underneath this key.</span></span>  <br/> |
   
   <span data-ttu-id="10b33-126">Obter as informações dessas chaves.</span><span class="sxs-lookup"><span data-stu-id="10b33-126">Obtain the information from these keys.</span></span>
    
2. <span data-ttu-id="10b33-127">Passe os valores que você obteve da etapa anterior para a função [FGetComponentPath](fgetcomponentpath.md) .</span><span class="sxs-lookup"><span data-stu-id="10b33-127">Pass the values that you obtained from the previous step to the [FGetComponentPath](fgetcomponentpath.md) function.</span></span> <span data-ttu-id="10b33-128">**FGetComponentPath** é uma função que é exportada pela biblioteca de stub MAPI Mapistub.</span><span class="sxs-lookup"><span data-stu-id="10b33-128">**FGetComponentPath** is a function that is exported by the MAPI stub library Mapistub.dll.</span></span> <span data-ttu-id="10b33-129">Ele retorna o caminho da versão personalizada de MAPI.</span><span class="sxs-lookup"><span data-stu-id="10b33-129">It returns the path of the custom version of MAPI.</span></span> 


### <a name="to-load-the-implementation-of-mapi-marked-as-default"></a><span data-ttu-id="10b33-130">Para carregar a implementação do MAPI marcado como padrão</span><span class="sxs-lookup"><span data-stu-id="10b33-130">To load the implementation of MAPI marked as default</span></span>

1. <span data-ttu-id="10b33-131">Leitura de `HKLM\Software\Clients\Mail::(default)` valor do registro.</span><span class="sxs-lookup"><span data-stu-id="10b33-131">Read the  `HKLM\Software\Clients\Mail::(default)` registry value.</span></span> 
    
2. <span data-ttu-id="10b33-132">Procure as informações para o cliente indicado conforme descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="10b33-132">Look up the information for the indicated client as described earlier.</span></span>
    
> [!NOTE]
> <span data-ttu-id="10b33-133">Observe que o cliente de email padrão não pode implementar o MAPI estendido.</span><span class="sxs-lookup"><span data-stu-id="10b33-133">Note that the default mail client might not implement Extended MAPI.</span></span> 
  
#### <a name="example"></a><span data-ttu-id="10b33-134">Example</span><span class="sxs-lookup"><span data-stu-id="10b33-134">Example</span></span>

<span data-ttu-id="10b33-135">Para carregar MAPI conforme implementado pelo Outlook, procure as chaves do registro em `HKLM\Software\Clients\Mail\Microsoft Outlook` e passá-las para **FGetComponentPath**.</span><span class="sxs-lookup"><span data-stu-id="10b33-135">To load MAPI as implemented by Outlook, look up the registry keys under  `HKLM\Software\Clients\Mail\Microsoft Outlook` and pass them to **FGetComponentPath**.</span></span> <span data-ttu-id="10b33-136">**FGetComponentPath** retornará o caminho para a implementação do Outlook de MAPI.</span><span class="sxs-lookup"><span data-stu-id="10b33-136">**FGetComponentPath** will return the path for Outlook's implementation of MAPI.</span></span> 
  
<span data-ttu-id="10b33-137">Se as teclas **MSIComponentID**, **MSIApplicationLCID**e **MSIOfficeLCID** não estiver definidas, verifique o valor de registro **DLLPathEx** .</span><span class="sxs-lookup"><span data-stu-id="10b33-137">If the keys **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID** are not set, check the **DLLPathEx** registry value.</span></span> <span data-ttu-id="10b33-138">Se as teclas estiverem definidas, **FGetComponentPath** oferece o caminho da implementação do cliente de MAPI.</span><span class="sxs-lookup"><span data-stu-id="10b33-138">If the keys are set, **FGetComponentPath** gives the path of the client's implementation of MAPI.</span></span> 
  
## <a name="implementing-the-mapi-client-lookup-algorithm"></a><span data-ttu-id="10b33-139">Implementando o algoritmo de pesquisa de cliente MAPI</span><span class="sxs-lookup"><span data-stu-id="10b33-139">Implementing the MAPI Client Lookup algorithm</span></span>

<span data-ttu-id="10b33-140">A tabela a seguir lista as quatro funções de MFCMAPI que são usadas para procurar o caminho para uma implementação personalizada de MAPI:</span><span class="sxs-lookup"><span data-stu-id="10b33-140">The following table lists the four functions from MFCMAPI that are used to look up the path for a custom implementation of MAPI:</span></span>
  
|<span data-ttu-id="10b33-141">**Função**</span><span class="sxs-lookup"><span data-stu-id="10b33-141">**Function**</span></span>|<span data-ttu-id="10b33-142">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="10b33-142">**Description**</span></span>|
|:-----|:-----|
| `GetMAPIPath` <br/> |<span data-ttu-id="10b33-143">Obtém o caminho da biblioteca MAPI.</span><span class="sxs-lookup"><span data-stu-id="10b33-143">Gets the MAPI library path.</span></span>  <br/> |
| `GetMailKey` <br/> |<span data-ttu-id="10b33-144">Obtém a chave de registro de email MAPI.</span><span class="sxs-lookup"><span data-stu-id="10b33-144">Gets the MAPI mail registry key.</span></span>  <br/> |
| `GetMapiMsiIds` <br/> |<span data-ttu-id="10b33-145">Obtém o identificador do Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="10b33-145">Gets the Windows Installer identifier.</span></span>  <br/> |
| `GetComponentPath` <br/> |<span data-ttu-id="10b33-146">Obtém o caminho de componente usando [FGetComponentPath](fgetcomponentpath.md).</span><span class="sxs-lookup"><span data-stu-id="10b33-146">Gets the component path using [FGetComponentPath](fgetcomponentpath.md).</span></span>  <br/> |
   
<span data-ttu-id="10b33-147">Porque MFCMAPI carrega a implementação de padrão de MAPI por padrão, se você quiser usar uma implementação diferente de MAPI, você deve explicitamente direcionar para fazê-lo.</span><span class="sxs-lookup"><span data-stu-id="10b33-147">Because MFCMAPI loads the default implementation of MAPI by default, if you want to use a different implementation of MAPI, you must explicitly direct it to do so.</span></span> <span data-ttu-id="10b33-148">Isso é feito usando-se a rotina **Session\Load MAPI** .</span><span class="sxs-lookup"><span data-stu-id="10b33-148">This is performed by using the **Session\Load MAPI** routine.</span></span> 
  
### <a name="how-these-functions-work"></a><span data-ttu-id="10b33-149">Como essas funções funcionam</span><span class="sxs-lookup"><span data-stu-id="10b33-149">How these functions work</span></span>

1. <span data-ttu-id="10b33-150">MFCMAPI chamadas `GetMAPIPath`, passar nulo para o parâmetro do cliente, a implementação de MAPI padrão de carga.</span><span class="sxs-lookup"><span data-stu-id="10b33-150">MFCMAPI calls  `GetMAPIPath`, passing NULL for the client parameter, to load the default MAPI implementation.</span></span>
    
2.  <span data-ttu-id="10b33-151">`GetMAPIPath`chamadas `GetMapiMsiIds` ler os valores para **MSIComponentID**, **MSIApplicationLCID**e **MSIOfficeLCID**.</span><span class="sxs-lookup"><span data-stu-id="10b33-151">`GetMAPIPath` calls  `GetMapiMsiIds` to read the values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**.</span></span>
    
3.  <span data-ttu-id="10b33-152">`GetMapiMsiIds`chamadas `GetMailKey` para abrir a chave do registro para o cliente de email padrão.</span><span class="sxs-lookup"><span data-stu-id="10b33-152">`GetMapiMsiIds` calls  `GetMailKey` to open the registry key for the default mail client.</span></span> 
    
4.  <span data-ttu-id="10b33-153">`GetMapiMsiIds`usa o identificador do registro retornado por `GetMailKey` pesquise valores para **MSIComponentID**, **MSIApplicationLCID**e **MSIOfficeLCID**.</span><span class="sxs-lookup"><span data-stu-id="10b33-153">`GetMapiMsiIds` uses the registry handle returned by  `GetMailKey` to look up values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**.</span></span>
    
5. <span data-ttu-id="10b33-154">Os valores para **MSIComponentID**, **MSIApplicationLCID**e **MSIOfficeLCID**, são retornados para `GetMAPIPath`.</span><span class="sxs-lookup"><span data-stu-id="10b33-154">The values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**, are returned to  `GetMAPIPath`.</span></span>  <span data-ttu-id="10b33-155">`GetMAPIPath`em seguida, passa-los para `GetComponentPath`.</span><span class="sxs-lookup"><span data-stu-id="10b33-155">`GetMAPIPath` then passes them to  `GetComponentPath`.</span></span>
    
6.  <span data-ttu-id="10b33-156">`GetComponentPath`carrega a biblioteca de stub MAPI, Mapi32, do diretório do sistema.</span><span class="sxs-lookup"><span data-stu-id="10b33-156">`GetComponentPath` loads the MAPI stub library, Mapi32.dll, from the system directory.</span></span> 
    
7.  <span data-ttu-id="10b33-157">`GetComponentPath`em seguida, recupera o endereço da função **FGetComponentPath** do Mapi32, supondo que o Mapi32 exporta **FGetComponentPath**.</span><span class="sxs-lookup"><span data-stu-id="10b33-157">`GetComponentPath` then retrieves the address of the **FGetComponentPath** function from Mapi32.dll, assuming that Mapi32.dll exports **FGetComponentPath**.</span></span>
    
8. <span data-ttu-id="10b33-158">Se obter o endereço do **FGetComponentPath** do MAPI32 falhar, `GetComponentPath` recupera o endereço de Mapistub.</span><span class="sxs-lookup"><span data-stu-id="10b33-158">If getting the address of **FGetComponentPath** from Mapi32.dll fails,  `GetComponentPath` retrieves the address from Mapistub.dll.</span></span> 
    
9.  <span data-ttu-id="10b33-159">`GetComponentPath`em seguida, chama-se **FGetComponentPath**, obtendo o caminho da versão padrão do MAPI.</span><span class="sxs-lookup"><span data-stu-id="10b33-159">`GetComponentPath` then calls **FGetComponentPath**, obtaining the path of the default version of MAPI.</span></span>
    
10.  <span data-ttu-id="10b33-160">`GetMAPIPath`em seguida, retorna este caminho ao chamador, que carrega MAPI e vincula explicitamente a ele, conforme descrito no [Link para funções de MAPI](how-to-link-to-mapi-functions.md).</span><span class="sxs-lookup"><span data-stu-id="10b33-160">`GetMAPIPath` then returns this path to the caller, which then loads MAPI and explicitly links to it as described in [Link to MAPI Functions](how-to-link-to-mapi-functions.md).</span></span>
    
> [!NOTE] 
> - <span data-ttu-id="10b33-161">Para oferecer suporte a cópias localizadas de MAPI para inglês e localidades diferentes do inglês, `GetMAPIPath` lê os valores para as subchaves **MSIApplicationLCID** e **MSIOfficeLCID** .</span><span class="sxs-lookup"><span data-stu-id="10b33-161">To support localized copies of MAPI for English and non-English locales,  `GetMAPIPath` reads the values for the **MSIApplicationLCID** and **MSIOfficeLCID** subkeys.</span></span>  <span data-ttu-id="10b33-162">`GetMAPIPath`em seguida, chama-se **FGetComponentPath**, primeiro especificando **MSIApplicationLCID** como **szQualifier**e novamente, especificando **MSIOfficeLCID** como **szQualifier**.</span><span class="sxs-lookup"><span data-stu-id="10b33-162">`GetMAPIPath` then calls **FGetComponentPath**, first specifying **MSIApplicationLCID** as **szQualifier**, and again specifying **MSIOfficeLCID** as **szQualifier**.</span></span> <span data-ttu-id="10b33-163">Para obter mais informações sobre as chaves do registro para clientes de email que oferecem suporte a idiomas diferentes do inglês, consulte [Configuração de backup das MSI chaves para sua DLL de MAPI](http://msdn.microsoft.com/en-us/library/ee909494%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="10b33-163">For more information about registry keys for mail clients that support non-English languages, see [Setting Up the MSI Keys for Your MAPI DLL](http://msdn.microsoft.com/en-us/library/ee909494%28VS.85%29.aspx).</span></span>   
> - <span data-ttu-id="10b33-164">Se MFCMAPI não recebe um caminho para o uso de MAPI `GetMAPIPath`, ele carrega a biblioteca de stub MAPI do diretório do sistema.</span><span class="sxs-lookup"><span data-stu-id="10b33-164">If MFCMAPI does not receive a path for MAPI using  `GetMAPIPath`, it loads the MAPI stub library from the system directory.</span></span>
> - <span data-ttu-id="10b33-165">O valor de registro **MSMapiApps** discutido no [Mapeamento explicitamente as chamadas de MAPI para DLLs MAPI](http://msdn.microsoft.com/en-us/library/ee909490%28VS.85%29.aspx) só se aplica quando a biblioteca MAPI Stub é usada.</span><span class="sxs-lookup"><span data-stu-id="10b33-165">The **MSMapiApps** registry value discussed in [Explicitly Mapping MAPI Calls to MAPI DLLs](http://msdn.microsoft.com/en-us/library/ee909490%28VS.85%29.aspx) only applies when the MAPI Stub library is used.</span></span> <span data-ttu-id="10b33-166">Aplicativos que carregar uma implementação específica de MAPI ou a implementação de padrão de carga não precisará definir a chave de registro **MSMapiApps** .</span><span class="sxs-lookup"><span data-stu-id="10b33-166">Applications that load a specific implementation of MAPI or load the default implementation do not have to set the **MSMapiApps** registry key.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="10b33-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="10b33-167">See also</span></span>

- [<span data-ttu-id="10b33-168">FGetComponentPath</span><span class="sxs-lookup"><span data-stu-id="10b33-168">FGetComponentPath</span></span>](fgetcomponentpath.md)
- [<span data-ttu-id="10b33-169">Vis�o geral da programa��o MAPI</span><span class="sxs-lookup"><span data-stu-id="10b33-169">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
- [<span data-ttu-id="10b33-170">Link para funções MAPI</span><span class="sxs-lookup"><span data-stu-id="10b33-170">Link to MAPI Functions</span></span>](how-to-link-to-mapi-functions.md)
- [<span data-ttu-id="10b33-171">Configurações de registro de Stub Mapi32</span><span class="sxs-lookup"><span data-stu-id="10b33-171">Mapi32.dll Stub Registry Settings</span></span>](http://msdn.microsoft.com/en-us/library/ms531218%28EXCHG.10%29.aspx)
- [<span data-ttu-id="10b33-172">Configurando as chaves MSI para sua DLL MAPI</span><span class="sxs-lookup"><span data-stu-id="10b33-172">Setting Up the MSI Keys for Your MAPI DLL</span></span>](http://msdn.microsoft.com/en-us/library/ee909494%28VS.85%29.aspx)
- [<span data-ttu-id="10b33-173">Mapeando explicitamente chamadas MAPI para DLLs MAPI</span><span class="sxs-lookup"><span data-stu-id="10b33-173">Explicitly Mapping MAPI Calls to MAPI DLLs</span></span>](http://msdn.microsoft.com/en-us/library/ee909490%28VS.85%29.aspx)

