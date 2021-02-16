---
title: Novidades para provedores
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 92f59a0d-3834-424d-ad81-167fdeba9bd0
description: Este tópico lista as principais alterações no Outlook Social Connector 2013 (OSC). Ele apresenta uma comparação dos recursos disponíveis entre o Outlook Social Connector 2013 e o Outlook Social Connector 1.1.
ms.openlocfilehash: 6b735555d312c149d7dc8b827990b96bfc229678
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435450"
---
# <a name="whats-new-for-providers"></a>Novidades para provedores

Este tópico lista as principais alterações no Outlook Social Connector 2013 (OSC). Ele apresenta uma comparação dos recursos disponíveis entre o Outlook Social Connector 2013 e o Outlook Social Connector 1.1. Ele também descreve os membros da interface e os elementos XML que foram adicionados, alterados ou preterido. 
  
No Office 2013, o OSC funciona não apenas com o Outlook, mas também com o SharePoint Server, o SharePoint Workspace, o cliente do Lync e todos os outros aplicativos cliente do Office que suportam informações de presença e o Cartão de Visita. Um provedor do OSC pode surgir  atualizações de informações sociais na guia NOVIDADES no Painel de Pessoas do Outlook, bem como no Cartão de Visita. 
  
Algumas alterações importantes no Outlook Social Connector 2013 incluem o seguinte: 
  
- Se um provedor suportar a exibição de atividades, o provedor sempre sincroniza atividades sob demanda e não depende mais de atividades armazenadas em cache anteriormente. Isso significa que o provedor armazena atividades de amigos e não amigos na memória para exibir atividades mais atuais.
    
- Por motivos de segurança, os provedores que se comunicam com servidores pela Internet devem usar o protocolo HTTPS (Hypertext Transfer Protocol (HTTP) com SSL (Secure Socket Layer). Caso contrário, há um risco de que endereços de email, atividades de redes sociais e outros dados do usuário são interceptados ou expostos enquanto estão em trânsito.
    
- Se você tiver provedores que trabalham com uma versão anterior do Outlook, para dar suporte ao Office 2013, atualize o pacote de instalação. Consulte [a Lista de Verificação de Instalação](installation-checklist.md) para obter mais informações. 
    
A tabela a seguir mostra a disponibilidade de vários recursos no Outlook Social Connector 2013 em comparação com o Outlook Social Connector 1.1.
  
|**Característica**|**Outlook Social Connector 2013**|**Outlook Social Connector 1.1**|
|:-----|:-----|:-----|
|Interface do usuário final  <br/> |SharePoint Server, SharePoint Workspace, cliente do Lync, Cartão de Visita em todos os aplicativos cliente do Office e Painel de Pessoas no Outlook  <br/> |Painel de Pessoas no Outlook  <br/> |
|Autenticação básica  <br/> |Sim  <br/> |Sim  <br/> |
|Autenticação baseada em formulários  <br/> |Sim  <br/> |Sim  <br/> |
|Autenticação em cache  <br/> |Sim  <br/> |Sim  <br/> |
|Sincronização em cache para amigos com a pasta contatos no armazenamento padrão  <br/> |Sim  <br/> |Sim  <br/> |
|Sincronização de atividades em cache para amigos para **pasta do Newsfeed** oculta  <br/> |Não  <br/> |Sim  <br/> |
|Sincronização sob demanda (imagem, nome, título) para amigos e não amigos na rede  <br/> |Sim  <br/> |Sim  <br/> |
|Sincronização de atividades sob demanda para amigos e não amigos na rede  <br/> |Sim  <br/> |Sim  <br/> |
|Seguir na rede  <br/> |Sim  <br/> |Sim  <br/> |
|Não seguir na rede  <br/> |Sim  <br/> |Sim  <br/> |
|Visite a página de perfil do usuário  <br/> |Por meio de um link  <br/> |Por meio de um selo de rede  <br/> |
|Observar configurações de privacidade nas redes sociais (por exemplo, exibir perfil e atividades de não amigos que permitem a visualização de tal)  <br/> |Sim  <br/> |Sim  <br/> |
|Endereços de email com hashed passados para o provedor  <br/> |Sim  <br/> |Sim  <br/> |

<a name="OlSocialConnector_Changes"> </a>

## <a name="changes-from-the-previous-version-of-osc-provider-extensibility"></a>Alterações da versão anterior da extensibilidade do provedor OSC

A tabela a seguir mostra os membros que foram adicionados ou preterido da interface correspondente.
  
|**Interface e membro**|**Comentário**|
|:-----|:-----|
|**ISocialProfile::GetActivitiesOfFriendsAndColleagues** <br/> |Preterido no Outlook Social Connector 2013. Observe que **ISocialSession::GetActivities** também foi preterido desde o Outlook Social Connector 1.1.  <br/> Para sincronizar feeds de atividades, você deve implementar o [método ISocialSession2::GetActivitiesEx.](isocialsession2-getactivitiesex.md) Definir **dynamicActivitiesLookupEx** como **true**, que solicitará que o OSC chame **ISocialSession2::GetActivitiesEx** em vez disso.  <br/> |
   
A tabela a seguir mostra os elementos de esquema que foram alterados.
  
|**Elemento Schema**|**Comentário**|
|:-----|:-----|
|**capabilities** <br/> |Adicionado no Outlook Social Connector 2013: **elemento allowChangesToAutoConfigure.**  <br/> Preterido no Outlook Social Connector 2013: **elemento cacheActivities.**  <br/> |
|**person** <br/> |Adicionado no Outlook Social Connector 2013: **askmeabout**, **businessAddress**, **businessCity**, **businessCountryOrRegion**, **businessState**, **businessZip**, **industries**, **interests**, **location**, **otherAddress**, **otherCity**, **otherCountryOrRegion**, **otherState**, **otherZip**, **skills**, **schools** e elementos **de site.**  <br/> |
   
## <a name="see-also"></a>Confira também

- [XML para recursos](xml-for-capabilities.md)
- [XML para amigos](xml-for-friends.md)
- [Introdução ao desenvolvimento de um provedor de serviços do Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

