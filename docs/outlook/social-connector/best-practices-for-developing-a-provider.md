---
title: Práticas recomendadas para o desenvolvimento de um provedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22e3de8a-c4f2-41a4-a5b1-c5b1bf06f724
description: 'Você deve cumprir as seguintes práticas ao desenvolver um provedor do Outlook Social Connector 2013 (OSC):'
ms.openlocfilehash: 6a48a56d8065fb9a176ca6527340c99551cdb52a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425915"
---
# <a name="best-practices-for-developing-a-provider"></a>Práticas recomendadas para o desenvolvimento de um provedor

Você deve cumprir as seguintes práticas ao desenvolver um provedor do Outlook Social Connector 2013 (OSC):
  
- Por motivos de segurança, os provedores que se comunicam com servidores pela Internet devem usar o protocolo HTTPS (Hypertext Transfer Protocol (HTTP) com Secure Socket Layer (SSL)). Caso contrário, há um risco de que endereços de email, atividades de rede social e outros dados de usuário possam ser interceptados ou expostos enquanto estão em trânsito.
    
- Se você estiver desenvolvendo um provedor do OSC para uma rede social de terceiros, seu provedor deve cumprir os termos de serviço da rede social.
    
- Para minimizar o tamanho do pacote de download do provedor, crie o provedor usando um compilador nativo como C++ ou qualquer outra ferramenta que possa criar um componente COM.
    
- Em seu provedor, crie um agente de usuário exclusivo que é enviado para a rede social para rastrear as chamadas feitas pelo provedor para a rede social.
    
- O método [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md) não deve depender de chamar a rede social pela Internet para obter os recursos do provedor. Por exemplo, os usuários podem iniciar o Outlook offline; Se o OSC chamar **GetCapabilities** e não houver conexão de rede, a **** chamada GetCapabilities não retornará XML de **recursos** válidos. A prática recomendada é armazenar o XML de **recursos** como um recurso no provedor. 
    
- O provedor do OSC pode gerar um volume significativo de chamadas para uma rede social. Dependendo dos termos de serviço da sua rede social, considere o armazenamento em cache de amigos para uma pasta do Outlook a fim de reduzir o número de chamadas do OSC para o seu provedor e, por sua vez, de seu provedor para a rede social.
    
- O Office 2013 está disponível nas versões de 32 bits e 64 bits. As versões do Office anteriores ao Office 2010 estão disponíveis somente em uma versão de 32 bits. A instalação padrão do Office 2013 no Windows de 64 bits é de 32 bits. Se você pretende oferecer suporte à versão de 64 bits do OSC que é instalada com o Office de 64 bits 2013, você também deve liberar uma versão de 64 bits do provedor. 
    
## <a name="see-also"></a>Confira também

- [Sequências de chamada típicas do OSC](osc-typical-calling-sequences.md)  
- [Desenvolver um provedor com o esquema XML do OSC](developing-a-provider-with-the-osc-xml-schema.md)  
- [Implantar um provedor](deploying-a-provider.md)  
- [Introdução ao desenvolvimento de um provedor de serviços do Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

