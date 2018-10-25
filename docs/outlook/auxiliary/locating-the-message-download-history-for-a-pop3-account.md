---
title: Localizar o histórico de download de mensagens de uma conta POP3
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 90a51150-5c2c-4d5b-8717-5dacc8532744
description: Este tópico descreve como um cliente de email pode acessar a propriedade PidTagAttachDataBinary para obter o histórico de download de mensagens para uma conta POP3.
ms.openlocfilehash: ae12a044098aa4f42e1c2e5936e82da3d7a128dd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399548"
---
# <a name="locating-the-message-download-history-for-a-pop3-account"></a>Localizar o histórico de download de mensagens de uma conta POP3

Este tópico descreve como um cliente de email pode acessar a propriedade [PidTagAttachDataBinary](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) para obter o histórico de download de mensagens para uma conta POP3. 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_WhyGetUIDLHistory"> </a>

## <a name="why-get-the-message-download-history"></a>Por que obter o histórico de download de mensagens?

O provedor de protocolo POP (Post Office Protocol) do Outlook permite aos usuários recuperarem e baixarem novas mensagens de email em seu dispositivo local e, posteriormente, manter ou excluir essas mensagens de email no servidor de email. Quando o cliente de email verifica se há novas mensagens para baixar, deve ser capaz de identificar e baixar somente as novas mensagens dessa Caixa de Entrada. O cliente de email faz isso, primeiramente, usando o comando UIDL (listagem de ID exclusiva) para obter um mapa de cada mensagem que já foi enviada para essa Caixa de Entrada com uma UID (identificação exclusiva). O cliente também obtém o histórico de download de mensagens para mensagens baixadas ou excluídas na caixa de entrada desse cliente. Usando o mapa de UID e o histórico de download de mensagens, o cliente pode identificar as mensagens ausentes do histórico como novas e baixá-las em seguida.
  
Para obter o histórico de download de mensagens da Caixa de Entrada:
  
- Siga as etapas deste tópico para encontrar a propriedade **PidTagAttachDataBinary**, que contém o histórico em um BLOB (objeto grande binário) que segue um formato específico. 
    
- Continue com [Analisar o histórico de download de mensagens de uma conta POP3](parsing-the-message-download-history-for-a-pop3-account.md), que descreve como analisar este BLOB para identificar mensagens baixadas ou excluídas dessa Caixa de Entrada.
    
## <a name="core-concepts-to-know-for-locating-the-message-download-history"></a>Conheça os principais conceitos para localizar o histórico de download de mensagens

O histórico de downloads de mensagens da Caixa de Entrada é armazenado em uma propriedade MAPI binária, **PidTagAttachDataBinary**, em um anexo de uma mensagem oculta na Caixa de Entrada. A tabela 1 mostra os recursos para conceitos que ajudam a entender como localizar o histórico de download de mensagens.
  
**Tabela 1. Conceitos fundamentais**

|**Título do artigo**|**Descrição**|
|:-----|:-----|
|[Pastas ocultas MAPI](https://msdn.microsoft.com/library/8b3b9c80-f7f4-4f37-bd6b-323469d020f1%28Office.15%29.aspx) <br/> |O MAPI permite que os clientes de email armazenem informações em pastas e mensagens ocultas. As pastas ocultas estão na parte associada das pastas MAPI e normalmente contêm informações que não são visíveis e nem manipuladas pelos usuários. Os clientes decidem o formato e o conteúdo a ser armazenado em mensagens e pastas ocultas.  <br/> |
|[Mensagens MAPI](https://msdn.microsoft.com/library/417c113f-bd98-4515-85d1-09db7fc3a227%28Office.15%29.aspx) <br/> |O MAPI armazena mensagens em pastas, seja na subárvore IPM padrão, que é visível para os usuários do cliente, ou fora da subárvore e invisíveis aos usuários. As mensagens podem ter dados adicionais armazenados em um anexo, que pode estar no formato de um arquivo, de outra mensagem ou de um objeto OLE. No caso do histórico de download de mensagens, o histórico é armazenado na propriedade de uma mensagem anexada a outra mensagem oculta.  <br/> |
|[Visão geral das propriedades de mensagens](https://msdn.microsoft.com/library/447f54de-9f0d-4f73-89b6-bed9cfea9c15%28Office.15%29.aspx) <br/> |Quando um cliente armazena informações em uma mensagem, ele realmente armazena as informações nas propriedades da mensagem. O MAPI suporta muitas propriedades, algumas sempre existem e podem ser definidas pelos clientes, outras são opcionais e os clientes não esperam que estejam disponíveis ou definidas com valores válidos. O histórico de download de mensagens é armazenado na propriedade **PidTagAttachDataBinary** de um anexo da mensagem oculta.  <br/> |
|[Perfis MAPI](https://msdn.microsoft.com/library/493c87a4-317d-47ec-850b-342cac59594b%28Office.15%29.aspx) <br/> |Ao fazer logon em uma sessão, o cliente de email seleciona um perfil que descreve os provedores e serviços a serem usados. Um perfil é dividido em seções que contêm propriedades. Especificamente, as propriedades [PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) (**PR_SEARCH_KEY**) e [PidTagProfileName](https://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx) (**PR_PROFILE_NAME**) sempre existem. Uma chave de pesquisa do perfil é única entre todos os perfis e é armazenada na seção de perfil identificada por **MUID_PROFILE_INSTANCE** (que é definida em MAPIGUID.H). Use [IMAPISession::OpenProfileSection](https://msdn.microsoft.com/library/e2757028-27e7-4fc0-9674-e8e30737ef1d%28Office.15%29.aspx) para abrir a seção e [IMAPIProp::GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) para obter os valores das propriedades.  <br/> |
|[Tabelas de conteúdo](https://msdn.microsoft.com/library/7b8efb4e-b5be-41b8-81bb-9aa1da421433%28Office.15%29.aspx) <br/> |Provedores de repositório de mensagens implementam tabelas de conteúdo às suas pastas. Para mensagens ocultas na parte associada de uma pasta, os provedores de repositório de mensagens suportam tabelas de conteúdo associadas e os clientes podem usar o método [IMAPIContainer::GetContentsTable](https://msdn.microsoft.com/library/88c7a666-875d-473a-b126-dbbb7009f7d9%28Office.15%29.aspx) para retornar um apontador para a tabela de conteúdo associada.  <br/> |
|[Sobre restrições](https://msdn.microsoft.com/library/e119fa20-08b8-4c8d-93fc-56037220890d%28Office.15%29.aspx) <br/> [Tipos de restrições](https://msdn.microsoft.com/library/0d3bd58b-7100-4117-91ac-27139715c85b%28Office.15%29.aspx) <br/> [Criar uma restrição](https://msdn.microsoft.com/library/12abbd8c-f825-493e-af42-344371d9658e%28Office.15%29.aspx) <br/> [Exemplo de código de restrição](https://msdn.microsoft.com/library/9b82097c-dbd6-4ba0-a6cb-292301f9402b%28Office.15%29.aspx) <br/> |Em MAPI, os clientes podem usar restrições para filtrar tabelas de conteúdo a fim de procurar linhas que representam as mensagens que tenham uma determinada propriedade definidas como um valor específico. As restrições são definidas usando a estrutura de dados [SRestriction](https://msdn.microsoft.com/library/c12b4409-da6f-480b-87af-1e5baea2e8bd%28Office.15%29.aspx), que pode conter uma união de estruturas de restrição mais especializadas. O método [IMAPITable::FindRow](https://msdn.microsoft.com/library/6511368c-9777-497e-9eea-cf390c04b92e%28Office.15%29.aspx) aplica uma restrição e recupera a primeira linha em uma tabela que atende aos critérios de restrição.  <br/> |
|[Sobre como registrar repositórios para indexação](https://msdn.microsoft.com/library/dd2aa06a-96e8-1291-18b5-fc3c40b74e4d%28Office.15%29.aspx) <br/> |Use a propriedade [PidTagStoreProvider](https://msdn.microsoft.com/library/6f6cc66f-a08e-4f8e-b33a-d3674319248e%28Office.15%29.aspx) (**PR_MDB_PROVIDER**) para verificar o tipo de provedor de repositório. Por exemplo, para verificar se um repositório é do Exchange, a propriedade **PidTagStoreProvider** deve retornar um valor representado pela constante **pbExchangeProviderPrimaryUserGuid**, que é definida no arquivo de cabeçalho público edkmdb.h.  <br/> |
   
## <a name="locating-the-appropriate-hidden-message-and-attachment"></a>Localizar o anexo e a mensagem oculta apropriados

Agora que sabemos que o histórico de download de mensagens de uma Caixa de Entrada está na propriedade **PidTagAttachDataBinary** de um anexo de uma mensagem oculta, o procedimento para localizar o anexo apropriado da mensagem oculta apropriada envolve os seguintes procedimentos: 
  
1. [Localizar a mensagem oculta apropriada](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindHiddenMsg)
    
2. [Localizar o anexo apropriado da mensagem oculta](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindAttachment)
    
3. [Acessar a propriedade PidTagAttachDataBinary do anexo da mensagem](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_AccessProp)

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindHiddenMsg"> </a>

### <a name="find-the-appropriate-hidden-message"></a>Localizar a mensagem oculta apropriada

1. Obtenha a propriedade [PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) (**PR_SEARCH_KEY**) do perfil, na seção de perfil especificada por **MUID_PROFILE_INSTANCE**.
    
2. Abra os Conteúdos Associados na pasta da Caixa de Entrada chamando **IMAPIContainer::GetContentsTable**.
    
3. Crie uma restrição baseada nas propriedades [PidTagConversationKey](https://msdn.microsoft.com/library/52c97d6c-7f4b-4522-aeac-0c1ed8475952%28Office.15%29.aspx) (**PR_CONVERSATION_KEY**), **PidTagSearchKey** (**PR_SEARCH_KEY**) e [PidTagMessageClass](https://msdn.microsoft.com/library/1e704023-1992-4b43-857e-0a7da7bc8e87%28Office.15%29.aspx) (**PR_MESSAGE_CLASS**) para obter uma tabela que contém todas as mensagens ocultas nos Conteúdos Associados da Caixa de Entrada. A seguir apresentamos um exemplo de uma restrição extraída de [Localizar o histórico de UIDL POP3](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/03/locating-the-pop3-uidl-history.aspx).
    
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

4. Na tabela, encontre a mensagem oculta usando **IMAPITable::FindRow**.
    
5. Se a etapa 4 não conseguir localizar uma mensagem oculta, altere a restrição para usar **PidTagSearchKey** (**PR_SEARCH_KEY**) ao invés de **PidTagConversationKey**, conforme mostrado abaixo:
    
   ```cpp
    rgRes[1].res.resProperty.ulPropTag = rgProps[0].ulPropTag = PR_SEARCH_KEY;
   ```

6. Encontre a mensagem oculta usando **IMAPITable::FindRow**. 
    
7. Se houver falha na etapa 6, altere a restrição para usar [PidTagSubject](https://msdn.microsoft.com/library/aa7ba4d9-c5e0-4ce7-a34e-65f675223bc9%28Office.15%29.aspx) (**PR_SUBJECT**) como sendo igual ao seguinte valor (mostrado abaixo usando a substituição de estilo `printf` por brevidade). 
    
   ```cpp
    "Outlook Message Manager (%s) (KEY: %s)", PR_PROFILE_NAME, HexFromBin(PR_SEARCH_KEY)
   ```

8. Encontre a mensagem oculta usando **IMAPITable::FindRow**.
    
9. Se você estiver executando o Outlook 2010 ou posterior, use os seguintes valores para **PidTagProfileName** (**PR_PROFILE_NAME**) e **PidTagSearchKey** (**PR _SEARCH_KEY**), respectivamente.
    
   ```cpp
    CHAR g_szGeneralKey[] = "General Key"; 
    const SBinary g_binGeneralKey = {sizeof(g_szGeneralKey), (LPBYTE)g_szGeneralKey};
   ```

   Execute as etapas 3 a 8. Se isso não conseguir localizar uma mensagem, volte para as etapas originais 3 a 8.
    
10. Abra a mensagem oculta encontrada na etapa 4, 6 ou 8.

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindAttachment"> </a>

### <a name="find-the-appropriate-attachment-of-the-hidden-message"></a>Localizar o anexo apropriado da mensagem oculta

Como a mensagem oculta pode conter mais de um anexo, procure o anexo apropriado na seguinte ordem.
  
> [!NOTE]
> Este procedimento usa novamente a substituição de estilo `printf` para brevidade. 

1. Procure um anexo cuja [PidTagAttachLongFilename](https://msdn.microsoft.com/library/83b69e8f-0b5a-4992-b5b8-160d3bdfa22a%28Office.15%29.aspx) (**PR_ATTACH_LONG_FILENAME**) corresponde à seguinte cadeia de caracteres, em que `szEmailAddress` é o endereço SMTP do usuário, conforme especificado no perfil do usuário. . 
    
   ```cpp
    "BlobPOP%s", szEmailAddress
   ```

2. Procure um anexo cuja [PidTagAttachFilename](https://msdn.microsoft.com/library/cbf34dd6-7733-47f6-9c41-9d82656ca9dc%28Office.15%29.aspx) (**PR_ATTACH_FILENAME**) corresponde a "BlobPOP%s", `szEmailAddress`.
    
3. Procure um anexo cuja [PidTagDisplayName](https://msdn.microsoft.com/library/bd094e00-5c60-4bb3-9a45-b943fab52876%28Office.15%29.aspx) (**PR_DISPLAY_NAME**) corresponde a "BlobPOP%s", `szEmailAddress`.
    
4. Procure um anexo cuja **PidTagAttachFilename** (**PR_ATTACH_FILENAME**) corresponde a "Blob%.8x", `dwAcctUID` e em que `dwAcctUID` vem de [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md). Você pode usar o método [IOlkAccount::GetProp](iolkaccount-getprop.md) para acessar a propriedade **PROP_ACCT_MINI_UID**. 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_AccessProp"> </a>

### <a name="access-the-pidtagattachdatabinary-property-of-the-message-attachment"></a>Acessar a propriedade PidTagAttachDataBinary do anexo da mensagem

Após localizar o anexo de mensagem apropriado da mensagem oculta, use **IMAPIProp::GetProps** para ler a propriedade **PidTagAttachDataBinary** do anexo. 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_NextSteps"> </a>

## <a name="next-steps"></a>Próximas etapas

Você aprendeu neste tópico a localizar o histórico de download de mensagens na Caixa de Entrada de um cliente de email POP3. Consulte [Analisar o histórico de download de mensagens de uma conta POP3](parsing-the-message-download-history-for-a-pop3-account.md) para aprender como analisar este histórico a fim de identificar mensagens baixadas ou excluídas da Caixa de Entrada. 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_AdditionalRsc"> </a>

## <a name="see-also"></a>Confira também

- [Gerenciar o download de mensagens de contas POP3](managing-message-downloads-for-pop3-accounts.md)   
- [Analisar o histórico de download de mensagens de uma conta POP3](parsing-the-message-download-history-for-a-pop3-account.md)
- [Localizar o histórico de UIDL POP3](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/03/locating-the-pop3-uidl-history.aspx)
    

