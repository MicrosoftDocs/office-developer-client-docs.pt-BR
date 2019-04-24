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
  
A API de replicação fornece a funcionalidade de um provedor de armazenamento de mensagens MAPI para sincronizar os itens do Microsoft Outlook 2013 ou do Microsoft Outlook 2010 entre um servidor e um repositório local baseado em arquivo. pst privado criado para esse provedor. 
  
> [!NOTE]
> Um provedor de repositório de mensagens MAPI deve implementar a API de replicação de acordo com as instruções em [sobre a máquina de estado de replicação](about-the-replication-state-machine.md). O provedor deve usar a API somente em um repositório pessoal criado para si mesmo e não em repositórios pessoais criados para outros provedores, porque os repositórios pessoais criados para outros provedores podem já ter configurado seus próprios mecanismos de replicação com o respectivo servidor. Por exemplo, um arquivo de pasta offline (. ost) mantém sua própria relação de replicação com um servidor do Microsoft Exchange. 
  
Para usar a API de replicação, um provedor de repositório de mensagens MAPI deve primeiro abrir e encapsular um repositório local baseado em arquivo. pst chamando **[NSTServiceEntry](nstserviceentry.md)**. O provedor pode usar as principais interfaces da API, **[IOSTX](iostxiunknown.md)** e **[IPSTX](ipstxiunknown.md)**, para realizar a replicação. O **IPSTX** é fornecido pela consulta no [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)e **IOSTX** é fornecido por **[IPSTX::](ipstx-getsyncobject.md)** getsyncobject. 
  
## <a name="the-iostx-interface"></a>A interface IOSTX

A interface **IOSTX** é a interface principal que realiza a sincronização na API de replicação. O **IOSTX** move o repositório local por meio de uma série de Estados, recuperando informações em cada Estado sobre alterações no repositório local, bem como informando o repositório local de alterações no servidor. A API de replicação também especifica muitas estruturas de dados que dão suporte à sincronização. 
  
Um provedor de repositório, como um cliente para esta API, usa a API de replicação para encapsular o repositório local e se move através desses Estados, colocando as alterações no repositório local (como as alterações na hierarquia de pastas ou a adição de novos itens) no servidor e também recuperando informações sobre alterações no servidor e como fornecer essas informações para a interface do **IOSTX** . A interface **IOSTX** adota a sincronização de alteração incremental (ICS) fornecida pelo Microsoft Exchange Server. Para obter mais informações sobre o ICS, consulte [critérios de avaliação de ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx). Por meio do **IOSTX**, o cliente usa o ICS para monitorar e sincronizar as alterações incrementais na hierarquia ou no conteúdo de um repositório local. 
  
## <a name="the-ipstx-interface"></a>A interface IPSTX

 **IPSTX** e cinco outras interfaces * * IPSTX *n* * * que herdam de **IPSTX** fornecem funcionalidades auxiliares que podem ser usadas ao realizar a replicação por meio da interface **IOSTX** . Por exemplo, **[IPSTX:: EmulateSpooler](ipstx-emulatespooler.md)** permite que você faça com que o repositório local eMule o Gerenciador de protocolos do Outlook para o spool de mensagens de saída para um servidor. 
  
Para obter mais informações sobre as transições de estado durante a replicação, consulte [sobre a máquina de estado de replicação](about-the-replication-state-machine.md).
  
## <a name="the-replication-api"></a>A API de replicação

A API de replicação fornece os seguintes defintions, tipos de dados e interfaces. Para obter um exemplo de implementação de um provedor de repositório para arquivos de pastas particulares encapsuladas (PST), consulte [sobre o exemplo de provedor de repositório PST encapsulado](about-the-sample-wrapped-pst-store-provider.md).
  
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
    
- **[SINCRONIZAÇÃO](sync.md)**
    
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
    

