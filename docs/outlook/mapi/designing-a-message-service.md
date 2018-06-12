---
title: Projetar um serviço de mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 32627ebb-547f-4fac-a406-e7243ec5521b
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 04aa4348560396c8237811252fd96a2b461cd791
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766391"
---
# <a name="designing-a-message-service"></a>Projetar um serviço de mensagem

**Aplica-se a**: Outlook 
  
Antes de começar a escrever código para suportar o seu serviço de mensagem, é importante criar um design. Resolva os seguintes problemas em seu processo de design:
  
1. Determine quantos provedores de serviço devem ser incluídos no serviço de mensagem. Inclua apenas a provedores de serviço relacionado (ou seja, provedores que funcionam com o mesmo sistema de mensagens) em seu serviço. O mesmo serviço de mensagem não pertencem a provedores de serviços não relacionados. Use o perfil para a integração de serviços de mensagem e provedores de serviços não relacionados.
    
2. Determine que tipo de provedores de serviço deve ser incluído no serviço de mensagem. A maioria dos serviços de messge incluir um provedor de cada um dos tipos comuns. Ou seja, o serviço de mensagem típica tem o provedor de catálogo de endereços de um provedor de armazenamento de uma mensagem e provedor de transporte de um.
    
3. Determinar quantos DLLs deve conter o serviço de mensagem. O número de DLLs que usa um serviço de mensagem depende dos seguintes fatores:
    
   - O grau de complexidade que você, como o autor do serviço de mensagem está dispostos a lidar com.
    
   - O tipo de provedores de serviço no serviço de mensagem.
    
   - A relação entre o serviço de mensagem pode ter com outro serviço de mensagem.
    
   Como o MAPI armazena o ponto de entrada apenas um para cada tipo de provedor, não inclua vários provedores do mesmo tipo em uma única DLL. Se fizer sentido para incluir vários provedores de um tipo, implementá-las em DLLs separadas ou compartilhando uma função de ponto de entrada. Outra opção é a implementação de serviços de mensagem relacionadas ou serviços de mensagem que são capazes de usar a mesma instalação e o ponto de código de configuração e a mesma entrada DLL função, em uma DLL.
    
   Se possível, mantenha a simplicidade e usar uma DLL que contém a implementação de todos os provedores de serviço no serviço de mensagem e todo o código para instalar e configurar o serviço de mensagem. Se isso não for possível, você pode implementar uma DLL para o código de instalação e configuração e a uma única DLL para todos os provedores de serviço ou uma DLL para cada provedor.
    
4. Determine um nome para o serviço de mensagem DLL ou DLLs. 
    
## <a name="see-also"></a>Confira também

- [Implementação do serviço de mensagem](message-service-implementation.md)

