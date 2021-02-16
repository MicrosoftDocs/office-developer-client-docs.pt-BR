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
# <a name="create-a-simple-mail-item"></a><span data-ttu-id="cf5a3-103">Criar um item de email simples</span><span class="sxs-lookup"><span data-stu-id="cf5a3-103">Create a simple mail item</span></span>
  
<span data-ttu-id="cf5a3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf5a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf5a3-105">MAPI can be used to create and send a message that requests a read receipt.</span><span class="sxs-lookup"><span data-stu-id="cf5a3-105">MAPI can be used to create and send a message that requests a read receipt.</span></span> <span data-ttu-id="cf5a3-106">Quando uma confirmação de leitura é solicitada, o sistema de mensagens gera e retorna um relatório de leitura ao remetente quando o destinatário abre a mensagem.</span><span class="sxs-lookup"><span data-stu-id="cf5a3-106">When a read receipt is requested, the messaging system generates and returns a read report to the sender when the recipient opens the message.</span></span>
  
<span data-ttu-id="cf5a3-107">Para obter informações sobre como baixar, exibir e executar o código do aplicativo MFCMAPI e do projeto CreateOutlookItemsAddin referenciados neste tópico, consulte Instalar os [exemplos](how-to-install-the-samples-used-in-this-section.md)usados nesta seção.</span><span class="sxs-lookup"><span data-stu-id="cf5a3-107">For information about how to download, view, and run the code from the MFCMAPI application and CreateOutlookItemsAddin project referenced in this topic, see [Install the Samples Used in This Section](how-to-install-the-samples-used-in-this-section.md).</span></span>


### <a name="to-create-and-send-a-message-requesting-a-read-receipt"></a><span data-ttu-id="cf5a3-108">Para criar e enviar uma mensagem solicitando uma confirmação de leitura</span><span class="sxs-lookup"><span data-stu-id="cf5a3-108">To create and send a message requesting a read receipt</span></span>

1. <span data-ttu-id="cf5a3-109">Crie uma mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="cf5a3-109">Create an outgoing message.</span></span> <span data-ttu-id="cf5a3-110">Para obter informações sobre como criar uma mensagem de saída, consulte [Manipulando uma mensagem de saída.](handling-an-outgoing-message.md)</span><span class="sxs-lookup"><span data-stu-id="cf5a3-110">For information about how to create an outgoing message, see [Handling an Outgoing Message](handling-an-outgoing-message.md).</span></span>
    
2. <span data-ttu-id="cf5a3-111">Adicione a **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) e de definida como **true**.</span><span class="sxs-lookup"><span data-stu-id="cf5a3-111">Add the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property and set it to **true**.</span></span>
    
3. <span data-ttu-id="cf5a3-112">Adicione a **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) .</span><span class="sxs-lookup"><span data-stu-id="cf5a3-112">Add the **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) property.</span></span>
    
4. <span data-ttu-id="cf5a3-113">Adicione a **PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md)) .</span><span class="sxs-lookup"><span data-stu-id="cf5a3-113">Add the **PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md)) property.</span></span>
    
5. <span data-ttu-id="cf5a3-114">Envie a mensagem chamando o [método IMessage::SubmitMessage.](imessage-submitmessage.md)</span><span class="sxs-lookup"><span data-stu-id="cf5a3-114">Send the message by calling the [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> 
    
<span data-ttu-id="cf5a3-115">A função no arquivo de origem Mails.cpp do projeto  `AddMail` CreateOutlookItemsAddin demonstra estas etapas.</span><span class="sxs-lookup"><span data-stu-id="cf5a3-115">The  `AddMail` function in the Mails.cpp source file of the CreateOutlookItemsAddin project demonstrates these steps.</span></span> <span data-ttu-id="cf5a3-116">A função assume parâmetros da caixa de diálogo Adicionar Email que é exibida quando você clica no comando Adicionar Email no menu Addins no aplicativo de exemplo `AddMail` MFCMAPI.   </span><span class="sxs-lookup"><span data-stu-id="cf5a3-116">The  `AddMail` function takes parameters from the **Add Mail** dialog box that is displayed when you click the **Add Mail** command on the **Addins** menu in the MFCMAPI sample application.</span></span> <span data-ttu-id="cf5a3-117">A função em Mails.cpp exibe a caixa de diálogo e passa os valores da  `DisplayAddMailDialog` caixa de diálogo para a  `AddMail` função.</span><span class="sxs-lookup"><span data-stu-id="cf5a3-117">The  `DisplayAddMailDialog` function in Mails.cpp displays the dialog box and passes the values from the dialog box to the  `AddMail` function.</span></span> <span data-ttu-id="cf5a3-118">A função não está diretamente relacionada à criação de um item de email usando  `DisplayAddMailDialog` MAPI, portanto, ele não está listado aqui.</span><span class="sxs-lookup"><span data-stu-id="cf5a3-118">The  `DisplayAddMailDialog` function does not relate directly to creating a mail item using MAPI, so it is not listed here.</span></span> <span data-ttu-id="cf5a3-119">A  `AddMail` função está listada abaixo.</span><span class="sxs-lookup"><span data-stu-id="cf5a3-119">The  `AddMail` function is listed below.</span></span> 
  
<span data-ttu-id="cf5a3-120">Observe que o  _parâmetro lpFolder_ passado para o método é um ponteiro para uma  `AddMail` interface [IMAPIFolder](imapifolderimapicontainer.md) que representa a pasta onde a nova mensagem será criada.</span><span class="sxs-lookup"><span data-stu-id="cf5a3-120">Note that the  _lpFolder_ parameter passed to the  `AddMail` method is a pointer to an [IMAPIFolder](imapifolderimapicontainer.md) interface that represents the folder where the new message will be created.</span></span> <span data-ttu-id="cf5a3-121">Dado o _parâmetro lpFolder_ que representa uma interface **IMAPIFolder,** o código chama o [método IMAPIFolder::CreateMessage.](imapifolder-createmessage.md)</span><span class="sxs-lookup"><span data-stu-id="cf5a3-121">Given the  _lpFolder_ parameter that represents an **IMAPIFolder** interface, the code calls the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="cf5a3-122">O **método CreateMessage** retorna um código de sucesso e um ponteiro para um ponteiro para [uma IMessage : interface IMAPIProp.](imessageimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="cf5a3-122">The **CreateMessage** method returns a success code and a pointer to a pointer to an [IMessage : IMAPIProp](imessageimapiprop.md) interface.</span></span> 

<span data-ttu-id="cf5a3-123">A maioria do código de função lida com o trabalho de definição de propriedades em preparação para chamar o `AddMail` [método IMAPIProp::SetProps.](imapiprop-setprops.md)</span><span class="sxs-lookup"><span data-stu-id="cf5a3-123">Most of the  `AddMail` function code handles the work of setting properties in preparation for calling the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="cf5a3-124">Se a chamada para o método **SetProps** for bem-sucedida, uma chamada para o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) confirma as alterações no armazenamento e cria um novo item de email.</span><span class="sxs-lookup"><span data-stu-id="cf5a3-124">If the call to the **SetProps** method succeeds, a call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method commits the changes to the store and creates a new mail item.</span></span> <span data-ttu-id="cf5a3-125">Em seguida, se solicitado, o [método IMessage::SubmitMessage](imessage-submitmessage.md) é chamado para enviar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="cf5a3-125">Then, if requested, the [IMessage::SubmitMessage](imessage-submitmessage.md) method is called to send the message.</span></span> 
  
<span data-ttu-id="cf5a3-126">A função usa duas funções auxiliares para criar valores para as propriedades PR_CONVERSATION_INDEX e `AddMail` **PR_REPORT_TAG:**  o e as `BuildConversationIndex` `AddReportTag` funções.</span><span class="sxs-lookup"><span data-stu-id="cf5a3-126">The  `AddMail` function uses two helper functions to build values for the **PR_CONVERSATION_INDEX** and **PR_REPORT_TAG** properties: the  `BuildConversationIndex` and  `AddReportTag` functions.</span></span> <span data-ttu-id="cf5a3-127">A função, localizada em  `BuildConversationIndex` CreateOutlookItemsAddin.cpp, faz o mesmo trabalho que a função [MAPI ScCreateConversationIndex](sccreateconversationindex.md) faz quando um índice de conversa pai não é passado para ela.</span><span class="sxs-lookup"><span data-stu-id="cf5a3-127">The  `BuildConversationIndex` function, located in CreateOutlookItemsAddin.cpp, does the same work that the built-in MAPI [ScCreateConversationIndex](sccreateconversationindex.md) function does when a parent conversation index is not passed to it.</span></span> <span data-ttu-id="cf5a3-128">O formato do buffer de índice de conversa que essas funções geram está documentado na propriedade canônica [PidTagConversationIndex](pidtagconversationindex-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="cf5a3-128">The format of the conversation index buffer that these functions generate is documented in [PidTagConversationIndex Canonical Property](pidtagconversationindex-canonical-property.md).</span></span> 

<span data-ttu-id="cf5a3-129">A  `AddReportTag` função, localizada em Mails.cpp, chama a função para criar uma  `BuildReportTag` estrutura para a **PR_REPORT_TAG** propriedade.</span><span class="sxs-lookup"><span data-stu-id="cf5a3-129">The  `AddReportTag` function, located in Mails.cpp, in turn calls the  `BuildReportTag` function to build a structure for the **PR_REPORT_TAG** property.</span></span> <span data-ttu-id="cf5a3-130">Para obter informações sobre a estrutura que a função cria, consulte a propriedade canônica  `BuildReportTag` [PidTagReportTag](pidtagreporttag-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="cf5a3-130">For information about the structure that the  `BuildReportTag` function builds, see [PidTagReportTag Canonical Property](pidtagreporttag-canonical-property.md).</span></span>
  
<span data-ttu-id="cf5a3-131">A seguir está a listagem completa da  `AddMail` função.</span><span class="sxs-lookup"><span data-stu-id="cf5a3-131">The following is the complete listing of the  `AddMail` function.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="cf5a3-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf5a3-132">See also</span></span>

- [<span data-ttu-id="cf5a3-133">Usando MAPI para criar itens do Outlook 2007</span><span class="sxs-lookup"><span data-stu-id="cf5a3-133">Using MAPI to Create Outlook 2007 Items</span></span>](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

