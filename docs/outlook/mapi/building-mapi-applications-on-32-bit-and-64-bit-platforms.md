---
title: Compilar aplicativos MAPI em plataformas de 32 bits e 64 bits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
api_type:
- COM
ms.assetid: d218ba2d-7a2e-4c33-a09b-a8c7e27f9726
description: 'Última modificação: 9 de março de 2015'
localization_priority: Priority
ms.openlocfilehash: 74f321d2c6c8b5159191d4dcdb62e0db21132435
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700413"
---
# <a name="building-mapi-applications-on-32-bit-and-64-bit-platforms"></a>Compilar aplicativos MAPI em plataformas de 32 bits e 64 bits

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este tópico descreve as ações que os desenvolvedores MAPI devem executar para alterar e reconstruir aplicativos MAPI de 32 bits para execução em uma plataforma de 64 bits e aplicativos de 64 bits para execução em uma plataforma de 32 bits. Neste tópico, uma plataforma de 64 bits é um computador com o Windows e Microsoft Outlook de 64 bits instalados e uma plataforma de 32 bits é um computador com Outlook de 32 bits e Windows de 32 bits ou 64 bits instalados. 
  
## <a name="operating-system-and-office-support-for-64-bit-outlook"></a>Sistema operacional e suporte do Office para o Outlook de 64 bits

> [!NOTE]
> O termo número de bits se refere à distinção entre as arquiteturas de processador de 32 e 64 bits e à compatibilidade de aplicativos associada. Neste tópico, o número de bits é usado para qualificar a versão do Windows, do Microsoft Office, do Outlook ou de um aplicativo MAPI de acordo com a arquitetura de processador de 32 ou 64 bits de um computador e, possivelmente, outros aplicativos em execução no computador. 
  
A partir do Microsoft Office 2010, o Outlook está disponível como um aplicativo de 32 e 64 bits. No mesmo computador, o número de bits do Outlook depende do número de bits do sistema operacional Windows (x86 ou x64) e do Microsoft Office, se o Office já estiver instalado no computador. A seguir estão alguns dos fatores que determinam a viabilidade de instalar uma versão de 32 ou 64 bits do Outlook:
  
- o Office 32 bits (e o Outlook de 32 bits) podem ser instalados em uma versão de 32 ou 64 bits do sistema operacional Windows. o Office de 64 bits (e o Outlook de 64 bits) podem ser instalados apenas em um sistema operacional de 64 bits.
    
- A instalação padrão do Office em uma versão do sistema operacional Windows de 64 bits é o Office de 32 bits.
    
- O número de bits de uma versão instalada do Outlook é sempre o mesmo que o número de bits do Outlook, se o Outlook estiver instalado no mesmo computador. Em outras palavras, uma versão de 32 bits do Outlook não pode ser instalada no mesmo computador que já tenha versões de 64 bits de outros aplicativos do Office instalados, como o Microsoft Word ou Excel 64 bits. Da mesma forma, uma versão de 64 bits do Outlook não pode ser instalada no mesmo computador que já tiver versões de 32 bits de outros aplicativos do Office instalados.
    
## <a name="preparing-mapi-applications-for-32-bit-and-64-bit-platforms"></a>Preparar aplicativos MAPI para plataformas de 32 bits e 64 bits

Aplicativos MAPI incluem aplicativos autônomos como Microsoft Communicator e o MFCMAPI, e provedores de serviços como de catálogo de endereços, de repositório e de transporte. Para que as chamadas de funções e métodos MAPI funcionem em um aplicativo MAPI (com a exceção de uma função Simple da MAPI, MAPISendMail), o número de bits do aplicativo MAPI deve ser o mesmo do subsistema MAPI no computador em que o aplicativo será executado. Por sua vez, o número de bits do subsistema MAPI é determinado pelo e é sempre igual ao número de bits da versão instalada do Outlook. A tabela a seguir resume as ações necessárias para preparar os aplicativos MAPI para execução em computadores de destino configurados com o Office e o Windows de vários bits.
  
|Número de bits do aplicativo MAPI|Número de bits do Outlook no computador de destino|Número de bits do Windows no computador de destino|Ações necessárias para habilitar o aplicativo para execução no computador de destino|
|:-----|:-----|:-----|:-----|
|32 bits  <br/> |32 bits  <br/> |32 bits ou 64 bits  <br/> |Nenhuma ação específica é necessária.  <br/> |
|32 bits  <br/> |64 bits  <br/> |64 bits  <br/> |Recrie um aplicativo como um aplicativo de 64 bits. Caso contrário, todas as chamadas de função e método MAPI (exceto **MAPISendMail**) falharão.  <br/> |
|64 bits  <br/> |64 bits  <br/> |64 bits  <br/> |Nenhuma ação específica é necessária.  <br/> |
|64 bits  <br/> |32 bits  <br/> |32 bits ou 64 bits  <br/> |Recrie o aplicativo como um aplicativo de 32 bits. Caso contrário, todas as chamadas de função e método MAPI (exceto **MAPISendMail**) falharão.  <br/> |
   
As seções a seguir explicam melhor cada cenário. Para cenários que exigem recompilar o aplicativo MAPI, confira [Link para funções MAPI](how-to-link-to-mapi-functions.md) para saber mais sobre como vincular e chamar funções MAPI. 
  
### <a name="32-bit-mapi-application-and-32-bit-outlook"></a>Aplicativo MAPI de 32 bits e o Outlook de 32 bits

Os aplicativos MAPI compilados para um subsistema MAPI de 32 bits disponíveis em versões de 32 bits do Outlook, inclusive as versões anteriores ao Microsoft Outlook 2013, continuam a ter suporte em computadores instalados com o Outlook de 32 bits e o sistema operacional Windows de 32 ou 64 bits. Não há nenhuma ação específica necessária para os desenvolvedores de aplicativos.
  
### <a name="32-bit-mapi-application-and-64-bit-outlook"></a>Aplicativo MAPI de 32 bits e o Outlook de 64 bits

Aplicativos MAPI de 32 bits não têm suporte para execução em um computador instalado com o Outlook e o Windows de 64 bits. O desenvolvedor do aplicativo deverá atualizar e recompilar o aplicativo como um aplicativo de 64 bits para a plataforma de 64 bits. Isso ocorre porque o aplicativo de 32 bits não pode carregar o arquivo Msmapi32.dll de 64 bits. Há um pequeno número de alterações de API que os desenvolvedores de aplicativos devem incorporar para compilar seu código com êxito em um ambiente de 64 bits. Os arquivos de cabeçalho MAPI foram atualizados com essas alterações para oferecer suporte à plataforma de 64 bits. Você pode baixar esses arquivos de cabeçalho no [Outlook 2010: arquivos de cabeçalho MAPI](https://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1). Os desenvolvedores podem usar esse mesmo conjunto de arquivos de cabeçalho MAPI para compilar aplicativos MAPI de 32 bits e 64 bits.
  
### <a name="64-bit-mapi-application-and-64-bit-outlook"></a>Aplicativo MAPI de 64 bits e o Outlook de 64 bits

Aplicativos MAPI de 64 bits têm suporte em computadores instalados com o Outlook e o Windows de 64 bits. Não há nenhuma ação específica necessária para os desenvolvedores de aplicativos.
  
### <a name="64-bit-mapi-application-and-32-bit-outlook"></a>Aplicativo MAPI de 64 bits e o Outlook de 32 bits

Aplicativos MAPI de 64 bits não têm suporte para execução em um computador instalado com o Outlook de 32 bits e o Windows de 32 ou 64 bits. O desenvolvedor do aplicativo deverá atualizar e recompilar o aplicativo como um aplicativo de 32 bits para funcionar com o Outlook de 32 bits. Use os arquivos de cabeçalho MAPI atualizados, que podem ser baixados em [Outlook 2010: arquivos de cabeçalho MAPI](https://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1). Os desenvolvedores podem usar esse mesmo conjunto de arquivos de cabeçalho MAPI para compilar aplicativos MAPI de 32 bits e 64 bits.
  
### <a name="exception-mapisendmail"></a>Exceção: MAPISendMail

Em geral, um aplicativo MAPI de 32 bits não deve ser executado em uma plataforma de 64 bits (Outlook de 64 bits no Windows de 64 bits) sem primeiro ser recompilado como um aplicativo de 64 bits e um aplicativo MAPI de 64 bits não deve ser executado em um computador instalado com o Outlook de 32 bits e o Windows de 32 ou 64 bits sem primeiro ser recompilado como um aplicativo de 32 bits. A figura 1 mostra uma caixa de diálogo de alerta que seria exibida se um qualquer um desses cenários ocorrer.
  
**Figura 1. Mensagem de erro para a maioria das chamadas MAPI de bits cruzados.**

![Mensagem de erro para a maioria das chamadas MAPI de bits cruzados](media/738905fb-57ae-4af7-b54b-a1676c80d3c3.JPG "Mensagem de erro para a maioria das chamadas MAPI de bits cruzados")
  
No entanto, uma chamada de função entre todos os elementos de MAPI e MAPI simples, **MAPISendMail**, deve ter sucesso em um cenário de Windows-32-bits-em-Windows-64-bits (WOW64) ou Windows-64-bits-em-Windows-32-bits (WOW32) e não resultará no alerta acima. Esse cenário WOW64 só se aplica ao Windows 7. 

A figura 2 mostra um cenário WOW64 em que um aplicativo MAPI de 32 bits chama **MAPISendMail** em um computador instalado com o Windows 7 de 64 bits. Nesse cenário, a biblioteca MAPI faz uma chamada COM para iniciar um aplicativo Fixmapi de 64 bits. O aplicativo Fixmapi se vincula implicitamente à biblioteca MAPI, que encaminha a chamada de função para o esboço MAPI do Windows, que, por sua vez, encaminha a chamada para o esboço MAPI do Outlook, permitindo que a chamada da função **MAPISendMail** seja bem sucedida. 
  
**Figura 2. Processando MAPISendMail em um cenário WOW64.**

![Processando MAPISendMail em um cenário WOW64](media/346ba974-4844-4b64-9dd1-d0f829ab99b3.gif "Processando MAPISendMail em um cenário WOW64")
  
## <a name="see-also"></a>Confira também

- [Link para funções MAPI](how-to-link-to-mapi-functions.md)

