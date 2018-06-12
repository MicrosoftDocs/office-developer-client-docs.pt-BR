---
title: Abrir uma pasta de repositório de mensagens
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d858e4fe-822e-4330-9ed3-4b7d22fa51dc
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 63b8224ad56e2b9985c9d733e2a3c27c67eb2f7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768178"
---
# <a name="opening-a-message-store-folder"></a>Abrir uma pasta de repositório de mensagens

**Aplica-se a**: Outlook 
  
Antes de qualquer pasta pode ser aberta, seu identificador de entrada deve estar disponível. Para a maioria das pastas, isso significa que a recuperação de suas propriedades **PR_ENTRYID** . Para pastas especiais, como algumas das pastas subárvore IPM e outras pastas raiz, MAPI define propriedades de identificador de entrada especiais que estão acessíveis chamando o método de **IMAPIProp::GetProps** do armazenamento de mensagens. Esses identificadores de entrada são sempre longo prazo e são nomeados da seguinte maneira: 
  
|**Folder**|**Propriedade do identificador de entrada**|
|:-----|:-----|
|Pasta caixa de saída  <br/> |**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) (Somente para classe de mensagem IPM)  <br/> |
|Pasta de itens excluídos  <br/> |**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))  <br/> |
|Pasta Itens enviados  <br/> |**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))  <br/> |
|Pasta de raiz IPM  <br/> |**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))  <br/> |
|Pasta raiz de resultados de pesquisa  <br/> |**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))  <br/> |
|Pasta raiz de modos de exibição comuns  <br/> |**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))  <br/> |
|Pasta raiz de exibições pessoais  <br/> |**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))  <br/> |
|Pasta raiz de contatos  <br/> |**PR_IPM_CONTACT_ENTRYID** ([PidTagIpmContactEntryId](pidtagipmcontactentryid-canonical-property.md))  <br/> |
|Pasta raiz de rascunhos  <br/> |**PR_IPM_DRAFTS_ENTRYID** ([PidTagIpmDraftsEntryId](pidtagipmdraftsentryid-canonical-property.md))  <br/> |
|Pasta raiz de diário  <br/> |**PR_IPM_JOURNAL_ENTRYID** ([PidTagIpmJournalEntryId](pidtagipmjournalentryid-canonical-property.md))  <br/> |
|Pasta raiz de calendário  <br/> |**PR_IPM_APPOINTMENT_ENTRYID** ([PidTagIpmAppointmentEntryId](pidtagipmappointmententryid-canonical-property.md))  <br/> |
|Pasta raiz de anotações  <br/> |**PR_IPM_NOTE_ENTRYID** ([PidTagIpmNoteEntryId](pidtagipmnoteentryid-canonical-property.md))  <br/> |
|Pasta raiz de tarefas  <br/> |**PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md))  <br/> |
   
Antes de tentar recuperar um desses identificadores de entrada especial, recuperar o **PR\_VALID_FOLDER_MASK** propriedade ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) o armazenamento de mensagens. **PR\_VALID_FOLDER_MASK** é uma bitmask que identifica quais da entrada especial identificadores existirem. Não há um bit para cada uma das pastas especiais. Se o bit for definido, ele indica que a pasta correspondente é suportada e tem um identificador de entrada válida. Por exemplo, se a pasta Itens excluídos existe e tem um identificador de entrada válida, na pasta\_IPM_WASTEBASKET_VALID bit será definido em **PR_VALID_FOLDER_MASK**. 
  
## <a name="open-the-folder-where-all-incoming-messages-of-a-particular-class-are-placed"></a>Abra a pasta onde todas as mensagens recebidas de uma determinada classe são colocadas
  
1. Chame [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) para recuperar seu identificador de entrada, definindo o parâmetro _lpszMessageClass_ para apontar para uma cadeia de caracteres que identifica a classe de mensagem. Por exemplo, se você deseja abrir a caixa de entrada para sua subárvore IPM, aponte _lpszMessageClass_ IPM. Se você deseja abrir a pasta de recebimento de mensagens de CPI, defina-lo para apontar para CPI. 

   Se não houver nenhuma pasta de recebimento registrados para a classe de mensagem, **GetReceiveFolder** escolhe passados a pasta de recebimento cujo classe de mensagem associada corresponde ao prefixo possível mais longa da classe de mensagem. Para obter mais informações, consulte [Pastas de recebimento de MAPI](mapi-receive-folders.md). 
   
   Observe que a propriedade **PR_IPM_OUTBOX_ENTRYID** é usada para abrir a pasta caixa de saída apenas para mensagens IPM. Se você estiver abrindo a caixa de saída para mensagens de CPI, em vez disso, use o identificador de entrada para sua pasta de recebimento. Mensagens de CPI de entrada e saídas são colocadas na pasta de recebimento. 
    
2. Chame um dos quatro métodos **OpenEntry** para abrir a pasta e retornar um ponteiro de interface que você pode usar para acessá-lo. Você pode chamar qualquer um dos seguintes métodos para abrir uma pasta: 
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
   - [IMSLogon::OpenEntry](imslogon-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   O método específico que você escolher depende da pasta a ser aberto e os objetos que estão disponíveis no momento. Porque o método **IMAPISession** pode abrir qualquer pasta para qualquer armazenamento de mensagens no perfil atual, chame este **OpenEntry** quando você não souber nada sobre a pasta a ser aberto. Se você sabe qual armazenamento de mensagens possui a pasta e você tiver um ponteiro para o armazenamento de mensagens, chame **IMsgStore::OpenEntry**. 
    
   Por exemplo, use o método **IMsgStore** para abrir uma pasta de recebimento. Se você tiver um ponteiro para o objeto de logon do provedor de repositório a mensagem, chame **IMSLogon::OpenEntry**. Porque essas chamadas ir diretamente para o provedor de armazenamento de mensagens e não via MAPI, processamento é mais rápido. Se a pasta que você está abrindo uma subpasta de uma pasta que você já tenha aberto, chame o método de **IMAPIContainer::OpenEntry** de open da pasta. O método **IMAPIContainer** apenas abre as subpastas de uma pasta aberta no momento e é o único método garantido para trabalhar com identificadores de entrada de curto prazo. 
    
3. Se você deseja ser capaz de fazer alterações na pasta a ser aberto, especifique um nível de acesso, definindo o MAPI\_recomendadas\_acesso ou MAPI\_modificar sinalizador na chamada **OpenEntry** . Esses sinalizadores são sugestões para o provedor de armazenamento de mensagem para conceder o nível mais alto de acesso, para MAPI\_recomendadas\_acesso ou acesso de leitura/gravação, para MAPI\_modificar, ao abrir a pasta. 

   Como esses sinalizadores estão apenas sugestões, a pasta pode ou não poderá ser aberta com o nível de acesso que você espera. Recuperando a propriedade **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)), você pode determinar o intervalo de operações que podem ser executadas na pasta aberta. 
    
   No entanto, como vários provedores de armazenamento de mensagem calcular o valor para essa propriedade em propostas ao invés de suporte-lo como uma propriedade de pasta ou como uma coluna na tabela suas hierarquias, recuperá-los pode ser demorada. Uma estratégia alternativa é executar uma tentativa de qualquer operação que você precisa realizar e retornar um erro, se necessário.
    
## <a name="see-also"></a>Confira também

- [Propriedade canônico PidTagEntryId](pidtagentryid-canonical-property.md) 
- [IMAPIProp::GetProps](imapiprop-getprops.md)

