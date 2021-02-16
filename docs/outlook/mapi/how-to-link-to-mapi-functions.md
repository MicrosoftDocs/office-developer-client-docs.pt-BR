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
ms.openlocfilehash: 71108da8bb9914bb7ed0ad0b3adacc24e1d69e63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346877"
---
# <a name="link-to-mapi-functions"></a><span data-ttu-id="9b1a3-103">Link para funções MAPI</span><span class="sxs-lookup"><span data-stu-id="9b1a3-103">Link to MAPI functions</span></span>

<span data-ttu-id="9b1a3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b1a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b1a3-105">Há três métodos de vinculação: vinculação implícita, vinculação explícita e um novo modelo híbrido usando a Biblioteca de Stub MAPI.</span><span class="sxs-lookup"><span data-stu-id="9b1a3-105">There are three methods of linking: implicit linking, explicit linking, and a new hybrid model using the MAPI Stub Library.</span></span>
  
## <a name="implicit-linking"></a><span data-ttu-id="9b1a3-106">Vinculação implícita</span><span class="sxs-lookup"><span data-stu-id="9b1a3-106">Implicit linking</span></span>

<span data-ttu-id="9b1a3-107">Historicamente, chamar funções MAPI em um aplicativo de mensagens sempre envolvia a vinculação à biblioteca Mapi32.lib.</span><span class="sxs-lookup"><span data-stu-id="9b1a3-107">Historically, calling MAPI functions in a messaging application always involved linking to the Mapi32.lib library.</span></span> <span data-ttu-id="9b1a3-108">Isso incluiu o roteamento de chamadas MAPI para a biblioteca de stub mapi do Windows, Mapi32.dll, que encaminhou as chamadas para a implementação de cliente MAPI padrão em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="9b1a3-108">This included routing MAPI calls to the Windows MAPI stub library, Mapi32.dll, which then forwarded the calls to the default MAPI client implementation at run time.</span></span> <span data-ttu-id="9b1a3-109">Esse processo de chamada é conhecido como vinculação implícita.</span><span class="sxs-lookup"><span data-stu-id="9b1a3-109">This call process is known as implicit linking.</span></span> <span data-ttu-id="9b1a3-110">O lado esquerdo da figura a seguir mostra um exemplo de vinculação implícita usada em um processo de chamada de função MAPI.</span><span class="sxs-lookup"><span data-stu-id="9b1a3-110">The left side of the following figure shows an example of implicit linking used in a MAPI function call process.</span></span> <span data-ttu-id="9b1a3-111">O processo é iniciado por um aplicativo MAPI e envolve a biblioteca MAPI (Mapi32.lib) e o stub de MAPI do Windows (Mapi32.dll) e é concluído pela implementação do cliente MAPI do Outlook do stub (Msmapi32.dll).</span><span class="sxs-lookup"><span data-stu-id="9b1a3-111">The process is initiated by a MAPI application and involves the MAPI library (Mapi32.lib) and the Windows MAPI stub (Mapi32.dll) and is completed by the Outlook MAPI client implementation of the MAPI stub (Msmapi32.dll).</span></span>
  
<span data-ttu-id="9b1a3-112">**Comparação de vinculação implícita e explícita.**</span><span class="sxs-lookup"><span data-stu-id="9b1a3-112">**Comparison of implicit and explicit linking.**</span></span>

<span data-ttu-id="9b1a3-113">![Comparação de vinculação implícita e explícita](media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "Comparação de vinculação implícita e explícita")</span><span class="sxs-lookup"><span data-stu-id="9b1a3-113">![Comparison of implicit and explicit linking](media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "Comparison of implicit and explicit linking")</span></span>
  
## <a name="explicit-linking"></a><span data-ttu-id="9b1a3-114">Vinculação explícita</span><span class="sxs-lookup"><span data-stu-id="9b1a3-114">Explicit linking</span></span>

<span data-ttu-id="9b1a3-115">Como o cliente MAPI padrão dá suporte à instalação sob demanda usando o Windows Installer (MSI), você pode desenvolver aplicativos de mensagens diretamente no stub MAPI do Outlook em vez de usar a biblioteca MAPI e o stub de MAPI do Windows.</span><span class="sxs-lookup"><span data-stu-id="9b1a3-115">Because the default MAPI client supports on-demand installation using the Windows Installer (MSI), you can develop messaging applications directly on the Outlook MAPI stub instead of using the MAPI library and Windows MAPI stub.</span></span> <span data-ttu-id="9b1a3-116">O lado direito da figura anterior mostra um exemplo de um processo de chamada de função MAPI, começando com um aplicativo MAPI procurando o caminho e o nome DLL para o stub MAPI do Outlook (etapa 2 na seção a seguir) e fazendo chamadas de função para o stub MAPI do Outlook (etapa 3 na seção a seguir).</span><span class="sxs-lookup"><span data-stu-id="9b1a3-116">The right side of the previous figure shows an example of a MAPI function call process, starting with a MAPI application looking for the path and DLL name for the Outlook MAPI stub (step 2 in the following section), and making function calls into the Outlook MAPI stub (step 3 in the following section).</span></span> <span data-ttu-id="9b1a3-117">O procedimento a seguir mostra como chamar funções MAPI usando vinculação explícita.</span><span class="sxs-lookup"><span data-stu-id="9b1a3-117">The following procedure shows how to call MAPI functions by using explicit linking.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9b1a3-118">Essas informações sobre vinculação explícita podem ser supérfluas para suas necessidades com a introdução de MAPIStubLibrary.lib discutida na seção a seguir.</span><span class="sxs-lookup"><span data-stu-id="9b1a3-118">This information about explicit linking may be superfluous to your needs with the introduction of the MAPIStubLibrary.lib discussed in the following section.</span></span> <span data-ttu-id="9b1a3-119">Assim como o modelo implícito, a nova biblioteca gerencia tudo e implementa a lógica de vinculação explícita que carrega diretamente o MAPI do Outlook.</span><span class="sxs-lookup"><span data-stu-id="9b1a3-119">Like the implicit model, the new library manages everything and implements the explicit linking logic that loads Outlook's MAPI directly.</span></span> 
  
<span data-ttu-id="9b1a3-120">Para obter mais informações sobre vinculação explícita, consulte Vinculação Explícita.</span><span class="sxs-lookup"><span data-stu-id="9b1a3-120">For more information about explicit linking, see Linking Explicitly.</span></span>
  
### <a name="to-call-mapi-api-elements-without-the-mapi-library-and-the-windows-mapi-stub"></a><span data-ttu-id="9b1a3-121">Para chamar elementos da API MAPI sem a biblioteca MAPI e o stub MAPI do Windows</span><span class="sxs-lookup"><span data-stu-id="9b1a3-121">To call MAPI API elements without the MAPI library and the Windows MAPI stub</span></span>

1. <span data-ttu-id="9b1a3-122">No arquivo de programa, crie uma lista global de ponteiros de função para cada elemento da API MAPI que você está usando.</span><span class="sxs-lookup"><span data-stu-id="9b1a3-122">In your program file, create a global list of function pointers for each MAPI API element that you are using.</span></span> 
    
   <span data-ttu-id="9b1a3-123">O exemplo a seguir mostra esta etapa.</span><span class="sxs-lookup"><span data-stu-id="9b1a3-123">The following example shows this step.</span></span>
    
   ```cpp
    //Global MAPI function pointers
    LPMAPIINITIALIZE pfnMAPIInitialize = NULL;
    LPMAPIUNINITIALIZE pfnMAPIUninitialize = NULL;
   ```

2. <span data-ttu-id="9b1a3-124">Crie uma função que inicialize funções MAPI para vincular à DLL MAPI do cliente MAPI padrão (por exemplo, Msmapi32.dll do Microsoft Outlook).</span><span class="sxs-lookup"><span data-stu-id="9b1a3-124">Create a function that initializes MAPI functions to link to the MAPI DLL of the default MAPI client (for example, Msmapi32.dll of Microsoft Outlook).</span></span> <span data-ttu-id="9b1a3-125">Nesta função, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="9b1a3-125">In this function, do the following:</span></span> 
    
    1. <span data-ttu-id="9b1a3-126">Carregue mapi32.dll do diretório do sistema apropriado.</span><span class="sxs-lookup"><span data-stu-id="9b1a3-126">Load mapi32.dll from the appropriate system directory.</span></span> 
        
       |||
       |:-----|:-----|
       |<span data-ttu-id="9b1a3-127">x64 ou x86 de forma nativa</span><span class="sxs-lookup"><span data-stu-id="9b1a3-127">x64 or x86 natively</span></span>  <br/> |<span data-ttu-id="9b1a3-128">**%windir%\system32\mapi32.dll**</span><span class="sxs-lookup"><span data-stu-id="9b1a3-128">**%windir%\system32\mapi32.dll**</span></span> <br/> |
       |<span data-ttu-id="9b1a3-129">x86 no modo WoW</span><span class="sxs-lookup"><span data-stu-id="9b1a3-129">x86 on WoW mode</span></span>  <br/> |<span data-ttu-id="9b1a3-130">**%windir%\syswow64\mapi32.dll**</span><span class="sxs-lookup"><span data-stu-id="9b1a3-130">**%windir%\syswow64\mapi32.dll**</span></span> <br/> |
    
    2. <span data-ttu-id="9b1a3-131">Chame a [função FGetComponentPath](fgetcomponentpath.md) para obter o caminho e o nome da DLL que implementa o subsistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="9b1a3-131">Call the [FGetComponentPath](fgetcomponentpath.md) function to get the path and DLL name that implements the MAPI subsystem.</span></span> <span data-ttu-id="9b1a3-132">Para obter mais informações, [consulte Escolher uma versão específica do MAPI para carregar.](how-to-choose-a-specific-version-of-mapi-to-load.md)</span><span class="sxs-lookup"><span data-stu-id="9b1a3-132">For more information, see [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md).</span></span>
        
    3. <span data-ttu-id="9b1a3-133">Carregue a DLL chamando a função LoadLibrary.</span><span class="sxs-lookup"><span data-stu-id="9b1a3-133">Load the DLL by calling the LoadLibrary function.</span></span> 
        
    4. <span data-ttu-id="9b1a3-134">Inicialize a matriz de ponteiro da função MAPI chamando a função GetProcAddress.</span><span class="sxs-lookup"><span data-stu-id="9b1a3-134">Initialize the MAPI function pointer array by calling the GetProcAddress function.</span></span> 
        
    <span data-ttu-id="9b1a3-135">O exemplo a seguir mostra as etapas anteriores:</span><span class="sxs-lookup"><span data-stu-id="9b1a3-135">The following example shows the previous steps:</span></span>
        
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

3. <span data-ttu-id="9b1a3-136">Por fim, chame a função que você criou na etapa 2 em seu aplicativo de mensagens antes de fazer chamadas aos elementos da API MAPI.</span><span class="sxs-lookup"><span data-stu-id="9b1a3-136">Finally, call the function that you created in step 2 in your messaging application before you make calls to MAPI API elements.</span></span> 
    
   > [!CAUTION]
   > <span data-ttu-id="9b1a3-137">Você deve desincializar o subsistema MAPI antes de fechar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9b1a3-137">You must uninitialize the MAPI subsystem before closing your application.</span></span> 
  
   <span data-ttu-id="9b1a3-138">O exemplo a seguir mostra esta etapa:</span><span class="sxs-lookup"><span data-stu-id="9b1a3-138">The following example shows this step:</span></span> 
    
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

## <a name="mapistublibrarylib"></a><span data-ttu-id="9b1a3-139">MAPIStubLibrary.lib</span><span class="sxs-lookup"><span data-stu-id="9b1a3-139">MAPIStubLibrary.lib</span></span>

<span data-ttu-id="9b1a3-140">O advento do MAPI do Microsoft Outlook 2010 e de 64 bits, agora se estendendo ao Microsoft Outlook 2013, requer mais do que a API tradicional de 32 bits para implementação completa.</span><span class="sxs-lookup"><span data-stu-id="9b1a3-140">The advent of Microsoft Outlook 2010 and 64-bit MAPI, now extending to the Microsoft Outlook 2013, requires more than the traditional 32-bit API for full implementation.</span></span> <span data-ttu-id="9b1a3-141">Um novo projeto, a Biblioteca stub MAPI, postado no site do CodePlex fornece uma substituição de lista para Mapi32.lib que dá suporte à criação de aplicativos MAPI de 32 bits e 64 bits.</span><span class="sxs-lookup"><span data-stu-id="9b1a3-141">A new project, the MAPI Stub Library, posted on the CodePlex website provides a drop-in replacement for Mapi32.lib that supports building both 32-bit and 64-bit MAPI applications.</span></span> <span data-ttu-id="9b1a3-142">MAPIStubLibrary.lib elimina a necessidade de vincular explicitamente ao MAPI e, tendo criado isso, você pode remover Mapi32.lib das configurações do linker, substituindo-o por MAPIStubLibrary.lib; nenhuma outra modificação em seu código deve ser necessária.</span><span class="sxs-lookup"><span data-stu-id="9b1a3-142">MAPIStubLibrary.lib eliminates the need to explicitly link to MAPI, and having built it, you can remove Mapi32.lib from your linker settings, replacing it with MAPIStubLibrary.lib; no further modifications to your code should be needed.</span></span> <span data-ttu-id="9b1a3-143">Ele também elimina a necessidade de escrever o código **LoadLibrary**, **GetProcAddress** e **FreeLibrary** para lidar com exportações mais novas incluídas neste arquivo de biblioteca, mas não em Mapi32.lib, que seria necessário se você tivesse usado a vinculação explícita.</span><span class="sxs-lookup"><span data-stu-id="9b1a3-143">It also eliminates the need to write **LoadLibrary**, **GetProcAddress**, and **FreeLibrary** code to handle newer exports included in this library file but not in Mapi32.lib, which would be needed if you used explicit linking.</span></span> 
  
<span data-ttu-id="9b1a3-144">Algumas das novas funções vinculadas a partir dessa biblioteca que não estão disponíveis em Mapi32.lib incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="9b1a3-144">Some of the new functions linked from this library that are not available in Mapi32.lib include the following:</span></span>
  
- [<span data-ttu-id="9b1a3-145">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="9b1a3-145">GetDefCachedMode</span></span>](getdefcachedmode.md)    
- [<span data-ttu-id="9b1a3-146">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="9b1a3-146">HrGetGALFromEmsmdbUID</span></span>](hrgetgalfromemsmdbuid.md)   
- [<span data-ttu-id="9b1a3-147">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="9b1a3-147">HrOpenOfflineObj</span></span>](hropenofflineobj.md)    
- [<span data-ttu-id="9b1a3-148">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="9b1a3-148">MAPICrashRecovery</span></span>](mapicrashrecovery.md)   
- [<span data-ttu-id="9b1a3-149">OpenStreamOnFileW</span><span class="sxs-lookup"><span data-stu-id="9b1a3-149">OpenStreamOnFileW</span></span>](openstreamonfilew.md)    
- [<span data-ttu-id="9b1a3-150">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="9b1a3-150">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)
    
<span data-ttu-id="9b1a3-151">Um método alternativo de incorporar a Biblioteca stub MAPI é copiar os arquivos de origem, MapiStubLibrary.cpp e StubUtils.cpp, diretamente em seu projeto e remover qualquer vinculação a Mapi32.lib e qualquer código que explicitamente se vincula ao MAPI.</span><span class="sxs-lookup"><span data-stu-id="9b1a3-151">An alternate method of incorporating the MAPI Stub Library is to copy the source files, MapiStubLibrary.cpp and StubUtils.cpp, directly into your project and remove any linkage to Mapi32.lib and any code that explicitly links to MAPI.</span></span>
  
<span data-ttu-id="9b1a3-152">Para acessar os arquivos da Biblioteca de Stub MAPI e obter informações sobre como criar e integrá-la ao seu projeto, bem como perguntas sobre essa biblioteca, como quando e por que usá-la, consulte a Biblioteca [de Stub MAPI](https://mapistublibrary.codeplex.com/documentation) no site CodePlex.</span><span class="sxs-lookup"><span data-stu-id="9b1a3-152">To access the MAPI Stub Library files and for information about how to build and integrate it into your project, as well as questions about this library such as when and why to use it, see the [MAPI Stub Library](https://mapistublibrary.codeplex.com/documentation) on the CodePlex site.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9b1a3-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b1a3-153">See also</span></span>

- [<span data-ttu-id="9b1a3-154">Visão geral da programação MAPI</span><span class="sxs-lookup"><span data-stu-id="9b1a3-154">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
- [<span data-ttu-id="9b1a3-155">Instalar o subsistema MAPI</span><span class="sxs-lookup"><span data-stu-id="9b1a3-155">Installing the MAPI Subsystem</span></span>](installing-the-mapi-subsystem.md)
- [<span data-ttu-id="9b1a3-156">Instalar arquivos de header MAPI</span><span class="sxs-lookup"><span data-stu-id="9b1a3-156">Install MAPI Header Files</span></span>](how-to-install-mapi-header-files.md)
- [<span data-ttu-id="9b1a3-157">Choose a Specific Version of MAPI to Load</span><span class="sxs-lookup"><span data-stu-id="9b1a3-157">Choose a Specific Version of MAPI to Load</span></span>](how-to-choose-a-specific-version-of-mapi-to-load.md)
- [<span data-ttu-id="9b1a3-158">Determinando qual método de vinculação usar</span><span class="sxs-lookup"><span data-stu-id="9b1a3-158">Determining Which Linking Method to Use</span></span>](https://msdn.microsoft.com/library/253b8k2c.aspx)
- [<span data-ttu-id="9b1a3-159">Vinculando um executável a uma DLL</span><span class="sxs-lookup"><span data-stu-id="9b1a3-159">Linking an Executable to a DLL</span></span>](https://msdn.microsoft.com/library/9yd93633.aspx)
- [<span data-ttu-id="9b1a3-160">Configurando as chaves MSI para sua DLL MAPI</span><span class="sxs-lookup"><span data-stu-id="9b1a3-160">Setting Up the MSI Keys for Your MAPI DLL</span></span>](https://msdn.microsoft.com/library/ee909494%28v=VS.85%29.aspx)

