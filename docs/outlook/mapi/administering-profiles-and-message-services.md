---
title: Administrar perfis e serviços de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89a2ac43-9601-47fc-b736-db48585fe879
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 124f4875834e035e29d4c63e52789bf07f18258d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587541"
---
# <a name="administering-profiles-and-message-services"></a>Administrar perfis e serviços de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Perfil e a mensagem de administração do serviço pode envolver a criação de novos perfis, excluindo perfis antigos e modificar o conteúdo de perfis existentes, alterando os serviços de mensagem e os provedores de serviço contidos neles. Nem todos os clientes suportam administração do serviço de perfil e a mensagem como recursos padrão. Alguns clientes têm nada mais fazer com os perfis de permitir que os usuários selecionem um momento de logon.
  
Caso você ofereça suporte a administração do serviço de perfil ou mensagem, as chances são que você usará as seguintes interfaces que são implementadas pelo MAPI:
  
- [IMsgServiceAdmin: IUnknown](imsgserviceadminiunknown.md) para administrar um serviço de mensagem em um perfil, acessível através do [IMAPISession::AdminServices](imapisession-adminservices.md) ou [IProfAdmin::AdminServices](iprofadmin-adminservices.md). Clientes de mensagens normalmente chama **IMAPISession** durante a configuração de clientes ou clientes que não enviar ou receber mensagens, chame **IProfAdmin**. Sempre que possível, chame o método de **IProfAdmin** porque ele não faz com que o serviço de mensagem a ser iniciado. Para obter mais informações sobre como usar a interface **IMsgServiceAdmin** , consulte os seguintes tópicos: [Configurar um serviço de mensagem](configuring-a-message-service.md), [copiando um serviço de mensagem](copying-a-message-service.md)e [Excluindo um serviço de mensagem](deleting-a-message-service.md).
    
- [IProfAdmin: IUnknown](iprofadminiunknown.md) para administrar um perfil, acessado por meio da função [MAPIAdminProfiles](mapiadminprofiles.md) . Para obter mais informações sobre como usar a interface **IProfAdmin** , consulte os seguintes tópicos: [criação de um perfil usando código de sinalizador](creating-a-profile-by-using-custom-code.md), [copiando um perfil](copying-a-profile.md), [exclusão de um perfil](deleting-a-profile.md), [encontrando um nome de perfil](finding-a-profile-name.md)e [configuração um Perfil padrão](setting-a-default-profile.md).
    
- [IProfSect: IMAPIProp](iprofsectimapiprop.md) para manter as propriedades em uma seção de perfil, acessada por meio do método [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) ou [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) . Para obter mais informações sobre as seções de perfil, consulte [Perfis MAPI](mapi-profiles.md).
    
- [IProviderAdmin: IUnknown](iprovideradminiunknown.md) para administrar os provedores de serviços em um serviço de mensagem, acessível através do [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md). Para obter mais informações sobre como usar a interface **IProviderAdmin** , consulte [adicionando ou excluindo provedores em um serviço de mensagem](adding-or-deleting-providers-in-a-message-service.md).
    
Tenha cuidado no seu suporte da administração do serviço de perfil e mensagem. Não há nenhuma proteções para proteger contra adversamente para modificar um perfil que está em uso. MAPI pode impedir a exclusão de um perfil em uso, mas não pode impedir a exclusão de cada serviço de mensagem nela. Se você excluir cada serviço de mensagem em um perfil, todos os provedores de serviço nesses serviços irá parar causando assim resultados imprevisíveis ocorra.
  
## <a name="in-this-section"></a>Nesta seção

[Criação de um perfil](creating-a-profile.md)
  
> Descreve como criar um perfil.
    
[Copiando um perfil](copying-a-profile.md)
  
> Descreve como copiar um perfil.
    
[Exclusão de um perfil](deleting-a-profile.md)
  
> Descreve como excluir um perfil.
    
[Definir um perfil padrão](setting-a-default-profile.md)
  
> Descreve como definir um perfil padrão.
    
[Localizando um nome de perfil](finding-a-profile-name.md)
  
> Descreve como localizar um nome de um perfil.
    
[Adição de um serviço de mensagem](adding-a-message-service.md)
  
> Descreve como adicionar um serviço de mensagem.
    
[Configurando um serviço de mensagem](configuring-a-message-service.md)
  
> Descreve como configurar um serviço de mensagem.
    
[Copiar um serviço de mensagem](copying-a-message-service.md)
  
> Descreve como copiar um serviço de mensagem para um perfil.
    
[Excluindo um serviço de mensagem](deleting-a-message-service.md)
  
> Descreve como excluir um serviço de mensagem.
    
[Adicionando ou excluindo provedores em um serviço de mensagem](adding-or-deleting-providers-in-a-message-service.md)
  
> Descreve como adicionar ou excluir provedores em um serviço de mensagem.
    

