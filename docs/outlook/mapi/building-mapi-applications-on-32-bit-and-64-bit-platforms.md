---
title: Compilando aplicativos MAPI em plataformas de 32 bits e 64 bits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d218ba2d-7a2e-4c33-a09b-a8c7e27f9726
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: dce3f4b5bfdcb34148c25c880d8d2d8173755b37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766246"
---
# <a name="building-mapi-applications-on-32-bit-and-64-bit-platforms"></a>Compilando aplicativos MAPI em plataformas de 32 bits e 64 bits

**Aplica-se a**: Outlook 
  
Este tópico descreve as ações que os desenvolvedores MAPI devem ser adotada para alterar e reconstruir aplicativos MAPI de 32 bits para ser executado em uma plataforma de 64 bits e aplicativos de 64 bits sejam executados em uma plataforma de 32 bits. Neste tópico, uma plataforma de 64 bits é um computador instalado com o Windows de 64 bits e de 64 bits Microsoft Outlook e uma plataforma de 32 bits é um computador instalado com um Outlook de 32 bits e Windows de 32 bits ou 64 bits. 
  
## <a name="operating-system-and-office-support-for-64-bit-outlook"></a>Sistema operacional e suporte para o Outlook de 64 bits do Office

> [!NOTE]
> O número de bits de termo refere-se a distinção entre a associado compatibilidade de aplicativos e arquiteturas de processador de 32 bits e 64 bits. Neste tópico, bitness é usado para se qualificar a versão do Windows, Microsoft Office, Outlook, ou um aplicativo de MAPI criado de acordo com uma arquitetura de processador de 32 bits ou 64 bits de um computador e, possivelmente, outros aplicativos que são executados no computador. 
  
Iniciando no Microsoft Office 2010, Outlook está disponível como um aplicativo de 64 bits e de 32 bits. No mesmo computador, o número de bits do Outlook depende do sistema operacional Windows (x86 ou x64) e do Microsoft Office, o número de bits se Office já estiver instalado no computador. Estes são alguns dos fatores que determinam a viabilidade da instalação de 32 bits ou uma versão de 64 bits do Outlook:
  
- Office de 32 bits (e Outlook de 32 bits) podem ser instalado em uma versão de 32 bits ou 64 bits do sistema operacional Windows. Office de 64 bits (e Outlook de 64 bits) podem ser instalado somente em um sistema operacional de 64 bits.
    
- A instalação padrão do Office em uma versão de 64 bits do sistema operacional Windows é o Office de 32 bits.
    
- O número de bits de uma versão instalada do Outlook é sempre o mesmo que o número de bits do Office, se o Office for instalado no mesmo computador. Em outras palavras, uma versão de 32 bits do Outlook não pode ser instalada no mesmo computador que já tenha as versões de 64 bits dos outros aplicativos do Office instalados, como 64-bit Microsoft Word ou no Microsoft Excel de 64 bits. Da mesma forma, uma versão de 64 bits do Outlook não pode ser instalada no mesmo computador que já tenha as versões de 32 bits de outros aplicativos do Office instalados.
    
## <a name="preparing-mapi-applications-for-32-bit-and-64-bit-platforms"></a>Preparando aplicativos MAPI para plataformas de 32 bits e 64 bits

Aplicativos MAPI incluem aplicativos autônomos, como Microsoft Communicator e MFCMAPI e provedores de serviço, como o catálogo de endereços, armazenam e provedores de transporte. Para a função e método MAPI chamadas para trabalhar em um aplicativo de MAPI (com exceção de uma Simple MAPI função, MAPISendMail), o número de bits do aplicativo MAPI devem ser o mesmo que o número de bits do subsistema de MAPI no computador que o aplicativo está programado para Execute em. O número de bits do subsistema de MAPI, por sua vez, é determinado por e sempre o mesmo que o número de bits da versão instalada do Outlook. A tabela a seguir resume as ações necessárias para preparar aplicativos MAPI para executar nos computadores de destino configurados com o Office e janelas de vários bitness.
  
|Número de bits do aplicativo de MAPI|Número de bits do Outlook no computador de destino|Número de bits do Windows no computador de destino|Ação necessária para habilitar o aplicativo seja executado no computador de destino|
|:-----|:-----|:-----|:-----|
|32 bits  <br/> |32 bits  <br/> |32 bits ou 64 bits  <br/> |Nenhuma ação específica é necessária.  <br/> |
|32 bits  <br/> |64 bits  <br/> |64 bits  <br/> |Recrie o aplicativo como um aplicativo de 64 bits. Caso contrário, todas as chamadas de método e a função MAPI (exceto para **MAPISendMail**) falhará.  <br/> |
|64 bits  <br/> |64 bits  <br/> |64 bits  <br/> |Nenhuma ação específica é necessária.  <br/> |
|64 bits  <br/> |32 bits  <br/> |32 bits ou 64 bits  <br/> |Recrie o aplicativo como um aplicativo de 32 bits. Caso contrário, todas as chamadas de método e a função MAPI (exceto para **MAPISendMail**) falhará.  <br/> |
   
Ainda mais as seções a seguir explicam cada cenário. Para cenários que exigem a recriação do aplicativo de MAPI, consulte o [Link para funções de MAPI](how-to-link-to-mapi-functions.md) para obter informações adicionais sobre vinculando a e chamar funções de MAPI. 
  
### <a name="32-bit-mapi-application-and-32-bit-outlook"></a>aplicativo de MAPI de 32 bits e o Outlook de 32 bits

Aplicativos MAPI compilados por um subsistema MAPI de 32 bits que está disponível em versões de 32 bits do Outlook, incluindo as versões anteriores ao Microsoft Outlook 2013, continuem a ter suporte em computadores instalados com o Outlook de 32 bits e um Windows de 32 bits ou 64 bits Sistema Operacional. Não há nenhuma ação específica necessárias para os desenvolvedores de aplicativos.
  
### <a name="32-bit-mapi-application-and-64-bit-outlook"></a>aplicativo de MAPI de 32 bits e 64 bits Outlook

aplicativos MAPI de 32 bits não são suportados para executar em um computador instalado com o Outlook de 64 bits e Windows de 64 bits. O desenvolvedor do aplicativo deve atualizar e recriar o aplicativo como um aplicativo de 64 bits para a plataforma de 64 bits. Isso acontece porque um aplicativo de 32 bits não é possível carregar um arquivo de Msmapi32 de 64 bits. Há um pequeno número de alterações de API que os desenvolvedores de aplicativos devem incorporar para criar seu código com êxito para um ambiente de 64 bits. Arquivos de cabeçalho MAPI foram atualizados com essas alterações para oferecer suporte a plataforma de 64 bits. Você pode baixar esses arquivos de cabeçalho em [Outlook 2010: arquivos de cabeçalho de MAPI](http://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1). Os desenvolvedores podem usar esse mesmo conjunto de arquivos de cabeçalho MAPI para criar aplicativos de MAPI de 32 bits e 64 bits.
  
### <a name="64-bit-mapi-application-and-64-bit-outlook"></a>aplicativo de MAPI de 64 bits e 64 bits Outlook

aplicativos MAPI de 64 bits são suportados em computadores instalados com o Outlook de 64 bits e Windows de 64 bits. Não há nenhuma ação específica necessárias para os desenvolvedores de aplicativos.
  
### <a name="64-bit-mapi-application-and-32-bit-outlook"></a>Outlook de 32 bits e de aplicativo de MAPI de 64 bits

aplicativos MAPI de 64 bits não são suportados para executar em um computador instalado com o Outlook de 32 bits e Windows de 32 bits ou 64 bits. O desenvolvedor do aplicativo deve atualizar e recriar o aplicativo como um aplicativo de 32 bits para funcionar com o Outlook de 32 bits. Use os arquivos de cabeçalho MAPI atualizados, o que pode ser baixado em [Outlook 2010: arquivos de cabeçalho de MAPI](http://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1). Os desenvolvedores podem usar esse mesmo conjunto de arquivos de cabeçalho MAPI para criar aplicativos de MAPI de 32 bits e 64 bits.
  
### <a name="exception-mapisendmail"></a>Exceção: MAPISendMail

Em geral, não deve executar um aplicativo de MAPI de 32 bits de 64 bits plataforma (Outlook de 64 bits no Windows de 64 bits) sem primeiro sendo recriada como um aplicativo de 64 bits e um aplicativo de MAPI de 64 bits não precisará executar em um computador instalado com o Outlook de 32 bits e 32 bits ou 64 bits Windows sem primeiro sejam recriados como um aplicativo de 32 bits. Figura 1 mostra uma caixa de diálogo alerta que seria exibida se uma dessas situações ocorrerá.
  
**Figura 1. Mensagem de erro de MAPI de cross-bitness a maioria das chamadas.**

![Mensagem de erro para chamadas MAPI mais cross-bitness] (media/738905fb-57ae-4af7-b54b-a1676c80d3c3.JPG "Mensagem de erro para chamadas MAPI mais cross-bitness")
  
No entanto, uma chamada de função entre todos os MAPI simples e MAPI elementos, **MAPISendMail**, seria bem-sucedida em um cenário de Windows-64-bit-on-Windows-32-bit (WOW32) ou o Windows-32-bit-on-Windows-64-bit (WOW64) e não for resultar em alerta acima. Este cenário WOW64 só se aplica ao Windows 7. 

Figura 2 mostra um cenário de WOW64 no qual um aplicativo de MAPI de 32 bits chama **MAPISendMail** em um computador instalado com o Windows 7 de 64 bits. Neste cenário, a biblioteca MAPI faz uma chamada COM para iniciar um aplicativo de Fixmapi de 64 bits. O aplicativo Fixmapi implicitamente vincula a biblioteca MAPI, que roteia a chamada de função para o fragmento de código do MAPI do Windows, que por sua vez, encaminha a chamada para o fragmento de código de MAPI do Outlook, permitindo que a chamada de função **MAPISendMail** ter sucesso. 
  
**Figura 2. Processando MAPISendMail em um cenário de WOW64.**

![Processamento MAPISendMail em um cenário de WOW64] (media/346ba974-4844-4b64-9dd1-d0f829ab99b3.gif "Processamento MAPISendMail em um cenário de WOW64")
  
## <a name="see-also"></a>Confira também

- [Link para funções MAPI](how-to-link-to-mapi-functions.md)

