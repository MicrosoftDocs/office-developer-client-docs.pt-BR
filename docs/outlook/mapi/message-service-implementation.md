---
title: Implementação do serviço de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb529cc7-ad09-4f86-89bc-0e8ad29a3f38
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6ba2f9542fd021c544d73d8208ed356a7bf95309
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768127"
---
# <a name="message-service-implementation"></a>Implementação do serviço de mensagens

  
  
**Aplica-se a**: Outlook 
  
Um serviço de mensagem é um ou mais provedores de serviço relacionado agrupados para fins de simplifica a instalação e configuração. Todos os provedores de serviço devem ser incluídos em um serviço de mensagem.
  
Para implementar um serviço de mensagem com um ou mais provedores, use o procedimento a seguir:
  
1. Projete o serviço de mensagem, determinando o número e tipo de provedores de serviço a serem incluídas. Para obter mais informações sobre como projetar um serviço de mensagem, consulte [Criando um serviço de mensagem](designing-a-message-service.md).
    
2. Crie um programa de instalação para instalar os provedores de serviço no serviço de mensagem. Para obter mais informações sobre como escrever um programa de instalação do serviço de mensagem, consulte [Instalação do serviço de mensagem com suporte](supporting-message-service-installation.md). 
    
3. Crie uma função de ponto de entrada para executar a configuração. Para obter mais informações sobre como escrever uma entrada de serviço de mensagem ponto função, consulte [Configuração do serviço de mensagem com suporte](supporting-message-service-configuration.md) e [MSGSERVICEENTRY](msgserviceentry.md). 
    
4. Crie um arquivo de cabeçalho público que contém as marcas de propriedade e descrições dos valores válidos para quaisquer propriedades personalizadas que suporta o serviço de mensagem. 
    
## <a name="see-also"></a>Confira também



[Provedores de serviços MAPI](mapi-service-providers.md)

