---
title: Criar uma lista de distribuição
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b63a6024-910d-4569-a3b4-c3ebf0b32c3d
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: f0a6b7af196073d52ce98037b443569dcd1f41e6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582543"
---
# <a name="creating-a-distribution-list"></a>Criar uma lista de distribuição

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os clientes podem criar uma lista de distribuição diretamente em um contêiner modificável, como o catálogo de endereços pessoal (PAB).
  
**Para criar uma lista de distribuição no PAB**
  
1. Crie uma matriz de marca de propriedade dimensionado com marca de uma propriedade, **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)), da seguinte maneira:
    
   ```cpp
    SizedPropTagArray(1, tagaDefaultDL) =
    {
        1,
        {
            PR_DEF_CREATE_DL
        }
    };
   ```

2. Chame [IAddrBook::GetPAB](iaddrbook-getpab.md) para recuperar o identificador de entrada do PAB. Se houver um erro ou **GetPAB** retornará zero ou NULL, não continue. 
    
   ```cpp
    LPENTRYID peidPAB = NULL;
    ULONG cbeidPAB = 0;
    lpIAddrBook->GetPAB(&cbeidPAB, &peidPAB);
   ```

3. Chame [IAddrBook::OpenEntry](iaddrbook-openentry.md) para abrir o PAB. O parâmetro de saída _ulObjType_ deve ser definido como MAPI_ABCONT. 
    
   ```cpp
    ULONG ulObjType = 0;
    LPABCONT lpPABCont = NULL;
    lpIAddrBook->OpenEntry(cbeidPAB, peidPAB,
                    NULL,
                    MAPI_MODIFY,
                    &ulObjType,
                    &lpPABCont);
   ```

4. Chame o método de [IMAPIProp::GetProps](imapiprop-getprops.md) do PAB para recuperar a propriedade PR_DEF_CREATE_DL, o modelo que ele usa para criar uma lista de distribuição. 
    
   ```cpp
    lpPABCont->GetProps(0,
                tagaDefaultDL,
                &lpspvDefDLTpl);
    
   ```

5. Se **GetProps** falhar: 
    
   1. Chame o método de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) do PAB para abrir a propriedade **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) com a interface **IMAPITable** . 
      
   2. Criar uma restrição de propriedade para procurar a linha com a coluna **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) igual a "MAPIPDL". 
      
   3. Chame [IMAPITable:: FindRow](imapitable-findrow.md) para localizar essa linha. 
    
6. Salve o identificador de entrada retornado por **GetProps** ou **FindRow**.
    
   ```cpp
    peidDefDLTpl = lpspvDefDLTpl->Value.bin.pb;
    cbeidDefDLTpl = lpspvDefDLTpl->Value.bin.cb;
    
   ```

7. Chame o método de [IABContainer::CreateEntry](iabcontainer-createentry.md) do PAB para criar uma nova entrada usando o modelo representado pelo identificador de entrada salvas. Não presuma que o objeto retornado será uma lista de distribuição em vez de um usuário de mensagens quando essa chamada é remota. Observe que o sinalizador CREATE_CHECK_DUP é passado no parâmetro _ulFlags_ para impedir que a entrada que está sendo adicionado duas vezes. 
    
   ```cpp
    lpPABCont->CreateEntry(cbeidDefDLTpl,
                    peidDefDLTPL,
                    CREATE_CHECK_DUP_STRICT,
                    &lpNewPABEntry);
   ```

8. Chame **IUnknown:: QueryInterface** método a nova entrada, passando IID_IDistList como o identificador de interface, para determinar se a entrada é uma lista de distribuição e oferece suporte a [IDistList: IMAPIContainer](idistlistimapicontainer.md) interface. Como **CreateEntry** retorna um ponteiro **IMAPIProp** ao invés o ponteiro **IMailUser** ou **IDistList** mais específico, verifique se um objeto de lista de distribuição foi criado. Se **QueryInterface** tiver êxito, você pode ter certeza de que você tenha criado uma lista de distribuição em vez de um usuário de mensagens. 
    
9. Chame [IMAPIProp::SetProps](imapiprop-setprops.md) método a lista de distribuição para definir seu nome para exibição e outras propriedades. 
    
10. Chame o método de [IABContainer::CreateEntry](iabcontainer-createentry.md) da lista de distribuição para adicionar um ou mais usuários de mensagens. 
    
11. Chame o método de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) da lista de distribuição quando estiver pronto para salvá-lo. Para recuperar o identificador de entrada da lista de distribuição salvas, defina o sinalizador KEEP_OPEN_READWRITE e, em seguida, chame [IMAPIProp::GetProps](imapiprop-getprops.md) solicitando a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
12. Libere a nova lista de distribuição e o PAB chamando os métodos **IUnknown:: Release** . 
    
13. Chame [MAPIFreeBuffer](mapifreebuffer.md) para liberar a memória para o identificador de entrada do PAB e a matriz de marca de propriedade dimensionada. 
    

