---
title: Testando amigos
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 109c34b6-911b-4dfc-9799-aadf47172e84
description: Este tópico descreve os testes e cenários para verificar que o provedor do Outlook Social Connector (OSC) apropriadamente retorna dados de amigos e não-amigos, onde aplicável, dependendo do modo de sincronização suportado pelo provedor.
ms.openlocfilehash: 232977836833a9ef981ebef38c9ee243ea2dd2ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770973"
---
# <a name="testing-friends"></a>Testando amigos

Este tópico descreve os testes e cenários para verificar que o provedor do Outlook Social Connector (OSC) apropriadamente retorna dados de amigos e não-amigos, onde aplicável, dependendo do modo de sincronização suportado pelo provedor.

<a name="olosc_TestingFriends_CachedSync"> </a>

## <a name="cached-synchronization"></a>Sincronização de cache

Um provedor OSC implementa [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md), que o OSC chamadas para determinar se o provedor oferece suporte à sincronização de cache de dados de amigos dos. Depois de chamar [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md), o OSC armazena dados de amigos dos retornados em uma pasta de contatos específica para a rede social no armazenamento do Outlook do usuário conectado no padrão. O OSC também chama [ISocialSession::GetPerson](isocialsession-getperson.md) e [ISocialPerson::GetPicture](isocialperson-getpicture.md) para obter uma imagem de perfil para cada amigo. 
  
### <a name="initiate-synchronization"></a>Iniciar a sincronização

Para iniciar a sincronização, você pode ativar e use o botão de depuração **Sincronizar contatos** no componente da faixa de opções da interface de usuário do Microsoft Office Fluent. Para obter mais informações sobre os botões de depuração do OSC, consulte [depurando um provedor](debugging-a-provider.md). 
  
### <a name="test-scenarios"></a>Cenários de teste

Teste os itens a seguir para verificar se os dados dos amigos é armazenado em cache corretamente.
  
|**Item de teste**|**Comportamento esperado**|
|:-----|:-----|
|Pasta de contatos  <br/> |A pasta Contatos de específicos de rede social existe no armazenamento do Outlook do usuário padrão.  <br/> |
|Dados de amigos dos retornados pelo **ISocialPerson::GetFriendsAndColleagues** <br/> |Cada amigo corresponde a um contato na pasta Contatos específicos de rede.  <br/> |
|Dados de amigos dos  <br/> |Campos de contato para cada amigo tem os dados corretos.  <br/> |
|Imagens de perfil de amigos dos retornado por **ISocialPerson::GetPicture** <br/> |O item de contato para cada amigo contém a imagem de perfil.  <br/> |

<a name="olosc_TestingFriends_OnDemandSync"> </a>

## <a name="on-demand-synchronization"></a>Sincronização sob demanda

Um provedor OSC implementa **ISocialProvider::GetCapabilities**, que o OSC chamadas para determinar se o provedor oferece suporte a sincronização sob demanda de amigos e não-amigos. Para as pessoas exibidas no painel de pessoas do Outlook, obtém o OSC e hashes lida com seu SMTP, chama [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md)e armazena (na memória) os dados retornam para essas pessoas. 
  
### <a name="determining-friends-and-non-friends"></a>Determinando amigos e não-amigos

Os endereços SMTP com hash passados para **GetPeopleDetails** são a chave para determinar se uma pessoa é um amigo ou não-amigo. Se uma pessoa não incluir esse endereço SMTP em sua conta de rede social, ou mesmo se essa pessoa é um amigo por um endereço de email diferentes na rede social, **GetPeopleDetails** ainda retorna o **nonfriend** dessa pessoa como o ** friendStatus** no parâmetro _personsCollection_ . Além disso, para uma pessoa que não é um amigo, mas Especifica o endereço SMTP em sua conta de rede social, os dados retornados incluem apenas o que está disponível para um não-amigo conforme permitido pelas configurações de privacidade da pessoa. 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a>Criando assuntos de teste de amigos e não-amigos

Para criar um teste de assunto de um amigo, identifique o endereço SMTP de uma pessoa que inclui esse endereço na sua conta de rede social e que tem um status de amigo com o usuário conectado desta rede. Crie uma mensagem de email que inclua esse endereço SMTP. Da mesma forma, para criar um assunto de teste para um não-amigo, identifique o endereço SMTP de uma pessoa que não é um amigo do usuário conectado por esse endereço e ainda que tenha especificado nas configurações de privacidade de seu para permitir que não-amigos exibir suas atividades na rede social k. Crie uma mensagem de email que inclua esse endereço SMTP. 
  
No Gerenciador de Outlook, quando você seleciona a mensagem de email que inclua um amigo (ou não-amigo), o painel de pessoas exibe os destinatários. Selecionar o amigo (ou não-amigo) no painel de pessoas permite que você teste que o provedor está fornecendo informações sobre a pessoa.
  
### <a name="test-scenarios"></a>Cenários de teste

Para verificar se o seu provedor está fornecendo informações sobre amigos e não-amigos apropriadamente, teste para os seguintes cenários.
  
|**Cenário**|**Comportamento esperado**|
|:-----|:-----|
|Pessoa selecionada no painel de pessoas é um amigo com o usuário de logon na rede social.  <br/> |O painel de pessoas exibe atividades dessa pessoa na rede social.  <br/> |
|Pessoa selecionada no painel de pessoas é um não-amigo do usuário conectado na rede social, mas permitiu que suas atividades sejam exibidas por não-amigos.  <br/> |O painel de pessoas exibe atividades dessa pessoa na rede social.  <br/> |

<a name="olosc_TestingFriends_OnDemandSync"> </a>

## <a name="hybrid-synchronization"></a>Sincronização de híbrido

Se um provedor OSC oferece suporte à sincronização de híbrido de amigos e não-amigos, o OSC faz o seguinte: 
  
- O OSC armazena informações de amigos do usuário registrado na pasta contato específicos de rede social.
    
- O OSC recupera informações de não-amigos sob demanda da rede social e o armazena apenas na memória, mas não em uma pasta.
    
Para testar a sincronização de híbrida, siga as sugestões de testes na seção [Sincronização de cache](#olosc_TestingFriends_CachedSync) para amigos e aqueles na seção [Sincronização sob demanda](#olosc_TestingFriends_OnDemandSync) de não-amigos. 
  
## <a name="see-also"></a>Confira também

- [Sincronização de amigos e atividades](synchronizing-friends-and-activities.md) 
- [XML para amigos](xml-for-friends.md)
- [Preparando-se para o lançamento de um provedor OSC](getting-ready-to-release-an-osc-provider.md)

