---
title: Novidades para provedores
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 92f59a0d-3834-424d-ad81-167fdeba9bd0
description: Este tópico lista as principais alterações no Outlook Social Connector 2013 (OSC). Apresenta uma comparação dos recursos disponíveis entre o Outlook Social Connector 2013 e Outlook Social Connector 1.1.
ms.openlocfilehash: bdd7f7998f34a0ad096964050543f3f687bd0841
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770970"
---
# <a name="whats-new-for-providers"></a>Novidades para provedores

Este tópico lista as principais alterações no Outlook Social Connector 2013 (OSC). Apresenta uma comparação dos recursos disponíveis entre o Outlook Social Connector 2013 e Outlook Social Connector 1.1. Também descreve os membros de interface e os elementos XML que foram adicionados, alterados ou preteridos. 
  
No Office 2013, o OSC funciona com não apenas Outlook, mas também SharePoint Server, SharePoint Workspace, cliente do Lync e todos os outro Office aplicativos cliente que oferecem suporte a informações de presença e o cartão de visita. Um provedor OSC pode representar atualizações de informações sociais na guia **What's NEW** no painel de pessoas do Outlook, bem como no cartão de visita. 
  
Alguns grandes alterações no Outlook Social Connector 2013 incluem o seguinte: 
  
- Se um provedor suporta mostrando as atividades, o provedor sempre sincroniza atividades sob demanda e não depende mais atividades armazenadas em cache anteriormente. Isso significa que o provedor armazena atividades de amigos e não-amigos na memória para exibir as atividades mais atuais.
    
- Por motivos de segurança, os provedores que se comunicam com servidores pela Internet devem usar o protocolo HTTPS (Hypertext Transfer Protocol (HTTP) com a camada de soquete seguro (SSL)). Caso contrário, há um risco de endereços de email, atividades de redes sociais e outro usuário dados são interceptados ou expostos em trânsito.
    
- Se você tiver os provedores que funcionam com uma versão anterior do Outlook, para suportar o Office 2013, você deverá atualizar o pacote de instalação. Consulte a [Lista de verificação de instalação](installation-checklist.md) para obter mais informações. 
    
A tabela a seguir mostra a disponibilidade dos vários recursos no Outlook Social Connector 2013 em comparação com o Outlook Social Connector 1.1.
  
|**Recurso**|**Outlook Social Connector 2013**|**Outlook Social Connector 1.1**|
|:-----|:-----|:-----|
|Interface do usuário final  <br/> |SharePoint Server, SharePoint Workspace, cliente do Lync, cartão de visita em todos os aplicativos de cliente do Office e o painel de pessoas no Outlook  <br/> |Painel de pessoas no Outlook  <br/> |
|Autenticação básica  <br/> |Sim  <br/> |Sim  <br/> |
|Autenticação baseada em formulários  <br/> |Sim  <br/> |Sim  <br/> |
|Cache de autenticação  <br/> |Sim  <br/> |Sim  <br/> |
|Armazenar em cache sync para amigos à pasta Contatos padrão  <br/> |Sim  <br/> |Sim  <br/> |
|Sincronização de atividades em cache para amigos à pasta oculta de **news feed**  <br/> |Não  <br/> |Sim  <br/> |
|Sincronização sob demanda (imagem, nome, título) de amigos e amigos na rede  <br/> |Sim  <br/> |Sim  <br/> |
|Sincronização de atividades sob demanda de amigos e amigos na rede  <br/> |Sim  <br/> |Sim  <br/> |
|Siga na rede  <br/> |Sim  <br/> |Sim  <br/> |
|Não seguem na rede  <br/> |Sim  <br/> |Sim  <br/> |
|Visite a página de perfil de usuário  <br/> |Por meio de um link  <br/> |Por meio de um emblema de rede  <br/> |
|Observando as configurações de privacidade em uma rede social (por exemplo, exibir perfil e atividades de não-amigos que permitem a visualização de como)  <br/> |Sim  <br/> |Sim  <br/> |
|Endereços de email com hash passadas para o provedor  <br/> |Sim  <br/> |Sim  <br/> |

<a name="OlSocialConnector_Changes"> </a>

## <a name="changes-from-the-previous-version-of-osc-provider-extensibility"></a>Alterações da versão anterior de extensibilidade do provedor OSC

A tabela a seguir mostra os membros que foram adicionados ou preteridos da interface correspondente.
  
|**Interface e o membro**|**Comment**|
|:-----|:-----|
|**ISocialProfile::GetActivitiesOfFriendsAndColleagues** <br/> |Obsoleto no conector Social do Outlook 2013. Observe que **ISocialSession::GetActivities** também foi preterido desde o Outlook Social Connector 1.1.  <br/> Para sincronizar os feeds de atividades, você deve implementar o método [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) . Defina **dynamicActivitiesLookupEx** como **true**, que solicitará que o OSC chamada **ISocialSession2::GetActivitiesEx** em vez disso.  <br/> |
   
A tabela a seguir mostra os elementos de esquema que foram alterados.
  
|**Elemento de esquema**|**Comment**|
|:-----|:-----|
|**capabilities** <br/> |Adicionado no Outlook Social Connector 2013: **allowChangesToAutoConfigure** elemento.  <br/> Reduzidos no Outlook Social Connector 2013: **cacheActivities** elemento.  <br/> |
|**person** <br/> |Adicionado no Outlook Social Connector 2013: **askmeabout**, **businessAddress**, **Cidade do endereço comercial**, **businessCountryOrRegion**, **businessState**, **businessZip**, **setores**, **interesses**, ** local**, elementos **otherAddress**, **otherCity**, **otherCountryOrRegion**, **otherState**, **otherZip**, **habilidades**, **escolas**e **site** .  <br/> |
   
## <a name="see-also"></a>Confira também

- [XML para recursos](xml-for-capabilities.md)
- [XML para amigos](xml-for-friends.md)
- [Introdução ao desenvolvimento de um Outlook Social Connector Provider](getting-started-with-developing-an-outlook-social-connector-provider.md)

