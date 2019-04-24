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
# <a name="link-to-mapi-functions"></a><span data-ttu-id="03c8d-103">Link para funções MAPI</span><span class="sxs-lookup"><span data-stu-id="03c8d-103">Link to MAPI functions</span></span>

<span data-ttu-id="03c8d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03c8d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03c8d-105">Há três métodos de vinculação: vínculo implícito, vínculo explícito e um novo modelo híbrido usando a biblioteca de stub MAPI.</span><span class="sxs-lookup"><span data-stu-id="03c8d-105">There are three methods of linking: implicit linking, explicit linking, and a new hybrid model using the MAPI Stub Library.</span></span>
  
## <a name="implicit-linking"></a><span data-ttu-id="03c8d-106">Vinculação implícita</span><span class="sxs-lookup"><span data-stu-id="03c8d-106">Implicit linking</span></span>

<span data-ttu-id="03c8d-107">Historicamente, chamar funções MAPI em um aplicativo de mensagens sempre envolvia o vínculo com a biblioteca Mapi32. lib.</span><span class="sxs-lookup"><span data-stu-id="03c8d-107">Historically, calling MAPI functions in a messaging application always involved linking to the Mapi32.lib library.</span></span> <span data-ttu-id="03c8d-108">Isso incluiu chamadas de MAPI de roteamento para a biblioteca de stub MAPI do Windows, Mapi32. dll, que, em seguida, encaminharam as chamadas para a implementação de cliente MAPI padrão em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="03c8d-108">This included routing MAPI calls to the Windows MAPI stub library, Mapi32.dll, which then forwarded the calls to the default MAPI client implementation at run time.</span></span> <span data-ttu-id="03c8d-109">Esse processo de chamada é conhecido como vinculação implícita.</span><span class="sxs-lookup"><span data-stu-id="03c8d-109">This call process is known as implicit linking.</span></span> <span data-ttu-id="03c8d-110">O lado esquerdo da figura a seguir mostra um exemplo de vínculo implícito usado em um processo de chamada de função MAPI.</span><span class="sxs-lookup"><span data-stu-id="03c8d-110">The left side of the following figure shows an example of implicit linking used in a MAPI function call process.</span></span> <span data-ttu-id="03c8d-111">O processo é iniciado por um aplicativo MAPI e envolve a biblioteca MAPI (Mapi32. lib) e o stub MAPI do Windows (Mapi32. dll) e é concluído pela implementação do cliente MAPI do Outlook do stub MAPI (Msmapi32. dll).</span><span class="sxs-lookup"><span data-stu-id="03c8d-111">The process is initiated by a MAPI application and involves the MAPI library (Mapi32.lib) and the Windows MAPI stub (Mapi32.dll) and is completed by the Outlook MAPI client implementation of the MAPI stub (Msmapi32.dll).</span></span>
  
<span data-ttu-id="03c8d-112">**Comparação de vínculos implícitos e explícitos.**</span><span class="sxs-lookup"><span data-stu-id="03c8d-112">**Comparison of implicit and explicit linking.**</span></span>

<span data-ttu-id="03c8d-113">![Comparação de vínculos implícitos e explícitos] (media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "Comparação de vínculos implícitos e explícitos")</span><span class="sxs-lookup"><span data-stu-id="03c8d-113">![Comparison of implicit and explicit linking](media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "Comparison of implicit and explicit linking")</span></span>
  
## <a name="explicit-linking"></a><span data-ttu-id="03c8d-114">Vinculação explícita</span><span class="sxs-lookup"><span data-stu-id="03c8d-114">Explicit linking</span></span>

<span data-ttu-id="03c8d-115">Como o cliente MAPI padrão oferece suporte à instalação sob demanda usando o Windows Installer (MSI), você pode desenvolver aplicativos de mensagens diretamente no stub MAPI do Outlook em vez de usar a biblioteca MAPI e o stub MAPI do Windows.</span><span class="sxs-lookup"><span data-stu-id="03c8d-115">Because the default MAPI client supports on-demand installation using the Windows Installer (MSI), you can develop messaging applications directly on the Outlook MAPI stub instead of using the MAPI library and Windows MAPI stub.</span></span> <span data-ttu-id="03c8d-116">O lado direito da figura anterior mostra um exemplo de um processo de chamada de função MAPI, começando com um aplicativo MAPI procurando o caminho e o nome da DLL para o stub MAPI do Outlook (etapa 2 na seção a seguir) e fazendo chamadas de função no stub MAPI do Outlook ( etapa 3 da seção a seguir).</span><span class="sxs-lookup"><span data-stu-id="03c8d-116">The right side of the previous figure shows an example of a MAPI function call process, starting with a MAPI application looking for the path and DLL name for the Outlook MAPI stub (step 2 in the following section), and making function calls into the Outlook MAPI stub (step 3 in the following section).</span></span> <span data-ttu-id="03c8d-117">O procedimento a seguir mostra como chamar funções MAPI usando vinculação explícita.</span><span class="sxs-lookup"><span data-stu-id="03c8d-117">The following procedure shows how to call MAPI functions by using explicit linking.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="03c8d-118">Essas informações sobre vinculação explícita podem ser supérfluas para suas necessidades com a introdução do MAPIStubLibrary. lib abordado na seção a seguir.</span><span class="sxs-lookup"><span data-stu-id="03c8d-118">This information about explicit linking may be superfluous to your needs with the introduction of the MAPIStubLibrary.lib discussed in the following section.</span></span> <span data-ttu-id="03c8d-119">Como o modelo implícito, a nova biblioteca gerencia tudo e implementa a lógica de vinculação explícita que carrega diretamente o MAPI do Outlook.</span><span class="sxs-lookup"><span data-stu-id="03c8d-119">Like the implicit model, the new library manages everything and implements the explicit linking logic that loads Outlook's MAPI directly.</span></span> 
  
<span data-ttu-id="03c8d-120">Para obter mais informações sobre vinculação explícita, consulte vinculação explícita.</span><span class="sxs-lookup"><span data-stu-id="03c8d-120">For more information about explicit linking, see Linking Explicitly.</span></span>
  
### <a name="to-call-mapi-api-elements-without-the-mapi-library-and-the-windows-mapi-stub"></a><span data-ttu-id="03c8d-121">Para chamar elementos de API MAPI sem a biblioteca MAPI e o stub MAPI do Windows</span><span class="sxs-lookup"><span data-stu-id="03c8d-121">To call MAPI API elements without the MAPI library and the Windows MAPI stub</span></span>

1. <span data-ttu-id="03c8d-122">No arquivo de programa, crie uma lista global de ponteiros de função para cada elemento de API MAPI que você estiver usando.</span><span class="sxs-lookup"><span data-stu-id="03c8d-122">In your program file, create a global list of function pointers for each MAPI API element that you are using.</span></span> 
    
   <span data-ttu-id="03c8d-123">O exemplo a seguir mostra esta etapa.</span><span class="sxs-lookup"><span data-stu-id="03c8d-123">The following example shows this step.</span></span>
    
   ```cpp
    //Global MAPI function pointers
    LPMAPIINITIALIZE pfnMAPIInitialize = NULL;
    LPMAPIUNINITIALIZE pfnMAPIUninitialize = NULL;
   ```

2. <span data-ttu-id="03c8d-124">Crie uma função que inicializa funções MAPI para vincular à DLL MAPI do cliente MAPI padrão (por exemplo, Msmapi32. dll do Microsoft Outlook).</span><span class="sxs-lookup"><span data-stu-id="03c8d-124">Create a function that initializes MAPI functions to link to the MAPI DLL of the default MAPI client (for example, Msmapi32.dll of Microsoft Outlook).</span></span> <span data-ttu-id="03c8d-125">Nesta função, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="03c8d-125">In this function, do the following:</span></span> 
    
    1. <span data-ttu-id="03c8d-126">Carregue Mapi32. dll do diretório de sistema adequado.</span><span class="sxs-lookup"><span data-stu-id="03c8d-126">Load mapi32.dll from the appropriate system directory.</span></span> 
        
       |||
       |:-----|:-----|
       |<span data-ttu-id="03c8d-127">x64 ou x86 nativamente</span><span class="sxs-lookup"><span data-stu-id="03c8d-127">x64 or x86 natively</span></span>  <br/> |<span data-ttu-id="03c8d-128">**%WINDIR%\system32\mapi32.dll**</span><span class="sxs-lookup"><span data-stu-id="03c8d-128">**%windir%\system32\mapi32.dll**</span></span> <br/> |
       |<span data-ttu-id="03c8d-129">x86 no modo WoW</span><span class="sxs-lookup"><span data-stu-id="03c8d-129">x86 on WoW mode</span></span>  <br/> |<span data-ttu-id="03c8d-130">**%WINDIR%\syswow64\mapi32.dll**</span><span class="sxs-lookup"><span data-stu-id="03c8d-130">**%windir%\syswow64\mapi32.dll**</span></span> <br/> |
    
    2. <span data-ttu-id="03c8d-131">Chame a função [FGetComponentPath](fgetcomponentpath.md) para obter o caminho e o nome da dll que implementam o subsistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="03c8d-131">Call the [FGetComponentPath](fgetcomponentpath.md) function to get the path and DLL name that implements the MAPI subsystem.</span></span> <span data-ttu-id="03c8d-132">Para obter mais informações, consulte [escolher uma versão específica de MAPI para carregar](how-to-choose-a-specific-version-of-mapi-to-load.md).</span><span class="sxs-lookup"><span data-stu-id="03c8d-132">For more information, see [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md).</span></span>
        
    3. <span data-ttu-id="03c8d-133">Carregue a DLL chamando a função LoadLibrary.</span><span class="sxs-lookup"><span data-stu-id="03c8d-133">Load the DLL by calling the LoadLibrary function.</span></span> 
        
    4. <span data-ttu-id="03c8d-134">Inicialize a matriz de ponteiro de função MAPI chamando a função GetProcAddress.</span><span class="sxs-lookup"><span data-stu-id="03c8d-134">Initialize the MAPI function pointer array by calling the GetProcAddress function.</span></span> 
        
    <span data-ttu-id="03c8d-135">O exemplo a seguir mostra as etapas anteriores:</span><span class="sxs-lookup"><span data-stu-id="03c8d-135">The following example shows the previous steps:</span></span>
        
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

3. <span data-ttu-id="03c8d-136">Por fim, chame a função que você criou na etapa 2 em seu aplicativo de mensagens antes de fazer chamadas para elementos da API MAPI.</span><span class="sxs-lookup"><span data-stu-id="03c8d-136">Finally, call the function that you created in step 2 in your messaging application before you make calls to MAPI API elements.</span></span> 
    
   > [!CAUTION]
   > <span data-ttu-id="03c8d-137">Você deve cancelar a inicialização do subsistema MAPI antes de fechar seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="03c8d-137">You must uninitialize the MAPI subsystem before closing your application.</span></span> 
  
   <span data-ttu-id="03c8d-138">O exemplo a seguir mostra esta etapa:</span><span class="sxs-lookup"><span data-stu-id="03c8d-138">The following example shows this step:</span></span> 
    
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

## <a name="mapistublibrarylib"></a><span data-ttu-id="03c8d-139">MAPIStubLibrary. lib</span><span class="sxs-lookup"><span data-stu-id="03c8d-139">MAPIStubLibrary.lib</span></span>

<span data-ttu-id="03c8d-140">O advento do Microsoft Outlook 2010 e o MAPI de 64 bits, que agora se estende para o Microsoft Outlook 2013, requer mais do que a API tradicional de 32 bits para implementação completa.</span><span class="sxs-lookup"><span data-stu-id="03c8d-140">The advent of Microsoft Outlook 2010 and 64-bit MAPI, now extending to the Microsoft Outlook 2013, requires more than the traditional 32-bit API for full implementation.</span></span> <span data-ttu-id="03c8d-141">Um novo projeto, a biblioteca de stub MAPI, publicado no site CodePlex, fornece uma substituição de redistribuição para Mapi32. lib que oferece suporte à criação de aplicativos MAPI de 32 bits e de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="03c8d-141">A new project, the MAPI Stub Library, posted on the CodePlex website provides a drop-in replacement for Mapi32.lib that supports building both 32-bit and 64-bit MAPI applications.</span></span> <span data-ttu-id="03c8d-142">MAPIStubLibrary. lib elimina a necessidade de vincular explicitamente ao MAPI e de tê-lo criado, você pode remover o Mapi32. lib das configurações do vinculador, substituindo-o por MAPIStubLibrary. lib; Não será necessário fazer mais modificações no código.</span><span class="sxs-lookup"><span data-stu-id="03c8d-142">MAPIStubLibrary.lib eliminates the need to explicitly link to MAPI, and having built it, you can remove Mapi32.lib from your linker settings, replacing it with MAPIStubLibrary.lib; no further modifications to your code should be needed.</span></span> <span data-ttu-id="03c8d-143">Ele também elimina a necessidade de escrever o código **LoadLibrary**, **GetProcAddress**e **FreeLibrary** para lidar com exportações mais recentes incluídas nesse arquivo de biblioteca, mas não em Mapi32. lib, que seriam necessárias se você usava vinculação explícita.</span><span class="sxs-lookup"><span data-stu-id="03c8d-143">It also eliminates the need to write **LoadLibrary**, **GetProcAddress**, and **FreeLibrary** code to handle newer exports included in this library file but not in Mapi32.lib, which would be needed if you used explicit linking.</span></span> 
  
<span data-ttu-id="03c8d-144">Algumas das novas funções vinculadas a essa biblioteca que não estão disponíveis em Mapi32. lib incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="03c8d-144">Some of the new functions linked from this library that are not available in Mapi32.lib include the following:</span></span>
  
- [<span data-ttu-id="03c8d-145">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="03c8d-145">GetDefCachedMode</span></span>](getdefcachedmode.md)    
- [<span data-ttu-id="03c8d-146">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="03c8d-146">HrGetGALFromEmsmdbUID</span></span>](hrgetgalfromemsmdbuid.md)   
- [<span data-ttu-id="03c8d-147">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="03c8d-147">HrOpenOfflineObj</span></span>](hropenofflineobj.md)    
- [<span data-ttu-id="03c8d-148">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="03c8d-148">MAPICrashRecovery</span></span>](mapicrashrecovery.md)   
- [<span data-ttu-id="03c8d-149">OpenStreamOnFileW</span><span class="sxs-lookup"><span data-stu-id="03c8d-149">OpenStreamOnFileW</span></span>](openstreamonfilew.md)    
- [<span data-ttu-id="03c8d-150">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="03c8d-150">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)
    
<span data-ttu-id="03c8d-151">Um método alternativo de incorporação da biblioteca de stub MAPI é copiar os arquivos de origem, MapiStubLibrary. cpp e StubUtils. cpp, diretamente para o seu projeto e remover qualquer vínculo para Mapi32. lib e qualquer código que explicitamente se vincule a MAPI.</span><span class="sxs-lookup"><span data-stu-id="03c8d-151">An alternate method of incorporating the MAPI Stub Library is to copy the source files, MapiStubLibrary.cpp and StubUtils.cpp, directly into your project and remove any linkage to Mapi32.lib and any code that explicitly links to MAPI.</span></span>
  
<span data-ttu-id="03c8d-152">Para acessar os arquivos da biblioteca de stub MAPI e obter informações sobre como criar e integrá-lo ao seu projeto, bem como as perguntas sobre essa biblioteca, como quando e por que usá-lo, consulte a [biblioteca de stub MAPI](https://mapistublibrary.codeplex.com/documentation) no site do CodePlex.</span><span class="sxs-lookup"><span data-stu-id="03c8d-152">To access the MAPI Stub Library files and for information about how to build and integrate it into your project, as well as questions about this library such as when and why to use it, see the [MAPI Stub Library](https://mapistublibrary.codeplex.com/documentation) on the CodePlex site.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="03c8d-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="03c8d-153">See also</span></span>

- [<span data-ttu-id="03c8d-154">Visão geral da programação MAPI</span><span class="sxs-lookup"><span data-stu-id="03c8d-154">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
- [<span data-ttu-id="03c8d-155">Instalar o subsistema MAPI</span><span class="sxs-lookup"><span data-stu-id="03c8d-155">Installing the MAPI Subsystem</span></span>](installing-the-mapi-subsystem.md)
- [<span data-ttu-id="03c8d-156">Instalar arquivos de cabeçalho MAPI</span><span class="sxs-lookup"><span data-stu-id="03c8d-156">Install MAPI Header Files</span></span>](how-to-install-mapi-header-files.md)
- [<span data-ttu-id="03c8d-157">Escolher uma versão específica de MAPI para carregar</span><span class="sxs-lookup"><span data-stu-id="03c8d-157">Choose a Specific Version of MAPI to Load</span></span>](how-to-choose-a-specific-version-of-mapi-to-load.md)
- [<span data-ttu-id="03c8d-158">Determinando o método de vinculação a ser usado</span><span class="sxs-lookup"><span data-stu-id="03c8d-158">Determining Which Linking Method to Use</span></span>](https://msdn.microsoft.com/library/253b8k2c.aspx)
- [<span data-ttu-id="03c8d-159">Vincular um executável a uma DLL</span><span class="sxs-lookup"><span data-stu-id="03c8d-159">Linking an Executable to a DLL</span></span>](https://msdn.microsoft.com/library/9yd93633.aspx)
- [<span data-ttu-id="03c8d-160">ConFigurando as chaves MSI para sua DLL MAPI</span><span class="sxs-lookup"><span data-stu-id="03c8d-160">Setting Up the MSI Keys for Your MAPI DLL</span></span>](https://msdn.microsoft.com/library/ee909494%28v=VS.85%29.aspx)

