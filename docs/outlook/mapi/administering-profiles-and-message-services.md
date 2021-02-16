---
title: Administrando perfis e serviços de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89a2ac43-9601-47fc-b736-db48585fe879
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1e64241008a4adde4431b2c9683199294f21e396
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410557"
---
# <a name="administering-profiles-and-message-services"></a>Administrando perfis e serviços de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A administração de perfil e serviço de mensagens pode envolver a criação de novos perfis, a exclusão de perfis antigos e a modificação do conteúdo de perfis existentes, alterando os serviços de mensagens e os provedores de serviços contidos neles. Nem todos os clientes suportam a administração de perfil e serviço de mensagens como recursos padrão. Alguns clientes não têm nada mais a ver com perfis do que permitir que seus usuários selecionem um no momento do logon.
  
Se você tiver suporte para a administração de perfil ou serviço de mensagens, provavelmente usará as seguintes interfaces implementadas pelo MAPI:
  
- [IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md) para administrar um serviço de mensagem em um perfil, acessível por meio de [IMAPISession::AdminServices](imapisession-adminservices.md) ou [IProfAdmin::AdminServices](iprofadmin-adminservices.md). Clientes de mensagens normalmente chamam **IMAPISession** enquanto clientes de configuração, ou clientes que não enviam ou recebem mensagens, chamam **IProfAdmin**. Sempre que possível, chame **o método IProfAdmin** porque ele não faz com que o serviço de mensagens seja iniciado. Para obter mais informações sobre como usar a interface **IMsgServiceAdmin,** consulte os seguintes tópicos: [Configuring a Message Service](configuring-a-message-service.md), [Copying a Message Service](copying-a-message-service.md), and [Deleting a Message Service](deleting-a-message-service.md).
    
- [IProfAdmin : IUnknown](iprofadminiunknown.md) para administrar um perfil, acessível por meio da [função MAPIAdminProfiles.](mapiadminprofiles.md) For more information about using the **IProfAdmin** interface, see the following topics: [Creating a Profile by Using Custom Code](creating-a-profile-by-using-custom-code.md), [Copying a Profile](copying-a-profile.md), [Deleting a Profile](deleting-a-profile.md), Finding a Profile [Name](finding-a-profile-name.md), and Setting a [Default Profile](setting-a-default-profile.md).
    
- [IProfSect : IMAPIProp](iprofsectimapiprop.md) para manter as propriedades em uma seção de perfil, acessível por meio do método [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) ou [IProviderAdmin::OpenProfileSection.](iprovideradmin-openprofilesection.md) Para obter mais informações sobre seções de perfil, consulte [Perfis MAPI.](mapi-profiles.md)
    
- [IProviderAdmin : IUnknown](iprovideradminiunknown.md) para administrar os provedores de serviço em um serviço de mensagens, acessível por meio de [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md). Para obter mais informações sobre como usar a interface **IProviderAdmin,** consulte Adicionando ou [excluindo provedores em um serviço de mensagens.](adding-or-deleting-providers-in-a-message-service.md)
    
Tenha cuidado com o suporte à administração de perfil e serviço de mensagens. Não há proteções para proteger contra modificação adversa de um perfil que está em uso. MAPI can prevent you from deleting a profile in use, but cannot prevent you from deleting every message service in it. Se você excluir todos os serviços de mensagens em um perfil, todos os provedores de serviços nesses serviços param de causar resultados imprevisíveis.
  
## <a name="in-this-section"></a>Nesta seção

[Criando um perfil](creating-a-profile.md)
  
> Descreve como criar um perfil.
    
[Copiando um perfil](copying-a-profile.md)
  
> Descreve como copiar um perfil.
    
[Excluindo um perfil](deleting-a-profile.md)
  
> Descreve como excluir um perfil.
    
[Definindo um perfil padrão](setting-a-default-profile.md)
  
> Descreve como definir um perfil padrão.
    
[Localizar um nome de perfil](finding-a-profile-name.md)
  
> Descreve como encontrar o nome de um perfil.
    
[Adicionando um serviço de mensagens](adding-a-message-service.md)
  
> Descreve como adicionar um serviço de mensagens.
    
[Configurando um serviço de mensagens](configuring-a-message-service.md)
  
> Descreve como configurar um serviço de mensagens.
    
[Copiando um serviço de mensagens](copying-a-message-service.md)
  
> Descreve como copiar um serviço de mensagens para um perfil.
    
[Excluindo um serviço de mensagens](deleting-a-message-service.md)
  
> Descreve como excluir um serviço de mensagens.
    
[Adicionando ou excluindo provedores em um serviço de mensagens](adding-or-deleting-providers-in-a-message-service.md)
  
> Descreve como adicionar ou excluir provedores em um serviço de mensagens.
    

