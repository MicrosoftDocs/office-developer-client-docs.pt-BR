---
title: Criar um item de email simples
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bbf99c4b-3008-4475-a60a-648eaed59d01
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8b7afa8f3c04cb479906f721db8de90e8cf66f11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345190"
---
# <a name="create-a-simple-mail-item"></a>Criar um item de email simples
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
MAPI can be used to create and send a message that requests a read receipt. Quando uma confirmação de leitura é solicitada, o sistema de mensagens gera e retorna um relatório de leitura ao remetente quando o destinatário abre a mensagem.
  
Para obter informações sobre como baixar, exibir e executar o código do aplicativo MFCMAPI e do projeto CreateOutlookItemsAddin referenciados neste tópico, consulte Instalar os [exemplos](how-to-install-the-samples-used-in-this-section.md)usados nesta seção.


### <a name="to-create-and-send-a-message-requesting-a-read-receipt"></a>Para criar e enviar uma mensagem solicitando uma confirmação de leitura

1. Crie uma mensagem de saída. Para obter informações sobre como criar uma mensagem de saída, consulte [Manipulando uma mensagem de saída.](handling-an-outgoing-message.md)
    
2. Adicione a **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) e de definida como **true**.
    
3. Adicione a **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) .
    
4. Adicione a **PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md)) .
    
5. Envie a mensagem chamando o [método IMessage::SubmitMessage.](imessage-submitmessage.md) 
    
A função no arquivo de origem Mails.cpp do projeto  `AddMail` CreateOutlookItemsAddin demonstra estas etapas. A função assume parâmetros da caixa de diálogo Adicionar Email que é exibida quando você clica no comando Adicionar Email no menu Addins no aplicativo de exemplo `AddMail` MFCMAPI.    A função em Mails.cpp exibe a caixa de diálogo e passa os valores da  `DisplayAddMailDialog` caixa de diálogo para a  `AddMail` função. A função não está diretamente relacionada à criação de um item de email usando  `DisplayAddMailDialog` MAPI, portanto, ele não está listado aqui. A  `AddMail` função está listada abaixo. 
  
Observe que o  _parâmetro lpFolder_ passado para o método é um ponteiro para uma  `AddMail` interface [IMAPIFolder](imapifolderimapicontainer.md) que representa a pasta onde a nova mensagem será criada. Dado o _parâmetro lpFolder_ que representa uma interface **IMAPIFolder,** o código chama o [método IMAPIFolder::CreateMessage.](imapifolder-createmessage.md) O **método CreateMessage** retorna um código de sucesso e um ponteiro para um ponteiro para [uma IMessage : interface IMAPIProp.](imessageimapiprop.md) 

A maioria do código de função lida com o trabalho de definição de propriedades em preparação para chamar o `AddMail` [método IMAPIProp::SetProps.](imapiprop-setprops.md) Se a chamada para o método **SetProps** for bem-sucedida, uma chamada para o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) confirma as alterações no armazenamento e cria um novo item de email. Em seguida, se solicitado, o [método IMessage::SubmitMessage](imessage-submitmessage.md) é chamado para enviar a mensagem. 
  
A função usa duas funções auxiliares para criar valores para as propriedades PR_CONVERSATION_INDEX e `AddMail` **PR_REPORT_TAG:**  o e as `BuildConversationIndex` `AddReportTag` funções. A função, localizada em  `BuildConversationIndex` CreateOutlookItemsAddin.cpp, faz o mesmo trabalho que a função [MAPI ScCreateConversationIndex](sccreateconversationindex.md) faz quando um índice de conversa pai não é passado para ela. O formato do buffer de índice de conversa que essas funções geram está documentado na propriedade canônica [PidTagConversationIndex](pidtagconversationindex-canonical-property.md). 

A  `AddReportTag` função, localizada em Mails.cpp, chama a função para criar uma  `BuildReportTag` estrutura para a **PR_REPORT_TAG** propriedade. Para obter informações sobre a estrutura que a função cria, consulte a propriedade canônica  `BuildReportTag` [PidTagReportTag](pidtagreporttag-canonical-property.md).
  
A seguir está a listagem completa da  `AddMail` função. 
  
```cpp
HRESULT AddMail(LPMAPISESSION lpMAPISession,
            LPMAPIFOLDER lpFolder,
            LPWSTR szSubject, // PR_SUBJECT_W, PR_CONVERSATION_TOPIC
            LPWSTR szBody, // PR_BODY_W
            LPWSTR szRecipientName, // Recipient table
            BOOL bHighImportance, // PR_IMPORTANCE
            BOOL bReadReceipt, // PR_READ_RECEIPT_REQUESTED
            BOOL bSubmit,
            BOOL bDeleteAfterSubmit)
{
   if (!lpFolder) return MAPI_E_INVALID_PARAMETER;
   HRESULT hRes = S_OK;
   LPMESSAGE lpMessage = 0;
   // Create a message and set its properties
   hRes = lpFolder->CreateMessage(0,
      0,
      &lpMessage);
   if (SUCCEEDED(hRes))
   {
      // Because the properties to be set are known in advance, 
      // most of the structures involved can be statically declared 
      // to minimize expensive MAPIAllocateBuffer calls.
      SPropValue spvProps[NUM_PROPS] = {0};
      spvProps[p_PR_MESSAGE_CLASS_W].ulPropTag          = PR_MESSAGE_CLASS_W;
      spvProps[p_PR_ICON_INDEX].ulPropTag                 = PR_ICON_INDEX;
      spvProps[p_PR_SUBJECT_W].ulPropTag                = PR_SUBJECT_W;
      spvProps[p_PR_CONVERSATION_TOPIC_W].ulPropTag     = PR_CONVERSATION_TOPIC_W;
      spvProps[p_PR_BODY_W].ulPropTag                   = PR_BODY_W;
      spvProps[p_PR_IMPORTANCE].ulPropTag               = PR_IMPORTANCE;
      spvProps[p_PR_READ_RECEIPT_REQUESTED].ulPropTag   = PR_READ_RECEIPT_REQUESTED;
      spvProps[p_PR_MESSAGE_FLAGS].ulPropTag             = PR_MESSAGE_FLAGS;
      spvProps[p_PR_MSG_EDITOR_FORMAT].ulPropTag         = PR_MSG_EDITOR_FORMAT;
      spvProps[p_PR_MESSAGE_LOCALE_ID].ulPropTag         = PR_MESSAGE_LOCALE_ID;
      spvProps[p_PR_INETMAIL_OVERRIDE_FORMAT].ulPropTag = PR_INETMAIL_OVERRIDE_FORMAT;
      spvProps[p_PR_DELETE_AFTER_SUBMIT].ulPropTag      = PR_DELETE_AFTER_SUBMIT;
      spvProps[p_PR_INTERNET_CPID].ulPropTag            = PR_INTERNET_CPID;
      spvProps[p_PR_CONVERSATION_INDEX].ulPropTag         = PR_CONVERSATION_INDEX;
      spvProps[p_PR_MESSAGE_CLASS_W].Value.lpszW = L"IPM.Note";
      spvProps[p_PR_ICON_INDEX].Value.l = 0x103; // Unsent Mail
      spvProps[p_PR_SUBJECT_W].Value.lpszW = szSubject;
      spvProps[p_PR_CONVERSATION_TOPIC_W].Value.lpszW = szSubject;
      spvProps[p_PR_BODY_W].Value.lpszW = szBody;
      spvProps[p_PR_IMPORTANCE].Value.l = bHighImportance?IMPORTANCE_HIGH:IMPORTANCE_NORMAL;
      spvProps[p_PR_READ_RECEIPT_REQUESTED].Value.b = bReadReceipt?true:false;
      spvProps[p_PR_MESSAGE_FLAGS].Value.l = MSGFLAG_UNSENT;
      spvProps[p_PR_MSG_EDITOR_FORMAT].Value.l = EDITOR_FORMAT_PLAINTEXT;
      spvProps[p_PR_MESSAGE_LOCALE_ID].Value.l = 1033; // (en-us)
      spvProps[p_PR_INETMAIL_OVERRIDE_FORMAT].Value.l = NULL; // Mail system chooses default encoding scheme
      spvProps[p_PR_DELETE_AFTER_SUBMIT].Value.b = bDeleteAfterSubmit?true:false;
      spvProps[p_PR_INTERNET_CPID].Value.l = cpidASCII;
      hRes = BuildConversationIndex(
         &spvProps[p_PR_CONVERSATION_INDEX].Value.bin.cb,
         &spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb);
      if (SUCCEEDED(hRes))
      {
         hRes = lpMessage->SetProps(NUM_PROPS, spvProps, NULL);
         if (SUCCEEDED(hRes))
         {
            hRes = AddRecipient(lpMAPISession,
               lpMessage,
               MAPI_TO,
               szRecipientName);
            AddInLog(true,L"CallMenu: AddRecipient - returned hRes = 0x%08X\n",hRes);
            if (SUCCEEDED(hRes))
            {
               if (bReadReceipt)
               {
                  hRes = AddReportTag(lpMessage);
               }
               if (SUCCEEDED(hRes))
               {
                  hRes = lpMessage->SaveChanges(KEEP_OPEN_READWRITE);
                  if (SUCCEEDED(hRes) && bSubmit)
                  {
                     hRes = lpMessage->SubmitMessage(NULL);
                  }
               }
            }
         }
      }
      if (spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb)
         delete[] spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb;
   }
   if (lpMessage) lpMessage->Release();
   return hRes;
}
```

## <a name="see-also"></a>Confira também

- [Usando MAPI para criar itens do Outlook 2007](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

