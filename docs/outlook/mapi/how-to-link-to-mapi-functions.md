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
# <a name="link-to-mapi-functions"></a>Link para funções MAPI

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Há três métodos de vinculação: vinculação implícita, vinculação explícita e um novo modelo híbrido usando a Biblioteca de Stub MAPI.
  
## <a name="implicit-linking"></a>Vinculação implícita

Historicamente, chamar funções MAPI em um aplicativo de mensagens sempre envolvia a vinculação à biblioteca Mapi32.lib. Isso incluiu o roteamento de chamadas MAPI para a biblioteca de stub mapi do Windows, Mapi32.dll, que encaminhou as chamadas para a implementação de cliente MAPI padrão em tempo de execução. Esse processo de chamada é conhecido como vinculação implícita. O lado esquerdo da figura a seguir mostra um exemplo de vinculação implícita usada em um processo de chamada de função MAPI. O processo é iniciado por um aplicativo MAPI e envolve a biblioteca MAPI (Mapi32.lib) e o stub de MAPI do Windows (Mapi32.dll) e é concluído pela implementação do cliente MAPI do Outlook do stub (Msmapi32.dll).
  
**Comparação de vinculação implícita e explícita.**

![Comparação de vinculação implícita e explícita](media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "Comparação de vinculação implícita e explícita")
  
## <a name="explicit-linking"></a>Vinculação explícita

Como o cliente MAPI padrão dá suporte à instalação sob demanda usando o Windows Installer (MSI), você pode desenvolver aplicativos de mensagens diretamente no stub MAPI do Outlook em vez de usar a biblioteca MAPI e o stub de MAPI do Windows. O lado direito da figura anterior mostra um exemplo de um processo de chamada de função MAPI, começando com um aplicativo MAPI procurando o caminho e o nome DLL para o stub MAPI do Outlook (etapa 2 na seção a seguir) e fazendo chamadas de função para o stub MAPI do Outlook (etapa 3 na seção a seguir). O procedimento a seguir mostra como chamar funções MAPI usando vinculação explícita. 
  
> [!NOTE]
> Essas informações sobre vinculação explícita podem ser supérfluas para suas necessidades com a introdução de MAPIStubLibrary.lib discutida na seção a seguir. Assim como o modelo implícito, a nova biblioteca gerencia tudo e implementa a lógica de vinculação explícita que carrega diretamente o MAPI do Outlook. 
  
Para obter mais informações sobre vinculação explícita, consulte Vinculação Explícita.
  
### <a name="to-call-mapi-api-elements-without-the-mapi-library-and-the-windows-mapi-stub"></a>Para chamar elementos da API MAPI sem a biblioteca MAPI e o stub MAPI do Windows

1. No arquivo de programa, crie uma lista global de ponteiros de função para cada elemento da API MAPI que você está usando. 
    
   O exemplo a seguir mostra esta etapa.
    
   ```cpp
    //Global MAPI function pointers
    LPMAPIINITIALIZE pfnMAPIInitialize = NULL;
    LPMAPIUNINITIALIZE pfnMAPIUninitialize = NULL;
   ```

2. Crie uma função que inicialize funções MAPI para vincular à DLL MAPI do cliente MAPI padrão (por exemplo, Msmapi32.dll do Microsoft Outlook). Nesta função, faça o seguinte: 
    
    1. Carregue mapi32.dll do diretório do sistema apropriado. 
        
       |||
       |:-----|:-----|
       |x64 ou x86 de forma nativa  <br/> |**%windir%\system32\mapi32.dll** <br/> |
       |x86 no modo WoW  <br/> |**%windir%\syswow64\mapi32.dll** <br/> |
    
    2. Chame a [função FGetComponentPath](fgetcomponentpath.md) para obter o caminho e o nome da DLL que implementa o subsistema MAPI. Para obter mais informações, [consulte Escolher uma versão específica do MAPI para carregar.](how-to-choose-a-specific-version-of-mapi-to-load.md)
        
    3. Carregue a DLL chamando a função LoadLibrary. 
        
    4. Inicialize a matriz de ponteiro da função MAPI chamando a função GetProcAddress. 
        
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

3. Por fim, chame a função que você criou na etapa 2 em seu aplicativo de mensagens antes de fazer chamadas aos elementos da API MAPI. 
    
   > [!CAUTION]
   > Você deve desincializar o subsistema MAPI antes de fechar o aplicativo. 
  
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

O advento do MAPI do Microsoft Outlook 2010 e de 64 bits, agora se estendendo ao Microsoft Outlook 2013, requer mais do que a API tradicional de 32 bits para implementação completa. Um novo projeto, a Biblioteca stub MAPI, postado no site do CodePlex fornece uma substituição de lista para Mapi32.lib que dá suporte à criação de aplicativos MAPI de 32 bits e 64 bits. MAPIStubLibrary.lib elimina a necessidade de vincular explicitamente ao MAPI e, tendo criado isso, você pode remover Mapi32.lib das configurações do linker, substituindo-o por MAPIStubLibrary.lib; nenhuma outra modificação em seu código deve ser necessária. Ele também elimina a necessidade de escrever o código **LoadLibrary**, **GetProcAddress** e **FreeLibrary** para lidar com exportações mais novas incluídas neste arquivo de biblioteca, mas não em Mapi32.lib, que seria necessário se você tivesse usado a vinculação explícita. 
  
Algumas das novas funções vinculadas a partir dessa biblioteca que não estão disponíveis em Mapi32.lib incluem o seguinte:
  
- [GetDefCachedMode](getdefcachedmode.md)    
- [HrGetGALFromEmsmdbUID](hrgetgalfromemsmdbuid.md)   
- [HrOpenOfflineObj](hropenofflineobj.md)    
- [MAPICrashRecovery](mapicrashrecovery.md)   
- [OpenStreamOnFileW](openstreamonfilew.md)    
- [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)
    
Um método alternativo de incorporar a Biblioteca stub MAPI é copiar os arquivos de origem, MapiStubLibrary.cpp e StubUtils.cpp, diretamente em seu projeto e remover qualquer vinculação a Mapi32.lib e qualquer código que explicitamente se vincula ao MAPI.
  
Para acessar os arquivos da Biblioteca de Stub MAPI e obter informações sobre como criar e integrá-la ao seu projeto, bem como perguntas sobre essa biblioteca, como quando e por que usá-la, consulte a Biblioteca [de Stub MAPI](https://mapistublibrary.codeplex.com/documentation) no site CodePlex. 
  
## <a name="see-also"></a>Confira também

- [Visão geral da programação MAPI](mapi-programming-overview.md)
- [Instalar o subsistema MAPI](installing-the-mapi-subsystem.md)
- [Instalar arquivos de header MAPI](how-to-install-mapi-header-files.md)
- [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md)
- [Determinando qual método de vinculação usar](https://msdn.microsoft.com/library/253b8k2c.aspx)
- [Vinculando um executável a uma DLL](https://msdn.microsoft.com/library/9yd93633.aspx)
- [Configurando as chaves MSI para sua DLL MAPI](https://msdn.microsoft.com/library/ee909494%28v=VS.85%29.aspx)

