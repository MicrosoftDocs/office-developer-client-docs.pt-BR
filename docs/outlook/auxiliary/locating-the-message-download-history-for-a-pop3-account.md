---
title: Localizando o histórico de download de mensagens para uma conta POP3
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 90a51150-5c2c-4d5b-8717-5dacc8532744
description: Este tópico descreve como um cliente de email pode acessar a propriedade PidTagAttachDataBinary para obter o histórico de download de mensagens para uma conta POP3.
ms.openlocfilehash: 00cf5b02e29a22b5165a4aa339230b604722ab6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765986"
---
# <a name="locating-the-message-download-history-for-a-pop3-account"></a>Localizando o histórico de download de mensagens para uma conta POP3

Este tópico descreve como um cliente de email pode acessar a propriedade [PidTagAttachDataBinary](http://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) para obter o histórico de download de mensagens para uma conta POP3. 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_WhyGetUIDLHistory"> </a>

## <a name="why-get-the-message-download-history"></a>Por que obtém o histórico de download de mensagens?

O provedor de Post Office Protocol (POP) para o Outlook permite que os usuários para recuperar e baixar novas mensagens de email no seu dispositivo local e subsequentemente deixar ou excluir essas mensagens de email no servidor de email. Quando o cliente de email verifica novas mensagens baixar, ele deve ser capaz de identificar e baixe somente as novas mensagens para essa caixa de entrada. O cliente de email faz isso usando primeiro o comando UIDL (ID exclusiva listando), que obtém um mapa de cada mensagem que nunca foi entregue para essa caixa de entrada para um identificador exclusivo (UID). O cliente também obtém o histórico de download da mensagem para mensagens que foram baixadas ou excluídas da caixa de entrada em que o cliente. Usando o mapa UID da mensagem e o histórico de download, o cliente pode, em seguida, identifique essas mensagens ausentes no histórico de como novo e, portanto, deve ser baixado.
  
Para obter o histórico de download de mensagens para uma caixa de entrada:
  
- Siga as etapas deste tópico para localizar a propriedade **PidTagAttachDataBinary** , que contém o histórico de um objeto binário grande (BLOB) que segue um formato específico. 
    
- Continue com [ao analisar o histórico de download de mensagens para uma conta POP3](parsing-the-message-download-history-for-a-pop3-account.md), que descreve como analisar este BLOB para identificar as mensagens que foram baixadas ou excluídas para essa caixa de entrada.
    
## <a name="core-concepts-to-know-for-locating-the-message-download-history"></a>Principais conceitos saber para localizar a mensagem de histórico de downloads

O histórico de download de mensagem para uma caixa de entrada é armazenado em uma propriedade MAPI binária, **PidTagAttachDataBinary**, em um anexo de uma mensagem oculta na caixa de entrada. A tabela 1 mostra os recursos de conceitos que ajudam você a compreender como localizar a mensagem histórico de downloads.
  
**Tabela 1. Principais conceitos**

|**Título do artigo**|**Descrição**|
|:-----|:-----|
|[Pastas ocultada de MAPI](http://msdn.microsoft.com/library/8b3b9c80-f7f4-4f37-bd6b-323469d020f1%28Office.15%29.aspx) <br/> |MAPI permite que os clientes de email armazenar informações em pastas ocultas e mensagens ocultas. Pastas ocultas estão na parte associado de pastas MAPI e normalmente contêm informações que não é visíveis para e não a ser manipulados pelos usuários. Clientes decidir o formato e o conteúdo para armazenar em mensagens ocultas em pastas ocultas.  <br/> |
|[Mensagens MAPI](http://msdn.microsoft.com/library/417c113f-bd98-4515-85d1-09db7fc3a227%28Office.15%29.aspx) <br/> |MAPI armazena mensagens nas pastas, tanto em subárvore IPM padrão que é visível para os usuários de um cliente, ou fora a subárvore e invisível para usuários. As mensagens podem ter adicionais dados armazenados em um anexo, que pode ser na forma de um arquivo, outra mensagem ou um objeto OLE. No caso do histórico de download da mensagem, o histórico é armazenado em uma propriedade de uma mensagem que é anexada a outra mensagem oculta.  <br/> |
|[Visão geral das propriedades de mensagem](http://msdn.microsoft.com/library/447f54de-9f0d-4f73-89b6-bed9cfea9c15%28Office.15%29.aspx) <br/> |Quando um cliente armazena informações em uma mensagem, ela realmente armazena as informações em uma propriedade da mensagem. Muitas propriedades oferece suporte a MAPI — alguns sempre existem e podem ser definidas por clientes, outros são opcionais — e os clientes não podem esperar que eles sejam disponível ou está definida como valores válidos. O histórico de download da mensagem é armazenado na propriedade **PidTagAttachDataBinary** de um anexo para uma mensagem oculta.  <br/> |
|[Perfis MAPI](http://msdn.microsoft.com/library/493c87a4-317d-47ec-850b-342cac59594b%28Office.15%29.aspx) <br/> |Ao fazer logon em uma sessão, o cliente de email seleciona um perfil que descreve os provedores e serviços a serem usados. Um perfil é dividido em seções que contêm propriedades. Especificamente, os [PidTagSearchKey](http://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) (**PR_SEARCH_KEY**) e as propriedades de [PidTagProfileName](http://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx) (**PR_PROFILE_NAME**) sempre existem. Chave de pesquisa de um perfil é exclusivo entre todos os perfis e é armazenado na seção de perfil que é identificada pela **MUID_PROFILE_INSTANCE** (que é definida em MAPIGUID. H). Use [IMAPISession::OpenProfileSection](http://msdn.microsoft.com/library/e2757028-27e7-4fc0-9674-e8e30737ef1d%28Office.15%29.aspx) para abrir a seção e use [IMAPIProp::GetProps](http://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) para obter os valores de propriedade.  <br/> |
|[Tabelas de conteúdo](http://msdn.microsoft.com/library/7b8efb4e-b5be-41b8-81bb-9aa1da421433%28Office.15%29.aspx) <br/> |Provedores de armazenamento de mensagem implementam tabelas de conteúdo para suas pastas. Para mensagens ocultas na parte de uma pasta associado, provedores de armazenamento de mensagem oferecer suporte a tabelas de conteúdo associado e clientes podem usar o método [IMAPIContainer::GetContentsTable](http://msdn.microsoft.com/library/88c7a666-875d-473a-b126-dbbb7009f7d9%28Office.15%29.aspx) para retornar um ponteiro para a tabela de conteúdo associado.  <br/> |
|[Sobre as restrições](http://msdn.microsoft.com/library/e119fa20-08b8-4c8d-93fc-56037220890d%28Office.15%29.aspx) <br/> [Tipos de restrições](http://msdn.microsoft.com/library/0d3bd58b-7100-4117-91ac-27139715c85b%28Office.15%29.aspx) <br/> [Criando uma restrição](http://msdn.microsoft.com/library/12abbd8c-f825-493e-af42-344371d9658e%28Office.15%29.aspx) <br/> [Exemplos de código de restrição](http://msdn.microsoft.com/library/9b82097c-dbd6-4ba0-a6cb-292301f9402b%28Office.15%29.aspx) <br/> |Na MAPI, os clientes podem usar restrições para filtrar tabelas de conteúdo, para pesquisar por linhas que representam as mensagens que têm determinadas propriedades definida como um valor específico. Restrições são definidas usando a estrutura de dados [SRestriction](http://msdn.microsoft.com/library/c12b4409-da6f-480b-87af-1e5baea2e8bd%28Office.15%29.aspx) , que pode conter uma união de estruturas de restrição mais especializadas. O método [IMAPITable:: FindRow](http://msdn.microsoft.com/library/6511368c-9777-497e-9eea-cf390c04b92e%28Office.15%29.aspx) aplica uma restrição e recupera a primeira linha em uma tabela que corresponde aos critérios de restrição.  <br/> |
|[Sobre como registrar repositórios para indexação](http://msdn.microsoft.com/library/dd2aa06a-96e8-1291-18b5-fc3c40b74e4d%28Office.15%29.aspx) <br/> |Use a propriedade [PidTagStoreProvider](http://msdn.microsoft.com/library/6f6cc66f-a08e-4f8e-b33a-d3674319248e%28Office.15%29.aspx) (**PR_MDB_PROVIDER**) para verificar o tipo de provedor de armazenamento. Por exemplo, para verificar se um repositório é um repositório do Exchange, a propriedade **PidTagStoreProvider** deve retornar um valor representado pela constante **pbExchangeProviderPrimaryUserGuid**, que é definida em que o arquivo de cabeçalho público Edkmdb. h.  <br/> |
   
## <a name="locating-the-appropriate-hidden-message-and-attachment"></a>Localizando a mensagem oculta apropriada e o anexo

Agora que sabemos que o histórico de download de mensagem para uma caixa de entrada é na propriedade **PidTagAttachDataBinary** de um anexo para uma mensagem oculta, o procedimento para localizar o anexo apropriado da mensagem oculta apropriado envolve o seguinte procedimentos: 
  
1. [Encontre a mensagem oculta apropriada](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindHiddenMsg)
    
2. [Localizar o anexo apropriado da mensagem oculta](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindAttachment)
    
3. [Acessar a propriedade PidTagAttachDataBinary do anexo da mensagem](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_AccessProp)

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindHiddenMsg"> </a>

### <a name="find-the-appropriate-hidden-message"></a>Encontre a mensagem oculta apropriada

1. Obtenha a propriedade [PidTagSearchKey](http://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) (**PR_SEARCH_KEY**) do perfil, na seção perfil especificada pelo **MUID_PROFILE_INSTANCE**.
    
2. Abra o conteúdo associados para a pasta de caixa de entrada chamando **IMAPIContainer::GetContentsTable**.
    
3. Criar uma restrição com base nos [PidTagConversationKey](http://msdn.microsoft.com/library/52c97d6c-7f4b-4522-aeac-0c1ed8475952%28Office.15%29.aspx) (**PR_CONVERSATION_KEY**), **PidTagSearchKey** (**PR_SEARCH_KEY**) e propriedades de [PidTagMessageClass](http://msdn.microsoft.com/library/1e704023-1992-4b43-857e-0a7da7bc8e87%28Office.15%29.aspx) (**PR_MESSAGE_CLASS**) para obter uma tabela que contém todas as mensagens ocultas no conteúdo associados da caixa de entrada. O exemplo a seguir é um exemplo de uma restrição extraída de [localizar o histórico de UIDL POP3](http://blogs.msdn.com/b/stephen_griffin/archive/2012/12/03/locating-the-pop3-uidl-history.aspx).
    
   ```cpp
      SRestriction rgRes[3]; 
      SPropValue rgProps[3]; 
      rgRes[0].rt = RES_AND; 
      rgRes[0].res.resAnd.cRes = 2; 
      rgRes[0].res.resAnd.lpRes = &amp;rgRes[1]; 
      rgRes[1].rt = RES_PROPERTY; 
      rgRes[1].res.resProperty.relop = RELOP_EQ; 
      rgRes[1].res.resProperty.ulPropTag = PR_CONVERSATION_KEY; 
      rgRes[1].res.resProperty.lpProp = &amp;rgProps[0]; 
      rgRes[2].rt = RES_PROPERTY; 
      rgRes[2].res.resProperty.relop = RELOP_EQ; 
      rgRes[2].res.resProperty.ulPropTag = PR_MESSAGE_CLASS; 
      rgRes[2].res.resProperty.lpProp = &amp;rgProps[1]; 
      rgProps[0].ulPropTag = PR_CONVERSATION_KEY; 
      rgProps[0].Value.bin = pVals[iSearchKey].Value.bin; // PR_SEARCH_KEY from the profile 
      rgProps[1].ulPropTag = PR_MESSAGE_CLASS; 
      rgProps[1].Value.LPSZ = (LPTSTR)"IPM.MessageManager";
   ```

4. Na tabela, encontre a mensagem oculta usando **IMAPITable:: FindRow**.
    
5. Se a etapa 4 não conseguir localizar uma mensagem oculta, altere a restrição para usar o **PidTagSearchKey** (**PR_SEARCH_KEY**) em vez de **PidTagConversationKey**, conforme mostrado a seguir:
    
   ```cpp
    rgRes[1].res.resProperty.ulPropTag = rgProps[0].ulPropTag = PR_SEARCH_KEY;
   ```

6. Encontre a mensagem oculta usando **IMAPITable:: FindRow**. 
    
7. Se a etapa 6 falhar, alterar a restrição para usar [PidTagSubject](http://msdn.microsoft.com/library/aa7ba4d9-c5e0-4ce7-a34e-65f675223bc9%28Office.15%29.aspx) (**PR_SUBJECT**) sendo igual ao valor seguinte (conforme mostrado abaixo usando `printf` estilo de substituição para fins de concisão). 
    
   ```cpp
    "Outlook Message Manager (%s) (KEY: %s)", PR_PROFILE_NAME, HexFromBin(PR_SEARCH_KEY)
   ```

8. Encontre a mensagem oculta usando **IMAPITable:: FindRow**.
    
9. Se você estiver executando o Outlook 2010 ou versão posterior, use os seguintes valores para **PidTagProfileName** (**PR_PROFILE_NAME**) e **PidTagSearchKey** (**PR_SEARCH_KEY**), respectivamente.
    
   ```cpp
    CHAR g_szGeneralKey[] = "General Key"; 
    const SBinary g_binGeneralKey = {sizeof(g_szGeneralKey), (LPBYTE)g_szGeneralKey};
   ```

   Execute as etapas 3 a 8. Se isso não conseguir localizar uma mensagem, volte para as originais etapas 3 a 8.
    
10. Abra a mensagem oculta encontrada na etapa 4, 6 ou 8.

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindAttachment"> </a>

### <a name="find-the-appropriate-attachment-of-the-hidden-message"></a>Localizar o anexo apropriado da mensagem oculta

Como a mensagem oculta pode ter mais de um anexo, procure o anexo apropriado na seguinte ordem.
  
> [!NOTE]
> Esse procedimento usa novamente o `printf` substituição para fins de concisão de estilo. 

1. Procure um anexo cuja [PidTagAttachLongFilename](http://msdn.microsoft.com/library/83b69e8f-0b5a-4992-b5b8-160d3bdfa22a%28Office.15%29.aspx) (**PR_ATTACH_LONG_FILENAME**) corresponde a sequência a seguir, onde `szEmailAddress` é o endereço SMTP do usuário, conforme especificado no perfil do usuário. . 
    
   ```cpp
    "BlobPOP%s", szEmailAddress
   ```

2. Procure um anexo cuja [PidTagAttachFilename](http://msdn.microsoft.com/library/cbf34dd6-7733-47f6-9c41-9d82656ca9dc%28Office.15%29.aspx) (**PR_ATTACH_FILENAME**) corresponde a "BlobPOP %s", `szEmailAddress`.
    
3. Procure um anexo cuja [PidTagDisplayName](http://msdn.microsoft.com/library/bd094e00-5c60-4bb3-9a45-b943fab52876%28Office.15%29.aspx) (**PR_DISPLAY_NAME**) corresponde a "BlobPOP %s", `szEmailAddress`.
    
4. Procure um anexo cuja **PidTagAttachFilename** (**PR_ATTACH_FILENAME**) corresponde a "Blob%.8x", `dwAcctUID`, onde `dwAcctUID` proveniente [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md). Você pode usar o método [IOlkAccount::GetProp](iolkaccount-getprop.md) para acessar a propriedade **PROP_ACCT_MINI_UID** . 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_AccessProp"> </a>

### <a name="access-the-pidtagattachdatabinary-property-of-the-message-attachment"></a>Acessar a propriedade PidTagAttachDataBinary do anexo da mensagem

Após localizar o anexo da mensagem apropriado da mensagem oculto, use **IMAPIProp::GetProps** para ler a propriedade **PidTagAttachDataBinary** do anexo. 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_NextSteps"> </a>

## <a name="next-steps"></a>Próximas etapas

Você aprendeu deste tópico localizar o histórico de download de mensagens da caixa de entrada do cliente de email POP3. Consulte [ao analisar o histórico de download de mensagens para uma conta POP3](parsing-the-message-download-history-for-a-pop3-account.md) para aprender a analisar esse histórico para identificar mensagens que foram baixadas ou excluídas da caixa de entrada. 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_AdditionalRsc"> </a>

## <a name="see-also"></a>Confira também

- [Gerenciando mensagem downloads para contas POP3](managing-message-downloads-for-pop3-accounts.md)   
- [Analisar o histórico de download de mensagens para uma conta POP3](parsing-the-message-download-history-for-a-pop3-account.md)
- [Localizando o histórico UIDL POP3](http://blogs.msdn.com/b/stephen_griffin/archive/2012/12/03/locating-the-pop3-uidl-history.aspx)
    

