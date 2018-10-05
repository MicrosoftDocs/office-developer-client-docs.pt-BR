---
title: Sobre a API de replicação
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5133045a-b1e2-7728-5cd5-6d85eb940cf9
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: 532c01d6885e72753067b2d30bf2bd5f88207176
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396054"
---
# <a name="about-the-replication-api"></a>Sobre a API de replicação

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A API de replicação fornece a funcionalidade para um provedor de armazenamento de mensagem MAPI sincronizar o Microsoft Outlook 2013 ou o Microsoft Outlook 2010 itens entre um servidor e um repositório local privado baseada em. pst que é criado para o provedor. 
  
> [!NOTE]
> Um provedor de armazenamento de mensagem MAPI deve implementar a API de replicação de acordo com as instruções [Sobre a máquina de estado de replicação](about-the-replication-state-machine.md). O provedor deve usar a API somente em um repositório pessoal criado para si mesmo e não em repositórios de pessoais criados para outros provedores, pois armazenamentos pessoais criada para outros provedores talvez já tiver configurado seus próprios mecanismos de replicação com o respectivo servidor. Por exemplo, um arquivo de pasta offline (. ost) mantém sua própria relação de replicação com um servidor Microsoft Exchange. 
  
Para usar a API de replicação, um provedor de armazenamento de mensagem MAPI deve primeiro abrir e quebrar um armazenamento local com base em. pst chamando **[NSTServiceEntry](nstserviceentry.md)**. O provedor, em seguida, pode usar as interfaces principais da API, **[IOSTX](iostxiunknown.md)** e **[IPSTX](ipstxiunknown.md)**, para realizar a replicação. **IPSTX** é fornecida pelo consultando [IMsgStore: IMAPIProp](imsgstoreimapiprop.md), e **IOSTX** é fornecida pelo **[IPSTX::GetSyncObject](ipstx-getsyncobject.md)**. 
  
## <a name="the-iostx-interface"></a>A Interface IOSTX

A interface **IOSTX** é o principal que realiza a sincronização do API de replicação. **IOSTX** move o armazenamento local por meio de uma série de estados, recuperando informações em cada estado sobre alterações no armazenamento local, bem como informando o armazenamento local das alterações no servidor. A API de replicação também especifica muitas estruturas de dados que dão suporte a sincronização. 
  
Um provedor de armazenamento, como um cliente para essa API, usa a API de replicação para quebrar o armazenamento local e mover por meio desses estados, envio de alterações no repositório local (por exemplo, alterações para a hierarquia de pastas ou a adição de novos itens) para o servidor e também recuperar informações sobre alterações no servidor e fornecer essas informações para a interface **IOSTX** . A interface **IOSTX** adota sincronização de alteração Incremental (ICS) fornecidos pelo Microsoft Exchange Server. Para obter mais informações sobre o ICS, consulte [ICS critérios de avaliação](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx). Por meio de **IOSTX**, o cliente usa ICS para monitorar e sincronizar alterações incrementais a hierarquia ou conteúdo em um repositório local. 
  
## <a name="the-ipstx-interface"></a>A Interface IPSTX

 **IPSTX** e cinco outros * * IPSTX *n* * * as interfaces que herdam **IPSTX** fornecem funcionalidade de auxiliar que pode ser usada ao executar uma replicação por meio da interface **IOSTX** . Por exemplo, **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** permite que você faça com que o armazenamento local emular o Gerenciador de protocolo do Outlook para spool mensagens de saída para um servidor. 
  
Para obter mais informações sobre transições de estado durante a replicação, consulte [Sobre a máquina de estado de replicação](about-the-replication-state-machine.md).
  
## <a name="the-replication-api"></a>A API de replicação

A API de replicação fornece as seguintes definições, tipos de dados e interfaces. Para uma implementação da amostra de um provedor de repositório de arquivos com quebra de pastas particulares (. PST), consulte [Sobre o Sample quebradas PST Store Provider](about-the-sample-wrapped-pst-store-provider.md).
  
Definições:
  
- [Constantes para a API de replicação](mapi-constants.md)
    
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
    

