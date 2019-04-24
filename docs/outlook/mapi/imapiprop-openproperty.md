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
  
> no A marca de propriedade da propriedade a ser acessada. Tanto o identificador quanto o tipo devem ser incluídos na marca da propriedade.
    
 _lpiid_
  
> no Um ponteiro para o identificador da interface a ser usada para acessar a propriedade. O parâmetro _lpiid_ não deve ser **nulo**.
    
 _ulInterfaceOptions_
  
> no Dados relacionados à interface identificada pelo parâmetro _lpiid_ . 
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla o acesso à propriedade. Os seguintes sinalizadores podem ser definidos:
    
MAPI_CREATE 
  
> Se a propriedade não existir, ela deverá ser criada. Se a propriedade existir, o valor atual da propriedade deverá ser Descartado. Quando um chamador define o sinalizador MAPI_CREATE, ele também deve definir o sinalizador MAPI_MODIFY.
    
MAPI_DEFERRED_ERRORS 
  
> Permite **** que OpenProperty seja retornado com êxito, possivelmente antes que o objeto esteja totalmente disponível para o chamador. Se o objeto não estiver disponível, fazer uma chamada de objeto subsequente poderá gerar um erro. 
    
MAPI_MODIFY 
  
> O MAPI_MODIFY é necessário nestas situações:
    
  - Ao abrir uma propriedade Stream, como **IID_IStream**, para modificá-la.
    
  - Ao abrir um anexo de mensagem incorporado, como [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) aberto com **IID_IMessage**, para modificá-lo.
    
 _lppUnk_
  
> bota Um ponteiro para a interface solicitada a ser usada para acesso de propriedade.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O ponteiro de interface solicitado foi retornado com êxito.
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> A interface solicitada não tem suporte para essa propriedade.
    
MAPI_E_NO_ACCESS 
  
> O chamador tem permissões insuficientes para acessar a propriedade.
    
MAPI_E_NO_SUPPORT 
  
> O objeto não pode fornecer acesso a essa propriedade por meio da interface solicitada.
    
MAPI_E_NOT_FOUND 
  
> A propriedade solicitada não existe e MAPI_CREATE não foi definida no parâmetro _parâmetroulflags_ . 
    
MAPI_E_INVALID_PARAMETER 
  
> O tipo de propriedade na marca é definido como PT_UNSPECIFIED.
    
## <a name="remarks"></a>Comentários

O método **IMAPIProp:: OpenProperty** fornece acesso a uma propriedade por meio de uma interface específica. **OpenProperty** é uma alternativa para os métodos [IMAPIProp::](imapiprop-getprops.md) GetProps e [IMAPIProp::](imapiprop-setprops.md) SetProps. Quando getProps ou setProps falham porque a propriedade é muito grande ou muito complexa, chame **OpenProperty**. **** **** **OpenProperty** normalmente é usado para acessar propriedades do tipo PT_OBJECT. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para acessar os anexos de mensagens, abra a propriedade **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) com um identificador de interface diferente, dependendo do tipo de anexo. A tabela a seguir descreve como chamar **OpenProperty** para os diferentes tipos de anexos: 
  
|**Tipo de anexo**|**Identificador de interface a ser usado**|
|:-----|:-----|
|Binary  <br/> |IID_IStream  <br/> |
|String  <br/> |IID_IStream  <br/> |
|Mensagem  <br/> |IID_IMessage  <br/> |
|OLE 2,0  <br/> |IID_IStreamDocfile  <br/> |
   
**IStreamDocfile** é uma derivada da interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) que se baseia em um arquivo composto OLE 2,0. **IStreamDocfile** é a melhor opção para acessar anexos de OLE 2,0 porque envolve a menor quantidade de sobrecarga. Você pode usar IID_IStreamDocFile para as propriedades que contenham dados armazenados em um armazenamento estruturado disponível através da interface [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) . 
  
Para obter mais informações sobre como usar **OpenProperty** com anexos, consulte a propriedade **PR_ATTACH_DATA_OBJ** e [abrir um anexo](opening-an-attachment.md).
  
Não use o ponteiro de **IStream** que você recebeu para chamar o método [Seek](https://msdn.microsoft.com/library/aa380043%28v=VS.85%29.aspx) ou [SetSize](https://msdn.microsoft.com/library/aa380044%28v=VS.85%29.aspx) , a menos que você use uma posição zero de tamanho ou variável. Além disso, não confie no valor do parâmetro de saída _plibNewPosition_ retornado da chamada de **busca** . 
  
Se você chamar **OpenProperty** para acessar uma propriedade com a interface **IStream** , use somente essa interface para fazer alterações nele. Não tente atualizar a propriedade com nenhum dos outros métodos [IMAPIProp: IUnknown](imapipropiunknown.md) , como SetProps ou **** [IMAPIProp::D eleteprops](imapiprop-deleteprops.md). 
  
Não tente abrir uma propriedade com OpenProperty **** mais de uma vez. Os resultados estão indefinidos porque podem variar de provedor para provedor. 
  
Se você precisar modificar a propriedade a ser aberta, defina o sinalizador MAPI_MODIFY. Se você não tem certeza se o objeto oferece suporte à propriedade, mas você acha que deveria, defina os sinalizadores MAPI_CREATE e MAPI_MODIFY. Sempre que MAPI_CREATE for definido, MAPI_MODIFY também deverá ser definido.
  
Você é responsável por retransmitir o ponteiro de interface retornado no parâmetro _lppUnk_ para um que seja apropriado para a interface especificada no parâmetro _lpiid_ . Você também deve usar o ponteiro retornado para chamar seu método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) quando terminar de usá-lo. 
  
Às vezes, definir os sinalizadores no parâmetro _parâmetroulflags_ não é suficiente para indicar o tipo de acesso à propriedade que é necessária. Você pode colocar dados adicionais, como sinalizadores, no parâmetro _ulInterfaceOptions_ . Esses dados são dependentes da interface. Algumas interfaces (como **IStream**) o utilizam, e outras não. Por exemplo, ao abrir uma propriedade a ser modificada com **IStream**, defina o sinalizador STGM_WRITE no parâmetro _ulInterfaceOptions_ , além de MAPI_MODIFY. Ao abrir uma tabela usando a interface imApitable, você pode definir _ulInterfaceOptions_ como MAPI_UNICODE para indicar se as colunas na tabela que contém as propriedades da cadeia de caracteres devem estar no formato Unicode. [](imapitableiunknown.md) 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|StreamEditor. cpp  <br/> |CStreamEditor:: ReadTextStreamFromProperty  <br/> |MFCMAPI usa o método **IMAPIProp:: OpenProperty** para recuperar uma interface de fluxo para propriedades de texto e binário grandes.  <br/> |
   
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

