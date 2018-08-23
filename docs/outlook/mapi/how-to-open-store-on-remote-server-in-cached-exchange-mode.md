---
title: Abra um repositório no servidor remoto, quando o Outlook estiver no modo cache do Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: cf01eab7-164d-c3b3-8bb0-9281e2119bc5
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: 7c1b3d3d5eed6bc991f8e4fd702fa197d610c104
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584797"
---
# <a name="open-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a>Abra um repositório no servidor remoto, quando o Outlook estiver no modo cache do Exchange

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este tópico contém um exemplo de código em C++ que mostra como usar o sinalizador **MDB_ONLINE** para abrir um armazenamento de mensagens no servidor remoto, quando o Microsoft Outlook 2010 ou o Microsoft Outlook 2013 estiver em modo cache do Exchange. 
  
Modo cache do Exchange permite que o Outlook 2010 e o Outlook 2013 para usar uma cópia local da caixa de correio de um usuário com o Outlook 2010 ou Outlook 2013 mantém uma conexão on-line para uma cópia remota da caixa de correio do usuário no servidor Exchange remoto. Quando o Outlook 2010 ou Outlook 2013 está em execução no modo cache do Exchange, por padrão, qualquer soluções MAPI que faça logon mesma sessão também estão conectadas ao repositório de mensagens armazenadas em cache. Todos os dados que são acessados e quaisquer alterações que são feitas são feitas em relação a cópia local da caixa de correio.
  
Um provedor de cliente ou serviço pode substituir a conexão ao repositório de mensagem local e abra o repositório no servidor remoto, definindo o bit para **MDB_ONLINE** no parâmetro *ulFlags* ao chamar [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md). Depois que o repositório tiver sido aberto com êxito no servidor remoto para a sessão, você pode usar [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir itens ou pastas no repositório remoto. 
  
Você não pode abrir um repositório do Exchange no modo de cache e no modo em cache não ao mesmo tempo na mesma sessão MAPI. Se você já abriu o armazenamento de mensagens em cache, você deve fechar ou o repositório antes de abri-lo com esse sinalizador ou abra uma nova sessão MAPI, onde você pode abrir o armazenamento do Exchange no servidor remoto usando esse sinalizador.
  
O exemplo de código a seguir mostra como chamar **IMAPISession::OpenMsgStore** com o sinalizador **MDB_ONLINE** definido no parâmetro *ulFlags* para abrir o repositório padrão no servidor remoto. 
  
```cpp
HRESULT HrRemoteMessageStore( 
    LPMAPISESSION lpMAPISession, 
    LPMDB* lppMDB) 
{ 
    HRESULT hRes = S_OK; 
    LPMAPITABLE pStoresTbl = NULL; 
    SRestriction sres = {0}; 
    SPropValue spv = {0}; 
    LPSRowSet pRow = NULL; 
    LPMDB lpTempMDB = NULL; 
    enum {EID,NUM_COLS}; 
    static SizedSPropTagArray(NUM_COLS,sptCols) = {NUM_COLS, 
        PR_ENTRYID, 
    }; 
 
    //Obtain the table of all the message stores that are available 
    hRes = lpMAPISession-&gt;GetMsgStoresTable(0, &amp;pStoresTbl); 
     
    if (SUCCEEDED(hRes) &amp;&amp; pStoresTbl) 
    { 
        //Set up restrictions for the default store 
        sres.rt = RES_PROPERTY;                                  //Comparing a property 
        sres.res.resProperty.relop = RELOP_EQ;                   //Testing equality 
        sres.res.resProperty.ulPropTag = PR_DEFAULT_STORE;       //Tag to compare 
        sres.res.resProperty.lpProp = &amp;spv;                      //Prop tag and value to compare against 
     
        spv.ulPropTag = PR_DEFAULT_STORE;                        //Tag type 
        spv.Value.b   = TRUE;                                    //Tag value 
     
        //Convert the table to an array that can be stepped through 
        //Only one message store should have PR_DEFAULT_STORE set to true, so that only one will be returned 
        hRes = HrQueryAllRows( 
            pStoresTbl,                                          //Table to query 
            (LPSPropTagArray) &amp;sptCols,                          //Which columns to obtain 
            &amp;sres,                                               //Restriction to use 
            NULL,                                                //No sort order 
            0,                                                   //Max number of rows (0 means no limit) 
            &amp;pRow);                                              //Array to return 
 
        if (SUCCEEDED(hRes) &amp;&amp; pRow &amp;&amp; pRow-&gt;cRows) 
        {     
            //Open the first returned (default) message store 
            hRes = lpMAPISession-&gt;OpenMsgStore( 
                NULL,                                                //Window handle for dialogs 
                pRow-&gt;aRow[0].lpProps[EID].Value.bin.cb,             //size and... 
                (LPENTRYID)pRow-&gt;aRow[0].lpProps[EID].Value.bin.lpb, //value of entry to open 
                NULL,                                                //Use default interface (IMsgStore) to open store 
                MAPI_BEST_ACCESS | MDB_ONLINE,                       //Flags 
                &amp;lpTempMDB);                                         //Pointer to put the store in 
            if (SUCCEEDED(hRes) &amp;&amp; lppMDB) lppMDB* = lpTempMDB; 
        } 
    } 
    FreeProws(pRow); 
    if (pStoresTbl) pStoresTbl-&gt;Release(); 
 
    return hRes; 
}

```

## <a name="see-also"></a>Confira também

- [Sobre as adições de MAPI](about-mapi-additions.md) 
- [Constantes MAPI](mapi-constants.md)
- [Acessar um repositório em um servidor remoto quando o Outlook estiver no modo cache do Exchange](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)

