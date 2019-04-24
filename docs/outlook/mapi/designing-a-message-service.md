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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316720"
---
# <a name="designing-a-message-service"></a>Projetar um serviço de mensagens

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Antes de começar a escrever código para dar suporte ao serviço de mensagens, é importante criar um design. Resolva os seguintes problemas no seu processo de design:
  
1. Determinar quantos provedores de serviços devem ser incluídos no serviço de mensagens. Inclua somente provedores de serviços relacionados (ou seja, provedores que funcionam com o mesmo sistema de mensagens) em seu serviço. Os provedores de serviços não relacionados não pertencem ao mesmo serviço de mensagens. Use o perfil para integrar provedores de serviço não relacionados e serviços de mensagens.
    
2. Determine que tipo de provedores de serviço deve ser incluído no serviço de mensagens. A maioria dos serviços do messge inclui um provedor de cada tipo comum. Ou seja, o serviço de mensagens típico tem um provedor de catálogo de endereços, um provedor de armazenamento de mensagens e um provedor de transporte.
    
3. Determinar quantas DLLs devem conter o serviço de mensagens. O número de DLLs que um serviço de mensagens usa depende do seguinte:
    
   - O grau de complexidade que você como o escritor do serviço de mensagens está disposto a lidar.
    
   - O tipo de provedores de serviço no serviço de mensagens.
    
   - A relação que o serviço de mensagens pode ter com outro serviço de mensagens.
    
   Como o MAPI armazena somente um ponto de entrada para cada tipo de provedor, não inclua vários provedores do mesmo tipo em uma única DLL. Se fizer sentido incluir vários provedores de um tipo, implemente-os em DLLs separadas ou peça que compartilhem uma função de ponto de entrada. Outra opção é implementar serviços de mensagens relacionados ou serviços de mensagens que possam usar o mesmo código de instalação e configuração e a mesma função de ponto de entrada DLL, em uma DLL.
    
   Se possível, mantenha-o simples e use uma DLL que contenha a implementação de todos os provedores de serviços no serviço de mensagens e todo o código para instalar e configurar o serviço de mensagens. Se isso não for possível, você poderá implementar uma DLL para o código de instalação e configuração e uma única DLL para todos os provedores de serviços ou uma DLL para cada provedor.
    
4. Determine o nome da DLL ou DLLs do serviço de mensagens. 
    
## <a name="see-also"></a>Confira também

- [Implementação do serviço de mensagens](message-service-implementation.md)

