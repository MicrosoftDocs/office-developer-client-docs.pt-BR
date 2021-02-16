---
title: Testar amigos
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 109c34b6-911b-4dfc-9799-aadf47172e84
description: Este tópico descreve testes e cenários para verificar se o provedor do Outlook Social Connector (OSC) retorna adequadamente dados de amigos e não amigos, quando aplicável, dependendo do modo de sincronização suportado pelo provedor.
ms.openlocfilehash: 1c97342fd5b219b15b1f58dbc065fc268f8e81d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433665"
---
# <a name="testing-friends"></a>Testar amigos

Este tópico descreve testes e cenários para verificar se o provedor do Outlook Social Connector (OSC) retorna adequadamente dados de amigos e não amigos, quando aplicável, dependendo do modo de sincronização suportado pelo provedor.

<a name="olosc_TestingFriends_CachedSync"> </a>

## <a name="cached-synchronization"></a>Sincronização em cache

Um provedor OSC implementa [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md), que o OSC chama para determinar se o provedor oferece suporte à sincronização em cache de dados de amigos. Depois de chamar [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md), o OSC armazena os dados dos amigos retornados em uma pasta de contatos específica da rede social no armazenamento padrão do Outlook do usuário conectado. O OSC também chama [ISocialSession::GetPerson](isocialsession-getperson.md) e [ISocialPerson::GetPicture](isocialperson-getpicture.md) para obter uma imagem de perfil para cada amigo. 
  
### <a name="initiate-synchronization"></a>Iniciar sincronização

Para iniciar a sincronização, você pode ativar  e usar o botão de depuração Sincronizar Contatos no componente da faixa de opções da interface do usuário do Microsoft Office Fluent. Para obter mais informações sobre os botões de depuração do OSC, consulte [Depurando um provedor.](debugging-a-provider.md) 
  
### <a name="test-scenarios"></a>Cenários de teste

Teste os itens a seguir para verificar se os dados dos amigos estão armazenados em cache corretamente.
  
|**Item a ser testado**|**Comportamento esperado**|
|:-----|:-----|
|Pasta Contatos  <br/> |A pasta de contatos específica da rede social existe no armazenamento padrão do Outlook do usuário.  <br/> |
|Dados de amigos retornados por **ISocialPerson::GetFriendsAndColleagues** <br/> |Cada amigo corresponde a um contato na pasta de contatos específicos da rede.  <br/> |
|Dados de amigos  <br/> |Os campos de contato de cada amigo têm os dados corretos.  <br/> |
|Imagens de perfil de amigos retornadas **por ISocialPerson::GetPicture** <br/> |O item de contato de cada amigo contém a imagem do perfil.  <br/> |

<a name="olosc_TestingFriends_OnDemandSync"> </a>

## <a name="on-demand-synchronization"></a>Sincronização sob demanda

Um provedor OSC implementa **ISocialProvider::GetCapabilities**, que o OSC chama para determinar se o provedor oferece suporte à sincronização sob demanda de amigos e não amigos. Para as pessoas exibidas no Painel de Pessoas do Outlook, o OSC obtém e hashes seus endereços SMTP, chama [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md)e armazena (na memória) os dados retornados para essas pessoas. 
  
### <a name="determining-friends-and-non-friends"></a>Determinando amigos e não amigos

Os endereços SMTP com hashed passados para **GetPeopleDetails** são a chave para determinar se uma pessoa é um amigo ou não amigo. Se uma pessoa não incluir esse endereço SMTP em sua conta de rede social ou mesmo se ela for um amigo  por um endereço de email diferente na rede social, **GetPeopleDetails** ainda retornará não amigos dessa pessoa como **friendStatus** no parâmetro _personsCollection._ Além disso, para uma pessoa que não é um amigo, mas especifica o endereço SMTP em sua conta de rede social, os dados retornados incluem apenas o que está disponível para um não amigo, conforme permitido pelas configurações de privacidade dessa pessoa. 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a>Criando assuntos de teste para amigos e não amigos

Para criar um assunto de teste para um amigo, identifique o endereço SMTP de uma pessoa que inclua esse endereço em sua conta de rede social e que tenha um status de amigo com o usuário conectado nessa rede. Crie uma mensagem de email que inclua esse endereço SMTP. Da mesma forma, para criar um assunto de teste para um não amigo, identifique o endereço SMTP de uma pessoa que não seja amigo do usuário conectado por esse endereço e ainda que tenha especificado em suas configurações de privacidade para permitir que não amigos exigam suas atividades na rede social. Crie uma mensagem de email que inclua esse endereço SMTP. 
  
No Explorador do Outlook, quando você seleciona a mensagem de email que inclui um amigo (ou não amigo), o Painel de Pessoas exibe os destinatários. Selecionar o amigo (ou não amigo) no Painel de Pessoas permite que você teste se o provedor está fornecendo informações sobre a pessoa.
  
### <a name="test-scenarios"></a>Cenários de teste

Para verificar se o provedor está fornecendo informações sobre amigos e não amigos adequadamente, teste os cenários a seguir.
  
|**Cenário**|**Comportamento esperado**|
|:-----|:-----|
|A pessoa selecionada no Painel de Pessoas é um amigo com o usuário conectado na rede social.  <br/> |O Painel de Pessoas exibe as atividades dessa pessoa na rede social.  <br/> |
|A pessoa selecionada no Painel de Pessoas é um não amigo do usuário conectado na rede social, mas permitiu que suas atividades sejam visualizadas por não amigos.  <br/> |O Painel de Pessoas exibe as atividades dessa pessoa na rede social.  <br/> |

<a name="olosc_TestingFriends_OnDemandSync"> </a>

## <a name="hybrid-synchronization"></a>Sincronização híbrida

Se um provedor OSC oferecer suporte à sincronização híbrida de amigos e não amigos, o OSC fará o seguinte: 
  
- O OSC armazenará informações de amigos do usuário conectado na pasta de contatos específica da rede social.
    
- O OSC recupera informações de não amigos sob demanda da rede social e as armazena somente na memória, mas não em uma pasta.
    
Para testar a sincronização híbrida, siga as sugestões de teste [](#olosc_TestingFriends_OnDemandSync) na seção Sincronização em [Cache](#olosc_TestingFriends_CachedSync) para amigos e aquelas na seção Sincronização Sob Demanda para não amigos. 
  
## <a name="see-also"></a>Confira também

- [Sincronizar amigos e atividades](synchronizing-friends-and-activities.md) 
- [XML para amigos](xml-for-friends.md)
- [Preparar um provedor de OSC para lançamento](getting-ready-to-release-an-osc-provider.md)

