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
ms.openlocfilehash: 1e64241008a4adde4431b2c9683199294f21e396
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330230"
---
# <a name="administering-profiles-and-message-services"></a>Administrar perfis e serviços de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O perfil e a administração do serviço de mensagens podem envolver a criação de novos perfis, a exclusão de perfis antigos e a modificação do conteúdo de perfis existentes alterando os serviços de mensagens e provedores de serviços contidos neles. Nem todos os clientes dão suporte à administração de perfis e serviços de mensagens como recursos padrão. Alguns clientes não têm mais a ver com perfis do que permitem que os usuários selecionem um no momento do logon.
  
Se você oferecer suporte à administração de perfil ou serviço de mensagens, é provável que você use as seguintes interfaces implementadas por MAPI:
  
- [IMsgServiceAdmin: IUnknown](imsgserviceadminiunknown.md) para administrar um serviço de mensagens em um perfil, acessível por meio de [IMAPISession: adminservices](imapisession-adminservices.md) ou [IProfAdmin:: adminservices](iprofadmin-adminservices.md). Os clientes de mensagens normalmente chamam o **IMAPISession** de clientes de configuração, ou clientes que não enviam ou recebem mensagens, chamam **IProfAdmin**. Sempre que possível, chame o método **IProfAdmin** porque ele não faz com que o serviço de mensagem seja iniciado. Para obter mais informações sobre como usar a interface **IMsgServiceAdmin** , consulte os seguintes tópicos: Configurando [um serviço de mensagens](configuring-a-message-service.md), [copiando um serviço de mensagens](copying-a-message-service.md)e excluindo [um serviço de mensagens](deleting-a-message-service.md).
    
- [IProfAdmin: IUnknown](iprofadminiunknown.md) para administrar um perfil, acessível através da função [MAPIAdminProfiles](mapiadminprofiles.md) . Para obter mais informações sobre como usar a interface **IProfAdmin** , consulte os seguintes tópicos: [criando um perfil usando código personalizado](creating-a-profile-by-using-custom-code.md), [copiando](copying-a-profile.md)um perfil, excluindo um [perfil](deleting-a-profile.md), [encontrando um nome de perfil](finding-a-profile-name.md)e [definindo um Perfil padrão](setting-a-default-profile.md).
    
- [IProfSect: IMAPIProp](iprofsectimapiprop.md) para manter as propriedades em uma seção de perfil, acessível através do método [IMAPISession:: OpenProfileSection](imapisession-openprofilesection.md) ou [IProviderAdmin:: OpenProfileSection](iprovideradmin-openprofilesection.md) . Para obter mais informações sobre seções de perfil, consulte [MAPI](mapi-profiles.md)Profiles.
    
- [IProviderAdmin: IUnknown](iprovideradminiunknown.md) para administrar os provedores de serviço em um serviço de mensagens, acessível através de [IMsgServiceAdmin:: AdminProviders](imsgserviceadmin-adminproviders.md). Para obter mais informações sobre como usar a interface **IProviderAdmin** , confira [Adicionar ou excluir provedores em um serviço de mensagens](adding-or-deleting-providers-in-a-message-service.md).
    
Tenha cuidado ao dar suporte à administração de perfis e serviços de mensagens. Não há garantias de proteção contra a modificação adversa de um perfil que está em uso. O MAPI pode impedir a exclusão de um perfil em uso, mas não pode impedir a exclusão de todos os serviços de mensagens. Se você excluir todos os serviços de mensagens em um perfil, todos os provedores de serviços desses serviços serão interrompidos, fazendo com que ocorram resultados imprevisíveis.
  
## <a name="in-this-section"></a>Nesta seção

[Criar um perfil](creating-a-profile.md)
  
> Descreve como criar um perfil.
    
[Copiar um perfil](copying-a-profile.md)
  
> Descreve como copiar um perfil.
    
[Excluir um perfil](deleting-a-profile.md)
  
> Descreve como excluir um perfil.
    
[ConFigurando um perfil padrão](setting-a-default-profile.md)
  
> Descreve como definir um perfil padrão.
    
[Localizar um nome de perfil](finding-a-profile-name.md)
  
> Descreve como localizar o nome de um perfil.
    
[Adicionar um serviço de mensagens](adding-a-message-service.md)
  
> Descreve como adicionar um serviço de mensagens.
    
[ConFigurando um serviço de mensagens](configuring-a-message-service.md)
  
> Descreve como configurar um serviço de mensagens.
    
[Copiar um serviço de mensagens](copying-a-message-service.md)
  
> Descreve como copiar um serviço de mensagens para um perfil.
    
[Excluir um serviço de mensagens](deleting-a-message-service.md)
  
> Descreve como excluir um serviço de mensagens.
    
[Adicionar ou excluir provedores em um serviço de mensagens](adding-or-deleting-providers-in-a-message-service.md)
  
> Descreve como adicionar ou excluir provedores em um serviço de mensagens.
    

