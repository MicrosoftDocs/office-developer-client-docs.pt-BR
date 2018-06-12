---
title: Sobre a máquina de estado de replicação
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: cf36c6cb-57b4-7b2b-e23d-e0bc8696de96
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 9ea18f8e5c7eb758780727829fb1e18d2a19ec92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766103"
---
# <a name="about-the-replication-state-machine"></a>Sobre a máquina de estado de replicação

  
  
**Aplica-se a**: Outlook 
  
Este tópico contém uma visão geral da máquina de estado de replicação de dados do Microsoft Outlook 2013 e o Microsoft Outlook 2010.
  
> [!NOTE]
> A API de replicação deve ser totalmente implementada acordo com as instruções deste tópico para poder ser útil ou são suportados. A API de replicação é disponível exclusivamente para replicar as alterações do Outlook 2013 ou o Outlook 2010 para e de um servidor. 
  
## <a name="iostx-and-the-state-machine"></a>IOSTX e a máquina de estado

Um cliente chama **[IOSTX::SyncBeg](iostx-syncbeg.md)**, **[IOSTX::SyncEnd](iostx-syncend.md)**, **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** e **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** em uma sequência para sincronizar pastas do Outlook 2013 ou o Outlook 2010 e itens entre um repositório local e um servidor. A sequência real das chamadas depende dos dados que precisa ser replicado (por exemplo, uma hierarquia de pastas do Outlook 2013 ou o Outlook 2010, um Outlook 2013 ou pasta do Outlook 2010, itens de email, itens de calendário e assim por diante) e a direção da sincronização (se carregamento do armazenamento local para o servidor ou fazer o download do servidor para armazenamento local). Aqui está uma sequência típica de chamadas: 
  
1. O cliente chama **IOSTX::SyncBeg** para começar a replicação, especificando um identificador de estado e um ponteiro para um endereço de uma estrutura de dados correspondente. 
    
2. Outlook 2013 ou o Outlook 2010 aloca a estrutura de dados e inicializa a estrutura de dados com as informações necessárias para o cliente. 
    
3. O cliente executa a replicação, atualizando a estrutura de dados para transmitir no repositório local quaisquer informações necessárias sobre a replicação.
    
4. Depois de realizar a replicação, o cliente chama **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** e **IOSTX::SyncEnd** para notificar o armazenamento local da conclusão da replicação específica. 
    
> [!NOTE]
> O cliente sempre chama **IOSTX::SyncEnd** para encerrar uma replicação que o cliente tiver começado para um determinado estado. Dependendo dos dados gerais que o cliente precisa sincronizar, o cliente pode chamar o par de chamadas **IOSTX::SyncBeg** e **IOSTX::SyncEnd** mais de uma vez. 
  
## <a name="state-table"></a>Tabela de controle de sessão

> [!NOTE]
> A tabela a seguir lista todos os estados válidos na máquina de estado de replicação, juntamente com os identificadores de estado correspondentes e estruturas de dados. Na coluna de **Dados duplicados** , o termo "itens" inclui email, calendário, contatos, nota, diário e itens de tarefa. Quando a replicação de alterações do armazenamento local para o servidor, use os identificadores de estado especificando "Carregar" e estruturas de dados com o prefixo "Backup" (por exemplo, **LR_SYNC_UPLOAD_HIERARCHY** e **[UPHIER](uphier.md)** ). Quando a replicação de alterações no repositório local do servidor, use os identificadores de estado especificando "DOWNLOAD" e estruturas de dados com o prefixo "DN" (por exemplo, **LR_SYNC_DOWNLOAD_HIERARCHY** e **[DNHIER](dnhier.md)** ). 
  
|||||
|:-----|:-----|:-----|:-----|
|**Estado** <br/> |**Dados replicados** <br/> |**Identificador de controle de sessão** <br/> |**Estrutura de dados** <br/> |
|[Estado ocioso](idle-state.md) <br/> | *None*  <br/> |**LR_SYNC_IDLE** <br/> | *None*  <br/> |
|[Sincronizar o estado](synchronize-state.md) <br/> |Pastas ou itens  <br/> |**LR_SYNC** <br/> |**[SINCRONIZAÇÃO](sync.md)** <br/> |
|[Carregar o estado de hierarquia](upload-hierarchy-state.md) <br/> |Pastas  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**[UPHIER](uphier.md)** <br/> |
|[Carregar o estado de pasta](upload-folder-state.md) <br/> |Pasta  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**[UPFLD](upfld.md)** <br/> |
|[Sincronizar o estado de conteúdo](synchronize-contents-state.md) <br/> |Items  <br/> |**LR_SYNC_CONTENTS** <br/> |**[SYNCCONT](synccont.md)** <br/> |
|[Carregar o estado da tabela](upload-table-state.md) <br/> |Items  <br/> |**LR_SYNC_UPLOAD_TABLE** <br/> |**[UPTBL](uptbl.md)** <br/> |
|[Carregar o estado da mensagem](upload-message-state.md) <br/> |Item  <br/> |**LR_SYNC_UPLOAD_MESSAGE** <br/> |**[UPMSG](upmsg.md)** <br/> |
|[Carregar o estado de leitura de status](upload-read-status-state.md) <br/> |Items  <br/> |**LR_SYNC_UPLOAD_MESSAGE_READ** <br/> |**[UPREAD](upread.md)** <br/> |
|[Carregar excluir o estado de status](upload-delete-status-state.md) <br/> |Items  <br/> |**LR_SYNC_UPLOAD_MESSAGE_DEL** <br/> |**[UPDEL](updel.md)** <br/> |
|[Baixe o estado de hierarquia](download-hierarchy-state.md) <br/> |Pastas  <br/> |**LR_SYNC_DOWNLOAD_HIERARCHY** <br/> |**[DNHIER](dnhier.md)** <br/> |
|[Baixe o estado da tabela](download-table-state.md) <br/> |Items  <br/> |**LR_SYNC_DOWNLOAD_TABLE** <br/> |**[DNTBL](dntbl.md)** <br/> |
|[Baixe o estado do cabeçalho da mensagem](download-message-header-state.md) <br/> |Cabeçalho da mensagem  <br/> |**LR_SYNC_DOWNLOAD_HEADER** <br/> |**[HDRSYNC](hdrsync.md)** <br/> |
   
## <a name="state-transition-diagram"></a>Diagrama de transição de estado

O diagrama a seguir mostra as transições de estado que ocorrem quando o carregamento ou executar uma sincronização completa (Baixando seguido de carregamento) de pastas ou o conteúdo das pastas (email, calendário, contatos, nota, tarefa ou itens de diário). 
  
@@@NEED PARA INSERIR ARTE AQUI QUE ESTÁ FALTANDO @ @ @
  
## <a name="example-uploading-a-folder-hierarchy"></a>Exemplo: Carregar uma hierarquia de pastas

 Ao carregar uma hierarquia de pastas, ocorre a sequência das etapas a seguir: 
  
|||||
|:-----|:-----|:-----|:-----|
|**Etapa** <br/> |**Ação** <br/> |**Estado** <br/> |**Estrutura de dados relacionados** <br/> |
|1.  <br/> |O cliente inicia o carregamento de hierarquia com **IOSTX::SyncBeg**.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|2.  <br/> |Outlook 2013 ou o Outlook 2010 preenche **UPHIER** com informações para o cliente. Isso inclui Inicializando os parâmetros [out]: *iEnt* for definido como 0 e *cEnt* ao número de pastas na hierarquia que precisa de carregamento.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|3.  <br/> |O cliente faz o carregamento de hierarquia real. Por exemplo, se *cEnt* for 10, para cada uma das 10 pastas, o cliente chama **IOSTX::SyncBeg**, especificando o identificador de estado apropriado e a estrutura de dados para carregar uma pasta.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|4.  <br/> |Outlook 2013 ou o Outlook 2010 preenche **UPFLD** Inicializando seus parâmetros [out], incluindo o motivo para o carregamento de pasta, o ponteiro para o objeto de pasta e a identificação de entrada para a pasta.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|5.  <br/> |O cliente carrega a pasta especificada.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|6.  <br/> |O cliente notifica o armazenamento local após a conclusão do carregamento pasta: após o sucesso, o cliente define o [in] parâmetro *ulFlags* em **UPFLD** com **UPF_OK**e, em seguida, chamadas **IOSTX::SetSyncResult (S_OK)** e **IOSTX::SyncEnd **. Após a falha, o cliente não seria definido *ulFlags* com o sinalizador **UPF_OK** . Ele chama **IOSTX::SetSyncResult**, passando o valor de **HRESULT** e **IOSTX::SyncEnd**.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|7.  <br/> |Se **UPF_OK** estiver definida, o Outlook 2013 ou o Outlook 2010 limpará a solicitação interna para carregar a pasta. Em seguida, independentemente do estado *ulFlags* , ele irá limpar qualquer informação de escrituração contábil interno. Enquanto ainda houver pastas na hierarquia para carregar (*iEnt* é ainda menor *cEnt*), o cliente e o Outlook 2010 ou Outlook 2013 Repita as etapas 3 a 7.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|8.  <br/> |O cliente notifica o armazenamento local após a conclusão do carregamento hierarquia: após o sucesso, o cliente define o [in] sinalizar em **UPHIER** com **UPH_OK**e, em seguida, chamadas **IOSTX::SetSyncResult (S_OK)** e **IOSTX::SyncEnd**. Após a falha, o cliente não seria definido o sinalizador **UPH_OK** . Ele chama **IOSTX::SetSyncResult**, passando o valor de **HRESULT** e **IOSTX::SyncEnd**.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|9.  <br/> |Se **UPH_OK** estiver definida, o Outlook 2013 ou o Outlook 2010 limpará a solicitação interna de carregamento da hierarquia. Em seguida, independentemente do estado *ulFlags* , ele irá limpar qualquer informação de escrituração contábil interno.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
   
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[ESTADO DE SINCRONIZAÇÃO](syncstate.md)

