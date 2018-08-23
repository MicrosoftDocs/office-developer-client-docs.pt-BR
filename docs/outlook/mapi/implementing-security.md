---
title: Implementar a segurança
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62db34a0-887c-4607-94ad-d8cae68b35c2
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: c2926e7c94178d5a3135f34e2ab3b3ae11d145dd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568480"
---
# <a name="implementing-security"></a>Implementar a segurança

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Se o sistema de mensagens exigir, o provedor de transporte é responsável por implementar um nível apropriado de segurança de acesso ao sistema de mensagens. Cada mensagem de entrada ou saída enviada através de um provedor de transporte pelo spooler MAPI é manipulada no contexto de uma sessão de logon do provedor. O provedor de transporte pode exibir uma caixa de diálogo de logon para o usuário que solicita credenciais do usuário antes de estabelecer uma conexão tal. Como alternativa, o provedor de transporte pode armazenar as credenciais do usuário inseridos anteriormente no intervalo propriedade segura dentro de uma seção de perfil e usá-los para o access sem avisar.
  
Ao implementar a segurança do seu provedor de transporte, considere o seguinte:
  
- Com vários provedores de serviço instalado, pode haver uma infinidade de nomes e senhas associadas a um usuário.
    
- MAPI permite várias sessões com várias identidades. Provedores são incentivados a oferecer suporte a várias sessões, mas não são necessários para fazê-lo.
    
- Cada sessão com um provedor de transporte está associada por MAPI uma seção discreta no perfil do usuário. O provedor de transporte pode usar o método [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) para acessar os nesta seção, que pode ser usada para armazenar informações associadas a essa sessão, inclusive as credenciais. 
    
- Com vários provedores de transporte instalados, não é necessariamente verdadeiro se o usuário tem somente um único endereço de email. Um usuário pode ter um endereço de email separados para cada provedor de transporte instalados ou pode ter um endereço diferente para cada sessão em um único provedor.
    
Para obter mais informações sobre como armazenar credenciais nas seções de perfil, consulte [Serviços de mensagem e perfis](message-services-and-profiles.md) e [IProfSect: IMAPIProp](iprofsectimapiprop.md).
  

