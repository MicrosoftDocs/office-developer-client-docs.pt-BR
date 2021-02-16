---
title: Implementação do serviço de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb529cc7-ad09-4f86-89bc-0e8ad29a3f38
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ef3820afbd4ae7ff04a3f54071e56f4e0a856109
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434029"
---
# <a name="message-service-implementation"></a>Implementação do serviço de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um serviço de mensagens é um ou mais provedores de serviços relacionados agrupados para simplificar a instalação e a configuração. Todos os provedores de serviços devem ser incluídos em um serviço de mensagens.
  
Para implementar um serviço de mensagens com um ou mais provedores, use o procedimento a seguir:
  
1. Projete o serviço de mensagens, determinando o número e o tipo de provedores de serviços a serem incluídos. Para obter mais informações sobre como projetar um serviço de mensagem, consulte [Designing a Message Service](designing-a-message-service.md).
    
2. Crie um programa de instalação para instalar os provedores de serviços no serviço de mensagens. Para obter mais informações sobre como escrever um programa de configuração de serviço de mensagens, consulte [Suporte à instalação do serviço de mensagens.](supporting-message-service-installation.md) 
    
3. Crie uma função de ponto de entrada para executar a configuração. Para obter mais informações sobre como escrever uma função de ponto de entrada do serviço de mensagens, consulte Suporte à configuração do serviço de mensagens [e](supporting-message-service-configuration.md) [MSGSERVICEENTRY](msgserviceentry.md). 
    
4. Crie um arquivo de título público que contenha as marcas de propriedade e descrições de valores válidos para quaisquer propriedades personalizadas compatíveis com o serviço de mensagens. 
    
## <a name="see-also"></a>Confira também



[Provedores de Serviços MAPI](mapi-service-providers.md)

