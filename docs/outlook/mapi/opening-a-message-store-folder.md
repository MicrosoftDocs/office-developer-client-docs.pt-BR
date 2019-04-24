---
title: Abrir uma pasta do repositório de mensagens
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d858e4fe-822e-4330-9ed3-4b7d22fa51dc
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: df7db013cb435484c721388abab51ab4ba43828f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331371"
---
# <a name="opening-a-message-store-folder"></a>Abrir uma pasta do repositório de mensagens

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Antes que qualquer pasta possa ser aberta, seu identificador de entrada deve estar disponível. Para a maioria das pastas, isso significa recuperar suas propriedades de **PR_ENTRYID** . Para pastas especiais, como algumas das pastas de sub-árvore IPM e outras pastas raiz, MAPI define propriedades de identificador de entrada especiais que são acessíveis chamando o método **IMAPIProp::** GetProps do repositório de mensagens. Estes identificadores de entrada são sempre de longo prazo e são nomeados da seguinte maneira: 
  
|**Folder**|**Propriedade de identificador de entrada**|
|:-----|:-----|
|Pasta de saída  <br/> |**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) (Somente classe de mensagem IPM)  <br/> |
|pasta Itens Excluídos  <br/> |**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))  <br/> |
|Pasta Itens enviados  <br/> |**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))  <br/> |
|Pasta raiz IPM  <br/> |**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))  <br/> |
|Pasta raiz de resultados de pesquisa  <br/> |**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))  <br/> |
|Pasta raiz de exibições comuns  <br/> |**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))  <br/> |
|Pasta raiz de exibições pessoais  <br/> |**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))  <br/> |
|Pasta raiz de contatos  <br/> |**PR_IPM_CONTACT_ENTRYID** ([PidTagIpmContactEntryId](pidtagipmcontactentryid-canonical-property.md))  <br/> |
|Pasta raiz de rascunhos  <br/> |**PR_IPM_DRAFTS_ENTRYID** ([PidTagIpmDraftsEntryId](pidtagipmdraftsentryid-canonical-property.md))  <br/> |
|Pasta raiz do diário  <br/> |**PR_IPM_JOURNAL_ENTRYID** ([PidTagIpmJournalEntryId](pidtagipmjournalentryid-canonical-property.md))  <br/> |
|Pasta raiz do calendário  <br/> |**PR_IPM_APPOINTMENT_ENTRYID** ([PidTagIpmAppointmentEntryId](pidtagipmappointmententryid-canonical-property.md))  <br/> |
|Pasta raiz de anotações  <br/> |**PR_IPM_NOTE_ENTRYID** ([PidTagIpmNoteEntryId](pidtagipmnoteentryid-canonical-property.md))  <br/> |
|Pasta raiz de tarefas  <br/> |**PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md))  <br/> |
   
Antes de tentar recuperar um desses identificadores de entrada especiais, recupere a propriedade **PR\_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) do repositório de mensagens. **PR\_VALID_FOLDER_MASK** é uma bitmask que identifica qual dos identificadores de entrada especiais existem. Há um bit para cada uma das pastas especiais. Se o bit for definido, ele indica que a pasta correspondente é suportada e tem um identificador de entrada válido. Por exemplo, se a pasta itens excluídos existir e tiver um identificador de entrada válido, a\_pasta IPM_WASTEBASKET_VALID bit será definida no **PR_VALID_FOLDER_MASK**. 
  
## <a name="open-the-folder-where-all-incoming-messages-of-a-particular-class-are-placed"></a>Abrir a pasta onde todas as mensagens de entrada de uma determinada classe são colocadas
  
1. Chame [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md) para recuperar seu identificador de entrada, definindo o parâmetro _lpszMessageClass_ para apontar para uma cadeia de caracteres que identifica a classe de mensagem. Por exemplo, se você deseja abrir a caixa de entrada para sua subárvore IPM, aponte _lpszMessageClass_ para IPM. Se você deseja abrir a pasta de recebimento para mensagens de IPC, defina-a para apontar para IPC. 

   Se não houver uma pasta de recebimento registrada para a classe de mensagens, **GetReceiveFolder** escolherá a pasta de recebimento cuja classe de mensagens associada corresponde ao prefixo mais longo possível da classe de mensagem passada. Para obter mais informações, consulte [MAPI Receive Folders](mapi-receive-folders.md). 
   
   Observe que a propriedade **PR_IPM_OUTBOX_ENTRYID** é usada para abrir a pasta de saída somente para mensagens IPM. Se você estiver abrindo a mensagem de saída para mensagens de IPC, use o identificador de entrada para sua pasta receber. As mensagens de IPC de entrada e de saída são colocadas na pasta receber. 
    
2. Chame um dos quatro métodos **OpenEntry** para abrir a pasta e retornar um ponteiro de interface que você pode usar para acessá-la. Você pode chamar qualquer um dos seguintes métodos para abrir uma pasta: 
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
   - [IMSLogon::OpenEntry](imslogon-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   O método específico escolhido depende da pasta a ser aberta e dos objetos que estão disponíveis no momento. Como o método **IMAPISession** pode abrir qualquer pasta para qualquer repositório de mensagens no perfil atual, chame este **OpenEntry** quando não souber nada sobre a pasta a ser aberta. Se você souber qual é o repositório de mensagens proprietário da pasta e tiver um ponteiro para o repositório de mensagens, chame **IMsgStore:: OpenEntry**. 
    
   Por exemplo, use o método **IMsgStore** para abrir uma pasta de recebimento. Se você tiver um ponteiro para o objeto de logon do provedor de repositório de mensagens, chame **IMSLogon:: OpenEntry**. Como essas chamadas vão diretamente para o provedor de armazenamento de mensagens, e não por meio de MAPI, o processamento é mais rápido. Se a pasta que você está abrindo for uma subpasta de uma pasta que você já abriu, chame o método **IMAPIContainer:: OpenEntry** da pasta aberta. O método **IMAPIContainer** abre apenas subpastas de uma pasta aberta no momento e é o único método garantido para trabalhar com identificadores de entrada de curto prazo. 
    
3. Se você deseja fazer alterações na pasta a ser aberta, especifique um nível de acesso definindo o sinalizador de\_permissão de\_acesso MAPI ou de modificação de MAPI\_na chamada **OpenEntry** . Esses sinalizadores são sugestões para o provedor de repositórios de mensagens para conceder o nível mais alto de\_acesso\_, para o melhor acesso MAPI, ou acesso de\_leitura/gravação, para a modificação de MAPI, ao abrir a pasta. 

   Como esses sinalizadores são apenas sugestões, a pasta pode ou não ser aberta com o nível de acesso esperado. Ao recuperar a propriedade **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)), você pode determinar o intervalo de operações que podem ser executadas na pasta aberta. 
    
   No enTanto, como muitos provedores de repositório de mensagens calculam o valor para essa propriedade sob demanda, em vez de dar suporte a ela como uma propriedade de pasta ou uma coluna em sua tabela de hierarquia, recuperá-la pode ser demorado. Uma estratégia alternativa é tentar qualquer operação que você precise realizar e retornar um erro, se necessário.
    
## <a name="see-also"></a>Confira também

- [Propriedade canônica PidTagEntryId](pidtagentryid-canonical-property.md) 
- [IMAPIProp::GetProps](imapiprop-getprops.md)

