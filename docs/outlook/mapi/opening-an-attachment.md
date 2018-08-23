---
title: Abertura de um anexo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0350698-5304-40cd-903d-279471f3c226
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 768528c59d7aa5888c0d0427f86b8be8e1d33669
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579974"
---
# <a name="opening-an-attachment"></a>Abertura de um anexo

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abertura de um anexo envolve a exibição de seus dados. Por exemplo, quando um anexo de arquivo é aberto, o conteúdo do arquivo é exibido. Enquanto as mensagens e pastas são abertas usando seus identificadores de entrada, anexos abertos usando seus números de anexo — **PR_ATTACH_NUM** propriedades. Para obter mais informações, consulte **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)). Números de anexo estão disponíveis por meio da tabela de anexos da mensagem.
  
### <a name="to-open-all-attachments-in-a-message"></a>Para abrir todos os anexos em uma mensagem
  
1. Chame o método de [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) da mensagem para acessar sua tabela de anexo. 
    
2. Chame [HrQueryAllRows](hrqueryallrows.md) para recuperar todas as linhas na tabela. 
    
3. Para cada linha: 
    
    1. Abra o anexo passando o número de anexo representado na coluna **PR_ATTACH_NUM** em uma chamada ao método de **IMessage::OpenAttach** da mensagem. Para obter mais informações, consulte [IMessage::OpenAttach](imessage-openattach.md). **OpenAttach** retorna um ponteiro para uma implementação **IAttach** que fornece acesso às propriedades de anexo. 
        
    2. Chame o método de **IMAPIProp::GetProps** do anexo para recuperar sua propriedade **PR_ATTACH_METHOD** . Para obter mais informações, consulte [IMAPIProp::GetProps](imapiprop-getprops.md) e **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).
        
    3. Se **PR_ATTACH_METHOD** for definido como ATTACH_BY_REF_ONLY, chame **IMAPIProp::GetProps** para recuperar a propriedade **PR_ATTACH_PATHNAME** . Para obter mais informações, consulte **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)).
        
    4. Se **PR\_ATTACH_METHOD** estiver definida como ANEXAR\_BY_VALUE, chame **IMAPIProp::OpenProperty** para abrir o **PR\_ATTACH_DATA_BIN** propriedade com a interface **IStream** . Consulte o código de amostra seguindo este procedimento. Para obter mais informações, consulte [IMAPIProp::OpenProperty](imapiprop-openproperty.md) e **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).
        
    5. Se **PR_ATTACH_METHOD** for definido como ATTACH_OLE e o anexo é um objeto OLE 2: 
        
        1. Chamar **IMAPIProp::OpenProperty** para abrir o **PR\_ATTACH_DATA_OBJ** propriedade com a interface **IStreamDocfile** . Tente usar essa interface porque ele é uma implementação do **IStream** garantido para trabalhar com armazenamento estruturado com o mínimo de sobrecarga. Para obter mais informações, consulte **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).
            
        2. Se a chamada **OpenProperty** falhar, chame novamente para recuperar a propriedade **PR_ATTACH_DATA_BIN** com a interface **IStreamDocfile** . 
            
        3. Se essa segunda chamada **OpenProperty** falhar, tente novamente para chamar **OpenProperty** para recuperar **PR_ATTACH_DATA_OBJ**. No entanto, em vez de especificar **IStreamDocfile**, especifique a interface de **IStorage** . 
    
4. Se **PR_ATTACH_METHOD** for definido como ATTACH_EMBEDDED_MSG, não é incomum que o valor da **PR_ATTACH_DATA_OBJ** para conter um erro. Isso acontece porque você e o implementador tabela não têm como concordam com o tipo de objeto a ser retornado. Para recuperar um ponteiro para a mensagem anexada, abra o anexo usando **IMessage::OpenAttach**. Acesse os dados do anexo chamando o método **IMAPIProp::OpenProperty** . Para obter mais informações, consulte [IMessage::OpenAttach](imessage-openattach.md) e [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
    
Você pode solicitar que um anexo é aberto no modo somente leitura ou de leitura/gravação. Somente leitura é o modo padrão e vários provedores de armazenamento de mensagem abrir todos os anexos neste modo independente os clientes solicitam. Passe o sinalizador MAPI_BEST_ACCESS para solicitar que o provedor de armazenamento de mensagem conceder o nível mais alto de acesso, ele pode e recuperá-propriedade **PR_ACCESS_LEVEL** do anexo aberto para determinar o nível de acesso que realmente foi concedido. Para obter mais informações, consulte **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
O exemplo a seguir mostra como abrir os dados em um anexo **PR\_ATTACH_DATA_BIN** propriedade. Ele aloca ponteiros para dois fluxos: uma para o arquivo e outra para o anexo. A função **OpenStreamOnFile** abre o fluxo de arquivos no modo somente leitura. A chamada **IMAPIProp::OpenProperty** método do anexo abre o fluxo de anexos no modo de leitura/gravação. Para obter mais informações, consulte **PR_ATTACH_DATA_BIN**, [OpenStreamOnFile](openstreamonfile.md)e [IMAPIProp::OpenProperty](imapiprop-openproperty.md). O código copia do fluxo de arquivo para o fluxo de anexos e libera os dois fluxos.
  
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


