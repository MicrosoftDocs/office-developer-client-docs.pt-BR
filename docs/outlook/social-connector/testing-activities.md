---
title: Testar atividades
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 98343c36-5e32-4d07-b474-adfeca693135
description: Este tópico descreve os cenários para verificar que o provedor do Outlook Social Connector (OSC) usa a sincronização sob demanda para retornar apropriadamente atividades de amigos e não-amigos e testes.
ms.openlocfilehash: 82d24b106e8d429d20a2d396eb60155cbb95f91f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770958"
---
# <a name="testing-activities"></a>Testar atividades

Este tópico descreve os cenários para verificar que o provedor do Outlook Social Connector (OSC) usa a sincronização sob demanda para retornar apropriadamente atividades de amigos e não-amigos e testes.

<a name="olosc_TestingActivities_OnDemandSync"> </a>

## <a name="on-demand-synchronization"></a>Sincronização sob demanda

Um provedor OSC implementa **ISocialProvider::GetCapabilities**, que o OSC chamadas para determinar se o provedor oferece suporte a sincronização sob demanda de atividades de amigos e não-amigos. Para as pessoas exibidas no painel de pessoas do Outlook, obtém o OSC e hashes lida com seu SMTP, chama [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md)e armazena (na memória) os dados de atividades é retornada para essas pessoas. 
  
### <a name="determining-activities-to-get"></a>Determinando as atividades a obter

Os endereços SMTP com hash passados para **GetActivitiesEx** são a chave para determinar se o OSC receberá atividades para um amigo ou não-amigo. O OSC obtém as atividades de uma pessoa se a pessoa especifica esse endereço SMTP em sua conta de redes sociais. Se a pessoa não inclue esse endereço SMTP em sua conta de rede social, ou se a pessoa estiver um amigo mas por um endereço de email diferentes na rede social, **GetActivitiesEx** não obtiver atividades dessa pessoa. Além disso, para uma pessoa que não é um amigo, mas Especifica os endereços SMTP em sua conta de rede social, os dados retornados incluem apenas o que está disponível para um não-amigo conforme permitido pelas configurações de privacidade da pessoa. 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a>Criando assuntos de teste de amigos e não-amigos

Para criar um teste de assunto de um amigo, identifique o endereço SMTP de uma pessoa que inclui esse endereço na sua conta de rede social e que tem um status de amigo com o usuário conectado desta rede. Crie uma mensagem de email que inclua esse endereço SMTP. Da mesma forma, para criar um assunto de teste para um não-amigo, identifique o endereço SMTP de uma pessoa que não é um amigo do usuário conectado por esse endereço e quem tem especificado nas configurações de privacidade de seu para permitir que não-amigos exibir seu perfil na rede social. Crie uma mensagem de email que inclua esse endereço SMTP. 
  
No Gerenciador de Outlook, quando você seleciona a mensagem de email que inclua um amigo (ou não-amigo), o painel de pessoas exibe os destinatários. Selecionar o amigo (ou não-amigo) no painel de pessoas permite que você teste que o provedor está fornecendo informações sobre a pessoa.
  
### <a name="test-scenarios"></a>Cenários de teste

Para verificar que você está obtendo atividades apropriadas de amigos e não-amigos, teste para os seguintes cenários.
  
|**Cenário**|**Comportamento esperado**|
|:-----|:-----|
|Pessoa selecionada no painel de pessoas é um amigo com o usuário de logon na rede social.  <br/> |O painel de pessoas exibe perfil e a imagem de perfil conforme postada na rede social dessa pessoa.  <br/> |
|Pessoa selecionada no painel de pessoas é um não-amigo do usuário conectado na rede social, mas permitiu seu perfil sejam exibidas por não-amigos.  <br/> |O painel de pessoas exibe perfil e a imagem de perfil conforme postada na rede social dessa pessoa.  <br/> |
   
## <a name="see-also"></a>Confira também

- [Sincronização de amigos e atividades](synchronizing-friends-and-activities.md)  
- [XML para atividades](xml-for-activities.md)
- [Preparando-se para o lançamento de um provedor OSC](getting-ready-to-release-an-osc-provider.md)

