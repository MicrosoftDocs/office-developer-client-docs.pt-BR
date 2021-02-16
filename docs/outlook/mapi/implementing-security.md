---
title: Implementando a segurança
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62db34a0-887c-4607-94ad-d8cae68b35c2
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c430160ee508a86f36d840c7916c0516cfc10fbd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417284"
---
# <a name="implementing-security"></a>Implementando a segurança

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Se o sistema de mensagens exigir, o provedor de transporte será responsável pela implementação de um nível apropriado de segurança para acessar o sistema de mensagens. Cada mensagem de entrada ou saída enviada por um provedor de transporte pelo spooler MAPI é tratada no contexto de uma sessão de logon do provedor. O provedor de transporte pode exibir uma caixa de diálogo de logon para o usuário solicitando as credenciais de um usuário antes de estabelecer essa conexão. Como alternativa, o provedor de transporte pode armazenar as credenciais inseridas anteriormente pelo usuário no intervalo de propriedades seguras dentro de uma seção de perfil e usá-las para acesso sem aviso.
  
Ao implementar a segurança do provedor de transporte, considere o seguinte:
  
- Com vários provedores de serviços instalados, pode haver uma infinidade de nomes e senhas associados a um usuário.
    
- O MAPI permite várias sessões com várias identidades. Os provedores são incentivados a dar suporte a várias sessões, mas não são obrigados a fazê-lo.
    
- Cada sessão com um provedor de transporte é associada por MAPI com uma seção discreta no perfil do usuário. O provedor de transporte pode usar o método [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) para obter acesso a esta seção, que pode ser usada para armazenar qualquer informação associada a esta sessão, incluindo credenciais. 
    
- Com vários provedores de transporte instalados, não é necessariamente verdadeiro que o usuário tenha apenas um único endereço de email. Um usuário pode ter um endereço de email separado para cada provedor de transporte instalado ou pode ter um endereço diferente para cada sessão em um único provedor.
    
Para obter mais informações sobre como armazenar credenciais em seções de perfil, consulte Message [Services and Profiles](message-services-and-profiles.md) and [IProfSect : IMAPIProp](iprofsectimapiprop.md).
  

