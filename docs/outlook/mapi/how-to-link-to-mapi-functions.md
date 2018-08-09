---
title: Link para funções MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be72a893-a3bc-4dea-8234-47f3e1db4515
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: db5ce6576da6f925093ae413c5c5124b2a1a996f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766732"
---
# <a name="link-to-mapi-functions"></a><span data-ttu-id="f962b-103">Link para funções MAPI</span><span class="sxs-lookup"><span data-stu-id="f962b-103">Link to MAPI functions</span></span>

<span data-ttu-id="f962b-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f962b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f962b-105">Existem três métodos de vínculo: vinculação implícita, explícita de vinculação e um novo modelo de híbrida usando a biblioteca de Stub de MAPI.</span><span class="sxs-lookup"><span data-stu-id="f962b-105">There are three methods of linking: implicit linking, explicit linking, and a new hybrid model using the MAPI Stub Library.</span></span>
  
## <a name="implicit-linking"></a><span data-ttu-id="f962b-106">Vinculação de implícitas</span><span class="sxs-lookup"><span data-stu-id="f962b-106">Implicit linking</span></span>

<span data-ttu-id="f962b-107">Historicamente, chamar funções de MAPI em um aplicativo de mensagens sempre envolvida vinculação à biblioteca Mapi32.lib.</span><span class="sxs-lookup"><span data-stu-id="f962b-107">Historically, calling MAPI functions in a messaging application always involved linking to the Mapi32.lib library.</span></span> <span data-ttu-id="f962b-108">Isso incluiu o roteamento de chamadas MAPI para a biblioteca de stub MAPI do Windows, Mapi32, que então encaminhados as chamadas feitas na implementação de cliente MAPI padrão em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="f962b-108">This included routing MAPI calls to the Windows MAPI stub library, Mapi32.dll, which then forwarded the calls to the default MAPI client implementation at run time.</span></span> <span data-ttu-id="f962b-109">Esse processo de chamada é conhecido como vinculação implícita.</span><span class="sxs-lookup"><span data-stu-id="f962b-109">This call process is known as implicit linking.</span></span> <span data-ttu-id="f962b-110">O lado esquerdo da figura a seguir mostra um exemplo de vinculação implícita usado em um processo de chamada de função MAPI.</span><span class="sxs-lookup"><span data-stu-id="f962b-110">The left side of the following figure shows an example of implicit linking used in a MAPI function call process.</span></span> <span data-ttu-id="f962b-111">O processo é iniciado por um aplicativo de MAPI e envolve a biblioteca MAPI (Mapi32.lib) e o fragmento de código do MAPI do Windows (Mapi32) e é concluído pela implementação cliente MAPI do Outlook do fragmento de código do MAPI (Msmapi32).</span><span class="sxs-lookup"><span data-stu-id="f962b-111">The process is initiated by a MAPI application and involves the MAPI library (Mapi32.lib) and the Windows MAPI stub (Mapi32.dll) and is completed by the Outlook MAPI client implementation of the MAPI stub (Msmapi32.dll).</span></span>
  
<span data-ttu-id="f962b-112">**Comparação de vinculação implícitas e explícitas.**</span><span class="sxs-lookup"><span data-stu-id="f962b-112">**Comparison of implicit and explicit linking.**</span></span>

<span data-ttu-id="f962b-113">![Comparação de vínculo implícitas e explícitas] (media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "Comparação de vínculo implícitas e explícitas")</span><span class="sxs-lookup"><span data-stu-id="f962b-113">![Comparison of implicit and explicit linking](media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "Comparison of implicit and explicit linking")</span></span>
  
## <a name="explicit-linking"></a><span data-ttu-id="f962b-114">Explicit vinculação</span><span class="sxs-lookup"><span data-stu-id="f962b-114">Explicit linking</span></span>

<span data-ttu-id="f962b-115">Como o cliente MAPI padrão oferece suporte a instalação sob demanda usando o Windows Installer (MSI), você pode desenvolver aplicativos de mensagens diretamente no stub MAPI do Outlook em vez de usar a biblioteca MAPI e stub MAPI do Windows.</span><span class="sxs-lookup"><span data-stu-id="f962b-115">Because the default MAPI client supports on-demand installation using the Windows Installer (MSI), you can develop messaging applications directly on the Outlook MAPI stub instead of using the MAPI library and Windows MAPI stub.</span></span> <span data-ttu-id="f962b-116">Lado direito da figura anterior mostra um exemplo de um processo de chamada de função MAPI, começando com um aplicativo de MAPI procurando o caminho e o nome da DLL para o fragmento de código do MAPI do Outlook (etapa 2 da seção a seguir) e fazer chamadas de função em (de stub o MAPI do Outlook Etapa 3 na seção a seguir).</span><span class="sxs-lookup"><span data-stu-id="f962b-116">The right side of the previous figure shows an example of a MAPI function call process, starting with a MAPI application looking for the path and DLL name for the Outlook MAPI stub (step 2 in the following section), and making function calls into the Outlook MAPI stub (step 3 in the following section).</span></span> <span data-ttu-id="f962b-117">O procedimento a seguir mostra como chamar funções MAPI usando vinculação explícitas.</span><span class="sxs-lookup"><span data-stu-id="f962b-117">The following procedure shows how to call MAPI functions by using explicit linking.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f962b-118">Essas informações sobre a vinculação de explícitas podem ser supérfluas às suas necessidades com a introdução do MAPIStubLibrary.lib discutido na próxima seção.</span><span class="sxs-lookup"><span data-stu-id="f962b-118">This information about explicit linking may be superfluous to your needs with the introduction of the MAPIStubLibrary.lib discussed in the following section.</span></span> <span data-ttu-id="f962b-119">Como o modelo implícito, a nova biblioteca gerencia tudo e implementa a lógica de vinculação explícita que é carregado do Outlook MAPI diretamente.</span><span class="sxs-lookup"><span data-stu-id="f962b-119">Like the implicit model, the new library manages everything and implements the explicit linking logic that loads Outlook's MAPI directly.</span></span> 
  
<span data-ttu-id="f962b-120">Para obter mais informações sobre a vinculação de maneira explícita, consulte vinculação explicitamente.</span><span class="sxs-lookup"><span data-stu-id="f962b-120">For more information about explicit linking, see Linking Explicitly.</span></span>
  
### <a name="to-call-mapi-api-elements-without-the-mapi-library-and-the-windows-mapi-stub"></a><span data-ttu-id="f962b-121">Para chamar elementos de API de MAPI sem a biblioteca MAPI e o fragmento de código do MAPI do Windows</span><span class="sxs-lookup"><span data-stu-id="f962b-121">To call MAPI API elements without the MAPI library and the Windows MAPI stub</span></span>

1. <span data-ttu-id="f962b-122">Em seu arquivo de programa, crie uma lista global de ponteiros de função para cada elemento da API de MAPI que você está usando.</span><span class="sxs-lookup"><span data-stu-id="f962b-122">In your program file, create a global list of function pointers for each MAPI API element that you are using.</span></span> 
    
   <span data-ttu-id="f962b-123">O exemplo a seguir mostra esta etapa.</span><span class="sxs-lookup"><span data-stu-id="f962b-123">The following example shows this step.</span></span>
    
   ```cpp
    //Global MAPI function pointers
    LPMAPIINITIALIZE pfnMAPIInitialize = NULL;
    LPMAPIUNINITIALIZE pfnMAPIUninitialize = NULL;
   ```

2. <span data-ttu-id="f962b-124">Crie uma função que inicializa funções MAPI para vincular a DLL MAPI do cliente MAPI padrão (por exemplo, Msmapi32 do Microsoft Outlook).</span><span class="sxs-lookup"><span data-stu-id="f962b-124">Create a function that initializes MAPI functions to link to the MAPI DLL of the default MAPI client (for example, Msmapi32.dll of Microsoft Outlook).</span></span> <span data-ttu-id="f962b-125">Nesta função, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f962b-125">In this function, do the following:</span></span> 
    
    1. <span data-ttu-id="f962b-126">Carregar MAPI32. dll do diretório de sistema apropriado.</span><span class="sxs-lookup"><span data-stu-id="f962b-126">Load mapi32.dll from the appropriate system directory.</span></span> 
        
       |||
       |:-----|:-----|
       |<span data-ttu-id="f962b-127">x64 ou x86 nativamente</span><span class="sxs-lookup"><span data-stu-id="f962b-127">x64 or x86 natively</span></span>  <br/> |<span data-ttu-id="f962b-128">**%windir%\system32\mapi32.dll**</span><span class="sxs-lookup"><span data-stu-id="f962b-128">**%windir%\system32\mapi32.dll**</span></span> <br/> |
       |<span data-ttu-id="f962b-129">x86 no modo WoW</span><span class="sxs-lookup"><span data-stu-id="f962b-129">x86 on WoW mode</span></span>  <br/> |<span data-ttu-id="f962b-130">**%windir%\syswow64\mapi32.dll**</span><span class="sxs-lookup"><span data-stu-id="f962b-130">**%windir%\syswow64\mapi32.dll**</span></span> <br/> |
    
    2. <span data-ttu-id="f962b-131">Chame a função [FGetComponentPath](fgetcomponentpath.md) para obter o caminho e o nome da DLL que implementa o subsistema de MAPI.</span><span class="sxs-lookup"><span data-stu-id="f962b-131">Call the [FGetComponentPath](fgetcomponentpath.md) function to get the path and DLL name that implements the MAPI subsystem.</span></span> <span data-ttu-id="f962b-132">Para obter mais informações, consulte [Escolher uma versão específica de MAPI a carga](how-to-choose-a-specific-version-of-mapi-to-load.md).</span><span class="sxs-lookup"><span data-stu-id="f962b-132">For more information, see [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md).</span></span>
        
    3. <span data-ttu-id="f962b-133">Carrega a DLL chamando-se a função LoadLibrary.</span><span class="sxs-lookup"><span data-stu-id="f962b-133">Load the DLL by calling the LoadLibrary function.</span></span> 
        
    4. <span data-ttu-id="f962b-134">Inicialize a matriz de ponteiro de função MAPI chamando a função GetProcAddress.</span><span class="sxs-lookup"><span data-stu-id="f962b-134">Initialize the MAPI function pointer array by calling the GetProcAddress function.</span></span> 
        
    <span data-ttu-id="f962b-135">O exemplo a seguir mostra as etapas anteriores:</span><span class="sxs-lookup"><span data-stu-id="f962b-135">The following example shows the previous steps:</span></span>
        
   ```cpp
    void InitializeMapiFunctions()
    {
    {
        // Get the DLL path and name of the actual MAPI implementation.
        FGetComponentPath(g_szMapiComponentGUID, NULL, szMAPIDLL, MAX_PATH);
        // Load the DLL.
        hMod = LoadLibrary(szMAPIDLL);
        // Initialize MAPI functions.
        pfnMAPIInitialize = GetProcAddress(hMod, "MAPIInitialize");
        pfnMAPIUninitialize = GetProcAddress(hMod, "MAPIUninitialize");
    }
   ```

3. <span data-ttu-id="f962b-136">Finalmente, chame a função que você criou na etapa 2 no seu aplicativo de mensagens antes de fazer chamadas de elementos de API de MAPI.</span><span class="sxs-lookup"><span data-stu-id="f962b-136">Finally, call the function that you created in step 2 in your messaging application before you make calls to MAPI API elements.</span></span> 
    
   > [!CAUTION]
   > <span data-ttu-id="f962b-137">Você deve não inicializar o subsistema de MAPI antes de fechar o seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f962b-137">You must uninitialize the MAPI subsystem before closing your application.</span></span> 
  
   <span data-ttu-id="f962b-138">O exemplo a seguir mostra esta etapa:</span><span class="sxs-lookup"><span data-stu-id="f962b-138">The following example shows this step:</span></span> 
    
   ```cpp
    int main()
    {
        HRESULT hr;
        InitializeMapiFunctions();
        // Initialize the MAPI subsystem.
        hr = (*pfnMAPIInitialize)(NULL);
        if (hr!= S_OK)
        {
            // Handle the error case.
        }
        // Here is where you make calls to other MAPI interfaces.
        // Uninitialize the MAPI subsystem.
        (*pfnMAPIUninitialize)();
    return (0);
    }
   ```

## <a name="mapistublibrarylib"></a><span data-ttu-id="f962b-139">MAPIStubLibrary.lib</span><span class="sxs-lookup"><span data-stu-id="f962b-139">MAPIStubLibrary.lib</span></span>

<span data-ttu-id="f962b-140">O advento do Microsoft Outlook 2010 e 64-bit MAPI, estendendo agora para o Microsoft Outlook 2013, exige mais do que a API de 32 bits tradicional para implementação completa.</span><span class="sxs-lookup"><span data-stu-id="f962b-140">The advent of Microsoft Outlook 2010 and 64-bit MAPI, now extending to the Microsoft Outlook 2013, requires more than the traditional 32-bit API for full implementation.</span></span> <span data-ttu-id="f962b-141">Um novo projeto, a biblioteca Stub MAPI, postado no site do CodePlex fornece uma substituição para soltar para Mapi32.lib que ofereça suporte a criação de aplicativos de MAPI de 32 bits e 64 bits.</span><span class="sxs-lookup"><span data-stu-id="f962b-141">A new project, the MAPI Stub Library, posted on the CodePlex website provides a drop-in replacement for Mapi32.lib that supports building both 32-bit and 64-bit MAPI applications.</span></span> <span data-ttu-id="f962b-142">MAPIStubLibrary.lib elimina a necessidade para vincular explicitamente a MAPI e ele ter que ser construído, você pode remover Mapi32.lib de suas configurações de vinculador, substituindo-MAPIStubLibrary.lib; Nenhum mais modificações para o seu código seja necessária.</span><span class="sxs-lookup"><span data-stu-id="f962b-142">MAPIStubLibrary.lib eliminates the need to explicitly link to MAPI, and having built it, you can remove Mapi32.lib from your linker settings, replacing it with MAPIStubLibrary.lib; no further modifications to your code should be needed.</span></span> <span data-ttu-id="f962b-143">Ele também elimina a necessidade de escrever código **LoadLibrary**e **GetProcAddress** **FreeLibrary** para lidar com mais recentes exportações incluídas neste arquivo de biblioteca, mas não no Mapi32.lib, qual seria necessário se você tiver usado a vinculação explícitas.</span><span class="sxs-lookup"><span data-stu-id="f962b-143">It also eliminates the need to write **LoadLibrary**, **GetProcAddress**, and **FreeLibrary** code to handle newer exports included in this library file but not in Mapi32.lib, which would be needed if you used explicit linking.</span></span> 
  
<span data-ttu-id="f962b-144">Algumas das novas funções vinculadas a partir desta biblioteca que não estão disponíveis no Mapi32.lib incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f962b-144">Some of the new functions linked from this library that are not available in Mapi32.lib include the following:</span></span>
  
- [<span data-ttu-id="f962b-145">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="f962b-145">GetDefCachedMode</span></span>](getdefcachedmode.md)    
- [<span data-ttu-id="f962b-146">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="f962b-146">HrGetGALFromEmsmdbUID</span></span>](hrgetgalfromemsmdbuid.md)   
- [<span data-ttu-id="f962b-147">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="f962b-147">HrOpenOfflineObj</span></span>](hropenofflineobj.md)    
- [<span data-ttu-id="f962b-148">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="f962b-148">MAPICrashRecovery</span></span>](mapicrashrecovery.md)   
- [<span data-ttu-id="f962b-149">OpenStreamOnFileW</span><span class="sxs-lookup"><span data-stu-id="f962b-149">OpenStreamOnFileW</span></span>](openstreamonfilew.md)    
- [<span data-ttu-id="f962b-150">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="f962b-150">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)
    
<span data-ttu-id="f962b-151">Um método alternativo de incorporar a biblioteca de Stub MAPI é copiar os arquivos de origem, MapiStubLibrary.cpp e StubUtils.cpp, diretamente em seu projeto e remover qualquer vinculação com Mapi32.lib e qualquer código que explicitamente vincula a MAPI.</span><span class="sxs-lookup"><span data-stu-id="f962b-151">An alternate method of incorporating the MAPI Stub Library is to copy the source files, MapiStubLibrary.cpp and StubUtils.cpp, directly into your project and remove any linkage to Mapi32.lib and any code that explicitly links to MAPI.</span></span>
  
<span data-ttu-id="f962b-152">Para acessar os arquivos da biblioteca de Stub MAPI e para obter informações sobre como criar e integrá-lo em seu projeto, bem como dúvidas sobre esta biblioteca como quando e por que usá-lo, consulte a [Biblioteca de Stub MAPI](http://mapistublibrary.codeplex.com/documentation) no site do CodePlex.</span><span class="sxs-lookup"><span data-stu-id="f962b-152">To access the MAPI Stub Library files and for information about how to build and integrate it into your project, as well as questions about this library such as when and why to use it, see the [MAPI Stub Library](http://mapistublibrary.codeplex.com/documentation) on the CodePlex site.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f962b-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="f962b-153">See also</span></span>

- [<span data-ttu-id="f962b-154">Vis�o geral da programa��o MAPI</span><span class="sxs-lookup"><span data-stu-id="f962b-154">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
- [<span data-ttu-id="f962b-155">Instalar o subsistema MAPI</span><span class="sxs-lookup"><span data-stu-id="f962b-155">Installing the MAPI Subsystem</span></span>](installing-the-mapi-subsystem.md)
- [<span data-ttu-id="f962b-156">Instalar arquivos de cabeçalho MAPI</span><span class="sxs-lookup"><span data-stu-id="f962b-156">Install MAPI Header Files</span></span>](how-to-install-mapi-header-files.md)
- [<span data-ttu-id="f962b-157">Escolher uma versão MAPI específica para carregar</span><span class="sxs-lookup"><span data-stu-id="f962b-157">Choose a Specific Version of MAPI to Load</span></span>](how-to-choose-a-specific-version-of-mapi-to-load.md)
- [<span data-ttu-id="f962b-158">Determinando qual método vinculação de uso</span><span class="sxs-lookup"><span data-stu-id="f962b-158">Determining Which Linking Method to Use</span></span>](http://msdn.microsoft.com/en-us/library/253b8k2c.aspx)
- [<span data-ttu-id="f962b-159">Vinculando um arquivo executável para uma DLL</span><span class="sxs-lookup"><span data-stu-id="f962b-159">Linking an Executable to a DLL</span></span>](http://msdn.microsoft.com/en-us/library/9yd93633.aspx)
- [<span data-ttu-id="f962b-160">Configurando as chaves MSI para sua DLL MAPI</span><span class="sxs-lookup"><span data-stu-id="f962b-160">Setting Up the MSI Keys for Your MAPI DLL</span></span>](http://msdn.microsoft.com/en-us/library/ee909494%28v=VS.85%29.aspx)

