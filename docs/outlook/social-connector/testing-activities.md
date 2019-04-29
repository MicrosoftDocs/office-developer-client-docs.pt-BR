---
title: Testar atividades
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 98343c36-5e32-4d07-b474-adfeca693135
description: Este tópico descreve testes e cenários para verificar se o provedor do Outlook Social Connector (OSC) usa a sincronização sob demanda para retornar adequadamente as atividades de amigos e não amigos.
ms.openlocfilehash: 0a40dca84681a9e758c2f17d2647c339ded70462
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436297"
---
# <a name="testing-activities"></a>Testar atividades

Este tópico descreve testes e cenários para verificar se o provedor do Outlook Social Connector (OSC) usa a sincronização sob demanda para retornar adequadamente as atividades de amigos e não amigos.

<a name="olosc_TestingActivities_OnDemandSync"> </a>

## <a name="on-demand-synchronization"></a>Sincronização sob demanda

Um provedor OSC implementa **ISocialProvider:: GetCapabilities**, que o OSC chama para determinar se o provedor oferece suporte à sincronização sob demanda de atividades de amigos e não amigos. Para as pessoas exibidas no painel de pessoas do Outlook, o OSC Obtém e codifica seus endereços SMTP, chama [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md)e lojas (na memória) os dados de atividades retornados para essas pessoas. 
  
### <a name="determining-activities-to-get"></a>Determinando atividades a serem obtidas

Os endereços SMTP de hash passados para **GetActivitiesEx** são a chave para determinar se o OSC receberá atividades de um amigo ou não amigo. O OSC Obtém as atividades de uma pessoa se a pessoa especifica o endereço SMTP em sua conta de rede social. Se a pessoa não incluir esse endereço SMTP em sua conta de rede social ou se essa pessoa for um amigo, mas por um endereço de email diferente na rede social, o **GetActivitiesEx** não receberá atividades para essa pessoa. Além disso, para uma pessoa que não é um amigo mas especifica os endereços SMTP em sua conta de rede social, os dados retornados incluem apenas o que está disponível para um não amigo, conforme permitido pelas configurações de privacidade dessa pessoa. 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a>Criando entidades de teste para amigos e não amigos

Para criar um assunto de teste para um amigo, identifique o endereço SMTP de uma pessoa que inclui esse endereço em sua conta de rede social e que tenha um status de amigo com o usuário conectado na rede. Crie uma mensagem de email que inclua esse endereço SMTP. Da mesma forma, para criar um assunto de teste para um não amigo, identifique o endereço SMTP de uma pessoa que não é um amigo do usuário conectado por esse endereço e que tenha especificado em suas configurações de privacidade para permitir que não amigos exibam o perfil na rede social. Crie uma mensagem de email que inclua esse endereço SMTP. 
  
No Outlook Explorer, quando você seleciona a mensagem de email que inclui um amigo (ou não amigo), o painel de pessoas exibe os destinatários. Selecionar o amigo (ou não amigo) no painel pessoas permite testar se o provedor está fornecendo informações sobre a pessoa.
  
### <a name="test-scenarios"></a>Cenários de teste

Para verificar se você está obtendo as atividades apropriadas para amigos e não amigos, teste os cenários a seguir.
  
|**Cenário**|**Comportamento esperado**|
|:-----|:-----|
|A pessoa selecionada no painel de pessoas é um amigo com o usuário conectado na rede social.  <br/> |O painel de pessoas exibe o perfil e a imagem de perfil dessa pessoa como postados na rede social.  <br/> |
|A pessoa selecionada no painel de pessoas é um não amigo do usuário conectado na rede social, mas permitiu que seu perfil fosse exibido por não amigos do.  <br/> |O painel de pessoas exibe o perfil e a imagem de perfil dessa pessoa como postados na rede social.  <br/> |
   
## <a name="see-also"></a>Confira também

- [Sincronizar amigos e atividades](synchronizing-friends-and-activities.md)  
- [XML para atividades](xml-for-activities.md)
- [Preparar um provedor de OSC para lançamento](getting-ready-to-release-an-osc-provider.md)

