---
title: IMAPIPropOpenProperty
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.OpenProperty
api_type:
- COM
ms.assetid: e400e6cc-4e36-43fc-9304-b688a0a7fd77
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7bf1d6912e44319c36e288cd3870218e8c4e45ff
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395802"
---
# <a name="imapipropopenproperty"></a>IMAPIProp::OpenProperty

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna um ponteiro para uma interface que pode ser usada para acessar uma propriedade.
  
```cpp
HRESULT OpenProperty(
  ULONG ulPropTag,
  LPCIID lpiid,
  ULONG ulInterfaceOptions,
  ULONG ulFlags,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Parâmetros

 _ulPropTag_
  
> [in] A marca de propriedade para a propriedade a ser acessado. O identificador do e o tipo devem ser incluídos na marca de propriedade.
    
 _lpiid_
  
> [in] Um ponteiro para o identificador para a interface que será usada para acessar a propriedade. O parâmetro _lpiid_ não deve ser **nula**.
    
 _ulInterfaceOptions_
  
> [in] Dados relacionados à interface identificada pelo parâmetro _lpiid_ . 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla o acesso à propriedade. Sinalizadores a seguir podem ser definidos:
    
MAPI_CREATE 
  
> Se a propriedade não existir, ele deve ser criado. Se a propriedade existir, o valor atual da propriedade deverão ser descartado. Quando um chamador define o sinalizador MAPI_CREATE, ele também deve definir o sinalizador MAPI_MODIFY.
    
MAPI_DEFERRED_ERRORS 
  
> Permite **OpenProperty** retornar com êxito, possivelmente antes que o objeto esteja totalmente disponível ao chamador. Se o objeto não estiver disponível, fazendo uma chamada do objeto subsequente pode gerar um erro. 
    
MAPI_MODIFY 
  
> Nesses casos, é necessário MAPI_MODIFY:
    
  - Ao abrir uma propriedade de stream, como **IID_IStream**, para modificá-la.
    
  - Ao abrir um anexo de mensagens inseridas, como [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) aberto com **IID_IMessage**, para modificá-la.
    
 _lppUnk_
  
> [out] Um ponteiro para a interface solicitada a ser usada para acesso à propriedade.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O ponteiro de interface solicitada foi retornado com êxito.
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> A interface solicitada não é suportada para essa propriedade.
    
MAPI_E_NO_ACCESS 
  
> O chamador tem permissões insuficientes para acessar a propriedade.
    
MAPI_E_NO_SUPPORT 
  
> O objeto não pode fornecer acesso a essa propriedade por meio da interface solicitada.
    
E_NOT_FOUND 
  
> A propriedade solicitada não existe e MAPI_CREATE não foi definida no parâmetro _ulFlags_ . 
    
MAPI_E_INVALID_PARAMETER 
  
> O tipo de propriedade na marca é definido como PT_UNSPECIFIED.
    
## <a name="remarks"></a>Comentários

O método **IMAPIProp::OpenProperty** fornece acesso a uma propriedade por meio de uma interface específica. **OpenProperty** é uma alternativa para os métodos [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPIProp::SetProps](imapiprop-setprops.md) . Quando **GetProps** ou **SetProps** falha porque a propriedade é muito grande ou muito complexa, chame **OpenProperty**. **OpenProperty** geralmente é utilizado para acessar as propriedades do tipo PT_OBJECT. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para acessar os anexos de mensagens, abra a propriedade **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) com um identificador de interface diferente, dependendo do tipo de anexo. A tabela a seguir descreve como chamar **OpenProperty** para os diferentes tipos de anexos: 
  
|**Tipo de anexo**|**Identificador de interface usar**|
|:-----|:-----|
|Binário  <br/> |IID_IStream  <br/> |
|Cadeia de caracteres  <br/> |IID_IStream  <br/> |
|Message  <br/> |IID_IMessage  <br/> |
|OLE 2.0  <br/> |IID_IStreamDocfile  <br/> |
   
**IStreamDocfile** é um derivado da interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) que baseia-se em um arquivo de compostos OLE 2.0. **IStreamDocfile** é a melhor opção para acessar os anexos OLE 2.0 porque envolve o mínimo de sobrecarga. Você pode usar o IID_IStreamDocFile para essas propriedades que contenham dados armazenados em armazenamento estruturado disponível por meio da interface [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) . 
  
Para obter mais informações sobre como usar **OpenProperty** com anexos, consulte a propriedade **PR_ATTACH_DATA_OBJ** e a [abertura de um anexo](opening-an-attachment.md).
  
Não use o ponteiro de **IStream** recebidos para chamar o método seu [Seek](https://msdn.microsoft.com/library/aa380043%28v=VS.85%29.aspx) ou [SetSize](https://msdn.microsoft.com/library/aa380044%28v=VS.85%29.aspx) , a menos que você use uma zero variável de tamanho ou posição. Além disso, não confie no valor do parâmetro de saída _plibNewPosition_ retornado da chamada **Seek** . 
  
Se você chamar **OpenProperty** para acessar uma propriedade com a interface **IStream** , use apenas essa interface para fazer alterações nele. Não tente atualizar a propriedade com qualquer uma das outras [IMAPIProp: IUnknown](imapipropiunknown.md) métodos, como **SetProps** ou [IMAPIProp::DeleteProps](imapiprop-deleteprops.md). 
  
Não tente abrir uma propriedade com **OpenProperty** mais de uma vez. Os resultados são indefinidos porque eles podem variar de provedor. 
  
Se você precisar modificar a propriedade a ser aberto, defina o sinalizador MAPI_MODIFY. Se não esteja certo se o objeto oferece suporte à propriedade, mas você acha que deveria, defina os sinalizadores MAPI_CREATE e MAPI_MODIFY. Sempre que MAPI_CREATE for definido, MAPI_MODIFY também deve ser definida.
  
Você é responsável por reformulação o ponteiro de interface retornado no parâmetro _lppUnk_ para um que é apropriado para a interface especificada no parâmetro _lpiid_ . Você também deve usar o ponteiro retornado para chamar seu método de [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) quando terminar com ele. 
  
Em alguns casos, definindo os sinalizadores no parâmetro _ulFlags_ não é suficiente para indicar o tipo de acesso para a propriedade que é necessário. Você pode colocar os dados adicionais, como sinalizadores, no parâmetro _ulInterfaceOptions_ . Esses dados são dependentes de interface. Algumas interfaces (por exemplo, **IStream**) usá-lo e outros não. Por exemplo, quando você abre uma propriedade a ser modificado com **IStream**, defina o sinalizador STGM_WRITE no parâmetro _ulInterfaceOptions_ além dos MAPI_MODIFY. Quando você abre uma tabela por meio da interface [IMAPITable](imapitableiunknown.md) , você pode definir _ulInterfaceOptions_ como MAPI_UNICODE para indicar se as colunas na tabela que armazenam as propriedades de cadeia de caracteres devem estar no formato Unicode. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|StreamEditor.cpp  <br/> |CStreamEditor::ReadTextStreamFromProperty  <br/> |MFCMAPI usa o método **IMAPIProp::OpenProperty** para recuperar uma interface de fluxo de texto grande e propriedades binárias.  <br/> |
   
## <a name="see-also"></a>Confira também

- [HrIStorageFromStream](hristoragefromstream.md) 
- [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) 
- [IMAPIProp::GetProps](imapiprop-getprops.md)
- [IMAPIProp::SetProps](imapiprop-setprops.md)
- [IMAPISupport::IStorageFromStream](imapisupport-istoragefromstream.md)
- [IMAPITable : IUnknown](imapitableiunknown.md)
- [IMAPIProp : IUnknown](imapipropiunknown.md)
- [MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
- [Abrir um anexo](opening-an-attachment.md)

