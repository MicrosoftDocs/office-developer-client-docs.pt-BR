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
  
Há três métodos de vinculação: vínculo implícito, vínculo explícito e um novo modelo híbrido usando a biblioteca de stub MAPI.
  
## <a name="implicit-linking"></a>Vinculação implícita

Historicamente, chamar funções MAPI em um aplicativo de mensagens sempre envolvia o vínculo com a biblioteca Mapi32. lib. Isso incluiu chamadas de MAPI de roteamento para a biblioteca de stub MAPI do Windows, Mapi32. dll, que, em seguida, encaminharam as chamadas para a implementação de cliente MAPI padrão em tempo de execução. Esse processo de chamada é conhecido como vinculação implícita. O lado esquerdo da figura a seguir mostra um exemplo de vínculo implícito usado em um processo de chamada de função MAPI. O processo é iniciado por um aplicativo MAPI e envolve a biblioteca MAPI (Mapi32. lib) e o stub MAPI do Windows (Mapi32. dll) e é concluído pela implementação do cliente MAPI do Outlook do stub MAPI (Msmapi32. dll).
  
**Comparação de vínculos implícitos e explícitos.**

![Comparação de vínculos implícitos e explícitos] (media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "Comparação de vínculos implícitos e explícitos")
  
## <a name="explicit-linking"></a>Vinculação explícita

Como o cliente MAPI padrão oferece suporte à instalação sob demanda usando o Windows Installer (MSI), você pode desenvolver aplicativos de mensagens diretamente no stub MAPI do Outlook em vez de usar a biblioteca MAPI e o stub MAPI do Windows. O lado direito da figura anterior mostra um exemplo de um processo de chamada de função MAPI, começando com um aplicativo MAPI procurando o caminho e o nome da DLL para o stub MAPI do Outlook (etapa 2 na seção a seguir) e fazendo chamadas de função no stub MAPI do Outlook ( etapa 3 da seção a seguir). O procedimento a seguir mostra como chamar funções MAPI usando vinculação explícita. 
  
> [!NOTE]
> Essas informações sobre vinculação explícita podem ser supérfluas para suas necessidades com a introdução do MAPIStubLibrary. lib abordado na seção a seguir. Como o modelo implícito, a nova biblioteca gerencia tudo e implementa a lógica de vinculação explícita que carrega diretamente o MAPI do Outlook. 
  
Para obter mais informações sobre vinculação explícita, consulte vinculação explícita.
  
### <a name="to-call-mapi-api-elements-without-the-mapi-library-and-the-windows-mapi-stub"></a>Para chamar elementos de API MAPI sem a biblioteca MAPI e o stub MAPI do Windows

1. No arquivo de programa, crie uma lista global de ponteiros de função para cada elemento de API MAPI que você estiver usando. 
    
   O exemplo a seguir mostra esta etapa.
    
   ```cpp
    //Global MAPI function pointers
    LPMAPIINITIALIZE pfnMAPIInitialize = NULL;
    LPMAPIUNINITIALIZE pfnMAPIUninitialize = NULL;
   ```

2. Crie uma função que inicializa funções MAPI para vincular à DLL MAPI do cliente MAPI padrão (por exemplo, Msmapi32. dll do Microsoft Outlook). Nesta função, faça o seguinte: 
    
    1. Carregue Mapi32. dll do diretório de sistema adequado. 
        
       |||
       |:-----|:-----|
       |x64 ou x86 nativamente  <br/> |**%WINDIR%\system32\mapi32.dll** <br/> |
       |x86 no modo WoW  <br/> |**%WINDIR%\syswow64\mapi32.dll** <br/> |
    
    2. Chame a função [FGetComponentPath](fgetcomponentpath.md) para obter o caminho e o nome da dll que implementam o subsistema MAPI. Para obter mais informações, consulte [escolher uma versão específica de MAPI para carregar](how-to-choose-a-specific-version-of-mapi-to-load.md).
        
    3. Carregue a DLL chamando a função LoadLibrary. 
        
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

3. Por fim, chame a função que você criou na etapa 2 em seu aplicativo de mensagens antes de fazer chamadas para elementos da API MAPI. 
    
   > [!CAUTION]
   > Você deve cancelar a inicialização do subsistema MAPI antes de fechar seu aplicativo. 
  
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

## <a name="mapistublibrarylib"></a>MAPIStubLibrary. lib

O advento do Microsoft Outlook 2010 e o MAPI de 64 bits, que agora se estende para o Microsoft Outlook 2013, requer mais do que a API tradicional de 32 bits para implementação completa. Um novo projeto, a biblioteca de stub MAPI, publicado no site CodePlex, fornece uma substituição de redistribuição para Mapi32. lib que oferece suporte à criação de aplicativos MAPI de 32 bits e de 64 bits. MAPIStubLibrary. lib elimina a necessidade de vincular explicitamente ao MAPI e de tê-lo criado, você pode remover o Mapi32. lib das configurações do vinculador, substituindo-o por MAPIStubLibrary. lib; Não será necessário fazer mais modificações no código. Ele também elimina a necessidade de escrever o código **LoadLibrary**, **GetProcAddress**e **FreeLibrary** para lidar com exportações mais recentes incluídas nesse arquivo de biblioteca, mas não em Mapi32. lib, que seriam necessárias se você usava vinculação explícita. 
  
Algumas das novas funções vinculadas a essa biblioteca que não estão disponíveis em Mapi32. lib incluem o seguinte:
  
- [GetDefCachedMode](getdefcachedmode.md)    
- [HrGetGALFromEmsmdbUID](hrgetgalfromemsmdbuid.md)   
- [HrOpenOfflineObj](hropenofflineobj.md)    
- [MAPICrashRecovery](mapicrashrecovery.md)   
- [OpenStreamOnFileW](openstreamonfilew.md)    
- [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)
    
Um método alternativo de incorporação da biblioteca de stub MAPI é copiar os arquivos de origem, MapiStubLibrary. cpp e StubUtils. cpp, diretamente para o seu projeto e remover qualquer vínculo para Mapi32. lib e qualquer código que explicitamente se vincule a MAPI.
  
Para acessar os arquivos da biblioteca de stub MAPI e obter informações sobre como criar e integrá-lo ao seu projeto, bem como as perguntas sobre essa biblioteca, como quando e por que usá-lo, consulte a [biblioteca de stub MAPI](https://mapistublibrary.codeplex.com/documentation) no site do CodePlex. 
  
## <a name="see-also"></a>Confira também

- [Visão geral da programação MAPI](mapi-programming-overview.md)
- [Instalar o subsistema MAPI](installing-the-mapi-subsystem.md)
- [Instalar arquivos de cabeçalho MAPI](how-to-install-mapi-header-files.md)
- [Escolher uma versão específica de MAPI para carregar](how-to-choose-a-specific-version-of-mapi-to-load.md)
- [Determinando o método de vinculação a ser usado](https://msdn.microsoft.com/library/253b8k2c.aspx)
- [Vincular um executável a uma DLL](https://msdn.microsoft.com/library/9yd93633.aspx)
- [ConFigurando as chaves MSI para sua DLL MAPI](https://msdn.microsoft.com/library/ee909494%28v=VS.85%29.aspx)

