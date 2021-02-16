---
title: Abrir um anexo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0350698-5304-40cd-903d-279471f3c226
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 39da1e02622d81cd12a2d4673b827d49bf418128
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430620"
---
# <a name="opening-an-attachment"></a>Abrir um anexo

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abrir um anexo envolve a exibição de seus dados. Por exemplo, quando um anexo de arquivo é aberto, o conteúdo do arquivo é exibido. Enquanto as mensagens e pastas são abertas usando seus identificadores de entrada, os anexos são abertos usando seus números de anexo **—** PR_ATTACH_NUM propriedades. Para obter mais informações, **consulte PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)). Os números de anexo estão disponíveis por meio da tabela de anexos de uma mensagem.
  
### <a name="to-open-all-attachments-in-a-message"></a>Para abrir todos os anexos em uma mensagem
  
1. Chame o método [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) da mensagem para acessar sua tabela de anexos. 
    
2. Chame [HrQueryAllRows](hrqueryallrows.md) para recuperar todas as linhas na tabela. 
    
3. Para cada linha: 
    
    1. Abra o anexo passando o número do anexo representado **na coluna PR_ATTACH_NUM** em uma chamada para o método **IMessage::OpenAttach** da mensagem. Para obter mais informações, consulte [IMessage::OpenAttach](imessage-openattach.md). **OpenAttach** retorna um ponteiro para uma implementação **IAttach** que fornece acesso a propriedades de anexo. 
        
    2. Chame o método **IMAPIProp::GetProps** do anexo para recuperar sua **PR_ATTACH_METHOD** propriedade. Para obter mais informações, consulte [IMAPIProp::GetProps](imapiprop-getprops.md) and **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).
        
    3. Se **PR_ATTACH_METHOD** estiver definido como ATTACH_BY_REF_ONLY, chame **IMAPIProp::GetProps** para recuperar a **PR_ATTACH_PATHNAME** propriedade. Para obter mais informações, **consulte PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)).
        
    4. Se **o \_ ATTACH_METHOD** PR estiver definido como ATTACH BY_VALUE, chame \_ **IMAPIProp::OpenProperty** para abrir a propriedade **PR \_ ATTACH_DATA_BIN** com a interface **IStream.** Consulte o código de exemplo após este procedimento. Para obter mais informações, consulte [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).
        
    5. Se **PR_ATTACH_METHOD** for definido como ATTACH_OLE e o anexo for um objeto OLE 2: 
        
        1. Chame **IMAPIProp::OpenProperty** para abrir a propriedade **pr \_ ATTACH_DATA_OBJ** com a interface **IStreamDocfile.** Tente usar essa interface porque é uma implementação do **IStream** garantida para trabalhar com armazenamento estruturado com o mínimo de sobrecarga. Para obter mais informações, **consulte PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).
            
        2. Se a **chamada OpenProperty** falhar, chame-a novamente para recuperar a propriedade **PR_ATTACH_DATA_BIN** com a interface **IStreamDocfile.** 
            
        3. Se esta segunda **chamada OpenProperty** falhar, tente novamente chamar **OpenProperty** para **recuperar** PR_ATTACH_DATA_OBJ . No entanto, em vez de especificar **IStreamDocfile**, especifique a interface **IStorage.** 
    
4. Se **PR_ATTACH_METHOD** for definido como ATTACH_EMBEDDED_MSG, não será incomum que o valor de PR_ATTACH_DATA_OBJ **contenha** um erro. Isso porque você e o implementador da tabela não têm como concordar com o tipo de objeto a ser retornada. Para recuperar um ponteiro para a mensagem anexada, abra o anexo **usando IMessage::OpenAttach**. Em seguida, acesse os dados do anexo chamando seu **método IMAPIProp::OpenProperty.** Para obter mais informações, consulte [IMessage::OpenAttach](imessage-openattach.md) e [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
    
Você pode solicitar que um anexo seja aberto no modo de leitura/gravação ou somente leitura. Somente leitura é o modo padrão, e muitos provedores de armazenamento de mensagens abrem todos os anexos nesse modo, independentemente do que os clientes solicitam. Passe o sinalizador MAPI_BEST_ACCESS para solicitar que o provedor de armazenamento de mensagens conceda o nível mais alto de acesso possível e recupere **a** propriedade PR_ACCESS_LEVEL do anexo aberto para determinar o nível de acesso realmente concedido. Para obter mais informações, **consulte PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
O exemplo a seguir mostra como abrir os dados na propriedade **PR \_ ATTACH_DATA_BIN** anexo. Ele aloca ponteiros para dois fluxos: um para o arquivo e outro para o anexo. A **função OpenStreamOnFile** abre o fluxo de arquivo no modo somente leitura. A chamada para o método **IMAPIProp::OpenProperty** do anexo abre o fluxo de anexos no modo de leitura/gravação. Para obter mais informações, **PR_ATTACH_DATA_BIN**, [OpenStreamOnFile](openstreamonfile.md)e [IMAPIProp::OpenProperty](imapiprop-openproperty.md). Em seguida, o código copia do fluxo de arquivo para o fluxo de anexo e libera ambos os fluxos.
  
```cpp
LPSTREAM pStreamFile, pStreamAtt;
HRESULT hr;
hr = OpenStreamOnFile (MAPIAllocateBuffer, MAPIFreeBuffer,
                       STGM_READ, "myfile.doc", NULL, &pStreamFile);
if (HR_SUCCEEDED(hr))
{
    // Open the destination stream in the attachment object
    hr = pAttach->OpenProperty (PR_ATTACH_DATA_BIN,
                                &IID_IStream,
                                0,
                                MAPI_MODIFY | MAPI_CREATE,
                                (LPUNKNOWN *)&pStreamAtt);
    if (HR_SUCCEEDED(hr))
    {
        STATSTG StatInfo;
        pStreamFile->Stat (&StatInfo, STATFLAG_NONAME);
        hResult = pStreamFile->CopyTo (pStreamAtt, StatInfo.cbSize,
                                       NULL, NULL);
        pStreamAtt->Release();
    }
    pStreamFile->Release();
}
```


