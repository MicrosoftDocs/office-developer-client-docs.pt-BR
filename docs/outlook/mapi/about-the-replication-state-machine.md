---
title: Sobre a máquina de estado de replicação
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: cf36c6cb-57b4-7b2b-e23d-e0bc8696de96
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a0644e4bf5c6847d61cc59e203d50f61ad142e84
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416479"
---
# <a name="about-the-replication-state-machine"></a>Sobre a máquina de estado de replicação

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este tópico contém uma visão geral da máquina de estado para a replicação de dados do Microsoft Outlook 2013 e do Microsoft Outlook 2010.
  
> [!NOTE]
> A API de replicação deve ser totalmente implementada de acordo com as instruções deste tópico para ser útil ou compatível. A API de replicação está disponível exclusivamente para replicar as alterações do Outlook 2013 ou Outlook 2010 em um servidor. 
  
## <a name="iostx-and-the-state-machine"></a>IOSTX e a máquina de estado

Um cliente chama **[IOSTX:: SyncBeg](iostx-syncbeg.md)**, **[IOSTX:: SyncEnd](iostx-syncend.md)**, **[IOSTX:: SyncHdrBeg](iostx-synchdrbeg.md)** e **[IOSTX::](iostx-synchdrend.md)** SyncHdrEnd em uma sequência para sincronizar pastas e itens do Outlook 2013 ou do Outlook 2010 entre um repositório local e um servidor. A sequência real de chamadas depende dos dados que precisam ser replicados (por exemplo, uma hierarquia de pastas do Outlook 2013 ou do Outlook 2010, uma pasta do Outlook 2013 ou do Outlook 2010, itens de email, itens de calendário e assim por diante) e a direção da sincronização (se carregar do repositório local para o servidor ou baixar do servidor para o repositório local. Veja a seguir uma sequência típica de chamadas: 
  
1. O cliente chama **IOSTX:: SyncBeg** para iniciar a replicação, especificando um identificador de estado e um ponteiro para um endereço de uma estrutura de dados correspondente. 
    
2. O Outlook 2013 ou o Outlook 2010 aloca a estrutura de dados e inicializa a estrutura de dados com as informações necessárias para o cliente. 
    
3. O cliente realiza a replicação, atualizando a estrutura de dados para transmitir ao repositório local quaisquer informações necessárias sobre a replicação.
    
4. Após executar a replicação, o cliente chama **[IOSTX:: SetSyncResult](iostx-setsyncresult.md)** e **IOSTX:: SyncEnd** para notificar o repositório local da conclusão da replicação específica. 
    
> [!NOTE]
> O cliente sempre chama **IOSTX:: SyncEnd** para encerrar uma replicação que o cliente iniciou para um determinado estado. Dependendo dos dados gerais que o cliente precisa sincronizar, o cliente pode chamar o par de chamadas **IOSTX:: SyncBeg** e **IOSTX:: SyncEnd** mais de uma vez. 
  
## <a name="state-table"></a>Tabela de estado

> [!NOTE]
> A tabela a seguir lista todos os Estados válidos na máquina de estado de replicação, junto com os identificadores de estado e estruturas de dados correspondentes. Na coluna **replicada de dados** , o termo "itens" inclui email, calendário, contato, nota, diário e itens de tarefa. Ao replicar alterações do repositório local para o servidor, use identificadores de estado especificando "UPLOAD" e estruturas de dados com o prefixo "UP" (por exemplo, **LR_SYNC_UPLOAD_HIERARCHY** e **[UPHIER](uphier.md)** ). Ao replicar alterações do servidor para o repositório local, use identificadores de estado especificando "DOWNLOAD" e estruturas de dados com o prefixo "DN" (por exemplo, **LR_SYNC_DOWNLOAD_HIERARCHY** e **[DNHIER](dnhier.md)** ). 
  
|||||
|:-----|:-----|:-----|:-----|
|**State** <br/> |**Dados replicados** <br/> |**Identificador de estado** <br/> |**Estrutura de dados** <br/> |
|[Estado Ocioso](idle-state.md) <br/> | *None*  <br/> |**LR_SYNC_IDLE** <br/> | *None*  <br/> |
|[Estado Sincronizar](synchronize-state.md) <br/> |Pastas ou itens  <br/> |**LR_SYNC** <br/> |**[SINCRONIZAÇÃO](sync.md)** <br/> |
|[Estado de hierarquia de upload](upload-hierarchy-state.md) <br/> |Folders  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**[UPHIER](uphier.md)** <br/> |
|[Carregar estado da pasta](upload-folder-state.md) <br/> |Folder  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**[UPFLD](upfld.md)** <br/> |
|[Sincronizar o estado do conteúdo](synchronize-contents-state.md) <br/> |Itens  <br/> |**LR_SYNC_CONTENTS** <br/> |**[SYNCCONT](synccont.md)** <br/> |
|[Carregar estado da tabela](upload-table-state.md) <br/> |Itens  <br/> |**LR_SYNC_UPLOAD_TABLE** <br/> |**[UPTBL](uptbl.md)** <br/> |
|[Carregar estado da mensagem](upload-message-state.md) <br/> |Item  <br/> |**LR_SYNC_UPLOAD_MESSAGE** <br/> |**[UPMSG](upmsg.md)** <br/> |
|[Carregar estado de status de leitura](upload-read-status-state.md) <br/> |Itens  <br/> |**LR_SYNC_UPLOAD_MESSAGE_READ** <br/> |**[UPREAD](upread.md)** <br/> |
|[Carregar estado de status de exclusão](upload-delete-status-state.md) <br/> |Itens  <br/> |**LR_SYNC_UPLOAD_MESSAGE_DEL** <br/> |**[UPDEL](updel.md)** <br/> |
|[Estado de hierarquia de download](download-hierarchy-state.md) <br/> |Folders  <br/> |**LR_SYNC_DOWNLOAD_HIERARCHY** <br/> |**[DNHIER](dnhier.md)** <br/> |
|[Baixar o estado da tabela](download-table-state.md) <br/> |Itens  <br/> |**LR_SYNC_DOWNLOAD_TABLE** <br/> |**[DNTBL](dntbl.md)** <br/> |
|[Baixar o estado do cabeçalho da mensagem](download-message-header-state.md) <br/> |Cabeçalho da mensagem  <br/> |**LR_SYNC_DOWNLOAD_HEADER** <br/> |**[HDRSYNC](hdrsync.md)** <br/> |
   
## <a name="state-transition-diagram"></a>Diagrama de transição de estado

O diagrama a seguir mostra as transições de estado que ocorrem ao carregar ou executar uma sincronização completa (download seguido de upload) de pastas ou conteúdo de pastas (email, calendário, contato, nota, tarefa ou itens de diário). 
  
@ @ @ @ @NEED INSERIR ARTE AQUI QUE ESTÁ AUSENTE @ @ @ @ @ @
  
## <a name="example-uploading-a-folder-hierarchy"></a>Exemplo: upload de uma hierarquia de pastas

 Ao carregar uma hierarquia de pastas, a seguinte sequência de etapas ocorre: 
  
|||||
|:-----|:-----|:-----|:-----|
|**Etapa** <br/> |**Ação** <br/> |**State** <br/> |**Estrutura de dados relacionada** <br/> |
|1.  <br/> |O cliente inicia o upload de hierarquia com **IOSTX:: SyncBeg**.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|2.  <br/> |O Outlook 2013 ou o Outlook 2010 preenche **UPHIER** com informações para o cliente. Isso inclui a inicialização dos parâmetros de [out]: *iEnt* é definido como 0 e a *cEnt* como o número de pastas na hierarquia que precisa de upload.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|3.  <br/> |O cliente faz o carregamento da hierarquia real. Por exemplo, se a *cento* for 10, para cada uma das 10 pastas, o cliente chamará **IOSTX:: SyncBeg**, especificando o identificador de estado apropriado e a estrutura de dados para carregar uma pasta.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|4.  <br/> |O Outlook 2013 ou o Outlook 2010 preenche o **UPFLD** inicializando seus parâmetros [out], incluindo o motivo do carregamento da pasta, o ponteiro para o objeto Folder e a identificação de entrada da pasta.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|5.  <br/> |O cliente carrega a pasta especificada.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|6.  <br/> |O cliente notifica o repositório local da conclusão do carregamento da pasta: após o êxito, o cliente define o parâmetro [in] *parâmetroulflags* no **UPFLD** com o **UPF_OK**e, em seguida, chama **IOSTX:: SetSyncResult (S_OK)** e **IOSTX:: SyncEnd **. Após a falha, o cliente não definiria *parâmetroulflags* com o sinalizador **UPF_OK** . Ele chama **IOSTX:: SetSyncResult**, passando o valor **HRESULT** e **IOSTX:: SyncEnd**.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|7.  <br/> |Se **UPF_OK** estiver definido, o Outlook 2013 ou o Outlook 2010 desmarcará a solicitação interna para carregar a pasta. Em seguida, independentemente do estado de *parâmetroulflags* , ele limpará qualquer informação de escrituração interna. Enquanto ainda houver pastas na hierarquia para carregar (o*iEnt* ainda é menor que a *cento*), o cliente e o Outlook 2013 ou o Outlook 2010 repetirão as etapas 3 a 7.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|8.  <br/> |O cliente notifica o repositório local da conclusão do carregamento da hierarquia: após o êxito, o cliente define o sinalizador [in] no **UPHIER** com **UPH_OK**e, em seguida, chama **IOSTX:: SetSyncResult (S_OK)** and **IOSTX:: SyncEnd**. Após a falha, o cliente não definiria o sinalizador **UPH_OK** . Ele chama **IOSTX:: SetSyncResult**, passando o valor **HRESULT** e **IOSTX:: SyncEnd**.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|9.  <br/> |Se **UPH_OK** estiver definido, o Outlook 2013 ou o Outlook 2010 desmarcará a solicitação interna para carregar a hierarquia. Em seguida, independentemente do estado de *parâmetroulflags* , ele limpará qualquer informação de escrituração interna.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
   
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[SYNCSTATE](syncstate.md)

