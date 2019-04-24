---
title: Testar amigos
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 109c34b6-911b-4dfc-9799-aadf47172e84
description: Este tópico descreve testes e cenários para verificar se o provedor do Outlook Social Connector (OSC) retorna apropriadamente dados de amigos e não amigos, quando aplicável, dependendo do modo de sincronização suportado pelo provedor.
ms.openlocfilehash: 1c97342fd5b219b15b1f58dbc065fc268f8e81d7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338784"
---
# <a name="testing-friends"></a>Testar amigos

Este tópico descreve testes e cenários para verificar se o provedor do Outlook Social Connector (OSC) retorna apropriadamente dados de amigos e não amigos, quando aplicável, dependendo do modo de sincronização suportado pelo provedor.

<a name="olosc_TestingFriends_CachedSync"> </a>

## <a name="cached-synchronization"></a>Sincronização em cache

Um provedor OSC implementa [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md), que o OSC chama para determinar se o provedor oferece suporte à sincronização em cache dos dados dos amigos. Após chamar [ISocialPerson:: GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md), o OSC armazena os dados dos amigos retornados em uma pasta de contatos específica da rede social na loja do Outlook padrão do usuário conectado. O OSC também chama [ISocialSession:: GetPerson](isocialsession-getperson.md) e [ISocialPerson:: GetPicture](isocialperson-getpicture.md) para obter uma imagem de perfil de cada amigo. 
  
### <a name="initiate-synchronization"></a>Iniciar a sincronização

Para iniciar a sincronização, você pode ativar e usar o botão de depuração **sincronizar contatos** no componente faixa de opções da interface do usuário do Microsoft Office Fluent. Para obter mais informações sobre os botões de depuração do OSC, consulte [Debugging a Provider](debugging-a-provider.md). 
  
### <a name="test-scenarios"></a>Cenários de teste

Teste os itens a seguir para verificar se os dados dos amigos estão armazenados em cache corretamente.
  
|**Item a ser testado**|**Comportamento esperado**|
|:-----|:-----|
|Pasta de contatos  <br/> |A pasta contatos específica da rede social existe no repositório padrão do usuário do usuário.  <br/> |
|Dados dos amigos retornados por **ISocialPerson:: GetFriendsAndColleagues** <br/> |Cada amigo corresponde a um contato na pasta contatos específicos de rede.  <br/> |
|Dados dos amigos  <br/> |Os campos de contato de cada amigo têm os dados corretos.  <br/> |
|Imagens de perfil dos amigos retornadas por **ISocialPerson:: GetPicture** <br/> |O item de contato para cada amigo contém a imagem de perfil.  <br/> |

<a name="olosc_TestingFriends_OnDemandSync"> </a>

## <a name="on-demand-synchronization"></a>Sincronização sob demanda

Um provedor OSC implementa **ISocialProvider:: GetCapabilities**, que o OSC chama para determinar se o provedor oferece suporte à sincronização sob demanda de amigos e não amigos. Para as pessoas exibidas no painel de pessoas do Outlook, o OSC Obtém e codifica seus endereços SMTP, chama [ISocialSession2:: GetPeopleDetails](isocialsession2-getpeopledetails.md)e lojas (na memória) os dados retornados para essas pessoas. 
  
### <a name="determining-friends-and-non-friends"></a>Determinando amigos e não amigos

Os endereços SMTP de hash passados para **GetPeopleDetails** são a chave para determinar se uma pessoa é um amigo ou não amigo. Se uma pessoa não incluir esse endereço SMTP em sua conta de rede social, ou mesmo se essa pessoa for um amigo por um endereço de email diferente na rede social, o **GetPeopleDetails** ainda retornará o **** **não amigo dessa pessoa como friendStatus** no parâmetro _Persons_ . Além disso, para uma pessoa que não é um amigo mas especifica o endereço SMTP em sua conta de rede social, os dados retornados incluem apenas o que está disponível para um não amigo, conforme permitido pelas configurações de privacidade dessa pessoa. 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a>Criando entidades de teste para amigos e não amigos

Para criar um assunto de teste para um amigo, identifique o endereço SMTP de uma pessoa que inclui esse endereço em sua conta de rede social e que tenha um status de amigo com o usuário conectado na rede. Crie uma mensagem de email que inclua esse endereço SMTP. Da mesma forma, para criar um assunto de teste para um não amigo, identifique o endereço SMTP de uma pessoa que não é um amigo do usuário conectado por esse endereço e, ainda que tenha especificado em suas configurações de privacidade para permitir que não amigos exibam suas atividades no networ social f. Crie uma mensagem de email que inclua esse endereço SMTP. 
  
No Outlook Explorer, quando você seleciona a mensagem de email que inclui um amigo (ou não amigo), o painel de pessoas exibe os destinatários. Selecionar o amigo (ou não amigo) no painel pessoas permite testar se o provedor está fornecendo informações sobre a pessoa.
  
### <a name="test-scenarios"></a>Cenários de teste

Para verificar se seu provedor está fornecendo informações sobre amigos e não amigos apropriadamente, teste para os cenários a seguir.
  
|**Cenário**|**Comportamento esperado**|
|:-----|:-----|
|A pessoa selecionada no painel de pessoas é um amigo com o usuário conectado na rede social.  <br/> |O painel de pessoas exibe as atividades dessa pessoa na rede social.  <br/> |
|A pessoa selecionada no painel de pessoas é um não amigo do usuário conectado na rede social, mas permitiu que suas atividades sejam visualizadas por não amigos.  <br/> |O painel de pessoas exibe as atividades dessa pessoa na rede social.  <br/> |

<a name="olosc_TestingFriends_OnDemandSync"> </a>

## <a name="hybrid-synchronization"></a>Sincronização híbrida

Se um provedor OSC oferecer suporte à sincronização híbrida de amigos e não amigos, o OSC fará o seguinte: 
  
- O OSC armazenará informações de amigos do usuário conectado na pasta de contatos específica da rede social.
    
- O OSC recupera informações para não amigos por demanda da rede social e as armazena apenas na memória, mas não em uma pasta.
    
Para testar a sincronização híbrida, siga as sugestões de teste na seção [sincronização em cache](#olosc_TestingFriends_CachedSync) para os amigos e aqueles da seção de [sincronização sob demanda](#olosc_TestingFriends_OnDemandSync) para não amigos. 
  
## <a name="see-also"></a>Confira também

- [Sincronizar amigos e atividades](synchronizing-friends-and-activities.md) 
- [XML para amigos](xml-for-friends.md)
- [Preparar um provedor de OSC para lançamento](getting-ready-to-release-an-osc-provider.md)

