---
title: Sincronizar amigos e atividades
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6e91b765-a207-4d8c-8763-5d643ca4d0c0
description: Outlook Social Connector (OSC) oferece suporte a exibindo informações de uma rede social sobre uma pessoa no cartão de visita ou no painel de pessoas do Outlook. SharePoint Server, SharePoint Workspace, cliente do Lync e todos os aplicativos cliente do Office que dão suporte ao suporte de informações de presença cartão de visita.
ms.openlocfilehash: 9e843d8013b329a88de88232f16740edae77c1d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770957"
---
# <a name="synchronizing-friends-and-activities"></a>Sincronizar amigos e atividades

Outlook Social Connector (OSC) oferece suporte a exibindo informações de uma rede social sobre uma pessoa no cartão de visita ou no painel de pessoas do Outlook. SharePoint Server, SharePoint Workspace, cliente do Lync e todos os aplicativos cliente do Office que dão suporte ao suporte de informações de presença cartão de visita.
  
Você pode usar o cartão de visita em cenários de colaboração nos aplicativos do Office para obter mais informações sobre as pessoas que você está colaborando com. Exemplos desses cenários incluem mensagens no Outlook e coautoria em um documento do Word. Quando você clica na guia **What's new** de um cartão de contato, o exibe informações sobre essa pessoa. 
  
O painel de pessoas do Outlook exibe informações sobre uma pessoa que pode ser um remetente ou destinatário de um item do Outlook que você selecionou. Sempre que você selecione outra pessoa no painel de pessoas ou outro item do Explorer do Outlook ou abre um item do Outlook em um Inspetor, o Outlook Social Connector (OSC) atualiza o painel de pessoas. 
  
No cartão de visita ou painel de pessoas exibir informações atuais para a pessoa selecionada, o OSC sincroniza tais informações por meio dos provedores OSC e alguma forma de cache. Esta sincronização depende os provedores OSC que estão instalados no computador cliente, o social redes que você fez logon através de seus provedores OSC e o modo de sincronização que cada um dos provedores OSC para esses social redes suporta.
  
O OSC suporta sincronização amigos, não-amigos e atividades de amigos e não-amigos de maneiras diferentes: cache de sincronização, sincronização sob demanda e sincronização híbrida. A principal diferença entre esses modos de sincronização é onde o OSC armazena os dados — se ele está em uma pasta no repositório de Outlook padrão do usuário ou na memória no computador do usuário. Em cada caso conforme observado neste tópico, há um tempo mínimo padrão que os dados permanecerão na pasta ou memória antes que os dados são atualizados. Em alguns casos, a quantidade mínima de tempo pode ser personalizada pela diretiva de grupo. Para obter mais informações sobre diretivas de grupo que controlam o comportamento do OSC, consulte [como gerenciar o conector Social do Outlook usando a diretiva de grupo](http://support.microsoft.com/default.aspx?scid=kb%3Ben-US%3B2020103).
  
Observe que se a pessoa selecionada não for um membro da rede social, o OSC não exibir qualquer informação pessoa ou atividade dessa pessoa no cartão de visita ou painel pessoas.
  
## <a name="cached-synchronization"></a>Sincronização de cache

Um provedor OSC pode armazenar informações de amigos na rede social em uma pasta específica no repositório de Outlook padrão do usuário e atualizar periodicamente nesse cache após um período de tempo especificado tiver expirado. Cache de informações em uma pasta tem a vantagem de reduzir o tráfego na rede social.
  
> [!NOTE]
> Iniciando no Outlook Social Connector 2013, o OSC não suporta mais cache sincronização de atividades. 
  
### <a name="cached-synchronization-of-friends"></a>Sincronização de cache de amigos

Se um provedor OSC oferece suporte à sincronização de cache para amigos, o OSC caches de informações de amigos do usuário conectado na rede social. As informações são armazenadas em cache em uma pasta de contatos do Outlook que é específica para a rede social no armazenamento do Outlook do usuário padrão. O nome da pasta Contatos baseia-se no nome da rede social, o que o OSC obtém usando a propriedade [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) . 
  
Na sincronização do cache, o OSC armazena informações de amigos do usuário conectado somente na rede social. O OSC não acessar informações de não-amigos.
  
O intervalo padrão para que o OSC atualizar a pasta de contatos para obter informações de amigos da rede social é uma vez por dia (ou uma vez por 1440 minutos). Este intervalo de atualização também pode ser definido pela diretiva de grupo, conforme descrito no início deste tópico.
  
Se ocorrer um erro durante uma atualização, o OSC repete em um intervalo especificado pelo elemento **contactSyncRestartInterval** em **recursos** XML. Este intervalo de repetição tem um valor padrão de 30 minutos e também pode ser definido pela diretiva de grupo. 
  
Quando um usuário abre um cartão de visita e seleciona a guia **What's new** , atualiza a guia **What's new** . Da mesma forma, quando um usuário do Outlook reselects um item do Outlook ou reselects uma pessoa no painel de pessoas, atualiza o painel de pessoas. Se o intervalo de atualização de cache não tiver expirado, o OSC vai para o cache para obter todas as informações para o usuário selecionado. Isso evita a sobrecarga de uso estensibilidade do provedor do OSC para acessar a rede social. Se o intervalo de atualização tiver expirado, o OSC chama o método [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) para obter informações dos amigos atual para o usuário conectado e atualiza o cache da pasta Contatos. 
  
O provedor do OSC informa o OSC que suporta a sincronização em cache de amigos, especificando os seguintes elementos nas **capacidades** XML: 
  
- **getFriends** = **true**
    
- **cacheFriends** = **true**
    
- **dynamicContactsLookup** = **false**
    
## <a name="on-demand-synchronization"></a>Sincronização sob demanda

Quando um usuário seleciona a guia **What's new** em um cartão de contato, ou seleciona um item do Outlook diferente ou uma pessoa diferente no painel de pessoas no Outlook, o OSC atualiza o painel de pessoas ou um cartão de visita respectivamente. Se um provedor OSC suporta a sincronização sob demanda de pessoas ou atividades, o OSC sincroniza com um cache na memória e atualiza os detalhes, como nome, título, imagens e fluxos de atividade, no painel pessoas ou cartão de visita. Para a sincronização sob demanda, ao contrário de sincronização de cache, o OSC tenta atualizar as informações para a pessoa independentemente se essa pessoa é um amigo ou amigo do usuário conectado na rede social. 
  
Dados de pessoa (ou atividade) sob demanda são armazenados na memória apenas. Os dados na memória estão desmarcados, quando o aplicativo cliente do Office desligado, ou o usuário faz uma atualização do cartão de visita ou painel de pessoas e os dados permaneceu na memória por mais de um intervalo de atualização. Observe que a atualização da rede social é sempre iniciada por um usuário atualizar o cartão de visita ou o painel de pessoas, (por exemplo, por selecionando um usuário diferente no painel de pessoas, ou selecionar um item diferente na janela do explorer do Outlook). 

No entanto, o inverso não é sempre true — não cada atualização do cartão de visita ou painel pessoas necessariamente provoca uma atualização da rede social. Se o usuário atualiza o cartão de visita ou dados do painel de pessoas e a pessoa (ou atividade) permaneceu na memória por mais de um intervalo de atualização, o OSC chama [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) (ou [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md)) para Atualize as informações na memória da rede social. O período permitido para obter informações de amigo e não-amigo na memória é 24 horas e para atividades, 30 minutos. 
  
Uma das diferenças importante entre a sincronização de cache e sob demanda é que sincronização sob demanda pode buscar informações de pessoa e a atividade de amigos e não-amigos na rede. Se a pessoa selecionada é um não-amigo, o OSC atualiza informações e atividades dessa pessoa se qualquer um dos seguintes requisitos for atingido: 
  
- A pessoa é um usuário na rede social e permite a exibição pública de informações de perfil e atividade.
    
- A pessoa estiver na mesma rede que o usuário conectado em rede social (por exemplo, na mesma rede para alunos university).
    
A sincronização sob demanda de pessoas e atividades resulta em mais chamadas para o provedor de mecanismo OSC central. Redes sociais devem ser capazes de lidar com os requisitos de largura de banda maior de sincronização sob demanda.
  
### <a name="specifying-xml-elements-for-on-demand-synchronization"></a>Especificando os elementos XML para a sincronização sob demanda

O provedor do OSC informa o OSC que ele oferece suporte a sincronização sob demanda de amigos e não-amigos, especificando os seguintes elementos nas **capacidades** XML: 
  
- **getFriends** = **true**
    
- **cacheFriends** = **false**
    
- **dynamicContactsLookup** = **true**
    
O provedor do OSC informa o OSC que ele oferece suporte a sincronização sob demanda de atividades, especificando os seguintes elementos nas **capacidades** XML: 
  
- **getActivities** = **true**
    
- **cacheActivities** = **false**
    
- **dynamicActivitiesLookupEx** = **true**
    
## <a name="hybrid-synchronization"></a>Sincronização de híbrido

Um provedor OSC pode oferecer suporte à sincronização de híbrido de amigos e não-amigos. Isso pode otimizar as chamadas entre o mecanismo de núcleo do OSC e o provedor do OSC, as chamadas para a rede social para a sincronização sob demanda de amigos e a moeda de dados dos amigos. O tempo mínimo que de dados podem permanecer em uma pasta ou a memória, onde aplicável, é o mesmo que os limites nos modos de sincronização do armazenamento em cache ou sob demanda.
  
> [!NOTE]
> Iniciando no Outlook Social Connector 2013, o OSC suporta apenas a sincronização de atividades sob demanda e não oferece suporte para sincronização de híbrido das atividades. 
  
### <a name="hybrid-synchronization-of-friends-and-non-friends"></a>Sincronização de híbrido de amigos e não-amigos

Se um provedor OSC oferece suporte à sincronização de híbrido de amigos e não-amigos, o OSC faz o seguinte: 
  
- O OSC armazena informações de amigos do usuário registrado na pasta contato específicos de rede social.
    
- O OSC armazena informações de não-amigos do usuário registrado na memória.
    
O provedor do OSC informa o OSC que ele oferece suporte a sincronização híbrido de amigos e não-amigos, especificando os seguintes elementos nas **capacidades** XML: 
  
- **getFriends** = **true**
    
- **cacheFriends** = **true**
    
- **dynamicContactsLookup** = **true**
    
## <a name="synchronization-intervals"></a>Intervalos de sincronização

A tabela a seguir resume os intervalos de sincronização de amigos e informações de não-amigos entre o cache correspondente (pasta ou memória) e a rede social, dependendo do modo de sincronização com suporte. Para o modo de sincronização de híbrido, consulte as linhas para o modo em cache para amigos e na linha para o modo de não-amigos sob demanda.
  
|**Modo de sincronização para as pessoas**|**Onde o intervalo de atualização está definido**|**Padrão de tempo mínimo antes da atualização**|**Substituição de diretiva de grupo**|
|:-----|:-----|:-----|:-----|
|Cache  <br/> |Definir dentro OSC  <br/> |1440 minutos (24 horas)  <br/> |Valor de registro do Windows **NetContactSyncInterval** <br/> |
|Cache  <br/> |elemento de **contactSyncRestartInterval** em **recursos** XML  <br/> |30 minutos se **contactSyncRestartInterval** não estiver definida.  <br/> |De valor do registro do Windows **contactSyncRestartInterval** <br/> |
|Sob demanda  <br/> |Definir dentro OSC  <br/> |1440 minutos (24 horas)  <br/> |Valor de registro do Windows **OnlineSearchExpiryTime** <br/> |
   
A tabela a seguir resume os intervalos de sincronização para atividades de amigos e amigos entre o cache correspondente (pasta ou memória) e a rede social, dependendo os modos de sincronização com suporte. 
  
|**Modo de sincronização de atividades**|**Onde o intervalo de atualização está definido**|**Padrão de tempo mínimo antes da atualização**|**Substituição de diretiva de grupo**|
|:-----|:-----|:-----|:-----|
|Sob demanda  <br/> |Definir dentro OSC  <br/> |30 minutos  <br/> |Valor de registro do Windows **OnlineSearchExpiryTime** <br/> |
   
As informações a seguir aplica-se para os valores do registro do Windows listados nas duas tabelas:
  
- Chave:`HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\Outlook\SocialConnector`
    
- Valor: O valor DWORD entre 1 e 10080
    
## <a name="see-also"></a>Confira também

- [Exemplo de XML de recursos](capabilities-xml-example.md)  
- [XML para recursos](xml-for-capabilities.md)
- [Desenvolvendo um provedor com o esquema OSC XML](developing-a-provider-with-the-osc-xml-schema.md)  
- [Como gerenciar o conector Social do Outlook usando a diretiva de grupo](http://support.microsoft.com/default.aspx?scid=kb%3Ben-US%3B2020103)

