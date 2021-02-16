---
title: IMAPISupportOpenTemplateID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenTemplateID
api_type:
- COM
ms.assetid: 532f7af0-b2cc-49dd-b1de-e3ec1dc9a3e7
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 07aa508b473f4a87d5b4909f83771549c301a600
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418502"
---
# <a name="imapisupportopentemplateid"></a>IMAPISupport::OpenTemplateID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre uma entrada de destinatário em um provedor de agendas externas.
  
```cpp
HRESULT OpenTemplateID(
ULONG cbTemplateID,
LPENTRYID lpTemplateID,
ULONG ulTemplateFlags,
LPMAPIPROP lpMAPIPropData,
LPCIID lpInterface,
LPMAPIPROP FAR * lppMAPIPropNew,
LPMAPIPROP lpMAPIPropSibling
);
```

## <a name="parameters"></a>Parâmetros

 _cbTemplateID_
  
> [in] A contagem de byte no identificador de modelo apontado por  _lpTemplateID_. 
    
 _lpTemplateID_
  
> [in] Um ponteiro para o identificador **de PR_TEMPLATEID** propriedade ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) da entrada do destinatário a ser aberta.
    
 _ulTemplateFlags_
  
> [in] Uma máscara de bits de sinalizadores usada para descrever como abrir a entrada. O sinalizador a seguir pode ser definido:
    
FILL_ENTRY 
  
> Uma nova entrada está sendo criada. Quando o provedor estrangeiro recebe a chamada [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) subsequente do MAPI, ele pode controlar como a entrada é criada modificando as propriedades apontadas pelo parâmetro  _lpMAPIPropData_ ou retornando uma implementação de interface específica em  _lppMAPIPropNew_ para controlar como as propriedades da nova entrada são definidas. 
    
 _lpMAPIPropData_
  
> [in] Um ponteiro para a implementação da interface que o chamador usa para acessar a entrada. Esta é a implementação que o provedor externo pode quebrar com sua própria implementação e retornar no _parâmetro lppMAPIPropNew._ O _parâmetro lpMAPIPropData_ deve apontar para uma implementação de interface de leitura/gravação derivada de [IMAPIProp : IUnknown](imapipropiunknown.md) e dá suporte à interface que está sendo solicitada no parâmetro _lpInterface._ 
    
 _lpInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar a entrada. O  _parâmetro lppMAPIPropNew_ aponta para uma interface do tipo especificado por  _lpInterface_. Passar NULL retorna a interface padrão para um usuário de mensagens, IID_IMailUser. 
    
 _lppMAPIPropNew_
  
> [out] Um ponteiro para a implementação da interface que o provedor estrangeiro fornece para acessar a entrada.
    
 _lpMAPIPropSibling_
  
> Reservado; deve ser NULL.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O processo de associação foi bem-sucedido.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> O provedor de agendas externas não existe.
    
## <a name="remarks"></a>Comentários

O **método IMAPISupport::OpenTemplateID** é implementado somente para objetos de suporte do provedor de agendas de endereços. **OpenTemplateID** é chamado apenas por provedores de agendas que podem atuar como hosts para entradas que pertencem a outros provedores de agendas, também conhecidos como provedores externos. Os provedores de host chamam **OpenTemplateID** para abrir uma entrada externa, que ocorre quando os dados no provedor host estão vinculados ao código no provedor estrangeiro. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Chame **OpenTemplateID** somente se você suportar o armazenamento de entradas com identificadores de modelo de provedores de agendamento externo. Esse suporte coloca requisitos adicionais nas implementações [IABContainer::CreateEntry](iabcontainer-createentry.md) e [IABLogon::OpenEntry.](iablogon-openentry.md) Para obter mais informações, consulte as descrições desses métodos e agindo como um provedor de [agenda de endereços de host.](acting-as-a-host-address-book-provider.md)
  
Se a **chamada OpenTemplateID** retornar como a interface vinculada da mesma implementação de objeto de propriedade que você passou, você poderá liberar sua referência ao objeto property. Isso porque o provedor externo chamou o método **AddRef** do objeto para manter sua própria referência. Se o provedor externo não precisar manter uma referência para o objeto de propriedade, **OpenTemplateID** retornará o objeto de propriedade não abound. 
  
Se **OpenTemplateID** falhar com MAPI_E_UNKNOWN_ENTRYID, tente continuar tratando a entrada como somente leitura. 
  
## <a name="see-also"></a>Confira também



[IABLogon::OpenTemplateID](iablogon-opentemplateid.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[Propriedade canônica PidTagTemplateid](pidtagtemplateid-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

