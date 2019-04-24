---
title: Sincronizar amigos e atividades
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6e91b765-a207-4d8c-8763-5d643ca4d0c0
description: O Outlook Connector Social (OSC) dá suporte à exibição de informações de uma rede social sobre uma pessoa no Cartão de Visita ou no Painel de Pessoas do Outlook. O SharePoint Server, o SharePoint Workspace, o cliente Lync e todos os aplicativos cliente do Office com suporte para informações de presença também incluem suporte ao Cartão de Visita.
ms.openlocfilehash: 0d6881c5d596519422d01ca61a00b1a68e610f2c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329198"
---
# <a name="synchronizing-friends-and-activities"></a>Sincronizar amigos e atividades

O Outlook Connector Social (OSC) dá suporte à exibição de informações de uma rede social sobre uma pessoa no Cartão de Visita ou no Painel de Pessoas do Outlook. O SharePoint Server, o SharePoint Workspace, o cliente Lync e todos os aplicativos cliente do Office com suporte para informações de presença também incluem suporte ao Cartão de Visita.
  
Você pode usar o Cartão de Visita em cenários de colaboração de aplicativos do Office para saber mais sobre as pessoas com as quais está colaborando. Exemplos desses cenários incluem mensagens no Outlook e coautoria de um documento no Word. Quando você clica na guia **Novidades** de um Cartão de Visita, ela exibe informações sobre essa pessoa. 
  
O Painel de Pessoas do Outlook exibe informações sobre uma pessoa, que pode ser um remetente ou destinatário de um item do Outlook que você selecionou. Sempre que você selecionar outra pessoa no Painel de Pessoas ou outro item no explorador do Outlook, ou abrir um item do Outlook em um inspetor, o Outlook Social Connector (OSC) atualizará o Painel de Pessoas. 
  
Para que o Cartão de Visita ou o Painel de Pessoas mostre informações atuais da pessoa selecionada, o OSC sincroniza essas informações por meio dos provedores OSC e de uma determinada forma de armazenamento em cache. Essa sincronização depende dos provedores OSC instalados no computador cliente, das redes sociais nas quais você fez logon por meio de seus provedores OSC e do modo de sincronização com suporte por cada um dos provedores OSC para essas redes sociais.
  
O OSC dá suporte à sincronização de amigos, não amigos e atividades de amigos e não amigos de diferentes maneiras: sincronização em cache, sincronização sob demanda e sincronização híbrida. A principal diferença entre esses modos de sincronização é o local em que o OSC armazena os dados: em uma pasta no repositório padrão do Outlook do usuário ou na memória do computador do usuário. Em cada caso, conforme observado neste tópico, há um tempo mínimo padrão em que os dados permanecem na pasta ou na memória antes de serem atualizados. Em alguns casos, o tempo mínimo pode ser personalizado por uma política de grupo. Para saber mais sobre políticas de grupo que controlam o comportamento do OSC, consulte [Como gerenciar o Outlook Social Connector usando uma política de grupo](https://support.microsoft.com/default.aspx?scid=kb%3Ben-US%3B2020103).
  
Observe que, se a pessoa selecionada não for membro da rede social, o OSC não exibirá informações pessoais ou de atividades para essa pessoa no Cartão de Visita ou no Painel de Pessoas.
  
## <a name="cached-synchronization"></a>Sincronização em cache

Um provedor OSC pode armazenar informações de amigos na rede social em uma pasta específica do repositório padrão do usuário no Outlook e atualizar periodicamente esse cache após um período de tempo especificado. O armazenamento de informações em cache em uma pasta tem a vantagem de reduzir o tráfego para a rede social.
  
> [!NOTE]
> Começando com o Outlook Social Connector 2013, o OSC não tem mais suporte para a sincronização de atividades em cache. 
  
### <a name="cached-synchronization-of-friends"></a>Sincronização em cache de amigos

Se um provedor OSC oferecer suporte à sincronização em cache para amigos, o OSC armazenará em cache as informações dos amigos do usuário conectado na rede social. As informações são armazenadas em cache em uma pasta de contatos do Outlook específica dessa rede social no repositório padrão do usuário no Outlook. O nome da pasta de contatos se baseia no nome da rede social, que o OSC obtém usando a propriedade [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md). 
  
Na sincronização em cache, o OSC armazena informações apenas para os amigos do usuário conectado na rede social. O OSC não acessa informações de não amigos.
  
O intervalo padrão para o OSC atualizar a pasta de contatos de informações dos amigos na rede social é uma vez por dia (ou uma vez a cada 1440 minutos). Esse intervalo de atualização também pode ser definido por uma política de grupo, conforme discutido no início desse tópico.
  
Se ocorrer um erro durante uma atualização, o OSC tentará novamente em um intervalo especificado pelo elemento **contactSyncRestartInterval** no XML de **capabilities**. Esse intervalo de repetição tem um valor padrão de 30 minutos e também pode ser definido por uma política de grupo. 
  
Quando um usuário abre um Cartão de Visita e seleciona a guia **Novidades**, essa guia**** é atualizada. Da mesma forma, quando um usuário do Outlook seleciona novamente um item no Outlook ou seleciona novamente uma pessoa no Painel de Pessoas, esse painel é atualizado. Se o intervalo de atualização de cache não tiver expirado, o OSC acessará o cache para saber mais sobre o usuário selecionado. Isso evita a sobrecarga de usar a extensibilidade do provedor OSC para acessar a rede social. Se o intervalo de atualização tiver expirado, o OSC chamará o método [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) para saber mais sobre os amigos atuais para o usuário conectado e atualizará o cache na pasta de contatos. 
  
O provedor OSC informa ao OSC que aceita a sincronização em cache de amigos, especificando os seguintes elementos no XML de **recursos**: 
  
- **getFriends** = **true**
    
- **cacheFriends** = **true**
    
- **dynamicContactsLookup** = **false**
    
## <a name="on-demand-synchronization"></a>Sincronização sob demanda

Quando um usuário seleciona a guia **Novidades** em um Cartão de Visita ou seleciona um item diferente do Outlook ou uma pessoa diferente no Painel de Pessoas no Outlook, o OSC atualiza o Cartão de Visita ou o Painel de Pessoas, respectivamente. Se um provedor OSC oferecer suporte à sincronização sob demanda de pessoas ou atividades, o OSC será sincronizado com um cache na memória e atualizará os detalhes, como nome, título, imagem e fluxos de atividades, no Cartão de Visita ou no Painel de Pessoas. Para sincronização sob demanda, diferentemente da sincronização em cache, o OSC tenta atualizar as informações da pessoa, independentemente de essa pessoa ser ou não um amigo do usuário conectado na rede social. 
  
Os dados sob demanda de pessoas (ou atividades) são armazenados apenas na memória. Os dados na memória são limpos quando o aplicativo cliente do Office é desligado ou quando o usuário gera uma atualização do Cartão de Visita ou do Painel de Pessoas e os dados permanecem na memória por mais tempo que o intervalo de atualização. Observe que a atualização da rede social é sempre iniciada por um usuário que atualiza o Cartão de Visita ou o Painel de Pessoas (por exemplo, selecionando um usuário diferente no Painel de Pessoas ou selecionando um item diferente na janela do explorador do Outlook). 

No entanto, o inverso nem sempre é verdade: nem todas as atualizações do Cartão de Visita ou do Painel de Pessoas implicam necessariamente uma atualização da rede social. Se o usuário atualizar o Cartão de Visita ou o Painel de Pessoas e os dados da pessoa (ou da atividade) permanecerem na memória por mais tempo que o intervalo de atualização, o OSC chamará [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) (ou [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md)) para atualizar as informações na memória da rede social. O período permitido para informações de amigos e não amigos na memória é de 24 horas e, para atividades, 30 minutos. 
  
Uma diferença importante entre a sincronização em cache e sob demanda é que a sincronização sob demanda pode buscar informações de pessoas e atividades para amigos e não amigos na rede. Se a pessoa selecionada não for um amigo, o OSC atualizará informações e atividades para essa pessoa se um dos seguintes requisitos for atendido: 
  
- A pessoa é um usuário na rede social e permite a visualização pública de informações de perfil e atividades.
    
- A pessoa está na mesma rede que o usuário conectado naquela rede social (por exemplo, na mesma rede de ex-alunos da universidade).
    
A sincronização sob demanda de pessoas e atividades resulta em mais chamadas para o provedor do provenientes do mecanismo principal do OSC. Redes sociais devem ser capazes de lidar com os requisitos de maior largura de banda da sincronização sob demanda.
  
### <a name="specifying-xml-elements-for-on-demand-synchronization"></a>Especificação de elementos XML para sincronização sob demanda

O provedor OSC informa ao OSC que aceita a sincronização sob demanda de amigos e não amigos, especificando os seguintes elementos no XML de **recursos**: 
  
- **getFriends** = **true**
    
- **cacheFriends** = **false**
    
- **dynamicContactsLookup** = **true**
    
O provedor OSC informa ao OSC que aceita a sincronização sob demanda de atividades, especificando os seguintes elementos no XML de **recursos**: 
  
- **getActivities** = **true**
    
- **cacheActivities** = **false**
    
- **dynamicActivitiesLookupEx** = **true**
    
## <a name="hybrid-synchronization"></a>Sincronização híbrida

Um provedor OSC pode oferecer suporte à sincronização híbrida de amigos e não amigos. Isso pode otimizar as chamadas entre o mecanismo principal do OSC e o provedor OSC, as chamadas para a rede social para sincronização sob demanda de amigos e a moeda dos dados dos amigos. O tempo mínimo que os dados podem permanecer em uma pasta ou na memória, quando aplicável, é o mesmo que os limites nos modos de sincronização em cache ou sob demanda.
  
> [!NOTE]
> Começando com o Outlook Social Connector 2013, o OSC oferece suporte apenas à sincronização sob demanda de atividades e não inclui mais suporte para a sincronização híbrida de atividades. 
  
### <a name="hybrid-synchronization-of-friends-and-non-friends"></a>Sincronização híbrida de amigos e não amigos

Se um provedor OSC oferecer suporte à sincronização híbrida de amigos e não amigos, o OSC fará o seguinte: 
  
- O OSC armazenará informações de amigos do usuário conectado na pasta de contatos específica da rede social.
    
- O OSC armazenará informações de não amigos do usuário conectado na memória.
    
O provedor OSC informa ao OSC que aceita a sincronização híbrida de amigos e não amigos, especificando os seguintes elementos no XML de **recursos**: 
  
- **getFriends** = **true**
    
- **cacheFriends** = **true**
    
- **dynamicContactsLookup** = **true**
    
## <a name="synchronization-intervals"></a>Intervalos de sincronização

A tabela a seguir resume os intervalos de sincronização para informações de amigos e não amigos entre o cache correspondente (pasta ou memória) e a rede social, dependendo do modo de sincronização com suporte. Para o modo de sincronização híbrida, consulte as linhas do modo em cache para amigos e a linha do modo sob demanda para pessoas que não são amigos.
  
|**Modo de sincronização para pessoas**|**Onde o intervalo de atualização é definido**|**Tempo mínimo padrão antes da atualização**|**Substituição da política de grupo**|
|:-----|:-----|:-----|:-----|
|Cache  <br/> |Definido no OSC  <br/> |1440 minutos (24 horas)  <br/> |Valor do Registro do Windows **NetContactSyncInterval** <br/> |
|Em cache  <br/> |Elemento **contactSyncRestartInterval** no XML de **recursos**  <br/> |30 minutos se **contactSyncRestartInterval** não estiver definido  <br/> |Valor do Registro do Windows **contactSyncRestartInterval** <br/> |
|Sob demanda  <br/> |Definido no OSC  <br/> |1440 minutos (24 horas)  <br/> |Valor do Registro do Windows **OnlineSearchExpiryTime** <br/> |
   
A tabela a seguir resume os intervalos de sincronização para atividades de amigos e de não amigos entre o cache correspondente (pasta ou memória) e a rede social, dependendo dos modos de sincronização compatíveis. 
  
|**Modo de sincronização para atividades**|**Onde o intervalo de atualização é definido**|**Tempo mínimo padrão antes da atualização**|**Substituição da política de grupo**|
|:-----|:-----|:-----|:-----|
|Sob demanda  <br/> |Definido no OSC  <br/> |30 minutos  <br/> |Valor do Registro do Windows **OnlineSearchExpiryTime** <br/> |
   
As informações a seguir aplicam-se aos valores de Registro do Windows listados nas duas tabelas:
  
- Chave: `HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\Outlook\SocialConnector`
    
- Valor: valor DWORD entre 1 e 10080
    
## <a name="see-also"></a>Confira também

- [Exemplo do XML de recursos](capabilities-xml-example.md)  
- [XML para recursos](xml-for-capabilities.md)
- [Desenvolvimento de um provedor com o esquema XML do OSC](developing-a-provider-with-the-osc-xml-schema.md)  
- [Como gerenciar o Outlook Social Connector usando uma política de grupo](https://support.microsoft.com/default.aspx?scid=kb%3Ben-US%3B2020103)

