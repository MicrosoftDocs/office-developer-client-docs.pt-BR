---
title: Novidades para provedores
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 92f59a0d-3834-424d-ad81-167fdeba9bd0
description: Este tópico lista as principais alterações no Outlook Social Connector 2013 (OSC). Ele apresenta uma comparação dos recursos disponíveis entre o Outlook Social Connector 2013 e o Outlook Social Connector 1,1.
ms.openlocfilehash: 6b735555d312c149d7dc8b827990b96bfc229678
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435450"
---
# <a name="whats-new-for-providers"></a>Novidades para provedores

Este tópico lista as principais alterações no Outlook Social Connector 2013 (OSC). Ele apresenta uma comparação dos recursos disponíveis entre o Outlook Social Connector 2013 e o Outlook Social Connector 1,1. Também descreve membros de interface e elementos XML que foram adicionados, alterados ou preteridos. 
  
No Office 2013, o OSC funciona com não apenas o Outlook, mas também o SharePoint Server, o SharePoint Workspace, o cliente do Lync e todos os outros aplicativos cliente do Office que dão suporte a informações de presença e ao cartão de visita. Um provedor do OSC pode trazer as atualizações de informações sociais na guia **What ' s New** no painel de pessoas do Outlook, bem como no cartão de visita. 
  
Algumas alterações importantes no Outlook Social Connector 2013 incluem o seguinte: 
  
- Se um provedor oferecer suporte à exibição de atividades, o provedor sempre sincronizará as atividades sob demanda e não mais se redepender de atividades previamente armazenadas em cache. Isso significa que o provedor armazena atividades de amigos e não amigos na memória para exibir mais atividades atuais.
    
- Por motivos de segurança, os provedores que se comunicam com servidores pela Internet devem usar o protocolo HTTPS (Hypertext Transfer Protocol (HTTP) com Secure Socket Layer (SSL)). Caso contrário, há um risco de que endereços de email, atividades de rede social e outros dados de usuário sejam interceptados ou expostos enquanto estiverem em trânsito.
    
- Se você tiver provedores que funcionam com uma versão anterior do Outlook, para oferecer suporte ao Office 2013, você deve atualizar o pacote de instalação. Consulte a [lista de verificação de instalação](installation-checklist.md) para obter mais informações. 
    
A tabela a seguir mostra a disponibilidade de vários recursos no Outlook Social Connector 2013 em comparação com o conector social do Outlook 1,1.
  
|**Recurso**|**Outlook Social Connector 2013**|**Outlook Social Connector 1,1**|
|:-----|:-----|:-----|
|Interface de usuário final  <br/> |SharePoint Server, SharePoint Workspace, Lync Client, cartão de contato em todos os aplicativos clientes do Office e no painel de pessoas no Outlook  <br/> |Painel de pessoas no Outlook  <br/> |
|Autenticação básica  <br/> |Sim  <br/> |Sim  <br/> |
|Autenticação baseada em formulários  <br/> |Sim  <br/> |Sim  <br/> |
|Autenticação em cache  <br/> |Sim  <br/> |Sim  <br/> |
|Sincronização em cache para amigos na pasta contatos no repositório padrão  <br/> |Sim  <br/> |Sim  <br/> |
|Sincronização de atividades em cache para amigos na pasta de **News Feed** oculta  <br/> |Não  <br/> |Sim  <br/> |
|Sincronização sob demanda (imagem, nome, título) para amigos e não amigos na rede  <br/> |Sim  <br/> |Sim  <br/> |
|Sincronização de atividades sob demanda para amigos e não amigos na rede  <br/> |Sim  <br/> |Sim  <br/> |
|Acompanhar na rede  <br/> |Sim  <br/> |Sim  <br/> |
|Não acompanhar na rede  <br/> |Sim  <br/> |Sim  <br/> |
|Página visitar perfil de usuário  <br/> |Por meio de um link  <br/> |Por um crachá de rede  <br/> |
|Observar as configurações de privacidade na rede social (por exemplo, exibir perfil e atividades de não-amigos que permitem a visualização de tais)  <br/> |Sim  <br/> |Sim  <br/> |
|Endereços de email com hash passados ao provedor  <br/> |Sim  <br/> |Sim  <br/> |

<a name="OlSocialConnector_Changes"> </a>

## <a name="changes-from-the-previous-version-of-osc-provider-extensibility"></a>Alterações da versão anterior da extensibilidade do provedor OSC

A tabela a seguir mostra os membros que foram adicionados ou substituídos da interface correspondente.
  
|**Interface e membro**|**Comment**|
|:-----|:-----|
|**ISocialProfile::GetActivitiesOfFriendsAndColleagues** <br/> |PreTerido no Outlook Social Connector 2013. Observe que **ISocialSession:: getactivities** também foi preterido desde o Outlook Social Connector 1,1.  <br/> Para sincronizar feeds de atividades, você deve implementar o método [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) . Defina **dynamicActivitiesLookupEx** como **true**, que solicitará que o OSC chame **ISocialSession2:: GetActivitiesEx** em vez disso.  <br/> |
   
A tabela a seguir mostra os elementos do esquema que foram alterados.
  
|**Elemento Schema**|**Comment**|
|:-----|:-----|
|**poderosos** <br/> |Adicionado ao Outlook Social Connector 2013: elemento **allowChangesToAutoConfigure** .  <br/> PreTerido no Outlook Social Connector 2013: elemento **cacheActivities** .  <br/> |
|**person** <br/> |Adicionado ao Outlook Social Connector 2013: **askmeabout**, **businessAddress**, **businessCity**, **businessCountryOrRegion**, **businessstate**, **businessZip**, **indústrias**, **interesses**, ** local**, **otherAddress**, **otherCity**, **otherCountryOrRegion**, **otherstate**, **otherZip**, **Skills**, **escolas**e elementos de **site** .  <br/> |
   
## <a name="see-also"></a>Confira também

- [XML para recursos](xml-for-capabilities.md)
- [XML para amigos](xml-for-friends.md)
- [Introdução ao desenvolvimento de um provedor de serviços do Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

