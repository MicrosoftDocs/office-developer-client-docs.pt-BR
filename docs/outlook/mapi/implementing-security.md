---
title: Implementando a segurança
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62db34a0-887c-4607-94ad-d8cae68b35c2
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: f09d96fd8b35df6cafa81b3830642cf6d67806e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767445"
---
# <a name="implementing-security"></a>Implementando a segurança

  
  
**Aplica-se a**: Outlook 
  
Se o sistema de mensagens exigir, o provedor de transporte é responsável por implementar um nível apropriado de segurança de acesso ao sistema de mensagens. Cada mensagem de entrada ou saída enviada através de um provedor de transporte pelo spooler MAPI é manipulada no contexto de uma sessão de logon do provedor. O provedor de transporte pode exibir uma caixa de diálogo de logon para o usuário que solicita credenciais do usuário antes de estabelecer uma conexão tal. Como alternativa, o provedor de transporte pode armazenar as credenciais do usuário inseridos anteriormente no intervalo propriedade segura dentro de uma seção de perfil e usá-los para o access sem avisar.
  
Ao implementar a segurança do seu provedor de transporte, considere o seguinte:
  
- Com vários provedores de serviço instalado, pode haver uma infinidade de nomes e senhas associadas a um usuário.
    
- MAPI permite várias sessões com várias identidades. Provedores são incentivados a oferecer suporte a várias sessões, mas não são necessários para fazê-lo.
    
- Cada sessão com um provedor de transporte está associada por MAPI uma seção discreta no perfil do usuário. O provedor de transporte pode usar o método [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) para acessar os nesta seção, que pode ser usada para armazenar informações associadas a essa sessão, inclusive as credenciais. 
    
- Com vários provedores de transporte instalados, não é necessariamente verdadeiro se o usuário tem somente um único endereço de email. Um usuário pode ter um endereço de email separados para cada provedor de transporte instalados ou pode ter um endereço diferente para cada sessão em um único provedor.
    
Para obter mais informações sobre como armazenar credenciais nas seções de perfil, consulte [Serviços de mensagem e perfis](message-services-and-profiles.md) e [IProfSect: IMAPIProp](iprofsectimapiprop.md).
  

