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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436535"
---
# <a name="opening-a-message-store-folder"></a>Abrir uma pasta do repositório de mensagens

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para que qualquer pasta possa ser aberta, seu identificador de entrada deve estar disponível. Para a maioria das pastas, isso significa recuperar **suas** PR_ENTRYID propriedades. Para pastas especiais, como algumas das pastas de subárvore do IPM e outras pastas raiz, MAPI define propriedades de identificador de entrada especiais que podem ser acessadas chamando o método **IMAPIProp::GetProps** do armazenamento de mensagens. Esses identificadores de entrada são sempre a longo prazo e são nomeados da seguinte forma: 
  
|**Folder**|**Propriedade do identificador de entrada**|
|:-----|:-----|
|Pasta caixa de saída  <br/> |**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) (somente classe de mensagem IPM)  <br/> |
|pasta Itens Excluídos  <br/> |**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))  <br/> |
|Pasta Itens Enviados  <br/> |**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))  <br/> |
|Pasta raiz do IPM  <br/> |**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))  <br/> |
|Pasta raiz de resultados de pesquisa  <br/> |**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))  <br/> |
|Pasta raiz de exibições comuns  <br/> |**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))  <br/> |
|Pasta raiz de exibições pessoais  <br/> |**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))  <br/> |
|Pasta raiz contatos  <br/> |**PR_IPM_CONTACT_ENTRYID** ([PidTagIpmContactEntryId](pidtagipmcontactentryid-canonical-property.md))  <br/> |
|Pasta raiz rascunhos  <br/> |**PR_IPM_DRAFTS_ENTRYID** ([PidTagIpmDraftsEntryId](pidtagipmdraftsentryid-canonical-property.md))  <br/> |
|Pasta raiz do diário  <br/> |**PR_IPM_JOURNAL_ENTRYID** ([PidTagIpmJournalEntryId](pidtagipmjournalentryid-canonical-property.md))  <br/> |
|Pasta raiz do calendário  <br/> |**PR_IPM_APPOINTMENT_ENTRYID** ([PidTagIpmAppointmentEntryId](pidtagipmappointmententryid-canonical-property.md))  <br/> |
|Pasta raiz de anotações  <br/> |**PR_IPM_NOTE_ENTRYID** ([PidTagIpmNoteEntryId](pidtagipmnoteentryid-canonical-property.md))  <br/> |
|Pasta raiz de tarefas  <br/> |**PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md))  <br/> |
   
Antes de tentar recuperar um desses identificadores de entrada especiais, recupere a propriedade **PR \_ VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) do armazenamento de mensagens. **PR \_ VALID_FOLDER_MASK** é uma máscara de bits que identifica quais dos identificadores de entrada especiais existem. Há um bit para cada uma das pastas especiais. Se o bit estiver definido, ele indicará que a pasta correspondente é suportada e tem um identificador de entrada válido. Por exemplo, se a pasta Itens Excluídos existir e tiver um identificador de entrada válido, o bit FOLDER IPM_WASTEBASKET_VALID será definido em \_ **PR_VALID_FOLDER_MASK**. 
  
## <a name="open-the-folder-where-all-incoming-messages-of-a-particular-class-are-placed"></a>Abra a pasta onde todas as mensagens de entrada de uma classe específica são colocadas
  
1. Chame [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) para recuperar seu identificador de entrada, definindo o parâmetro  _lpszMessageClass_ para apontar para uma cadeia de caracteres identificando a classe de mensagem. Por exemplo, se você quiser abrir a Caixa de Entrada da subárvore do IPM, aponte  _lpszMessageClass_ para IPM. Se você quiser abrir a pasta de recebimento para mensagens IPC, de definida-a para apontar para IPC. 

   Se não houver pasta de recebimento registrada para a classe de mensagem, **GetReceiveFolder** escolherá a pasta de recebimento cuja classe de mensagem associada corresponde ao prefixo mais longo possível da classe de mensagem passada. Para obter mais informações, consulte [MapI Receive Folders](mapi-receive-folders.md). 
   
   Observe que a **PR_IPM_OUTBOX_ENTRYID** é usada para abrir a pasta Caixa de Saída somente para mensagens IPM. Se você estiver abrindo a Caixa de Saída para mensagens IPC, use o identificador de entrada para sua pasta de recebimento. As mensagens IPC de entrada e de saída são colocadas na pasta de recebimento. 
    
2. Chame um dos quatro **métodos OpenEntry** para abrir a pasta e retornar um ponteiro da interface que você pode usar para acessá-la. Você pode chamar qualquer um dos seguintes métodos para abrir uma pasta: 
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
   - [IMSLogon::OpenEntry](imslogon-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   O método específico que você escolher depende da pasta a ser aberta e dos objetos que estão disponíveis no momento. Como o **método IMAPISession** pode abrir qualquer pasta para qualquer armazenamento de mensagens no perfil atual, chame esse **OpenEntry** quando você não sabe nada sobre a pasta a ser aberta. Se você sabe qual repositório de mensagens possui a pasta e tem um ponteiro para o repositório de mensagens, chame **IMsgStore::OpenEntry**. 
    
   Por exemplo, use o **método IMsgStore** para abrir uma pasta de recebimento. Se você tiver um ponteiro para o objeto de logon do provedor de armazenamento de mensagens, chame **IMSLogon::OpenEntry**. Como essas chamadas vão diretamente para o provedor de armazenamento de mensagens em vez de por MAPI, o processamento é mais rápido. Se a pasta que você está abrindo for uma subpasta de uma pasta que você já abriu, chame o método **IMAPIContainer::OpenEntry** da pasta aberta. O **método IMAPIContainer** só abre subpastas de uma pasta aberta no momento e é o único método garantido para trabalhar com identificadores de entrada de curto prazo. 
    
3. Se você quiser fazer alterações na pasta a ser aberta, especifique um nível de acesso definindo o sinalizador MAPI BEST ACCESS ou MAPI MODIFY na chamada \_ \_ \_ **OpenEntry.** Esses sinalizadores são sugestões para o provedor de armazenamento de mensagens conceder o nível mais alto de acesso, para MAPI BEST ACCESS, ou acesso de \_ \_ leitura/gravação, para MAPI MODIFY, ao abrir \_ a pasta. 

   Como esses sinalizadores são apenas sugestões, a pasta pode ou não ser aberta com o nível de acesso esperado. Ao recuperar a PR_ACCESS **(** [PidTagAccess](pidtagaccess-canonical-property.md)), você pode determinar o intervalo de operações que podem ser executadas na pasta aberta. 
    
   No entanto, como muitos provedores de armazenamento de mensagens calculam o valor dessa propriedade sob demanda, em vez de dar suporte a ela como uma propriedade de pasta ou como uma coluna em sua tabela de hierarquia, recuperá-lo pode ser demorado. Uma estratégia alternativa é tentar qualquer operação que você precise executar e retornar um erro, se necessário.
    
## <a name="see-also"></a>Confira também

- [Propriedade canônica PidTagEntryId](pidtagentryid-canonical-property.md) 
- [IMAPIProp::GetProps](imapiprop-getprops.md)

