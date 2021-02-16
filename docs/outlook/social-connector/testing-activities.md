---
title: Testar atividades
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 98343c36-5e32-4d07-b474-adfeca693135
description: Este tópico descreve testes e cenários para verificar se o provedor do Outlook Social Connector (OSC) usa a sincronização sob demanda para retornar atividades adequadamente de amigos e não amigos.
ms.openlocfilehash: 0a40dca84681a9e758c2f17d2647c339ded70462
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436297"
---
# <a name="testing-activities"></a>Testar atividades

Este tópico descreve testes e cenários para verificar se o provedor do Outlook Social Connector (OSC) usa a sincronização sob demanda para retornar atividades adequadamente de amigos e não amigos.

<a name="olosc_TestingActivities_OnDemandSync"> </a>

## <a name="on-demand-synchronization"></a>Sincronização sob demanda

Um provedor OSC implementa **ISocialProvider::GetCapabilities**, que o OSC chama para determinar se o provedor oferece suporte à sincronização sob demanda de atividades de amigos e não amigos. Para as pessoas exibidas no Painel de Pessoas do Outlook, o OSC obtém e hashes seus endereços SMTP, chama [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md)e armazena (na memória) os dados de atividades retornadas para essas pessoas. 
  
### <a name="determining-activities-to-get"></a>Determinando atividades a obter

Os endereços SMTP com hashed passados para **GetActivitiesEx** são a chave para determinar se o OSC obterá atividades para um amigo ou não. O OSC obtém atividades para uma pessoa se a pessoa especificar esse endereço SMTP em sua conta de rede social. Se a pessoa não incluir esse endereço SMTP em sua conta de rede social ou se essa pessoa for um amigo, mas por um endereço de email diferente na rede social, **GetActivitiesEx** não obterá atividades para essa pessoa. Além disso, para uma pessoa que não é um amigo, mas especifica os endereços SMTP em sua conta de rede social, os dados retornados incluem apenas o que está disponível para um não amigo, conforme permitido pelas configurações de privacidade dessa pessoa. 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a>Criando assuntos de teste para amigos e não amigos

Para criar um assunto de teste para um amigo, identifique o endereço SMTP de uma pessoa que inclua esse endereço em sua conta de rede social e que tenha um status de amigo com o usuário conectado nessa rede. Crie uma mensagem de email que inclua esse endereço SMTP. Da mesma forma, para criar um assunto de teste para um não amigo, identifique o endereço SMTP de uma pessoa que não seja amigo do usuário conectado por esse endereço e que tenha especificado em suas configurações de privacidade para permitir que não amigos exigam seu perfil na rede social. Crie uma mensagem de email que inclua esse endereço SMTP. 
  
No Explorador do Outlook, quando você seleciona a mensagem de email que inclui um amigo (ou não amigo), o Painel de Pessoas exibe os destinatários. Selecionar o amigo (ou não amigo) no Painel de Pessoas permite que você teste se o provedor está fornecendo informações sobre a pessoa.
  
### <a name="test-scenarios"></a>Cenários de teste

Para verificar se você está recebendo atividades apropriadas para amigos e não amigos, teste os cenários a seguir.
  
|**Cenário**|**Comportamento esperado**|
|:-----|:-----|
|A pessoa selecionada no Painel de Pessoas é um amigo com o usuário conectado na rede social.  <br/> |O Painel de Pessoas exibe o perfil e a imagem de perfil dessa pessoa como postado na rede social.  <br/> |
|A pessoa selecionada no Painel de Pessoas é um não amigo do usuário conectado na rede social, mas permitiu que seu perfil fosse visualizado por não amigos.  <br/> |O Painel de Pessoas exibe o perfil e a imagem de perfil dessa pessoa como postado na rede social.  <br/> |
   
## <a name="see-also"></a>Confira também

- [Sincronizar amigos e atividades](synchronizing-friends-and-activities.md)  
- [XML para atividades](xml-for-activities.md)
- [Preparar um provedor de OSC para lançamento](getting-ready-to-release-an-osc-provider.md)

