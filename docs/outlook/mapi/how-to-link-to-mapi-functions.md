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
# <a name="link-to-mapi-functions"></a>Link para funções MAPI

**Aplica-se a**: Outlook 
  
Existem três métodos de vínculo: vinculação implícita, explícita de vinculação e um novo modelo de híbrida usando a biblioteca de Stub de MAPI.
  
## <a name="implicit-linking"></a>Vinculação de implícitas

Historicamente, chamar funções de MAPI em um aplicativo de mensagens sempre envolvida vinculação à biblioteca Mapi32.lib. Isso incluiu o roteamento de chamadas MAPI para a biblioteca de stub MAPI do Windows, Mapi32, que então encaminhados as chamadas feitas na implementação de cliente MAPI padrão em tempo de execução. Esse processo de chamada é conhecido como vinculação implícita. O lado esquerdo da figura a seguir mostra um exemplo de vinculação implícita usado em um processo de chamada de função MAPI. O processo é iniciado por um aplicativo de MAPI e envolve a biblioteca MAPI (Mapi32.lib) e o fragmento de código do MAPI do Windows (Mapi32) e é concluído pela implementação cliente MAPI do Outlook do fragmento de código do MAPI (Msmapi32).
  
**Comparação de vinculação implícitas e explícitas.**

![Comparação de vínculo implícitas e explícitas] (media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "Comparação de vínculo implícitas e explícitas")
  
## <a name="explicit-linking"></a>Explicit vinculação

Como o cliente MAPI padrão oferece suporte a instalação sob demanda usando o Windows Installer (MSI), você pode desenvolver aplicativos de mensagens diretamente no stub MAPI do Outlook em vez de usar a biblioteca MAPI e stub MAPI do Windows. Lado direito da figura anterior mostra um exemplo de um processo de chamada de função MAPI, começando com um aplicativo de MAPI procurando o caminho e o nome da DLL para o fragmento de código do MAPI do Outlook (etapa 2 da seção a seguir) e fazer chamadas de função em (de stub o MAPI do Outlook Etapa 3 na seção a seguir). O procedimento a seguir mostra como chamar funções MAPI usando vinculação explícitas. 
  
> [!NOTE]
> Essas informações sobre a vinculação de explícitas podem ser supérfluas às suas necessidades com a introdução do MAPIStubLibrary.lib discutido na próxima seção. Como o modelo implícito, a nova biblioteca gerencia tudo e implementa a lógica de vinculação explícita que é carregado do Outlook MAPI diretamente. 
  
Para obter mais informações sobre a vinculação de maneira explícita, consulte vinculação explicitamente.
  
### <a name="to-call-mapi-api-elements-without-the-mapi-library-and-the-windows-mapi-stub"></a>Para chamar elementos de API de MAPI sem a biblioteca MAPI e o fragmento de código do MAPI do Windows

1. Em seu arquivo de programa, crie uma lista global de ponteiros de função para cada elemento da API de MAPI que você está usando. 
    
   O exemplo a seguir mostra esta etapa.
    
   ```cpp
    //Global MAPI function pointers
    LPMAPIINITIALIZE pfnMAPIInitialize = NULL;
    LPMAPIUNINITIALIZE pfnMAPIUninitialize = NULL;
   ```

2. Crie uma função que inicializa funções MAPI para vincular a DLL MAPI do cliente MAPI padrão (por exemplo, Msmapi32 do Microsoft Outlook). Nesta função, faça o seguinte: 
    
    1. Carregar MAPI32. dll do diretório de sistema apropriado. 
        
       |||
       |:-----|:-----|
       |x64 ou x86 nativamente  <br/> |**%windir%\system32\mapi32.dll** <br/> |
       |x86 no modo WoW  <br/> |**%windir%\syswow64\mapi32.dll** <br/> |
    
    2. Chame a função [FGetComponentPath](fgetcomponentpath.md) para obter o caminho e o nome da DLL que implementa o subsistema de MAPI. Para obter mais informações, consulte [Escolher uma versão específica de MAPI a carga](how-to-choose-a-specific-version-of-mapi-to-load.md).
        
    3. Carrega a DLL chamando-se a função LoadLibrary. 
        
    4. Inicialize a matriz de ponteiro de função MAPI chamando a função GetProcAddress. 
        
    O exemplo a seguir mostra as etapas anteriores:
        
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

3. Finalmente, chame a função que você criou na etapa 2 no seu aplicativo de mensagens antes de fazer chamadas de elementos de API de MAPI. 
    
   > [!CAUTION]
   > Você deve não inicializar o subsistema de MAPI antes de fechar o seu aplicativo. 
  
   O exemplo a seguir mostra esta etapa: 
    
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

## <a name="mapistublibrarylib"></a>MAPIStubLibrary.lib

O advento do Microsoft Outlook 2010 e 64-bit MAPI, estendendo agora para o Microsoft Outlook 2013, exige mais do que a API de 32 bits tradicional para implementação completa. Um novo projeto, a biblioteca Stub MAPI, postado no site do CodePlex fornece uma substituição para soltar para Mapi32.lib que ofereça suporte a criação de aplicativos de MAPI de 32 bits e 64 bits. MAPIStubLibrary.lib elimina a necessidade para vincular explicitamente a MAPI e ele ter que ser construído, você pode remover Mapi32.lib de suas configurações de vinculador, substituindo-MAPIStubLibrary.lib; Nenhum mais modificações para o seu código seja necessária. Ele também elimina a necessidade de escrever código **LoadLibrary**e **GetProcAddress** **FreeLibrary** para lidar com mais recentes exportações incluídas neste arquivo de biblioteca, mas não no Mapi32.lib, qual seria necessário se você tiver usado a vinculação explícitas. 
  
Algumas das novas funções vinculadas a partir desta biblioteca que não estão disponíveis no Mapi32.lib incluem o seguinte:
  
- [GetDefCachedMode](getdefcachedmode.md)    
- [HrGetGALFromEmsmdbUID](hrgetgalfromemsmdbuid.md)   
- [HrOpenOfflineObj](hropenofflineobj.md)    
- [MAPICrashRecovery](mapicrashrecovery.md)   
- [OpenStreamOnFileW](openstreamonfilew.md)    
- [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)
    
Um método alternativo de incorporar a biblioteca de Stub MAPI é copiar os arquivos de origem, MapiStubLibrary.cpp e StubUtils.cpp, diretamente em seu projeto e remover qualquer vinculação com Mapi32.lib e qualquer código que explicitamente vincula a MAPI.
  
Para acessar os arquivos da biblioteca de Stub MAPI e para obter informações sobre como criar e integrá-lo em seu projeto, bem como dúvidas sobre esta biblioteca como quando e por que usá-lo, consulte a [Biblioteca de Stub MAPI](http://mapistublibrary.codeplex.com/documentation) no site do CodePlex. 
  
## <a name="see-also"></a>Confira também

- [Vis�o geral da programa��o MAPI](mapi-programming-overview.md)
- [Instalar o subsistema MAPI](installing-the-mapi-subsystem.md)
- [Instalar arquivos de cabeçalho MAPI](how-to-install-mapi-header-files.md)
- [Escolher uma versão MAPI específica para carregar](how-to-choose-a-specific-version-of-mapi-to-load.md)
- [Determinando qual método vinculação de uso](http://msdn.microsoft.com/en-us/library/253b8k2c.aspx)
- [Vinculando um arquivo executável para uma DLL](http://msdn.microsoft.com/en-us/library/9yd93633.aspx)
- [Configurando as chaves MSI para sua DLL MAPI](http://msdn.microsoft.com/en-us/library/ee909494%28v=VS.85%29.aspx)

