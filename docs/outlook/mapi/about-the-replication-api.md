---
title: Sobre a API de replicação
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5133045a-b1e2-7728-5cd5-6d85eb940cf9
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: 532c01d6885e72753067b2d30bf2bd5f88207176
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329516"
---
# <a name="about-the-replication-api"></a>Sobre a API de replicação

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A API de Replicação fornece a funcionalidade para um provedor de armazenamento de mensagens MAPI sincronizar os itens do Microsoft Outlook 2013 ou do Microsoft Outlook 2010 entre um servidor e um armazenamento local baseado em .pst privado criado para esse provedor. 
  
> [!NOTE]
> Um provedor de armazenamento de mensagens MAPI deve implementar a API de replicação de acordo com as instruções em [Sobre a máquina de estado de replicação](about-the-replication-state-machine.md). O provedor deve usar a API somente em um armazenamento pessoal criado para si mesmo, e não em armazenamentos pessoais criados para outros provedores, porque os armazenamentos pessoais criados para outros provedores podem já ter definido seus próprios mecanismos de replicação com o respectivo servidor. Por exemplo, um arquivo de pasta offline (.ost) mantém sua própria relação de replicação com um servidor Microsoft Exchange. 
  
Para usar a API de Replicação, um provedor de armazenamento de mensagens MAPI deve primeiro abrir e quebrar um armazenamento local baseado em .pst chamando **[NSTServiceEntry](nstserviceentry.md)**. Em seguida, o provedor pode usar as principais interfaces da API, **[IOSTX](iostxiunknown.md)** e **[IPSTX](ipstxiunknown.md)** para realizar a replicação. **IPSTX** é fornecido consultando [em IMsgStore : IMAPIProp](imsgstoreimapiprop.md)e **IOSTX** é fornecido pelo **[IPSTX::GetSyncObject](ipstx-getsyncobject.md)**. 
  
## <a name="the-iostx-interface"></a>A interface IOSTX

A interface **IOSTX** é a interface principal que executa a sincronização na API de Replicação. **O IOSTX** move o armazenamento local por uma série de estados, recuperando informações em cada estado sobre alterações no armazenamento local, bem como informando o armazenamento local de alterações no servidor. A API de Replicação também especifica muitas estruturas de dados que suportam a sincronização. 
  
Um provedor de armazenamento, como um cliente para essa API, usa a API de replicação para quebrar o armazenamento local e mover-se por esses estados, pressionando alterações no armazenamento local (como alterações na hierarquia de pastas ou a adição de novos itens) ao servidor e também recuperando informações sobre alterações no servidor e fornecendo essas informações para a interface **IOSTX.** A interface **IOSTX** adota a Sincronização de Alteração Incremental (ICS) fornecida pelo Microsoft Exchange Server. Para obter mais informações sobre ICS, consulte [Critérios de Avaliação do ICS.](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx) Por **meio do IOSTX,** o cliente usa o ICS para monitorar e sincronizar as alterações incrementais para a hierarquia ou o conteúdo em um armazenamento local. 
  
## <a name="the-ipstx-interface"></a>A interface IPSTX

 **O IPSTX** e cinco outras interfaces **IPSTX *n* ** herdada do **IPSTX** fornecem funcionalidades auxiliares que podem ser usadas ao executar a replicação por meio da interface **IOSTX.** Por exemplo, **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** permite que você faça o armazenamento local emular o Outlook Protocol Manager para fazer o spool de mensagens de saída para um servidor. 
  
Para obter mais informações sobre transições de estado durante a replicação, [consulte Sobre a Máquina de Estado de Replicação.](about-the-replication-state-machine.md)
  
## <a name="the-replication-api"></a>A API de Replicação

A API de Replicação fornece as seguintes definições, tipos de dados e interfaces. Para ver um exemplo de implementação de um provedor de armazenamento para arquivos PST (Pastas Particulares) empacotados, consulte Sobre o Provedor [de Armazenamento PST com Fim](about-the-sample-wrapped-pst-store-provider.md)de Exemplo.
  
Definições:
  
- [Constantes para a API de Replicação](mapi-constants.md)
    
Funções:
  
- **[NSTServiceEntry](nstserviceentry.md)**
    
Tipos de dados:
  
- **[DNHIER](dnhier.md)**
    
- **[DNTBL](dntbl.md)**
    
- **[DNTBLE](dntble.md)**
    
- **[FEID](feid.md)**
    
- **[HDRSYNC](hdrsync.md)**
    
- **[LTID](ltid.md)**
    
- **[MEID](meid.md)**
    
- **[OLFI](olfi.md)**
    
- **[SKEY](skey.md)**
    
- **[SYNC](sync.md)**
    
- **[SYNCCONT](synccont.md)**
    
- **[SYNCSTATE](syncstate.md)**
    
- **[UPDEL](updel.md)**
    
- **[UPDELE](updele.md)**
    
- **[UPFLD](upfld.md)**
    
- **[UPHIER](uphier.md)**
    
- **[UPMOV](upmov.md)**
    
- **[UPMSG](upmsg.md)**
    
- **[UPREAD](upread.md)**
    
- **[UPREADE](upreade.md)**
    
- **[UPTBL](uptbl.md)**
    
- **[UPTBLE](uptble.md)**
    
Interfaces:
  
- **[IOSTX](iostxiunknown.md)**
    
- **[IPSTX](ipstxiunknown.md)**
    
- **[IPSTX2](ipstx2ipstx.md)**
    
- **[IPSTX3](ipstx3ipstx2.md)**
    
- **[IPSTX4](ipstx4ipstx3.md)**
    
- **[IPSTX5](ipstx5ipstx4.md)**
    
- **[IPSTX6](ipstx6ipstx5.md)**
    

