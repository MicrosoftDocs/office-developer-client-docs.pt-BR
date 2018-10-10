---
title: Requisitos técnicos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eff6d5d6-8855-4e54-a781-9deab8cc0aca
description: Este tópico descreve os idiomas com suporte de programação, método e a visibilidade COM e requisitos de método de retorno e os detalhes da extensibilidade DLL do provedor Outlook Social Connector (OSC).
ms.openlocfilehash: 14dfcf52d714177775c5610b5da91d174f81a132
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383111"
---
# <a name="technical-requirements"></a>Requisitos técnicos

Este tópico descreve os idiomas com suporte de programação, método e a visibilidade COM e requisitos de método de retorno e os detalhes da extensibilidade DLL do provedor Outlook Social Connector (OSC). 
  
## <a name="programming-language-and-com-requirements"></a>Linguagem de programação e requisitos de COM

Você pode criar um provedor OSC usando idiomas gerenciados como visuais c# ou o Visual Basic ou idiomas não gerenciados como Visual C++. Você pode usar qualquer ferramenta de que possa criar um componente DLL COM visível para desenvolver um provedor do OSC. A decisão de usar uma linguagem gerenciada ou não gerenciada para desenvolver um provedor deve levar em conta o tamanho do download e dependências do pacote de instalação do provedor.
  
Um provedor de OSC deve estar COM visível conforme definido pelo seguinte:
  
- Após a instalação, um provedor de OSC deve ser registrado usando registro COM automático ou regsvr32.
    
- Registro COM de um provedor OSC DLL de registra o provedor em HKCU ou HKLM. 
    
- Registrado em ProgID um provedor `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.
    
- Um provedor de OSC desenvolvido em um idioma gerenciado é COM visível.
    
- Um provedor de OSC deve adicionar valores no registro do Windows que indicam que o provedor DLL dá suporte tanto para os modelos de compartimento thread (STA) quanto para o compartimento multithread (MTA). Para mais informações sobre modelos COM de threading, confira[descrições e o funcionamento do modelo OLE Threading](https://support.microsoft.com/kb/150777).
    
Métodos de extensibilidade do provedor OSC devem retornar tipos primitivos como **cadeia de caracteres** ou **bool**. Determinadas **cadeias** que retornam valores devem ser compatíveis com a definição do esquema de extensibilidade provedor do OSC. Apenas XML é aceito como um valor de retorno. 
  
## <a name="details-of-the-osc-provider-extensibility-dll"></a>Detalhes da extensibilidade OSC provedor DLL

O componente que suporta a extensibilidade do provedor OSC é a extensibilidade OSC do provedor DLL. Desenvolvedores terceiros podem criar o OSC do provedor DLLs usando essas extensibilidade de interfaces. A lista a seguir mostra os detalhes da extensibilidade OSC do provedor DLL:
  
- Nome do arquivo extensibilidade DLL: socialprovider.dll
    
- Nome amigável da extensibilidade DLL: Microsoft Outlook Social provedor extensibilidade
    
- Versão principal do extensibilidade DLL: 15.0
    
- Versão Extensibiilty DLL TypeLib: 1.1
    
## <a name="miscellaneous-technical-information"></a>Informações técnicas diversas

JSON (JavaScript Object Notation) não é suportada no modelo de extensibilidade OSC provedor.
  
Não há nenhuma dependência no analisador de XML. O provedor do OSC pode usar um analisador XML que está incluído no Office, e também o Microsoft XML Core Services (MSXML), usar os recursos de análise do XML integrado ao Microsoft .NET Framework ou usar um analisador XML de terceiros. 
  
## <a name="see-also"></a>Confira também

- [Práticas recomendadas para o desenvolvimento de um provedor](best-practices-for-developing-a-provider.md)  
- [Etapas rápidas para aprender a desenvolver um provedor](quick-steps-for-learning-to-develop-a-provider.md)
- [Implantar um provedor](deploying-a-provider.md)  
- [Introdução ao desenvolvimento de um provedor de serviços do Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

