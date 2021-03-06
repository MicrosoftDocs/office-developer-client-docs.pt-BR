---
title: Abrir um armazenamento no servidor remoto quando o Outlook estiver no Modo Cache do Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: cf01eab7-164d-c3b3-8bb0-9281e2119bc5
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: 419c9ae734e8b58d0958970e7127b94d220b8382
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417816"
---
# <a name="open-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a>Abrir um armazenamento no servidor remoto quando o Outlook estiver no Modo Cache do Exchange

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este tópico contém um exemplo de código em C++ que mostra como usar o sinalizador **MDB_ONLINE** para abrir um armazenamento de mensagens no servidor remoto quando o Microsoft Outlook 2010 ou o Microsoft Outlook 2013 estiver no Modo Cache do Exchange. 
  
O Modo Cache do Exchange permite que o Outlook 2010 e o Outlook 2013 usem uma cópia local da caixa de correio de um usuário enquanto o Outlook 2010 ou o Outlook 2013 mantém uma conexão online com uma cópia remota da caixa de correio do usuário no servidor Remoto do Exchange. Quando o Outlook 2010 ou o Outlook 2013 está sendo executado no Modo Cache do Exchange, por padrão, todas as soluções MAPI que fazem logon na mesma sessão também são conectadas ao armazenamento de mensagens em cache. Todos os dados acessados e quaisquer alterações feitas serão feitas na cópia local da caixa de correio.
  
Um cliente ou provedor de serviços pode substituir a conexão com o repositório de mensagens local e abrir o repositório no servidor remoto definindo o bit para **MDB_ONLINE** no  *parâmetro ulFlags*  ao chamar [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md). Depois que o armazenamento tiver sido aberto com êxito no servidor remoto para essa sessão, você poderá usar [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir itens ou pastas no armazenamento remoto. 
  
Não é possível abrir um armazenamento do Exchange no modo em cache e no modo não armazenado em cache ao mesmo tempo na mesma sessão MAPI. Se você já tiver aberto o arquivo de cache mensagens, você deve fechar o repositório antes de abri-lo com esse sinalizador ou abrir uma nova sessão MAPI onde você pode abrir o armazenamento do Exchange no servidor remoto usando esse sinalizador.
  
O exemplo de código a seguir mostra como chamar **IMAPISession::OpenMsgStore** com o sinalizador **MDB_ONLINE** definido no parâmetro  *ulFlags*  para abrir o repositório padrão no servidor remoto. 
  
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
- [Acessar o Store em um servidor remoto quando o Outlook estiver no modo cache do Exchange](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)

