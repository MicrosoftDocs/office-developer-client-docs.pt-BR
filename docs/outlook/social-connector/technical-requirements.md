---
title: Requisitos técnicos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eff6d5d6-8855-4e54-a781-9deab8cc0aca
description: Este tópico descreve os idiomas com suporte de programação, método e a visibilidade COM retornam requisitos de tipo e detalhes de DLL de extensibilidade do provedor do Outlook Social Connector (OSC).
ms.openlocfilehash: 94b57e20957f3d8d779c4d3324ecbb8ccd37f60a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770952"
---
# <a name="technical-requirements"></a>Requisitos técnicos

Este tópico descreve os idiomas com suporte de programação, método e a visibilidade COM retornam requisitos de tipo e detalhes de DLL de extensibilidade do provedor do Outlook Social Connector (OSC). 
  
## <a name="programming-language-and-com-requirements"></a>Requisitos de COM e linguagem de programação

Você pode criar um provedor OSC utilizando linguagens gerenciadas como Visual c# ou Visual Basic ou não gerenciado de idiomas como o Visual C++. Você pode usar qualquer ferramenta que pode criar um componente DLL COM visíveis para desenvolver um provedor OSC. A decisão de usar um idioma gerenciado ou para desenvolver um provedor deve levar em conta o tamanho do download e dependências do pacote de instalação do provedor.
  
Um provedor OSC deve ser visível em COM, conforme definido pelo seguinte:
  
- Após a instalação, um provedor OSC deve ser registrado usando self-registro COM ou regsvr32.
    
- Registro COM de um provedor OSC DLL registra o provedor em HKCU ou HKLM. 
    
- ProgID de um provedor está registrado em `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.
    
- Um provedor OSC desenvolvido em um idioma gerenciado é visível em COM.
    
- Um provedor OSC adicione valores no registro do Windows que indicam que o provedor DLL suporta compartimento de segmentação única (STA) e o MTA (multithreaded apartment) modelos de threading. Para obter mais informações sobre o COM modelos de threading, consulte [as descrições e funcionamento de OLE Threading modelos](http://support.microsoft.com/kb/150777).
    
Métodos na extensibilidade do provedor OSC devem retornar tipos primitivos como **cadeia de caracteres** ou **bool**. Determinada **cadeia de caracteres** retornam valores devem estar em conformidade com a definição de esquema para fornecer extensibilidade de provedor do OSC. Somente XML é aceito como um valor de retorno. 
  
## <a name="details-of-the-osc-provider-extensibility-dll"></a>Detalhes da extensibilidade do provedor OSC DLL

O componente que ofereça suporte a estensibilidade do provedor do OSC é a extensibilidade do provedor OSC DLL. Desenvolvedores de terceiros podem criar DLLs de provedor do OSC usando essas interfaces de extensibilidade. A lista a seguir mostra os detalhes da extensibilidade do provedor OSC DLL:
  
- Nome do arquivo DLL extensibilidade: socialprovider.dll
    
- Nome amigável da DLL de extensibilidade: extensibilidade do Microsoft Outlook Social provedor
    
- Versão principal de DLL de extensibilidade: 15.0
    
- Versão Extensibiilty DLL TypeLib: 1.1
    
## <a name="miscellaneous-technical-information"></a>Diversas informações técnicas

Não há suporte para o JavaScript Object Notation (JSON) no modelo de extensibilidade do provedor do OSC.
  
Não há nenhuma dependência em um analisador XML. O provedor do OSC pode usar um analisador XML que está incluído no Office, como o Microsoft XML Core Services (MSXML), use o recursos incorporados ao Microsoft .NET Framework de análise de XML ou usar um analisador XML de terceiros. 
  
## <a name="see-also"></a>Confira também

- [Práticas recomendadas para o desenvolvimento de um provedor](best-practices-for-developing-a-provider.md)  
- [Etapas rápidas de aprendizado para desenvolver um provedor](quick-steps-for-learning-to-develop-a-provider.md)
- [Implantando um provedor](deploying-a-provider.md)  
- [Introdução ao desenvolvimento de um Outlook Social Connector Provider](getting-started-with-developing-an-outlook-social-connector-provider.md)

