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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319807"
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
  
> [in] A marca da propriedade a ser acessada. O identificador e o tipo devem ser incluídos na marca de propriedade.
    
 _lpiid_
  
> [in] Um ponteiro para o identificador da interface a ser usada para acessar a propriedade. O _parâmetro lpiid_ não deve ser **nulo.**
    
 _ulInterfaceOptions_
  
> [in] Dados relacionados à interface identificada pelo _parâmetro lpiid._ 
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla o acesso à propriedade. Os sinalizadores a seguir podem ser definidos:
    
MAPI_CREATE 
  
> Se a propriedade não existir, ela deverá ser criada. Se a propriedade existir, o valor atual da propriedade deverá ser descartado. Quando um chamador define o sinalizador MAPI_CREATE, ele também deve definir o MAPI_MODIFY sinalizador.
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **OpenProperty** retorne com êxito, possivelmente antes que o objeto seja totalmente disponível para o chamador. Se o objeto não estiver disponível, fazer uma chamada de objeto subsequente poderá criar um erro. 
    
MAPI_MODIFY 
  
> MAPI_MODIFY é necessário nestas situações:
    
  - Ao abrir uma propriedade de fluxo, como **IID_IStream,** modifique-a.
    
  - Ao abrir um anexo de mensagem incorporado, como [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) aberto **com IID_IMessage**, para modificá-lo.
    
 _lppUnk_
  
> [out] Um ponteiro para a interface solicitada a ser usada para o acesso à propriedade.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O ponteiro da interface solicitado foi retornado com êxito.
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> A interface solicitada não tem suporte para essa propriedade.
    
MAPI_E_NO_ACCESS 
  
> O chamador tem permissões insuficientes para acessar a propriedade.
    
MAPI_E_NO_SUPPORT 
  
> O objeto não pode fornecer acesso a essa propriedade por meio da interface solicitada.
    
MAPI_E_NOT_FOUND 
  
> A propriedade solicitada não existe e MAPI_CREATE não foi definida no _parâmetro ulFlags._ 
    
MAPI_E_INVALID_PARAMETER 
  
> O tipo de propriedade na marca é definido como PT_UNSPECIFIED.
    
## <a name="remarks"></a>Comentários

O **método IMAPIProp::OpenProperty** fornece acesso a uma propriedade por meio de uma interface específica. **OpenProperty é** uma alternativa aos métodos [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPIProp::SetProps.](imapiprop-setprops.md) Quando **GetProps ou** **SetProps** falhar porque a propriedade é muito grande ou muito complexa, chame **OpenProperty**. **OpenProperty** é normalmente usado para acessar propriedades do tipo PT_OBJECT. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para acessar anexos de mensagens, abra a propriedade **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) com um identificador de interface diferente, dependendo do tipo de anexo. A tabela a seguir descreve como chamar **OpenProperty** para os diferentes tipos de anexos: 
  
|**Tipo de anexo**|**Identificador de interface a ser usado**|
|:-----|:-----|
|Binária  <br/> |IID_IStream  <br/> |
|String  <br/> |IID_IStream  <br/> |
|Mensagem  <br/> |IID_IMessage  <br/> |
|OLE 2.0  <br/> |IID_IStreamDocfile  <br/> |
   
**IStreamDocfile** é uma derivativa da interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) baseada em um arquivo composto OLE 2.0. **IStreamDocfile** é a melhor opção para acessar anexos OLE 2.0 porque envolve a menor quantidade de sobrecarga. Você pode usar IID_IStreamDocFile para as propriedades que contêm dados armazenados em armazenamento estruturado disponível por meio da interface [IStorage.](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) 
  
For more information about how to use **OpenProperty** with attachments, see the **PR_ATTACH_DATA_OBJ** property and [Opening an Attachment](opening-an-attachment.md).
  
Não use o ponteiro **IStream** recebido para chamar o método [Seek](https://msdn.microsoft.com/library/aa380043%28v=VS.85%29.aspx) ou [SetSize,](https://msdn.microsoft.com/library/aa380044%28v=VS.85%29.aspx) a menos que você use uma variável de posição zero ou tamanho. Além disso, não confie no valor do parâmetro de saída _plibNewPosition_ retornado da **chamada Seek.** 
  
Se você chamar **OpenProperty para** acessar uma propriedade com a interface **IStream,** use somente essa interface para fazer alterações a ela. Não tente atualizar a propriedade com nenhum dos outros [métodos IMAPIProp : IUnknown,](imapipropiunknown.md) como **SetProps** ou [IMAPIProp::D eleteProps](imapiprop-deleteprops.md). 
  
Não tente abrir uma propriedade com **OpenProperty** mais de uma vez. Os resultados são indefinido porque podem variar de provedor para provedor. 
  
Se você precisar modificar a propriedade a ser aberta, de definida a MAPI_MODIFY sinalizador. Se você não tiver certeza se o objeto dá suporte à propriedade, mas acha que deve, de definida a MAPI_CREATE e MAPI_MODIFY sinalizadores. Sempre MAPI_CREATE configuração, MAPI_MODIFY também deve ser definido.
  
Você é responsável por recasting do ponteiro da interface retornado no parâmetro _lppUnk_ para um que seja apropriado para a interface especificada no parâmetro _lpiid._ Você também deve usar o ponteiro retornado para chamar seu [método IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) quando terminar. 
  
Às vezes, definir os sinalizadores no  _parâmetro ulFlags_ não é suficiente para indicar o tipo de acesso à propriedade necessária. Você pode colocar dados adicionais, como sinalizadores, no _parâmetro ulInterfaceOptions._ Esses dados dependem da interface. Algumas interfaces (como **IStream**) o usam e outras não. Por exemplo, quando você abre uma propriedade a ser modificada com **IStream**, de definir o sinalizador STGM_WRITE no  _parâmetro ulInterfaceOptions_ além de MAPI_MODIFY. Ao abrir uma tabela usando a interface [IMAPITable,](imapitableiunknown.md) você pode definir  _ulInterfaceOptions_ como MAPI_UNICODE para indicar se as colunas na tabela que reter as propriedades de cadeia de caracteres devem estar no formato Unicode. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|StreamEditor.cpp  <br/> |CStreamEditor::ReadTextStreamFromProperty  <br/> |MFCMAPI usa o **método IMAPIProp::OpenProperty** para recuperar uma interface de fluxo para texto grande e propriedades binárias.  <br/> |
   
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

