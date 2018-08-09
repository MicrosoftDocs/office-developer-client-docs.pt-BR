---
title: Práticas recomendadas para o desenvolvimento de um provedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22e3de8a-c4f2-41a4-a5b1-c5b1bf06f724
description: 'Você deve aderir às práticas a seguir ao desenvolver um provedor do Outlook Social Connector 2013 (OSC):'
ms.openlocfilehash: a6ee9d54f33bbc855d178aba844a8f65ec92f964
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770819"
---
# <a name="best-practices-for-developing-a-provider"></a>Práticas recomendadas para o desenvolvimento de um provedor

Você deve aderir às práticas a seguir ao desenvolver um provedor do Outlook Social Connector 2013 (OSC):
  
- Por motivos de segurança, os provedores que se comunicam com servidores pela Internet devem usar o protocolo HTTPS (Hypertext Transfer Protocol (HTTP) com a camada de soquete seguro (SSL)). Caso contrário, há um risco que endereços de email, atividades de redes sociais e outro usuário dados poderiam ser interceptados ou expostos em trânsito.
    
- Se você estiver desenvolvendo um provedor OSC para uma rede social de terceiros, seu provedor deve aderir ao termos da rede social de serviço.
    
- Para minimizar o tamanho do pacote de download do provedor, crie o provedor usando um compilador nativo como C++ ou qualquer outra ferramenta que pode construir um componente COM.
    
- Em seu provedor, crie um agente de usuário exclusiva que será enviado para a rede social para controlar as chamadas feitas pelo provedor à rede social.
    
- O método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) não deve confiar em chamadas da rede social na Internet para obter os recursos do provedor. Por exemplo, os usuários podem iniciar o Outlook offline; Se o OSC chama **GetCapabilities** e não há nenhuma conexão de rede, a chamada **GetCapabilities** não retornará válido **recursos** XML. A prática recomendada é armazenar **recursos** XML como um recurso em seu provedor. 
    
- Seu provedor OSC pode gerar um volume significativo de chamadas para uma rede social. Dependendo dos termos de serviço para a sua rede social, considere a possibilidade de cache amigos para uma pasta do Outlook para reduzir o número de chamadas do seu provedor de OSC e, em seguida, do seu provedor à rede social.
    
- Office 2013 está disponível nas versões de 32 bits e 64 bits. Versões do Office anteriores ao Office 2010 estão disponíveis apenas em uma versão de 32 bits. A instalação padrão do Office 2013 no Windows de 64 bits é de 32 bits. Se você pretende oferecer suporte à versão de 64 bits do OSC que é instalado com o Office 2013 de 64 bits, você também deve liberar uma versão de 64 bits do seu provedor. 
    
## <a name="see-also"></a>Confira também

- [Sequências de chamadas comuns do OSC](osc-typical-calling-sequences.md)  
- [Desenvolvendo um provedor com o esquema OSC XML](developing-a-provider-with-the-osc-xml-schema.md)  
- [Implantando um provedor](deploying-a-provider.md)  
- [Introdução ao desenvolvimento de um Outlook Social Connector Provider](getting-started-with-developing-an-outlook-social-connector-provider.md)

