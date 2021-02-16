---
title: Projetar um serviço de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 32627ebb-547f-4fac-a406-e7243ec5521b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 19a8a939685c440901f3f57d72baf673a579e590
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404292"
---
# <a name="designing-a-message-service"></a>Projetar um serviço de mensagens

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Antes de começar a escrever código para dar suporte ao serviço de mensagens, é importante criar um design. Resolva os seguintes problemas no processo de design:
  
1. Determine quantos provedores de serviços devem ser incluídos no serviço de mensagens. Inclua somente provedores de serviços relacionados (ou seja, provedores que trabalham com o mesmo sistema de mensagens) em seu serviço. Provedores de serviços não relacionados não pertencem ao mesmo serviço de mensagens. Use o perfil para integrar provedores de serviços não relacionados e serviços de mensagens.
    
2. Determine que tipo de provedores de serviços devem ser incluídos no serviço de mensagens. A maioria dos serviços de serviço inclui um provedor de cada um dos tipos comuns. Ou seja, o serviço de mensagens típico tem um provedor de agenda, um provedor de armazenamento de mensagens e um provedor de transporte.
    
3. Determine quantas DLLs devem conter o serviço de mensagens. O número de DLLs que um serviço de mensagens usa depende do seguinte:
    
   - O grau de complexidade que você, como o autor do serviço de mensagens, está disposto a lidar.
    
   - O tipo de provedores de serviços no serviço de mensagens.
    
   - A relação que o serviço de mensagens pode ter com outro serviço de mensagens.
    
   Como o MAPI armazena apenas um ponto de entrada para cada tipo de provedor, não inclua vários provedores do mesmo tipo em uma única DLL. Se fizer sentido incluir vários provedores de um tipo, implemente-os em DLLs separados ou faça com que eles compartilhem uma função de ponto de entrada. Outra opção é implementar serviços de mensagem relacionados ou serviços de mensagem que são capazes de usar o mesmo código de instalação e configuração e a mesma função de ponto de entrada de DLL, em uma DLL.
    
   Se possível, seja simples e use uma DLL que contenha a implementação de todos os provedores de serviços no serviço de mensagens e todo o código para instalar e configurar o serviço de mensagens. Se isso não for possível, você pode implementar uma DLL para o código de instalação e configuração e uma única DLL para todos os provedores de serviços ou uma DLL para cada provedor.
    
4. Determine um nome para a DLL ou DLLs do serviço de mensagens. 
    
## <a name="see-also"></a>Confira também

- [Implementação do serviço de mensagens](message-service-implementation.md)

